---
title: "Data & Resources"
layout: archive
permalink: /data/
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.45"
  overlay_image: /assets/images/visium_clusters.png
excerpt: "Open single-cell, multiome and spatial datasets from human and mouse kidney, with the code to reproduce every analysis."
---

<p class="section-sub">All sequencing data from our published studies are deposited in NCBI GEO. Each dataset links to its paper and, where available, a containerized analysis workflow.</p>

{% assign lab = site.data.datasets | where: "role", "lab" %}
{% assign collab = site.data.datasets | where: "role", "collab" %}

<h2 class="section-title">Wilson lab datasets</h2>
<div class="data-grid">
{% for d in lab %}{% include dataset-card.html d=d %}{% endfor %}
</div>

<h2 class="section-title">Collaborative datasets</h2>
<div class="data-grid">
{% for d in collab %}{% include dataset-card.html d=d %}{% endfor %}
</div>

<h2 class="section-title">Software &amp; workflows</h2>
<p>Containerized pipelines and methods for single-cell, allele-specific and copy-number analysis are on our <a href="/software/">Software</a> page and on <a href="https://github.com/p4rkerw">GitHub</a>.</p>

<h2 class="section-title">Related community resources</h2>
<ul class="pill-list">
  <li><a href="https://atlas.kpmp.org/">Kidney Precision Medicine Project (KPMP) Atlas</a></li>
  <li><a href="http://humphreyslab.com/SingleCell/">Humphreys Lab Kidney Interactive Transcriptomics</a></li>
  <li><a href="https://hpap.pmacs.upenn.edu/">Human Pancreas Analysis Program (HPAP)</a></li>
</ul>

<p class="section-sub">Questions about data access or reuse? <a href="mailto:parker.wilson@pennmedicine.upenn.edu">Email us</a>.</p>
