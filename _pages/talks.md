---
title: "Talks"
layout: archive
permalink: /talks/
author_profile: false
classes: wide
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/philadelphia_skyline.png
excerpt: "Invited lectures, grand rounds and conference presentations by Dr. Wilson and the lab."
---

{% assign talks = site.categories.talks %}
<div class="stats">
  {% assign arch = site.data.talks_archive %}
  {% assign inv = talks | where_exp: "t", "t.tags contains 'invited talk'" %}
  {% assign gr = talks | where_exp: "t", "t.tags contains 'grand rounds'" %}
  {% assign conf = talks | where_exp: "t", "t.tags contains 'conference'" %}
  <div class="card stat"><div class="stat__num">{{ talks | size | plus: arch.total }}</div><div class="stat__label">Total talks</div></div>
  <div class="card stat"><div class="stat__num">{{ conf | size | plus: arch.conference }}</div><div class="stat__label">Conferences</div></div>
  <div class="card stat"><div class="stat__num">{{ gr | size | plus: arch.grand_rounds }}</div><div class="stat__label">Grand Rounds</div></div>
  <div class="card stat"><div class="stat__num">{{ inv | size | plus: arch.invited }}</div><div class="stat__label">Invited Lectures</div></div>
</div>
<p class="section-sub">Totals include {{ arch.total }} talks given before the lab moved to Penn in January 2023. Talks since then are listed below.</p>

<table class="talks-table">
  <thead><tr><th>Date</th><th>Talk</th><th>Venue</th></tr></thead>
  <tbody>
  {% for post in talks %}
    <tr>
      <td>{{ post.date | date: "%b %Y" }}</td>
      <td><a href="{{ post.url | relative_url }}">{{ post.talk_title }}</a></td>
      <td>{{ post.venue }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
