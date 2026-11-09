---
layout: splash
title: " "
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/banner.png
  actions:
    - label: "Learn More"
      url: /about/
    - label: "Meet the Team"
      url: /people/
excerpt: "The Wilson lab at the University of Pennsylvania uses cutting edge technologies like single cell sequencing and spatial profiling to develop new therapies for chronic kidney disease."

feature_row:
  - image_path: assets/images/single_cell_overview.png
    excerpt: "We can analyze thousands or even millions of cells in a single experiment to ask how cell composition and signaling pathways change in disease"
    title: "Single cell sequencing"
    url: /about/#single-cell-multiomics
    btn_label: "Read More"
    btn_class: "btn--primary"

  - image_path: assets/images/genetic_variation_overview.png
    excerpt: "We can measure the effect of germline and somatic variation in single cells to ask how genetic background affects disease progression"
    title: "Genetics in single cells"
    url: /about/#genetics-in-single-cells
    btn_label: "Read More"
    btn_class: "btn--primary"

  - image_path: assets/images/visium_clusters.png
    excerpt: "We can determine the location of injured cell types in the kidney and quantify changes in intercellular signaling"
    title: "Spatial profiling"
    url: /about/#spatial-profiling
    btn_label: "Read More"
    btn_class: "btn--primary"

  - image_path: assets/images/digital_pcr_overview.png
    excerpt: "We have developed digital PCR assays to quantify the abundance of chromosomal gains and losses in complex tissues"
    title: "Digital PCR and Somatic Mosaicism"
    url: /about/#somatic-mosaicism
    btn_label: "Read More"
    btn_class: "btn--primary"
---


<div class="home-section">
  <div class="home-section__head"><h2>Our research</h2><a href="/about/">About the lab &rarr;</a></div>
</div>

{% include feature_row %}

<div class="home-section">
  <div class="home-section__head"><h2>Latest news</h2><a href="/year-archive/#news">All news &rarr;</a></div>
  <div class="news-grid">
  {% assign shown = 0 %}
  {% for post in site.posts %}{% unless post.categories contains "talks" %}{% if shown < 3 %}{% assign shown = shown | plus: 1 %}
    <article class="card news-card">
      <div class="timeline__meta"><time>{{ post.date | date: "%b %-d, %Y" }}</time><span class="badge">News</span></div>
      <h3 class="timeline__title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="timeline__excerpt">{{ post.excerpt | markdownify | strip_html | truncate: 140 }}</p>
    </article>
  {% endif %}{% endunless %}{% endfor %}
  </div>
</div>

<div class="home-section">
  <div class="home-section__head"><h2>Recent talks</h2><a href="/talks/">All talks &rarr;</a></div>
  <div class="news-grid">
  {% for post in site.categories.talks limit:3 %}
    <article class="card news-card">
      <div class="timeline__meta"><time>{{ post.date | date: "%b %Y" }}</time><span class="badge badge--talk">Talk</span></div>
      <h3 class="timeline__title"><a href="{{ post.url | relative_url }}">{{ post.talk_title }}</a></h3>
      <p class="timeline__excerpt"><i class="fas fa-map-marker-alt"></i> {{ post.venue }}</p>
    </article>
  {% endfor %}
  </div>
</div>

<div class="home-section">
  <figure class="lab-photo">
    <img src="/assets/images/labphotos/wilsonlab_2026.jpg" alt="The Wilson Lab, 2026" loading="lazy">
    <figcaption>The Wilson Lab, 2026 &middot; <a href="/people/">Meet the team</a></figcaption>
  </figure>
</div>

<div class="home-section join-cta">
  <div>
    <h2>Join the lab!</h2>
    <p>We're always looking for talented researchers and collaborators. Send us an email or find us on social media.</p>
  </div>
  <a class="btn btn--large" href="mailto:parker.wilson@pennmedicine.upenn.edu">Get in touch</a>
</div>
