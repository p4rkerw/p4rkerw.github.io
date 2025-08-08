---
layout: archive
title: " "
permalink: /people/
author_profile: true
header:
  overlay_image: /assets/images/labphotos/wilsonlab_july_2025.png
---

{% include base_path %}

{% for post in site.people %}
  {% include archive-single-person.html %}
{% endfor %}
