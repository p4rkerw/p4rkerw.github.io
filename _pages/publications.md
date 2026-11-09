---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.35"
  overlay_image: /assets/images/balloons.png
  actions:
    - label: "Google Scholar"
      url: https://scholar.google.com/citations?user=2bYknIUAAAAJ&hl=en&oi=ao
    - label: "PubMed"
      url: https://pubmed.ncbi.nlm.nih.gov/?term=wilson+parker+c
excerpt: "The Wilson lab is committed to open science. We make our manuscripts, data and analysis code available to the research community."
---

<script type="text/javascript" src="https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js" async></script>

<p class="section-sub">Selected publications and preprints. Lab members are shown in <strong>bold</strong>. See <a href="https://scholar.google.com/citations?user=2bYknIUAAAAJ&hl=en&oi=ao">Google Scholar</a> for a complete list.</p>

{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign byyear = pubs | group_by_exp: "p", "p.date | date: '%Y'" %}
{% for y in byyear %}
<div class="pub-year">{{ y.name }}</div>
<div class="pub-list">
{% for post in y.items %}{% include archive-single-pub.html %}{% endfor %}
</div>
{% endfor %}
