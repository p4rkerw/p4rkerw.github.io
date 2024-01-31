---
layout: archive
title: "People"
permalink: /people/
author_profile: true
---

{% include base_path %}

{% for post in site.publications %}
  {% include archive-single-pub.html %}
{% endfor %}
