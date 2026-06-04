---
layout: page
title: "PEPR: Privileged Event-based Predictive Regularization for Domain Generalization"
description: CVPR 2026 Findings
img: assets/img/projects/pepr/teaser.png
importance: 2
category: research
permalink: /projects/pepr/
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
    margin-bottom: 0.4rem;
  }
  .project-venue-note {
    display: inline-block;
    font-size: 0.8rem;
    color: var(--global-text-color-light);
    margin-left: 0.4rem;
  }
  .project-links { display: flex; justify-content: center; gap: 0.5rem; flex-wrap: wrap; margin: 1rem 0 2rem; }
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
  .img-placeholder {
    background: var(--global-card-bg-color);
    border: 2px dashed var(--global-divider-color);
    border-radius: 8px;
    padding: 3rem 1rem;
    text-align: center;
    color: var(--global-text-color-light);
    font-size: 0.9rem;
  }
---

<!-- ===================== HEADER ===================== -->
<div class="project-header">
  <div class="project-authors">
    Gabriele Magrini&ensp;·&ensp;
    Federico Becattini&ensp;·&ensp;
    <a href="https://niccobiondi.github.io">Niccolò Biondi</a>&ensp;·&ensp;
    Pietro Pala
  </div>
  <div style="margin-bottom:0.8rem;">
    <span class="project-venue-badge">CVPR 2026</span>
    <span class="project-venue-note">Findings</span>
  </div>
  <div class="project-links">
    <a href="https://arxiv.org/abs/2602.04583">📄 arXiv</a>
    <a href="https://miccunifi.github.io/PEPR/">🌐 Original page</a>
    <a href="https://github.com/miccunifi/PEPR">💻 Code</a>
  </div>
</div>

<!-- ===================== TEASER ===================== -->
<div class="row justify-content-center mb-4">
  <div class="col-md-10">
    <img src="/assets/img/projects/pepr/teaser.png" alt="PEPR teaser" style="width:100%; border-radius:8px;" />
    <div class="caption mt-2" style="text-align:center; font-size:0.85rem; color:var(--global-text-color-light);">
      PEPR trains an RGB encoder to <em>predict</em> event-derived latent representations,
      transferring domain robustness to a model that requires only RGB at test time.
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
    Train with event cameras as a privileged signal — discard them at test time — and get a
    more domain-robust RGB model <em>without any extra sensors at inference</em>.
  </div>

  <div class="tldr-panel d-none" id="tldr-medium">
    <span class="tldr-tag">~80 words</span>
    Domain shift is a key obstacle for visual perception models. PEPR exploits
    <strong>event cameras as privileged information</strong>: available only during training,
    they provide domain-invariant supervision via a predictor that trains the RGB encoder to
    <strong>predict event-derived latent representations</strong> rather than align features
    directly. This transfers robustness without forcing dense RGB features to match sparse
    event outputs. At test time, only the standard RGB model is used — no additional sensors
    or inference modules required.
  </div>

  <div class="tldr-panel d-none" id="tldr-long">
    <span class="tldr-tag">Abstract</span>
    Deep neural networks for visual perception are highly susceptible to domain shift,
    limiting their deployment under conditions that differ from the training data.
    Event cameras offer a compelling complement to RGB sensors, as their output is
    sparse yet more domain-invariant. However, directly aligning RGB and event features
    is difficult: RGB streams are semantically dense but domain-dependent, while event
    streams are sparse yet more domain-invariant. We propose PEPR, a cross-modal learning
    framework that uses event cameras exclusively during training as privileged information.
    Rather than directly aligning RGB and event features, PEPR trains the RGB encoder to
    predict event-derived representations through a dedicated predictor module. This
    transfers domain robustness from the event stream to the RGB encoder while preserving
    semantic detail. At inference, the event branch is discarded, leaving an RGB-only
    model with improved domain generalisation across semantic segmentation and object
    detection benchmarks.
  </div>
</div>

<!-- ===================== KEY IDEAS ===================== -->
<div class="section-title">Key Ideas</div>

<div class="row g-3">
  <div class="col-md-4">
    <div class="contrib-card">
      <div class="contrib-card-num">1</div>
      <h6>Prediction over Alignment</h6>
      <p>Instead of forcing dense RGB features to directly match sparse event outputs,
      PEPR trains the RGB encoder to <em>predict</em> event-derived latent targets via
      a lightweight predictor module.</p>
    </div>
  </div>
  <div class="col-md-4">
    <div class="contrib-card">
      <div class="contrib-card-num">2</div>
      <h6>Events as Privileged Information</h6>
      <p>Event cameras act as a training-only supervisory signal. They provide
      domain-invariant cues during training and are <em>completely discarded</em>
      after training — no paired data needed at deployment.</p>
    </div>
  </div>
  <div class="col-md-4">
    <div class="contrib-card">
      <div class="contrib-card-num">3</div>
      <h6>RGB-only Deployment</h6>
      <p>At test time, PEPR runs with the standard RGB model — no event camera,
      no additional sensors, no extra inference modules. The robustness is baked
      into the encoder weights.</p>
    </div>
  </div>
