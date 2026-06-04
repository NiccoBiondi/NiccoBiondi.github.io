---
layout: page
title: "A Stationary (and Therefore Compatible) Representation is All You Need"
description: IEEE Transactions on Pattern Analysis and Machine Intelligence, 2024
img: assets/img/projects/stationary_tpami/teaser.png
importance: 1
category: research
permalink: /projects/stationary-tpami/
_styles: >
  .project-header { text-align: center; margin-bottom: 2rem; }
  .project-authors { font-size: 1.05rem; margin-bottom: 0.6rem; }
  .project-authors a { color: var(--global-theme-color); }
  .project-venue-badge {
    display: inline-block;
    background: var(--global-theme-color);
    color: #fff;
    font-size: 0.85rem;
    font-weight: 600;
    padding: 5px 16px;
    border-radius: 20px;
    margin-bottom: 1rem;
  }
  .project-links { display: flex; justify-content: center; gap: 0.5rem; flex-wrap: wrap; margin-bottom: 2rem; }
  .project-links a {
    border: 1.5px solid var(--global-theme-color);
    color: var(--global-theme-color);
    padding: 5px 18px;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
    text-decoration: none;
    transition: background 0.15s, color 0.15s;
  }
  .project-links a:hover { background: var(--global-theme-color); color: #fff; text-decoration: none; }
  .section-title {
    font-size: 1.3rem;
    font-weight: 700;
    margin-top: 2.5rem;
    margin-bottom: 1rem;
    padding-bottom: 0.4rem;
    border-bottom: 2px solid var(--global-theme-color);
    color: var(--global-text-color);
  }
  .tldr-wrapper {
    background: var(--global-card-bg-color);
    border-radius: 12px;
    padding: 1.75rem 2rem;
    margin: 1rem 0 2rem;
    border: 1px solid var(--global-divider-color);
  }
  .tldr-depth-control { display: flex; justify-content: center; margin-bottom: 1.4rem; }
  .tldr-depth-btn {
    padding: 0.35rem 1.6rem;
    border: 1.5px solid var(--global-theme-color);
    background: transparent;
    color: var(--global-theme-color);
    cursor: pointer;
    font-size: 0.85rem;
    font-weight: 500;
    transition: background 0.15s, color 0.15s;
    outline: none;
  }
  .tldr-depth-btn:first-child { border-radius: 20px 0 0 20px; border-right: none; }
  .tldr-depth-btn:last-child  { border-radius: 0 20px 20px 0; border-left: none; }
  .tldr-depth-btn:nth-child(2){ border-left: none; border-right: none; }
  .tldr-depth-btn.tldr-active { background: var(--global-theme-color); color: #fff; }
  .tldr-panel { font-size: 0.98rem; line-height: 1.75; text-align: justify; }
  .tldr-tag {
    display: inline-block;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--global-theme-color);
    border: 1px solid var(--global-theme-color);
    border-radius: 4px;
    padding: 1px 6px;
    margin-right: 0.5rem;
    vertical-align: middle;
  }
  .contrib-card {
    background: var(--global-card-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 10px;
    padding: 1.2rem 1.4rem;
    height: 100%;
    transition: box-shadow 0.2s;
  }
  .contrib-card:hover { box-shadow: 0 4px 16px rgba(0,0,0,0.07); }
  .contrib-card-num {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 1.7rem;
    height: 1.7rem;
    background: var(--global-theme-color);
    color: #fff;
    border-radius: 50%;
    font-size: 0.78rem;
    font-weight: 700;
    margin-bottom: 0.6rem;
  }
  .contrib-card h6 {
    font-weight: 700;
    font-size: 0.95rem;
    color: var(--global-theme-color);
    margin-bottom: 0.4rem;
  }
  .contrib-card p { font-size: 0.88rem; line-height: 1.6; margin: 0; }
  .method-box {
    background: var(--global-card-bg-color);
    border-left: 4px solid var(--global-theme-color);
    border-radius: 0 8px 8px 0;
    padding: 1.2rem 1.5rem;
    margin: 1rem 0;
    font-size: 0.95rem;
    line-height: 1.7;
  }
  .results-highlight {
    background: var(--global-card-bg-color);
    border-radius: 8px;
    padding: 1.2rem 1.5rem;
    margin: 1rem 0;
    border: 1px solid var(--global-divider-color);
  }
  .results-highlight table { width: 100%; font-size: 0.88rem; border-collapse: collapse; }
  .results-highlight th { border-bottom: 2px solid var(--global-theme-color); padding: 0.3rem 0.6rem; text-align: center; font-weight: 700; }
  .results-highlight td { padding: 0.3rem 0.6rem; text-align: center; border-bottom: 1px solid var(--global-divider-color); }
  .results-highlight tr:last-child td { border-bottom: none; }
  .results-highlight td.method-col { text-align: left; font-weight: 500; }
  .results-highlight td.ours { color: var(--global-theme-color); font-weight: 700; }
  .citation-block {
    background: var(--global-card-bg-color);
    border: 1px solid var(--global-divider-color);
    border-radius: 8px;
    padding: 1.2rem 1.5rem;
    font-family: monospace;
    font-size: 0.82rem;
    line-height: 1.6;
    white-space: pre-wrap;
    overflow-x: auto;
    position: relative;
  }
  .copy-btn {
    position: absolute;
    top: 0.6rem;
    right: 0.6rem;
    padding: 3px 10px;
    font-size: 0.75rem;
    border: 1px solid var(--global-theme-color);
    color: var(--global-theme-color);
    background: transparent;
    border-radius: 4px;
    cursor: pointer;
    transition: background 0.15s, color 0.15s;
  }
  .copy-btn:hover { background: var(--global-theme-color); color: #fff; }
  .formula-box {
    background: var(--global-card-bg-color);
    border-radius: 8px;
    padding: 1rem 1.5rem;
    margin: 0.8rem 0;
    text-align: center;
    font-style: italic;
    font-size: 0.95rem;
    border: 1px solid var(--global-divider-color);
  }
---

<!-- ===================== HEADER ===================== -->
<div class="project-header">
  <div class="project-authors">
    <a href="https://niccobiondi.github.io">Niccolò Biondi</a>&ensp;·&ensp;
    Federico Pernici&ensp;·&ensp;
    Simone Ricci&ensp;·&ensp;
    Alberto Del Bimbo
  </div>
  <div style="margin-bottom:0.8rem;">
    <span class="project-venue-badge">IEEE TPAMI 2026</span>
  </div>
  <div class="project-links">
    <a href="https://www.computer.org/csdl/journal/tp/5555/01/11515089/2gpcsTtMN3i">📄 Paper</a>
    <a href="https://arxiv.org/abs/YOUR_ARXIV_ID">arXiv</a>
    <a href="https://github.com/YOUR_REPO">💻 Code</a>
  </div>
</div>

<!-- ===================== TEASER ===================== -->
<div class="row justify-content-center mb-4">
  <div class="col-md-10">
    {% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/teaser.png" class="img-fluid rounded z-depth-1" %}
    <div class="caption mt-2" style="text-align:center; font-size:0.85rem; color:var(--global-text-color-light);">
      When a model is updated, features learned with a d-Simplex fixed classifier stay
      <em>stationary</em> — new query features remain directly comparable to old gallery
      features, satisfying both compatibility inequalities in expectation.
    </div>
  </div>
</div>

<!-- ===================== TL;DR ===================== -->
<div class="section-title">TL;DR</div>

<div class="tldr-wrapper">
  <div class="tldr-depth-control">
    <button class="tldr-depth-btn tldr-active" onclick="switchTLDR(this,'short')">Short</button>
    <button class="tldr-depth-btn" onclick="switchTLDR(this,'medium')">Medium</button>
    <button class="tldr-depth-btn" onclick="switchTLDR(this,'long')">Abstract</button>
  </div>

  <div class="tldr-panel" id="tldr-short">
    <span class="tldr-tag">1 sentence</span>
    Training with a <strong>d-Simplex fixed classifier</strong> makes features provably backward-compatible —
    an updated model's queries can be matched against any old gallery <em>without re-indexing</em>.
  </div>

  <div class="tldr-panel d-none" id="tldr-medium">
    <span class="tldr-tag">~100 words</span>
    We establish the first rigorous proof that <strong>stationarity implies backward compatibility</strong>
    — features learned with a d-Simplex fixed classifier satisfy both compatibility inequalities
    (Definition 1) without approximation.
    For sequential fine-tuning, plain cross-entropy only aligns first-order statistics, so we
    introduce the <strong>HOC loss</strong>: a convex combination of cross-entropy and a contrastive
    objective that captures higher-order representation dependencies while being provably equivalent
    to training under the compatibility constraints.
    Experiments across the CL²R and a new <strong>IAM-CL²R</strong> benchmark — where pre-trained
    models are periodically replaced by stronger ones — show state-of-the-art compatibility and
    accuracy across all datasets and task lengths.
  </div>

  <div class="tldr-panel d-none" id="tldr-long">
    <span class="tldr-tag">Abstract</span>
    Learning compatible representations aims to learn feature representations that can be used
    interchangeably over time whenever a model undergoes updates. In this paper, we demonstrate
    that stationary representations learned by d-Simplex fixed classifiers imply compatibility
    as in its formal definition. This result establishes a foundation for future works and can
    be directly exploited in practical learning scenarios. We address the challenge of learning
    compatibility using d-Simplex fixed classifiers when the model is sequentially fine-tuned.
    Learning according to a d-Simplex fixed classifier with the cross-entropy loss aligns feature
    distributions at the first-order statistics. Consequently, it may not fully capture higher-order
    dependencies in the representation between model updates. To address this issue, we demonstrate
    that training the model using a d-Simplex fixed classifier through a convex combination of the
    cross-entropy loss and a contrastive loss not only captures higher-order dependencies, but is
    also equivalent to learning with the cross-entropy under the compatibility constraints. We
    confirm our findings with extensive experiments also considering a new scenario where a
    pre-trained model is sequentially fine-tuned and occasionally replaced with an improved model.
    We show that stationary representations enable uninterrupted retrieval services (without
    reprocessing gallery images) while improving performance during model updates and replacements,
    achieving state-of-the-art.
  </div>
</div>

<!-- ===================== KEY CONTRIBUTIONS ===================== -->
<div class="section-title">Key Contributions</div>

<div class="row g-3">
  <div class="col-md-6">
    <div class="contrib-card">
      <div class="contrib-card-num">1</div>
      <h6>Stationarity → Compatibility (Theorem 1)</h6>
      <p>First proof — without approximation — that d-Simplex fixed classifiers satisfy
      <em>both</em> compatibility inequalities in expectation. Prior work only verified the
      same-class case; we close the gap using cosine distance in hyperspherical space.</p>
    </div>
  </div>
  <div class="col-md-6">
    <div class="contrib-card">
      <div class="contrib-card-num">2</div>
      <h6>Higher-Order Compatibility (HOC) Loss</h6>
      <p>ℒ<sub>HOC</sub> = λ·ℒ<sub>SCE</sub> + (1−λ)·ℒ<sub>iNCE</sub> captures
      higher-order representation dependencies between updates and is provably equivalent
      to optimising cross-entropy under the compatibility constraints (Proposition 1).</p>
    </div>
  </div>
  <div class="col-md-6">
    <div class="contrib-card">
      <div class="contrib-card-num">3</div>
      <h6>New IAM-CL²R Benchmark</h6>
      <p>A realistic scenario where a fine-tuned model is periodically replaced by a
      stronger one — even a different architecture. The d-Simplex classifier matrix acts
      as a common interface, enabling seamless replacement without re-indexing.</p>
    </div>
  </div>
  <div class="col-md-6">
    <div class="contrib-card">
      <div class="contrib-card-num">4</div>
      <h6>State-of-the-Art Results</h6>
      <p>Outperforms 7 baselines on CIFAR100, TinyImageNet, CUB, and CelebA — the only
      method that maintains high compatibility through architecture changes across
      31-task sequences and model replacements.</p>
    </div>
  </div>
</div>

<!-- ===================== METHOD ===================== -->
<div class="section-title">Method</div>

<div class="row">
  <div class="col-md-6">
    <h5 style="font-weight:600; margin-bottom:0.8rem;">d-Simplex Fixed Classifier</h5>
    <p>
      Class prototypes <strong>w</strong><sub>1</sub>, …, <strong>w</strong><sub>K</sub>
      are fixed at the vertices of the regular d-Simplex polytope — maximally separated,
      equiangular prototypes on the unit hypersphere.
      Because the classifier is frozen, features remain <em>stationary</em> across model updates:
      each class's hyperspherical cap shares the same central axis before and after fine-tuning,
      only shrinking as the model improves (Theorem 1).
    </p>
  </div>
  <div class="col-md-6">
    {% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/caps_illustration.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

<h5 style="font-weight:600; margin: 1.5rem 0 0.8rem;">HOC Loss for Sequential Fine-Tuning</h5>
<p>
  When fine-tuning sequentially, cross-entropy with the d-Simplex aligns features at their
  <em>first-order statistics</em> only — the mean moves to the class prototype, but
  higher-order structure is ignored. This limits back-propagation and reduces compatibility.
  We address this with the <strong>Higher-Order Compatibility (HOC) loss</strong>:
</p>

{% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/hoc.png" class="img-fluid" %}

<p>
  The contrastive term ℒ<sub>iNCE</sub> approximates the KL divergence between the joint and
  marginal distributions of φ<sub>t</sub> and φ<sub>t−1</sub>, thereby capturing mutual
  information (i.e., higher-order dependencies) between successive representations.
  By Proposition 1, minimising ℒ<sub>HOC</sub> is equivalent to minimising ℒ<sub>SCE</sub>
  subject to the compatibility constraints of Definition 1.
</p>


<!-- ===================== RESULTS ===================== -->
<div class="section-title">Results</div>

<h5 style="font-weight:600; margin-bottom:0.8rem;">CL²R Scenario — CIFAR100/10</h5>

{% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/tab_cl2r.png" class="img-fluid rounded z-depth-1" %}

<div class="row mt-3">
  <div class="col-md-10 offset-md-1">
    {% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/compatibility_matrices.png" class="img-fluid rounded z-depth-1" zoomable=true caption="Compatibility Matrices (CIFAR100/10, 7 tasks). Entries not satisfying compatibility are highlighted in red. d-Simplex-HOC achieves the most compatible entries and highest cross-test accuracy." %}
  </div>
</div>

<h5 style="font-weight:600; margin: 1.5rem 0 0.8rem;">IAM-CL²R Scenario — Model Replacement</h5>
<p>
  We introduce a new benchmark where the fine-tuned model is periodically swapped for a
  stronger one (retrained from scratch, or with a different architecture).
  Only d-Simplex-based methods benefit from replacements — all others degrade.
</p>

{% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/tab_iamcl2r.png" class="img-fluid rounded z-depth-1" %}

<p style="font-size:0.9rem; color:var(--global-text-color-light); margin-top:0.8rem;">
  Results shown on CIFAR100/10 with 7 and 31 tasks. Extended experiments on TinyImageNet, CUB, and CelebA are reported in the <a href="https://www.computer.org/csdl/journal/tp/5555/01/11515089/2gpcsTtMN3i">full paper</a>.
</p>

<div class="row mt-3">
  <div class="col-md-10 offset-md-1">
    {% include figure.liquid loading="eager" path="assets/img/projects/stationary_tpami/iam_curves.png" class="img-fluid rounded z-depth-1" zoomable=true caption="Average Accuracy up to task τ (AAτ) for CIFAR100R/10 with 31 tasks and two model replacements (boxed indices). Only d-Simplex-HOC and d-Simplex-FD improve after each replacement; all other methods degrade." %}
  </div>
</div>

<!-- ===================== CITATION ===================== -->
<div class="section-title">Citation</div>

<div style="position:relative;">
<pre class="citation-block" id="citation-block">@article{biondi2024stationary_journal,
  title   = {A Stationary (and Therefore Compatible) Representation is All You Need},
  author  = {Biondi, Niccolò and Pernici, Federico and Ricci, Simone and Del Bimbo, Alberto},
  journal = {IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year    = {2026},
  html    = {https://www.computer.org/csdl/journal/tp/5555/01/11515089/2gpcsTtMN3i}
}</pre>
<button class="copy-btn" onclick="copyBib()">Copy</button>
</div>

<!-- ===================== SCRIPTS ===================== -->
<script>
function switchTLDR(btn, level) {
  document.querySelectorAll('.tldr-depth-btn').forEach(b => b.classList.remove('tldr-active'));
  btn.classList.add('tldr-active');
  document.querySelectorAll('.tldr-panel').forEach(p => p.classList.add('d-none'));
  document.getElementById('tldr-' + level).classList.remove('d-none');
}
function copyBib() {
  var text = document.getElementById('citation-block').innerText;
  navigator.clipboard.writeText(text).then(function() {
    var btn = document.querySelector('.copy-btn');
    btn.textContent = 'Copied!';
    setTimeout(function() { btn.textContent = 'Copy'; }, 2000);
  });
}
</script>
