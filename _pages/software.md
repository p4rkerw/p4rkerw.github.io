---
layout: archive
title: "Software and Repositories"
permalink: /software/
author_profile: true
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/bridge.png
  actions:
    - label: "Our GitHub"
      url: https://github.com/p4rkerw
excerpt: "The Wilson lab is committed to open and reproducible data analysis. We develop software, workflows and containerized environments that we make available to the research community."
---

{% include base_path %}

{% for post in site.software reversed %}
  {% include archive-single-software.html %}
{% endfor %}

