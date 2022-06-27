---
layout: archive
title: "Software and Repositories"
permalink: /software/
author_profile: true
---

{% include base_path %}

{% for post in site.software reversed %}
  {% include archive-single-software.html %}
{% endfor %}


# [**🌶️SALSA! Single Cell Allele Specific Analysis**](https://github.com/p4rkerw/SALSA) <br>
SALSA is a workflow for genotyping, phasing, mapping bias correction, and single cell allele-specific counting of single cell RNA and ATAC datasets.


# [**Muto_Wilson_NComm_2020**](https://github.com/p4rkerw/Muto_Wilson_NComm_2020) <br>
This repository includes all of the code for the corresponding manuscript by Muto and Wilson et al. It is a workflow for integration and analysis of paired single nucleus RNA and ATAC datasets from five control kidney cortex samples.
