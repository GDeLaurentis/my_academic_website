---
tile: "Towards the complete NNLO BFKL Kernel"
summary: 
authors: ["Giuseppe De Laurentis"]
tags: [QCD, Scattering Amplitudes]
categories: []
date: "2023-05-15T30:00:00Z"
markup: blackfriday
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: white
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula

---

{{< slide background-image="particle_tracks.jpg" >}}

<h3 style="margin-top:5mm; margin-left: -10mm; margin-right: -10mm;">
	<b style="margin-top:15mm; font-size: 31pt; text-transform: none;">
          Towards the complete NNLO BFKL Kernel
	</b>
</h3>

<div style="font-size: x-large; margin-top:8mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
<div style="font-size: 15pt; margin-bottom:0mm;"> One Emission at Two Loops </div>
<div style="font-size: 15pt; margin-bottom:0mm;"><a href="https://arxiv.org/pdf/2412.20578">arXiv:2412.20578</a> <a href="https://link.springer.com/article/10.1007/JHEP04(2025)161">(10.1007/JHEP04(2025)161)</a></div>
<div style="font-size: 15pt; margin-bottom:0mm;"> with S. Abreu, G. Falcioni, E. Gardi, C. Milloy, L. Vernazza </div>
<br>
<div style="font-size: 15pt; margin-bottom:0mm;"> Two Emissions at One Loop </div>
<div style="font-size: 15pt; margin-bottom:0mm;"> To Appear </div>
<div style="font-size: 15pt; margin-bottom:10mm;"> with E. Byrne, V. Del Duca, E. Gardi, J. Smillie </div>

REF Conference
<div style="font-size: large; margin-top:-5mm; margin-bottom:5mm"> Milan, IT </div>
<p style="line-height: 0.05;"> <img src="UniEdinburghLogo-transparent.png"; style="max-width:120px;float:center;border:none;margin-bottom:5mm;"> 
<br><br><br>
<span style="font-size: 11pt; margin-top: 10mm;">Find these slides at  <a href="/slides/REFOct2025/#/">gdelaurentis.github.io/slides/REFOct2025</a> </span>
</div>

---

<section>

{{< slide background-image="LHCcern.jpg" >}}

# Introduction

---

<b style="font-variant: small-caps; font-size: 32pt"> Large Logarithms from Big Rapidity Gaps  </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 0mm; margin-left: 0mm;">
     $\circ\,$ In <span style="font-size: 15pt">$2\to 2$</span> scattering, in the <b>forward limit</b> <span style="font-size: 15pt">$s \gg t$</span> (large CoM energy vs. momentum transfer)
</div>
<img src="forward_diagram.png" style="max-width:100mm; margin-top:-4mm; margin-bottom:-7mm;">
<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 0mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ final state emissions develop <b> large rapidity gaps </b>. The cross section grows as
</div>
<div style="font-size: 16pt; margin-top: 0mm; margin-bottom: -3mm">
$$
\sigma \approx \mathcal{O}\big(\alpha_s^n \log^n(s/|t|)\big )
$$
</div>
<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 0mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ which is unphysically large (e.g. it violates the Froissart bound).
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 8mm; margin-left: 0mm;">
     $\circ\,$ The BFKL kernel captures the <b>exponentiation</b> of these <b>large logarithms</b>,<br>
     $\phantom{\circ}\,$ allowing us to <b>resum</b> their contribution to the cross section.
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 8mm; margin-left: 0mm;">
     $\circ\,$ In this kinematic limit, known as <b>Multi-Regge Kinematics</b> (MRK), an effective particle is <br>
     $\phantom{\circ}\,$ exchanged in the t-channel, a Reggeon, from which more rapidity-gapped radiation is emitted.
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Expanding Amplitudes in MRK and NMRK </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ In the (N)MRK limit the amplitude factorizes as follows
</div>

---

<b style="font-variant: small-caps; font-size: 34pt; magin-bottom: -10mm;"> Minimal Variables for Multi-Regge Kinematics </b> <br>

<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: -4mm;">
$\circ$ The MRK limit is a two-variable problem
</div>


