---
tile: "Reconstructing and simplifying rational coefficients in multi-loop scattering amplitudes"
summary: 
authors: ["Giuseppe De Laurentis"]
tags: [QCD, Scattering Amplitudes]
categories: []
date: "2026-01-22T14:30:00Z"
markup: blackfriday
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: white
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula

---

<style>
.reveal mjx-container {
  font-size: 115% !important;
}

.reveal .MathJax,
.reveal .MathJax_Display,
.reveal .MathJax_CHTML {
  font-size: 115% !important;
}
</style>

<script>
window.addEventListener("load", function () {
  function relayoutReveal() {
    if (window.Reveal && typeof Reveal.layout === "function") {
      Reveal.layout();
    }
  }

  if (window.MathJax && MathJax.startup && MathJax.startup.promise) {
    MathJax.startup.promise.then(function () {
      relayoutReveal();
      setTimeout(relayoutReveal, 100);
      setTimeout(relayoutReveal, 500);
    });
  } else {
    setTimeout(relayoutReveal, 500);
  }
});
</script>

<!---
<style>
.reveal mjx-container[display="true"] {
  font-size: 130% !important;
}
</style>

<script>
window.addEventListener("load", function () {
  if (window.Reveal && typeof Reveal.configure === "function") {
    Reveal.configure({
      minScale: 1,
      maxScale: 1
    });
    Reveal.layout();
  }
});
</script>
--->

<section>

{{< slide background-image="LHCcern.jpg" >}}

<h3 style="margin-top: 2mm; margin-left: -10mm; margin-right: -10mm; margin-bottom: -5mm;">
	<b style="margin-top:15mm; font-size: 30pt; text-transform: none; font-variant-caps: small-caps;">
     Analytic Multi-Loop Helicity Amplitudes in QCD
     </b>
</h3>
<span style="margin-top:-5mm; font-size: 18pt;">
     Giuseppe De Laurentis
