---
title: "Analytic Reconstruction and Algebro-Geometric Structures in QCD: Two-Loop $pp \\rightarrow Vjj$ & One-Loop $pp \\rightarrow t\\bar{t}H$ & $HHH$"
event: SDU Seminar
event_url: 
location: SDU - Odense
summary: SDU Seminar - Oct 7, 2025 <br> Universe+ Seminar - Oct 22, 2025
abstract: 

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2025-10-07T15:00:00Z"
date_end: "2025-10-07T16:00:00Z"
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
slides: SDUOct2025

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.

# Enable math on this page?
math: true
---

*Abstract*

Loop amplitudes are central to precision collider phenomenology, yet their computation remains a major challenge due to the complexity of intermediate steps. A powerful modern strategy is to bypass this complexity through numerical evaluations over finite fields, followed by the reconstruction of the amplitudes’ analytic form from a set of numerical samples using number-theoretic and algebro-geometric techniques.

In this talk, I will present the recent re-computation of the two-loop leading-colour amplitudes for the production of a heavy electroweak vector boson, $V=\\\{W^\pm,Z,\gamma^*\\\}$, in association with two light jets at hadron colliders ($pp\rightarrow Vjj$) ([arXiv:2503.10595](https://arxiv.org/abs/2503.10595)), including leptonic decays of the electroweak boson ($V\rightarrow \ell\bar{\ell}$). Compared to the previous state-of-the-art result ([arXiv:2110.07541](https://arxiv.org/abs/2110.07541)), the new approach achieves a three-order-of-magnitude reduction in size (1.4 GB to 1.9 MB), while also lowering the number of required numerical samples from one million to fifty thousand. To illustrate the applicability of these techniques in settings with more massive external legs, I will also briefly discuss the one-loop processes $pp \to HHH$ and $pp \to t\bar t H$.

I will outline the core ingredients of this computation: a basis-change algorithm in the vector space of rational functions based on correlations among multivariate residues; numerical sampling in number fields with non-Archimedean metrics (finite fields and $p$-adic numbers); the use of redundant spinor-helicity variables organised via polynomial quotient rings; and the role of primary decompositions in identifying allowed multivariate partial fraction decompositions. These methods not only yield efficient and stable results ready for phenomenological applications, but also expose structural features that we expect to generalise to more complex multi-loop amplitudes.
