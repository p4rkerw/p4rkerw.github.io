---
layout: archive
title: " "
permalink: /people/
author_profile: true
header:
  overlay_color: "#000"
  overlay_filter: "0.25"
  overlay_image: /assets/images/labphotos/wilsonlab_july_2025.JPG
---

<style>
.page-title, .page-header h1 {
  display: none;
}
</style>

{% include base_path %}

{% for post in site.people %}
  {% include archive-single-person.html %}
{% endfor %}
