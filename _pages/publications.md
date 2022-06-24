---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

<!---You can find the complete publication list on <a href="https://scholar.google.co.uk/citations?user=-peQ4ZsAAAAJ&hl=en">
<span style="color:gray">my Google Scholar profile</span></a>. A complete list of bio<font color="red">R</font>xiv preprints on <a href="https://rxivist.org/authors/204048">
<span style="color:gray">my Rxivist profile</span></a>.--->

<ul style="margin:0;padding:0">
{% for post in site.publications reversed %}

  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2 id="y{{post.date | date: "%Y"}}"><span style="color:gray">{{ currentdate }}</span></h2>
    <ul style="margin:0;padding:0">
    {% assign date = currentdate %}
  {% endif %}
  {% if post.authors contains 'Giuseppe Vicidomini' %}
    {% include archive-single-pub.html %}
  {% endif %}
  {% if forloop.last %}</ul>{% endif %}

{% endfor %}

