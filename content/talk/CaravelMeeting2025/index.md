---
title: "Amplitude Reconstruction: Tools and Methods"
event: Caravel Meeting 2025
event_url: 
location: CERN
summary: Caravel Meeting - June 26, 2025
abstract: 

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2025-06-16T12:20:00Z"
date_end: "2025-06-16T12:45:00Z"
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
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: CaravelMeeting2025

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.

# Enable math on this page?
math: true
---

*Abstract*

Loop amplitudes are essential ingredients in precision simulations of particle collisions at the LHC. Their computation poses both conceptual and computational challenges. A powerful and increasingly popular strategy to bypass intermediate bottlenecks in integrand reduction is to first evaluate amplitudes numerically over finite fields, and then recover their analytic form through analytic reconstruction.

In this talk, I will present two recent computations of fully analytic amplitudes obtained using this approach. The first is for the two-loop process $pp\rightarrow V(\rightarrow \bar\ell\ell)jj$ in the leading-color approximation ([arXiv:2503.10595](https://arxiv.org/abs/2503.10595)). In this case, we revisited a previous result ([arXiv:2110.07541](https://arxiv.org/abs/2110.07541)) and drastically simplified the amplitude from 1.4 GB to 1.9 MB, while also reducing the number of numerical samples from 1 million to 50 thousand.

The second computation is for the one-loop amplitude for $q\bar{q}\rightarrow t\bar{t}H$
([arXiv:2504.19909](https://arxiv.org/abs/2504.19909)). This is the first time an amplitude has been reconstructed in the massive spinor-helicity formalism, which provides a minimal parametrisation. 

I will outline key aspects of both computations, focusing on the reconstruction technique, and in particular the role of minimal spinor-helicity parametrisations, the choice of efficient bases for master integral coefficients, and their representation via multivariate partial fractions. In this way, we uncover structural features of the amplitudes and provide numerically stable and efficient implementations suitable for phenomenological applications and further theoretical studies.