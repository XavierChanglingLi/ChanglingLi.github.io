<style>
.research-boxes {
  display: flex;
  gap: 1em;
  margin: 1.5em 0;
  flex-wrap: wrap;
}

.research-box {
  flex: 1;
  min-width: 150px;
  border-radius: 8px;
  padding: 1.2em;
  text-align: center;
  transition: all 0.3s ease;
}

.research-box:hover {
  transform: translateY(-3px);
}

.research-box.safety {
  background: rgba(179, 255, 240, 0.08);
  border: 1px solid rgba(179, 255, 240, 0.2);
}
.research-box.safety:hover {
  box-shadow: 0 6px 20px rgba(179, 255, 240, 0.15);
  border-color: #b3fff0;
}
.research-box.safety .research-box-icon,
.research-box.safety .research-box-title {
  color: #b3fff0;
}

.research-box.multiagent {
  background: rgba(255, 224, 179, 0.08);
  border: 1px solid rgba(255, 224, 179, 0.2);
}
.research-box.multiagent:hover {
  box-shadow: 0 6px 20px rgba(255, 224, 179, 0.15);
  border-color: #ffe0b3;
}
.research-box.multiagent .research-box-icon,
.research-box.multiagent .research-box-title {
  color: #ffe0b3;
}

.research-box.governance {
  background: rgba(200, 179, 255, 0.08);
  border: 1px solid rgba(200, 179, 255, 0.2);
}
.research-box.governance:hover {
  box-shadow: 0 6px 20px rgba(200, 179, 255, 0.15);
  border-color: #c8b3ff;
}
.research-box.governance .research-box-icon,
.research-box.governance .research-box-title {
  color: #c8b3ff;
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
  color: #cccccc;
  line-height: 1.4;
}
</style>

Welcome! I will be joining [MPI-IS](https://is.mpg.de/) as a PhD student in September, jointly supervised by Prof. [Maksym Andriushchenko](https://www.andriushchenko.me/) and Prof. [Rediet Abebe](https://scholar.google.com/citations?user=sDHHglIAAAAJ&hl=en). I recently completed my master's in computer science at [ETH Zurich](https://ethz.ch/en.html) majoring in machine intelligence and minoring in theoretical computer science. I have previously worked with Prof. [Zhijing Jin](https://zhijing-jin.com/home/), Prof. [Joni Pajarinen](https://rl.aalto.fi/), and Prof. [Pulkit Agrawal](https://people.csail.mit.edu/pulkitag/) on various projects. I obtained my B.A. degrees in computer science and physics with a concentration in astrophysics at [Colby College](https://www.colby.edu/) where I was fortunate to work with Prof. [Ying Li](https://cs.colby.edu/yingli/). I am also a [UWC](https://www.uwc.org/) alumnus.

<div class="research-boxes">
<div class="research-box safety">
<div class="research-box-icon"><i class="fa-solid fa-shield-halved"></i></div>
<div class="research-box-title">AI Safety</div>
<div class="research-box-desc">Developing methodologies to evaluate, detect, and mitigate high-stakes rare behaviors in frontier AI systems</div>
</div>
<div class="research-box multiagent">
<div class="research-box-icon"><i class="fa-solid fa-network-wired"></i></div>
<div class="research-box-title">Multi-Agent Systems</div>
<div class="research-box-desc">Understanding risk propagation through agent populations and designing safe multi-agent interactions</div>
</div>
<div class="research-box governance">
<div class="research-box-icon"><i class="fa-solid fa-scale-balanced"></i></div>
<div class="research-box-title">AI Governance</div>
<div class="research-box-desc">Connecting technical research and policy-making on evaluation standards, agent accountability, and interaction regulation</div>
</div>
</div>