</div>

<!-- ===================== METHOD ===================== -->
<div class="section-title">Method</div>

<p>
  During training, PEPR combines four components: an <strong>RGB encoder</strong> (backbone),
  a <strong>task prediction head</strong> (segmentation or detection), a
  <strong>privileged event encoder</strong>, and a <strong>predictor module</strong> that
  maps RGB latents to event latent targets.
  The total loss combines the standard task loss with the prediction loss between
  RGB-predicted and event-derived representations.
  After training, the event encoder and predictor are discarded.
</p>

<div class="method-box">
  <strong>Key insight:</strong> Predicting event latents forces the RGB encoder to learn
  representations that are predictive of domain-invariant event features — without
  requiring the two modalities to share the same feature space.
</div>

<h5 style="margin-top:2rem; margin-bottom:0.8rem; font-weight:700;">Patch Selection Mechanism</h5>

<p>
  A core challenge in cross-modal predictive learning is that event cameras produce
  <em>sparse</em> outputs: most of the spatial grid carries no signal at any given moment.
  Supervising every RGB patch against an empty event target would flood the predictor
  with uninformative gradients and destabilize training.
</p>
<p>
  PEPR addresses this with a <strong>patch selection mechanism</strong>: only the spatial
  patches where the event stream is active — i.e., where events actually fired — are
  selected as prediction targets for the RGB encoder. Concretely, the event representation
  is divided into non-overlapping patches and those with sufficient event density are
  retained. The predictor then aligns the corresponding RGB patches only at those locations,
  concentrating the supervision signal where the event modality is informative.
  This selective alignment makes the training loss meaningful and prevents the RGB encoder
  from being pulled toward trivial or noisy targets.
</p>

<div class="row justify-content-center mt-3">
  <div class="col-md-10">
    <img src="/assets/img/projects/pepr/patch_selection.png" alt="PEPR patch selection mechanism" style="width:100%; border-radius:8px;" />
    <div class="caption mt-2" style="text-align:center; font-size:0.85rem; color:var(--global-text-color-light);">
      Patch selection: only spatially active event patches (highlighted) are used as
      prediction targets, focusing supervision where the event signal is informative.
    </div>
  </div>
</div>

<!-- ===================== RESULTS ===================== -->
<div class="section-title">Results</div>

<p>
  PEPR is evaluated on three benchmarks spanning semantic segmentation and object detection
  under domain shift, using the FRED, DSEC, Hard-DSEC-DET, Cityscapes, and Cityscapes
  Adverse datasets. A selection of key results is shown below;
  <strong>many additional experiments and ablations are reported in the
  <a href="https://arxiv.org/pdf/2602.04583">full CVPR 2026 Findings paper</a></strong>.
</p>

<div class="row justify-content-center mt-3">
  <div class="col-md-10">
    <img src="/assets/img/projects/pepr/segmentation.png" alt="PEPR segmentation results" style="width:100%; border-radius:8px;" />
    <div class="caption mt-2" style="text-align:center; font-size:0.85rem; color:var(--global-text-color-light);">
      Semantic segmentation results under domain shift.
    </div>
  </div>
</div>

<div class="row justify-content-center mt-4">
  <div class="col-md-10">
    <img src="/assets/img/projects/pepr/fred.png" alt="PEPR FRED dataset results" style="width:100%; border-radius:8px;" />
    <div class="caption mt-2" style="text-align:center; font-size:0.85rem; color:var(--global-text-color-light);">
      Results on the FRED benchmark.
    </div>
  </div>
</div>

<div class="row justify-content-center mt-4">
  <div class="col-md-10">
    <img src="/assets/img/projects/pepr/harddsec.png" alt="PEPR Hard-DSEC-DET results" style="width:100%; border-radius:8px;" />
    <div class="caption mt-2" style="text-align:center; font-size:0.85rem; color:var(--global-text-color-light);">
      Object detection results on the Hard-DSEC-DET benchmark.
    </div>
  </div>
</div>

<!-- ===================== CITATION ===================== -->
<div class="section-title">Citation</div>

<div style="position:relative;">
<pre class="citation-block" id="citation-block">@inproceedings{magrini2026pepr,
  title     = {PEPR: Privileged Event-based Predictive Regularization for Domain Generalization},
  author    = {Magrini, Gabriele and Becattini, Federico and Biondi, Niccolò and Pala, Pietro},
  booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  note      = {Findings},
  year      = {2026},
  arxiv     = {2602.04583}
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
