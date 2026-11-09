---
layout: archive
title: "Software"
permalink: /software/
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/bridge.png
  actions:
    - label: "Our GitHub"
      url: https://github.com/p4rkerw
excerpt: "We develop open-source methods, workflows and containerized environments for single-cell, spatial and genomic analysis of kidney disease."
---

{% assign sw = site.software | sort: "date" | reverse %}
<div class="software-grid">
{% for post in sw %}{% include archive-single-software.html %}{% endfor %}
</div>