<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: 2mm;">
$\circ$ The NMRK limit is a five-variable problem
</div>


</section>

---

<section>

{{< slide background-image="Feynman-Diagrams-transparent.png" >}}

<h1 style="margin-top: -2mm;"> Kernel Components </h1>

---

<b style="font-variant: small-caps; font-size: 32pt"> Leading Order Kernel Components </b>
<div  style="text-align: left; font-size: 16pt; margin-bottom: 5mm; margin-top: -6mm; text-align: center;">
Leading-Log (LL) Resummation: <span style="font-size: 14pt;">$\mathcal{O}\big(\alpha_s^n \log^n(s/|t|)\big )$</span>
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 5mm; margin-top: 5mm;">
     $\circ\,$ The two components of the leading order (LO) BFKL kernel, <br>
     $\phantom{\circ}\,$ required for resummation of leading logarithms (LL), are
</div>

<img src="LOKernel.png" style="max-width: 130mm; margin-top: 0mm; margin-bottom: 0mm;">

<span style="font-size: 14pt; margin-top: -5mm; margin-bottom: 5mm; float: right; font-align: right;"> <a href="https://arxiv.org/abs/2204.12459"> Byrne, Del Duca, Dixon, Gardi, Smillie </a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 5mm; margin-top: 10mm;">
     $\phantom{\circ}\,$ (a) is a correction to the Regge trajectory <br>
     $\phantom{\circ}\,$ (b) is the leading order central emission vertex (CEV)
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> NLO Kernel </b>
<div  style="text-align: left; font-size: 16pt; margin-bottom: 5mm; margin-top: -6mm; text-align: center;">
Next-To-Leading-Log (NLL) Resummation: <span style="font-size: 14pt;">$\mathcal{O}\big(\alpha_s^n \log^{n-1}(s/|t|)\big )$</span>
</div>

<img src="NLOKernel.png" style="max-width: 180mm; margin-top: 0mm; margin-bottom:0 mm;">

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (a) two-loop correction to the Regge trajectory
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (b) one-loop correction to the one-emission CEV
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (c) leading two-emission CEV, this requires an next-to-MRK (NMRK) tree computation: <br>
     $\phantom{\circ}\,\kern4mm$ the two central gluons are <u>not</u> rapidity gapped
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> NNLO Kernel </b>
<div  style="text-align: left; font-size: 16pt; margin-bottom: 5mm; margin-top: -6mm; text-align: center;">
NNLL Resummation: <span style="font-size: 14pt;">$\mathcal{O}\big(\alpha_s^n \log^{n-2}(s/|t|)\big )$</span>
</div>


<img src="NNLOKernel.png" style="max-width: 280mm; margin-top: 0mm; margin-bottom:0 mm; margin-left: -16mm">

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (b) the two-loop correction to the central emission vertex for one gluon was computed last year
</div>
<span style="font-size: 14pt; margin-top: -3mm; margin-bottom: -5mm; float: right; font-align: right;"> <a href="https://arxiv.org/abs/2204.12459" > Abreu, GDL, Falcioni, Gardi, Milloy, Vernazza</a>;$\;$<a href="https://arxiv.org/abs/2204.12459"> Buccioni, Caola, Devoto, Gambuti</a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 8mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (d) The last missing component is the next-to-maximally-helicity-violiating (NMHV) one-loop two-gluon CEV
</div>


</section>

---

<section >

{{< slide background-image="varieties-no-background.png" >}}

# NMRK Expansion


