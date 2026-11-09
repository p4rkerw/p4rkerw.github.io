---
layout: archive
title: "Our Team"
permalink: /people/
author_profile: false
classes: [wide, people-page]
header:
  overlay_color: "#000"
  overlay_filter: "linear-gradient(rgba(1,31,91,0.15), rgba(1,31,91,0.55))"
  overlay_image: /assets/images/labphotos/wilsonlab_2026.jpg
  image_description: "The Wilson Lab, August 2026"
excerpt: "Physicians, scientists and engineers working together to understand kidney disease at single-cell resolution."
---

{% assign people = site.people | sort: "order" %}
{% assign pi = people | where: "status", "pi" %}
{% assign current = people | where: "status", "current" %}
{% assign alumni = people | where: "status", "alumni" %}

<h2 class="section-title">Principal Investigator</h2>
{% for p in pi %}{% include person-card.html person=p variant="pi" %}{% endfor %}

<h2 class="section-title">Lab Members</h2>
<div class="people-grid">
{% for p in current %}{% include person-card.html person=p %}{% endfor %}
</div>

<h2 class="section-title">Lab Photos</h2>
<div class="lab-photos-grid">
  <figure class="lab-photo">
    <img src="{{ '/assets/images/labphotos/wilsonlab_2026.jpg' | relative_url }}" alt="Wilson Lab 2026" loading="lazy">
    <figcaption><span class="year-chip">2026</span>Left to right: Huihan Liu, Lisa Traczyk, Yibo Shi, Yongqi Huang, Amit Verma, Roy Chen, Gary Wang, Parker Wilson</figcaption>
  </figure>
  <figure class="lab-photo">
    <img src="{{ '/assets/images/labphotos/wilsonlab_july_2025.JPG' | relative_url }}" alt="Wilson Lab 2025" loading="lazy">
    <figcaption><span class="year-chip">2025</span>Left to right: Gary Wang, Lisa Traczyk, Sidney Martin, Mia Pierce, Parker Wilson, Amit Verma</figcaption>
  </figure>
</div>

<h2 class="section-title">Alumni</h2>
<div class="people-grid people-grid--alumni">
{% for p in alumni %}{% include person-card.html person=p %}{% endfor %}
</div>
