<style>
.pubs-section-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #ff69b4;
  padding: 8px 14px;
  border-radius: 6px;
  margin-top: 1em;
  margin-bottom: 0.5em;
}

.pubs-section-bar h3 {
  margin: 0;
  color: #1a1a1a;
  font-size: 1em;
  font-weight: 700;
  border: none;
  padding: 0;
}

.pubs-section-toggle {
  cursor: pointer;
  font-size: 0.9em;
  color: #1a1a1a;
  background-color: rgba(0, 0, 0, 0.15);
  width: 22px;
  height: 22px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 3px;
  transition: all 0.3s ease;
  user-select: none;
}

.pubs-section-toggle:hover {
  background-color: rgba(0, 0, 0, 0.3);
}

.pubs-section-content {
  overflow-y: auto;
  overflow-x: visible;
  padding: 4px 8px 4px 8px;
  transition: max-height 0.4s ease;
}

#preprint-section {
  max-height: none;
  overflow-y: visible;
}

#accepted-section {
  max-height: 600px;
}

.pubs-section-content.expanded {
  max-height: none !important;
  overflow-y: visible;
}

.pubs-section-content::-webkit-scrollbar {
  width: 6px;
}

.pubs-section-content::-webkit-scrollbar-track {
  background: #2a2a2a;
  border-radius: 10px;
}

.pubs-section-content::-webkit-scrollbar-thumb {
  background: #ff69b4;
  border-radius: 10px;
}

.pubs-section-content::-webkit-scrollbar-thumb:hover {
  background: #ff85c2;
}
</style>

# 📝 Publications

<div class="pubs-section-bar">
<h3>Preprint</h3>
<span class="pubs-section-toggle" id="preprint-toggle" data-target="preprint-section">
<i class="fa-solid fa-plus"></i>
</span>
</div>

<div class="pubs-section-content" id="preprint-section">