</span>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     The full physical information of a color-ordered helicity amplitude is in the finite remainder:
</div>
<span style="font-size: 13pt; margin-bottom: -14mm; margin-top: -3mm; float: right; font-align: right;"> 
<a href=https://www.sciencedirect.com/science/article/abs/pii/S0370269398003323?via%3Dihub>Catani ('98) </a> 
</span>
<span style="font-size: 13pt; margin-bottom: -14mm; margin-top: 2mm; float: right; font-align: right;"> 
<a href=https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.102.162001>Becher, Neubert ('09) </a>
</span>
<span style="font-size: 13pt; margin-bottom: -14mm; margin-top: 7mm; float: right; font-align: right;"> 
<a  href=https://arxiv.org/abs/0901.1091>Gardi, Magnea ('09) </a> 
</span>
<span style="font-size: 13pt; margin-bottom: -20mm; margin-top: 12mm; float: right; font-align: right;"> 
<a href=https://inspirehep.net/literature/920274>Weinzierl ('11) </a>
</span>
<div style="font-size: 14pt; margin-top: 5mm; margin-bottom: 5mm; float: center;">
$$ 
\textstyle \mathcal{R}^{\ell-\text{loop}}_{n-\text{point}}(|i⟩_{\alpha}, [i|_{\dot\alpha}) = \sum_i {\color{red}{r_{i}}}(|i⟩_{\alpha}, [i|_{\dot\alpha}) \, {\color{blue}{G_i}}(|i⟩_{\alpha} {\scriptsize\times} [i|_{\dot\alpha}) \, .
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 0mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     <b><i>Challenges:</i></b>
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Compute the <span style="font-size: 15pt;">$\color{blue}{G_i}\,$</span>, a basis of transcendental functions, e.g. the <i>Pentagon Functions</i>;
</div>
<a style="font-size: 13pt; display: inline-block; text-align: right; float: right; margin-top: -2mm; margin-bottom: -2mm; margin-left: 2mm;" href=https://arxiv.org/abs/2306.15431> + Abreu, Ita, Page, Tschernow ('23) </a>
<a style="font-size: 13pt; display: inline-block; text-align: right; float: right; margin-top: -2mm; margin-bottom: -2mm; margin-left: 2mm;" href=https://arxiv.org/abs/2110.10111> + Zoia ('21) </a>
<a style="font-size: 13pt; display: inline-block; text-align: right; float: right; margin-top: -2mm; margin-bottom: -2mm; margin-right: 0mm; " href=https://arxiv.org/abs/2009.07803> Chicherin, Sotnikov ('20) </a> 

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 7mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Reconstruct the <span style="font-size: 15pt;">$\color{red}{r_{i}}\,$</span>, functions in the field of fractions over a polynomial quotient ring,
</div>
<a style="font-size: 13pt; display: inline-block; text-align: right; float: right; margin-top: -2mm; margin-bottom: -2mm; margin-left: 2mm;" href=https://arxiv.org/abs/1406.4513>
GDL, Page ('22).
</a>
<a style="font-size: 13pt; display: inline-block; text-align: right; float: right; margin-top: -2mm; margin-bottom: -2mm; margin-left: 2mm;" href=https://arxiv.org/abs/1406.4513>
GDL, Maitre ('19);
</a>
<a style="font-size: 13pt; display: inline-block; text-align: right; float: right; margin-top: -2mm; margin-bottom: -2mm; margin-left: 2mm;" href=https://arxiv.org/abs/1608.01902>
Peraro ('16); 
</a>
<div style="font-size: 14pt; margin-top: 9mm; margin-bottom: 1mm">
$$
\displaystyle \kern10mm R_{n} = \mathbb{F}\Big[|1⟩_{\alpha}, [1|_{\dot\alpha}, \dots, |n⟩_{\alpha}, [n|_{\dot\alpha} \Big] \Big/ J \qquad \text{with} \qquad J = \text{Ideal} \Big( {\textstyle \sum_{i=1}^n} |i\rangle[ i | \Big) \, ,
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 3mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ in connection with algebraic geometry, and extended to massive particles (spin-spinors).
</div>
<span style="font-size: 13pt; margin-bottom: -1mm; margin-top: -3mm; float: right; font-align: right;"> 
<a href="https://arxiv.org/abs/1709.04891"> Arkani-Hamed, Huang, Huang ('17); </a> 
<a href="https://arxiv.org/abs/1802.06730"> Ochirov ('18); </a>
<a href="https://arxiv.org/abs/1809.09644"> Shadmi, Weiss ('18); </a> 
<a href="https://arxiv.org/abs/arXiv:2504.19909"> Campbell, GDL, Ellis ('25); </a>
<a href="https://arxiv.org/abs/arXiv:2603.10269"> GDL, Melnikov, Tresoldi ('26) </a>
</span>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 7mm; margin-left: 2mm; margin-right: 2mm;">
     <b><i>Amplitudes we computed:</i></b> $\kern3mm$ <span style="font-size: 13pt;">GDL + [Abreu, Campbell, Ellis, Ita, Klinkert, Kuschke, Maitre, Page, Ruf, Seth, Sotnikov, ...]</span>
</div>
<div>
<img src="GDLTableTransparent2.png"; style="max-width:950px; float:center; border:none; margin-top: -3mm; margin-bottom: 0mm;">
</div>


<span style="font-size: 15pt;">$\color{red}{r_{i}}\,$</span> known since
<a style="font-size: large; display: inline-block; text-align: right; float: right; margin-top: 2mm; margin-right: 0mm; " href=https://arxiv.org/abs/2605.04009> GDL, Ita, Kuschke, Ruf, Sotnikov ('26) </a> 

LCD d.o.f.: 30K, 250K, 25M, 80M


</section>


<!-- REVEAL.JS CUSTOMIZATION -->

<!-- Include MathJax library -->
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.9/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

<!-- Include Reveal.js and the Math plugin -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/reveal.js/5.0.2/reveal.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/reveal.js/5.0.2/plugin/math/math.js"></script>

<!-- Initialize Reveal.js with the MathJax plugin -->
<script>
  Reveal.initialize({
    history: true,
    slideNumber: false,
    plugins: [ RevealMath ],
    math: {
      inlineMath: [ ['\\(', '\\)'] ],
      displayMath: [ ['\\[', '\\]'] ],
      mathjax: 'https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.9/MathJax.js',
      config: 'TeX-MML-AM_CHTML',
      CommonHTML: {
        scale: 100, // Adjust the font size as needed
      },
    }
  });
</script>
