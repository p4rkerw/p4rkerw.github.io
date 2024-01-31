---
layout: archive
title: "People"
permalink: /people/
author_profile: true
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /assets/images/balloons.png
  actions:
    - label: "Search PubMed"
      url: https://pubmed.ncbi.nlm.nih.gov/?term=parker+wilson
excerpt: "The Wilson lab is a dynamic community of physicans and scientists committed to open research."  
---

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single-pub.html %}
{% endfor %}