<div class='paper-box cat-safety'><span class='paper-box-label'>Preprint 2026</span><span class='paper-category-tag tag-safety'>AI Safety</span><div class='paper-box-image'><div><img src='images/EvalAware_2026.gif' alt="EvalAwareBench 2026" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Decomposing and Measuring Evaluation Awareness](https://arxiv.org/abs/2605.23055)

**Changling Li**, Terry Jingchen Zhang, Jie Zhang, Zhijing Jin, Sahar Abdelnabi, Maksym Andriushchenko

*arXiv preprint*, 2026

<i class="fa-brands fa-github"></i> [Code](https://github.com/aisa-group/decomposing-eval-awareness) / <i class="fa-solid fa-database"></i> [HuggingFace](https://huggingface.co/datasets/aisa-group/EvalAwareBench) / <i class="fa-solid fa-file-lines"></i> [arXiv](https://arxiv.org/abs/2605.23055)
</div>
</div>

</div>

<div class="pubs-section-bar">
<h3>Accepted</h3>
<span class="pubs-section-toggle" id="accepted-toggle" data-target="accepted-section">
<i class="fa-solid fa-plus"></i>
</span>
</div>

<div class="pubs-section-content" id="accepted-section">

<div class='paper-box cat-governance'><span class='paper-box-label'>ICML 2026</span><span class='paper-category-tag tag-governance'>AI Governance</span><div class='paper-box-image'><div><img src='images/ICML_2026.png' alt="ICML 2026" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Position: Safe Models Do Not Guarantee Safe Societies: The Case for Sociopolitical Risk](https://icml.cc/virtual/2026/poster/67167)

David Guzman Piedrahita, **Changling Li**, Dave Banerjee, Terry Zhang, Kevin Blin, Samuel Simko, Punya Pandey, Irene Strauss, Rada Mihalcea, Bernhard Schölkopf, Zhijing Jin

*International Conference on Machine Learning (**ICML Spotlight 🏆**)*, 2026
</div>
</div>

<div class='paper-box cat-multiagent'><span class='paper-box-label'>EMNLP 2025</span><span class='paper-category-tag tag-multiagent'>Multi-Agent Systems</span><div class='paper-box-image'><div><img src='images/EMNLP_2025.png' alt="EMNLP 2025" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Agent-to-Agent Theory of Mind: Testing Interlocutor Awareness among Large Language Models](https://arxiv.org/abs/2506.22957)

Ethan Choi\*, **Changling Li**\*, Yongjin Yang, Zhijing Jin

*Empirical Methods in Natural Language Processing (**EMNLP Main**)*, 2025

<i class="fa-brands fa-github"></i> [Code](https://github.com/younwoochoi/InterlocutorAwarenessLLM) / <i class="fa-solid fa-file-pdf"></i> [Poster](docs/EMNLP_2025_Poster.pdf) / <i class="fa-solid fa-person-chalkboard"></i> [Presentation](https://docs.google.com/presentation/d/1_mpKH68oVT3z-otLZBWj8AQAoT5Bs4kT5X6huYWYBIQ/edit?usp=sharing) / <i class="fa-solid fa-file-lines"></i> [arXiv](https://arxiv.org/abs/2506.22957)
</div>
</div>

<div class='paper-box'><span class='paper-box-label'>RLC 2024</span><div class='paper-box-image'><div><img src='images/RLC_2024.png' alt="RLC 2024" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[ROER: Regularized Optimal Experience Replay](https://rlj.cs.umass.edu/2024/papers/Paper198.html)

**Changling Li**, Zhang-Wei Hong, Pulkit Agrawal, Divyansh Garg, Joni Pajarinen

*Reinforcement Learning Conference (**RLC**)*, 2024

<i class="fa-brands fa-github"></i> [Code](https://github.com/XavierChanglingLi/Regularized-Optimal-Experience-Replay) / <i class="fa-solid fa-file-pdf"></i> [Poster](docs/RLC_2024_Poster.pdf) / <i class="fa-solid fa-person-chalkboard"></i> [Presentation](https://docs.google.com/presentation/d/1YnakiI81uulW6TWuJkysh-amYOHGFHylQizVeYoY1X0/edit?usp=sharing) / <i class="fa-solid fa-file-lines"></i> [arXiv](https://arxiv.org/abs/2407.03995)
</div>
</div>

<div class='paper-box cat-multiagent'><span class='paper-box-label'>IoT-J 2024</span><span class='paper-category-tag tag-multiagent'>Multi-Agent Systems</span><div class='paper-box-image'><div><img src='images/IoT_2024.png' alt="IoT-J 2024" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Scaling Up Energy-Aware Multiagent Reinforcement Learning for Mission-Oriented Drone Networks With Individual Reward](https://ieeexplore.ieee.org/abstract/document/10777009) (Bachelor Honors Thesis)

**Changling Li**, Ying Li

*Internet of Things Journal (**IoT-J**)*, 2024

<i class="fa-brands fa-github"></i> [Code](https://github.com/XavierChanglingLi/MARL_for_MODN) / <i class="fa-solid fa-file-lines"></i> [arXiv](https://www.researchgate.net/publication/386447478_Scaling_up_Energy-Aware_Multi-Agent_Reinforcement_Learning_for_Mission-Oriented_Drone_Networks_With_Individual_Reward)
</div>
</div>

<div class='paper-box cat-multiagent'><span class='paper-box-label'>ICCCN 2022</span><span class='paper-category-tag tag-multiagent'>Multi-Agent Systems</span><div class='paper-box-image'><div><img src='images/ICCCN_2022.png' alt="ICCCN 2022" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Energy-Aware Multi-Agent Reinforcement Learning for Collaborative Execution in Mission-Oriented Drone Networks](https://ieeexplore.ieee.org/abstract/document/9868945)

Ying Li, **Changling Li**, Jiyao Chen, Christine Roinou

*International Conference on Computer Communications and Networks (**ICCCN**)*, 2022

<i class="fa-brands fa-github"></i> [Code](https://github.com/XavierChanglingLi/MARL_for_MODN) / <i class="fa-solid fa-file-lines"></i> [arXiv](https://arxiv.org/abs/2410.22578)
</div>
</div>

</div>

<script>
document.querySelectorAll('.pubs-section-toggle').forEach(function(btn) {
  btn.addEventListener('click', function() {
    var target = document.getElementById(this.getAttribute('data-target'));
    target.classList.toggle('expanded');
    var icon = this.querySelector('i');
    if (target.classList.contains('expanded')) {
      icon.className = 'fa-solid fa-minus';
    } else {
      icon.className = 'fa-solid fa-plus';
    }
  });
});
</script>
