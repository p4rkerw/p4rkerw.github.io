---
layout: archive
title: 
permalink: /people/
author_profile: true
---

{% include base_path %}

{% for post in site.people %}
  {% include archive-single-person.html %}
{% endfor %}
