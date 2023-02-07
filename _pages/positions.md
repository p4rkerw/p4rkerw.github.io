---
title: "Positions"
layout: home
sitemap: false
permalink: /positions/
author_profile: true
---

{% include base_path %}

{% for post in site.positions reversed %}
  {% include archive-single-position.html %}
{% endfor %}

