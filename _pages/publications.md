---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /assets/images/balloons.png
  actions:
    - label: "Search PubMed"
      url: https://pubmed.ncbi.nlm.nih.gov/?term=parker+wilson
excerpt: "The Wilson lab is committed to open science. We strive to make our manuscripts, data and analysis available to the research community."  
---

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single-pub.html %}
{% endfor %}


