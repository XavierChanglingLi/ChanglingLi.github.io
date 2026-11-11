# News

<style>
.news-scrollable {
  max-height: 360px;
  overflow-y: scroll;
  padding-right: 8px;
}

.news-scrollable::-webkit-scrollbar {
  width: 6px;
}

.news-scrollable::-webkit-scrollbar-track {
  background: var(--scrollbar-track);
  border-radius: 10px;
}

.news-scrollable::-webkit-scrollbar-thumb {
  background: var(--accent);
  border-radius: 10px;
}

.news-scrollable::-webkit-scrollbar-thumb:hover {
  background: var(--accent-hover);
}

.news-item {
  background: var(--bg-card-gradient);
  border-left: 4px solid var(--accent);
  border-radius: 6px;
  padding: 12px 14px;
  margin-bottom: 10px;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px var(--img-shadow);
}

.news-item:hover {
  box-shadow: 0 4px 8px var(--accent-glow);
  transform: translateX(4px);
}

.news-date {
  display: inline-block;
  background-color: var(--accent);
  color: var(--bg);
  padding: 3px 8px;
  border-radius: 4px;
  font-size: 11px;
  font-weight: 600;
  margin-right: 8px;
  letter-spacing: 0.5px;
}

.news-content {
  font-size: 14px;
  line-height: 1.5;
  color: var(--text);
}

.news-content a {
  color: var(--accent);
  text-decoration: none;
  font-weight: 600;
  transition: all 0.2s ease;
}

.news-content a:hover {
  color: var(--accent-hover);
}

.news-item.news-item--highlight {
  border: 1px solid rgba(217, 119, 87, 0.6);
  border-left: 4px solid #D97757;
  background: linear-gradient(135deg, rgba(217, 119, 87, 0.32) 0%, rgba(217, 119, 87, 0.18) 100%);
  box-shadow: 0 2px 12px rgba(217, 119, 87, 0.35);
}

.news-item.news-item--highlight:hover {
  box-shadow: 0 4px 16px rgba(217, 119, 87, 0.5);
}

.news-badge {
  display: inline-block;
  background-color: #D97757;
  color: #ffffff;
  padding: 3px 8px;
  border-radius: 4px;
  font-size: 11px;
  font-weight: 700;
  margin-right: 8px;
  letter-spacing: 0.5px;
}
</style>

<div class="news-scrollable">

<div class="news-item">
  <span class="news-date">2026.10</span>
  <span class="news-content">🦀 Our paper <a href="https://arxiv.org/abs/2605.23055">Decomposing and Measuring Evaluation Awareness</a> is accepted to the NeurIPS 2026 Agents in the Wild workshop (Oral 🏆). See you in Sydney!</span>
</div>

<div class="news-item news-item--highlight">
  <span class="news-date">2026.09</span>
  <span class="news-badge"><i class="fa-solid fa-star"></i> Highlight</span>
  <span class="news-content">🐡 Our work on <a href="https://arxiv.org/abs/2605.23055">evaluation awareness</a> is used by <span style="color: #D97757; font-weight: 700;">Anthropic</span> in the alignment evaluation of Claude Opus 5.5 (<a href="https://www-cdn.anthropic.com/fc1b44717c85dc068bc6ba5024219938094694bd/Claude%20Opus%205.5%20System%20Card.pdf">System Card</a>, p. 137)!</span>
</div>

<div class="news-item">
  <span class="news-date">2026.07</span>
  <span class="news-content">🦭 I graduated from <a href="https://ethz.ch/en.html">ETH Zurich</a> with a Master's degree in Computer Science!</span>
</div>

<div class="news-item">
  <span class="news-date">2026.07</span>
  <span class="news-content">🐋 I will be co-organizing the 2nd <a href="https://trustworthy-ai-for-good.github.io/index.html">AI4GOOD workshop</a> at NeurIPS 2026 in Paris.</span>
</div>

<div class="news-item">
  <span class="news-date">2026.05</span>
  <span class="news-content">🦐 I will attend the <a href="https://www.far.ai/events/seoul-alignment-workshop-2026">FAR.AI Alignment Workshop</a> and the <a href="https://foresight.org/events/supercooperation-the-future-of-ai-for-democracy/">Foresight Institute Supercooperation Workshop</a> in Seoul. Let's chat!</span>
</div>

<div class="news-item">
  <span class="news-date">2026.05</span>
  <span class="news-content">🐙 Our position paper <a href="https://icml.cc/virtual/2026/poster/67167">Safe Models Do Not Guarantee Safe Societies</a> is accepted by ICML 2026 (<b>Spotlight 🏆</b>). See you in Seoul!</span>
</div>

<div class="news-item">
  <span class="news-date">2026.05</span>
  <span class="news-content">🪼 I will be co-organizing the 1st <a href="https://trustworthy-ai-for-good.github.io/icml-2026.html">AI4GOOD workshop</a> at ICML 2026.</span>
</div>

<div class="news-item">
  <span class="news-date">2026.05</span>
  <span class="news-content">🦑 I finished my master thesis on <a href="https://arxiv.org/abs/2605.23055">Decomposing and Measuring Evaluation Awareness</a>.</span>
</div>

<div class="news-item">
  <span class="news-date">2026.03</span>
  <span class="news-content">🌊 I will be joining MPI-IS as a PhD student in September, jointly supervised by <a href="https://www.andriushchenko.me/">Maksym Andriushchenko</a> and <a href="https://scholar.google.com/citations?user=sDHHglIAAAAJ&hl=en">Rediet Abebe</a>.</span>
</div>

<div class="news-item">
  <span class="news-date">2025.08</span>
  <span class="news-content">🐚 Our paper <a href="https://arxiv.org/abs/2506.22957">Agent-to-Agent Theory of Mind</a> is accepted by EMNLP 2025 (main conference).</span>
</div>

<div class="news-item">
  <span class="news-date">2024.05</span>
  <span class="news-content">🐠 Our paper <a href="https://rlj.cs.umass.edu/2024/papers/Paper198.html">ROER: Regularized Optimal Experience Replay</a> is accepted by RLC 2024.</span>
</div>

</div>
