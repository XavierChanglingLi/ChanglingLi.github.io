<style>
.research-boxes {
  display: flex;
  gap: 1em;
  margin: 1.5em 0;
  flex-wrap: wrap;
}

.research-box {
  display: block;
  color: var(--text);
  text-decoration: none;
  cursor: pointer;
  flex: 1;
  min-width: 150px;
  border-radius: 8px;
  padding: 1.2em;
  text-align: center;
  transition: all 0.3s ease;
}

.research-box:hover,
.research-box:focus {
  transform: translateY(-3px);
  color: var(--text);
  text-decoration: none;
}

.research-box:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 2px;
}

.research-box.safety {
  background: var(--cat-safety-bg);
  border: 1px solid var(--cat-safety-border);
}
.research-box.safety:hover {
  box-shadow: 0 6px 20px var(--cat-safety-glow);
  border-color: var(--cat-safety);
}
.research-box.safety .research-box-icon,
.research-box.safety .research-box-title {
  color: var(--cat-safety);
}

.research-box.multiagent {
  background: var(--cat-multiagent-bg);
  border: 1px solid var(--cat-multiagent-border);
}
.research-box.multiagent:hover {
  box-shadow: 0 6px 20px var(--cat-multiagent-glow);
  border-color: var(--cat-multiagent);
}
.research-box.multiagent .research-box-icon,
.research-box.multiagent .research-box-title {
  color: var(--cat-multiagent);
}

.research-box.governance {
  background: var(--cat-governance-bg);
  border: 1px solid var(--cat-governance-border);
}
.research-box.governance:hover {
  box-shadow: 0 6px 20px var(--cat-governance-glow);
  border-color: var(--cat-governance);
}
.research-box.governance .research-box-icon,
.research-box.governance .research-box-title {
  color: var(--cat-governance);
}

.research-box-icon {
  font-size: 1.8em;
  margin-bottom: 0.4em;
}

.research-box-title {
  font-weight: 700;
  font-size: 1em;
  margin-bottom: 0.4em;
}

.research-box-desc {
  font-size: 0.85em;
  color: var(--text-muted);
  line-height: 1.4;
}
</style>

Welcome! I will be joining the [Max Planck Institute for Intelligent Systems (MPI-IS)](https://is.mpg.de/) as a PhD student, jointly supervised by Prof. [Maksym Andriushchenko](https://www.andriushchenko.me/) and Prof. [Rediet Abebe](https://scholar.google.com/citations?user=sDHHglIAAAAJ&hl=en). I recently completed my master's in computer science at [ETH Zurich](https://ethz.ch/en.html) majoring in machine intelligence and minoring in theoretical computer science. I have previously worked with Prof. [Zhijing Jin](https://zhijing-jin.com/home/), Prof. [Joni Pajarinen](https://rl.aalto.fi/), and Prof. [Pulkit Agrawal](https://people.csail.mit.edu/pulkitag/) on various projects. I obtained my B.A. degrees in computer science and physics with a concentration in astrophysics at [Colby College](https://www.colby.edu/) where I was fortunate to work with Prof. [Ying Li](https://cs.colby.edu/yingli/). I am also a [UWC](https://www.uwc.org/) alumnus.

<p style="font-weight: 700; color: var(--accent); font-size: 1.1em;">Research Interests</p>

<div class="research-boxes">
<a class="research-box safety" href="#paper-eval-awareness" aria-label="AI Safety: jump to Decomposing and Measuring Evaluation Awareness">
<div class="research-box-icon"><i class="fa-solid fa-shield-halved"></i></div>
<div class="research-box-title">AI Safety</div>
<div class="research-box-desc">Studying emergent awareness of AI agents and developing methodologies for rare event estimation</div>
</a>
<a class="research-box multiagent" href="#paper-a2a-tom" aria-label="Multi-Agent Systems: jump to Agent-to-Agent Theory of Mind">
<div class="research-box-icon"><i class="fa-solid fa-network-wired"></i></div>
<div class="research-box-title">Multi-Agent Systems</div>
<div class="research-box-desc">Understanding risk propagation through agent populations and designing safe multi-agent interactions</div>
</a>
<a class="research-box governance" href="#paper-safe-societies" aria-label="AI Governance: jump to Safe Models Do Not Guarantee Safe Societies">
<div class="research-box-icon"><i class="fa-solid fa-scale-balanced"></i></div>
<div class="research-box-title">AI Governance</div>
<div class="research-box-desc">Connecting technical research and policy-making on evaluation standards, agent accountability, and interaction regulation</div>
</a>
</div>

<script>
document.addEventListener('click', function (e) {
  var link = e.target.closest && e.target.closest('a.research-box');
  if (!link) return;
  var target = document.querySelector(link.getAttribute('href'));
  if (!target) return;
  // Capture phase + stopPropagation keeps the theme's generic smooth-scroll (fixed 20px offset) from also firing.
  e.preventDefault();
  e.stopPropagation();
  var list = target.closest('.pubs-section-content');
  if (list && list.scrollHeight > list.clientHeight) {
    list.scrollTop += target.getBoundingClientRect().top - list.getBoundingClientRect().top - 20;
  }
  var masthead = document.querySelector('.masthead');
  var offset = (masthead ? masthead.offsetHeight : 0) + 28;
  var top = target.getBoundingClientRect().top + window.pageYOffset - offset;
  if (window.jQuery) {
    jQuery('html, body').stop().animate({ scrollTop: top }, 500);
  } else {
    window.scrollTo(0, top);
  }
  history.pushState(null, '', link.getAttribute('href'));
  target.classList.remove('paper-box--flash');
  void target.offsetWidth;
  target.classList.add('paper-box--flash');
}, true);
</script>
