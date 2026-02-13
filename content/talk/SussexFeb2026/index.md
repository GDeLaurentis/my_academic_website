---
title: "Analytic Reconstruction of Two-Loop QCD Amplitudes"
event: SDU Seminar
event_url: 
location: University of Sussex
summary: University of Sussex - Feb 16, 2026
abstract: 

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2026-02-16T15:30:00Z"
date_end: "2026-02-16T17:00:00Z"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2017-01-01T00:00:00Z"

authors: ["Giuseppe De Laurentis"]
tags: []

# Is this a featured talk? (true/false)
featured: false

# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
#   focal_point: Right

links:
- icon: arxiv
  icon_pack: ai
  name: arXiv:2503.10595
  url: https://arxiv.org/abs/2503.10595
- icon: arxiv
  icon_pack: ai
  name: arXiv:2504.19909
  url: https://arxiv.org/abs/2504.19909
- icon: arxiv
  icon_pack: ai
  name: arXiv:2507.19313
  url: https://arxiv.org/abs/2507.19313
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: SussexFeb2026

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.

# Enable math on this page?
math: true
---

*Abstract*

Loop amplitudes are central to precision collider phenomenology, yet their computation remains challenging due to the complexity of intermediate steps. A powerful modern strategy is to bypass much of this complexity by performing numerical evaluations over finite fields and reconstructing analytic expressions from numerical data using number-theoretic and algebro-geometric techniques.

In this talk, I will present a recent re-computation of the two-loop leading-colour amplitudes for the production of a heavy electroweak vector boson in association with two jets at hadron colliders (pp → Vjj). Compared to the previous state of the art, the new result achieves a three-order-of-magnitude reduction in size (from 1.4 GB to 1.9 MB) and reduces the required number of numerical samples from one million to fifty thousand. I will also briefly discuss applications to processes with massive external legs, including pp → tt̄H and HHH at one loop.

I will outline the core ingredients of this computation: a basis-change algorithm in the vector space of rational functions based on correlations among multivariate residues; numerical sampling in number fields with non-Archimedean metrics (finite fields and p-adic numbers); redundant spinor-helicity variables organised via polynomial quotient rings; and primary decompositions used to identify allowed multivariate partial fraction decompositions. Beyond enabling efficient phenomenological applications, these methods expose structural features that are expected to generalise to more complex QCD amplitudes.