---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Challenge from Spurious Cancellations </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ 
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle f(x,y), g(x, y), h(x, y) \in \mathbb{Q}[x, y] \, .
$$
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> <span style="font-size: 27pt;">$p\kern0.2mm$</span>-adic numbers </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Analytic computation is unfeasible (run out of both RAM and time), <br>
     $\phantom{\circ}$ while floating point calculations are very unstable due to 7-8 orders of spurious cancellations.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ You may be familiar with finite field (integers modulo a prime)
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle a \in \mathbb{F}_p : a \in \{0, \dots, p -1\} \; \text{ with } \; \{+, -, \times, \div\}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Limits (and calculus) is not well defined in $\mathbb{F}_p$. We can make things zero, but not small.
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle |a|_0 = 1 if a = 0 else 1
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ There exists just one more absolute value on the rationals, the $p$-adic absolute value.
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Let's start from $p$-adic integers, instead of working modulo p, expand in powers of p
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle a \in \mathbb{Z}_p : a_0 p^0 + a_1 p^1 + a_2 p^2 + \dots + \mathcal{O}(p^n)
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Think of $p$ as a small quantity, $\epsilon$, even if it is a large (by the real absolute value) prime in practice.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ $p$-adic numbers allow for negative powers of $p$, 
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle a \in \mathbb{Q}_p : a_{-\nu} p^{-\nu} + \dots + a_0 + a_1 p^1 + \dots + \mathcal{O}(p^n)
$$
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2203.04269>
   GDL, Page ('22)
</a>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> The <span style="font-size: 27pt;">$p\kern0.2mm$</span>-adic (N)MRK Limit </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Set the (N)MRK parameter controlling the rapidity gap to be large negative power of $p$
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Analytic Reconstruction </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 15pt;">$pp \rightarrow HHH$</span> we use the massive spinor-helicity (or spin-spinor) formalism, <br>
     $\phantom{\circ}$ albeit in a very simplified form since scalars have no states.
</div>
<a href="https://arxiv.org/abs/1809.09644" style="font-size: 14pt; margin-bottom: -6mm; margin-top: -5mm; float: right; font-align: right;"> Shadmi, Weiss </a> <a href="https://arxiv.org/abs/1802.06730" style="font-size: 14pt; margin-bottom: -6mm; margin-top: -5mm;  margin-right: 31mm; float: right; font-align: right;"> Ochirov; </a>
<a href="https://arxiv.org/abs/1709.04891" style="font-size: 14pt; margin-bottom: -10mm; margin-top: -11mm; margin-right: 0mm; float: right; font-align: right;"> Arkani-Hamed, Huang, Huang;</a>

<div style="font-size: 15pt; margin-top: 12mm; margin-bottom: 5mm">
$$ 
\displaystyle \kern10mm R_{NRMK} = \mathbb{F}\big[ z, \bar z, w, \bar w, X(=X_{45}) \big]
$$
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Multivariate Partial Fractions </b>
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -18mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/1904.04067>
   GDL, Maître ('19)
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -13mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2203.04269>
   GDL, Page ('22)
</a>

<div style="text-align: left; font-size:16pt; margin-top: -2mm; margin-bottom: 0mm;">
     $\circ$ We want a mathematically rigorous answer to the question
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 2mm; margin-bottom: 1mm;">
$$ 
\frac{\mathcal{N}}{\mathcal{D}_1\mathcal{D}_2} \stackrel{?}{=}
 \frac{\mathcal{N}_2}{\mathcal{D}_1} + \frac{\mathcal{N}_1}{\mathcal{D}_2} 
$$
</div>
<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\phantom{\circ}$ without knowing <span style="font-size: 15pt">$\mathcal{N}$</span> analytically. The complexity should not depend on <span style="font-size: 15pt">$\mathcal{N}$</span> (besided numerical evaluations). <br>
     $\phantom{\circ}$ The complexity will depend on the irreducible polynomials <span style="font-size: 15pt">$\mathcal{D}_1, \mathcal{D}_2$</span>.
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ Multivariate partial fraction decompositions follow from varieties where pairs of denominator factors vanish
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 2mm; margin-bottom: 1mm;">
$$ 
\frac{\mathcal{N}}{\mathcal{D}_1\mathcal{D}_2} \stackrel{?}{=}
 \frac{\mathcal{N}_2}{\mathcal{D}_1} + \frac{\mathcal{N}_1}{\mathcal{D}_2} \; \Longleftrightarrow \; \mathcal{N} \stackrel{?}{\in} \big\langle \mathcal{D}_1, \mathcal{D}_2 \big\rangle \, \text{ i.e. } \; \mathcal{N} \stackrel{?}{=} \mathcal{N}_1 \mathcal{D}_1 + \mathcal{N}_2 \mathcal{D}_2
$$
</div>
<div style="display: flex; margin-top:-6mm;">
    <div style="flex: 1;">
        <img src="V1.png" style="max-width:60%; height:auto;">
        <!--
        <div style="width:100%; font-size: 13pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\langle xy^2 + y^3 - z^2 \rangle$
        </div>
        -->
    </div>
    <div style="flex: 1; max-width:3%; margin-top:20mm;">
        $\cap$
    </div>
    <div style="flex: 1;">
        <img src="V2.png" style="max-width:60%; height:auto;">
        <!--
        <div style="width:100%; font-size: 13pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\langle x^3 + y^3 - z^2 \rangle$
        </div>
        -->
    </div>
    <div style="flex: 1; max-width:3%; margin-top:20mm;">
        $=$
    </div>
    <div style="flex: 1;">
        <img src="V3.png" style="max-width:53%; height:auto;">
        <!--
        <div style="width:120%; font-size: 14pt; margin-left:-10mm; margin-top: -3mm; margin-bottom: 1mm;">
          $\begin{gather}\langle 2y^3-z^2, x-y \rangle \cap \langle y^3-z^2, x \rangle \cap \langle z^2, x+y \rangle\end{gather}$ 
        </div>
        -->
    </div>
</div>
<div style="text-align: left; font-size: 13pt; margin-top: -4mm; margin-bottom: 1mm;">
$$ 
\langle {\color{orange}xy^2 + y^3 - z^2} \rangle + \langle {\color{blue}x^3 + y^3 - z^2} \rangle = \langle xy^2 + y^3 - z^2, x^3 + y^3 - z^2 \rangle = \langle {\color{red}2y^3-z^2, x-y} \rangle \cap \langle {\color{green}y^3-z^2, x} \rangle \cap \langle {\color{blue}z^2, x+y} \rangle
$$
</div>
<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\phantom{\circ}$ This is a primary decomposition, it is the equivalent for polynomials of say: <span style="font-size: 14pt">$12 = 2^2 \times 3$</span> <br> 
     $\phantom{\circ}$ If <span style="font-size: 14pt">$\mathcal{N}$</span> vanishes on all branches, than the partial fraction decomposition exists.
</div>

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Iterated Pole Subtraction </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (i.e. geometry at codimension greater than one)
     </p>
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -21mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/1904.04067>
   GDL, Maître ('19)
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -16mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2203.04269>
   GDL, Page ('22)
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -11mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2312.03672>
   Chawdhry ('23)
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -6mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2506.08452>
   Xia, Yang ('25)
</a>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Let's go back to our example
</div>


</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# <br> Conclusions <br> & <br> Outlook

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Towards the NMHV 2-Emission CEV </b>
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 4mm; margin-top: 2mm;">
     $\circ$ Tests: MRK, same functions from ++-+-- and +-+-+-, match part of the result to N=4 and N=1 SUSY
</div>

</section>

---

<section>

{{< slide background-image="dubrovnik.jpeg" >}}

<div style="margin-top: 50mm; margin-bottom: 30mm;">
<b style="font-variant: small-caps; font-size: xxx-large;"> Thank you <br> for your attention! </b>
<br>
<br>
<!---
<b style="font-variant: small-caps; font-size: xx-large;"> Questions? </b>
--->
</div>

<span style="font-size: 11pt; ">
    These slides are powered by:<br>
    <span style="display: block; margin-top: 2mm;">
        <a href="https://en.wikipedia.org/wiki/Markdown">markdown</a>, 
        <a href="https://en.wikipedia.org/wiki/HTML">html</a>, 
        <a href="https://revealjs.com/">revealjs</a>, 
        <a href="https://gohugo.io/">hugo</a>, 
        <a href="https://www.mathjax.org/">mathjax</a>, 
        <a href="https://github.com/">github</a>
    </span>
</span>
<!---
<br>
<font size=3>
     For open source packages: 
     <code>
          $   $ pip install [lips](https://github.com/GDeLaurentis/lips) [pyadic](https://github.com/GDeLaurentis/pyadic)
     </code>
</font size>
--->

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
