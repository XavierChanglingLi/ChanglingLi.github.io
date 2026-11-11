{% if site.visitor_map.sheet_id and site.visitor_map.sheet_id != "" %}
<style>
.visitor-map {
  margin: 3em auto 0;
  max-width: 560px;
  text-align: center;
}
.visitor-map-title {
  font-size: 0.85em;
  font-weight: 700;
  color: var(--accent);
  margin-bottom: 0.3em;
}
.visitor-map-chart {
  width: 100%;
  aspect-ratio: 2 / 1;
}
.visitor-map-count {
  font-size: 0.75em;
  color: var(--text-muted);
  margin-top: 0.3em;
}
</style>

<div class="visitor-map">
  <div class="visitor-map-title"><i class="fa-solid fa-earth-americas"></i> Visitors</div>
  <div class="visitor-map-chart" id="visitor-map-chart"></div>
  <div class="visitor-map-count" id="visitor-map-count"></div>
</div>

<script src="https://www.gstatic.com/charts/loader.js"></script>
<script>
(function () {
  var SHEET_ID = "{{ site.visitor_map.sheet_id }}";
  var LOG_URL = "{{ site.visitor_map.log_url }}";
  var LOGGED_KEY = "visitor-map-logged";
  var counts = null;

  var isLocal = ['localhost', '127.0.0.1', '[::1]'].indexOf(location.hostname) !== -1;
  var alreadyLogged = false;
  try { alreadyLogged = localStorage.getItem(LOGGED_KEY) === '1'; } catch (e) {}

  if (LOG_URL && !isLocal && !alreadyLogged) {
    fetch('https://www.cloudflare.com/cdn-cgi/trace')
      .then(function (r) { return r.text(); })
      .then(function (text) {
        var m = text.match(/^loc=([A-Z]{2})$/m);
        if (!m || m[1] === 'XX' || m[1] === 'T1') return;
        return fetch(LOG_URL + '?country=' + m[1], { mode: 'no-cors' }).then(function () {
          try { localStorage.setItem(LOGGED_KEY, '1'); } catch (e) {}
        });
      })
      .catch(function () {});
  }

  function cssVar(name) {
    return getComputedStyle(document.documentElement).getPropertyValue(name).trim();
  }

  var regionNames = window.Intl && Intl.DisplayNames ? new Intl.DisplayNames(['en'], { type: 'region' }) : null;

  function draw() {
    if (!counts || !window.google || !google.visualization) return;
    var data = new google.visualization.DataTable();
    data.addColumn('string', 'Country');
    data.addColumn('number', 'Visitors');
    counts.forEach(function (c) {
      var name = c.code;
      try { if (regionNames) name = regionNames.of(c.code) || c.code; } catch (e) {}
      data.addRow([{ v: c.code, f: name }, c.n]);
    });
    new google.visualization.GeoChart(document.getElementById('visitor-map-chart')).draw(data, {
      backgroundColor: 'transparent',
      datalessRegionColor: cssVar('--map-empty'),
      defaultColor: cssVar('--map-empty'),
      colorAxis: { colors: [cssVar('--map-low'), cssVar('--map-high')] },
      legend: 'none',
      keepAspectRatio: true
    });
  }

  google.charts.load('current', { packages: ['geochart'] });

  var query = encodeURIComponent('select B, count(A) where B is not null group by B');
  fetch('https://docs.google.com/spreadsheets/d/' + SHEET_ID + '/gviz/tq?tqx=out:json&tq=' + query)
    .then(function (r) { return r.text(); })
    .then(function (text) {
      var json = JSON.parse(text.substring(text.indexOf('{'), text.lastIndexOf('}') + 1));
      counts = [];
      var total = 0;
      json.table.rows.forEach(function (row) {
        var code = row.c[0] && row.c[0].v;
        var n = row.c[1] && row.c[1].v;
        if (code && n) { counts.push({ code: String(code).trim().toUpperCase(), n: n }); total += n; }
      });
      document.getElementById('visitor-map-count').textContent =
        total.toLocaleString('en') + (total === 1 ? ' visitor from ' : ' visitors from ') + counts.length + (counts.length === 1 ? ' country' : ' countries');
      google.charts.setOnLoadCallback(draw);
    })
    .catch(function () {});

  new MutationObserver(draw).observe(document.documentElement, { attributes: true, attributeFilter: ['data-theme'] });
  var resizeTimer;
  window.addEventListener('resize', function () { clearTimeout(resizeTimer); resizeTimer = setTimeout(draw, 200); });
})();
</script>
{% endif %}
