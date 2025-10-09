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
<div style="font-size: 14pt; margin-bottom:0mm;"> Two Loops One Emission </div>
<div style="font-size: 15pt; margin-bottom:0mm;"><a href="https://arxiv.org/pdf/2412.20578">arXiv:2412.20578</a> <a href="https://link.springer.com/article/10.1007/JHEP04(2025)161">(10.1007/JHEP04(2025)161)</a></div>
<div style="font-size: 14pt; margin-bottom:5mm;"> with S. Abreu, G. Falcioni, E. Gardi, C. Milloy, L. Vernazza </div>
<br>
<div style="font-size: 14pt; margin-bottom:0mm;"> One Loop Two Emissions - To Appear </div>
<div style="font-size: 14pt; margin-bottom:5mm;"> with E. Byrne, V. Del Duca, E. Gardi, J. Smillie </div>

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

---

<b style="font-variant: small-caps; font-size: 32pt"> Leading Order Kernel Components </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 0mm; margin-left: -4mm;">
     $\circ\,$ Direct probe of triple and quartic Higgs self-couplings at current and future colliders. <br>
     $\phantom{\circ}\,$ We write the potential in the kappa framwork (SM: <span style="font-size: 15pt">$\kappa_3 = \kappa_4 = 1$</span>)
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 5mm; margin-top: 5mm; margin-left: -4mm;">
     $\circ\,$ Facilitate phenomenological studies through faster and more stable evaluations: <br>
     $\phantom{\circ}\,$ we observe an order of magnitude speed up compared to <span style="font-variant: small-caps;">Recola2</span> and <span style="font-variant: small-caps;">OpenLoops2</span>.
</div>
<a href="https://arxiv.org/abs/1907.13071" style="font-size: 14pt; margin-top: 0mm; margin-bottom: -10mm; float: right; font-align: right;"> Buccioni, Lang, Lindert, Maierhöfer, Pozzorini, Zhang, Zoller</a>
<a href="https://arxiv.org/abs/1711.07388" style="font-size: 14pt; margin-top: -6mm; margin-bottom: 0mm; float: right; font-align: right;"> Denner, Lang, Uccirati</a>


---

<b style="font-variant: small-caps; font-size: 32pt"> NLO Kernel </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ The $\kappa_4$ and $\kappa_3^2$ diagrams are triangles (no contribution from pinch bubbles)
</div>

<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$
\def\mt{m}
\def\mh{M_H}
\def\spa#1.#2{\left\langle#1\,#2\right\rangle}
\def\spb#1.#2{\left[#1\,#2\right]}
\begin{eqnarray}
A_3^{++} &=& 
\frac{\spb1.2}{\spa1.2} \, \frac{6\mh^2}{\mt^2(s_{12}-\mh^2)} 
 \Bigl[(4\mt^2-s_{12}) C_0(p_1,p_2; \mt)+2\Bigr]\times
 \left(\kappa_4+ \frac{3\kappa_3^2 \mh^2}{s_{34}-\mh^2} + \text{perms.} \right) \, ,
\\
A_3^{-+} &=& 0 \, .
\end{eqnarray}
$$
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> NNLO Kernel </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ The $\kappa_3$ diagrams are boxes (and triangle pinches, but no bubble contribution)
</div>
<img src="diagrams_self_coupling_k3_transparent.png" style="max-width:70%; height:auto; margin-top: 0mm; margin-bottom: 0mm;">
<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ Their contribution is also fairly simple, it can be written in 4 or 5 lines.
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 8mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ The background diagrams are by far the most complicated,
</div>
<img src="diagrams_background_transparent.png" style="max-width:70%; height:auto; margin-top: 0mm; margin-bottom: 0mm;">
<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ We require a different approach to tackle them analytically.
</div>


</section>

---

<section>

{{< slide background-image="Feynman-Diagrams-transparent.png" >}}

<h1 style="margin-top: -2mm;"> Computation Setup </h1>

---

<b style="font-variant: small-caps; font-size: 34pt; magin-bottom: -10mm;"> Minimal Variables for Multi-Regge Kinematics </b> <br>

<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: -4mm;">
$\circ$ We perform a first analytic computation in two ways
     <div style="font-size: 16pt; width:99%; text-align: left; display: inline-block; margin-top: 2mm; margin-left:10mm;">
	     1. A standard computation directly from Feynman diagrams <br>
	     2. A generalized-unitarity computation from cut-diagrams (i.e. products of trees) <br>
          $\kern2mm$ In this approach the amplitude is constructed as (schematically)
	</div>
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 15pt; text-align: left; display: inline-block; margin-top: 1mm;">
	     $$
	     \require{color}
	     \displaystyle \sum_{\text{states}} \, \prod_{\text{trees}} A^{\text{tree}}(\lambda, \tilde\lambda, \ell)\big|_{\text{cut}_{\Gamma}} = \sum_{\Gamma' \ge \Gamma} \kern0mm {\color{black}{c_{\,\Gamma',i}(\lambda, \tilde\lambda)}} \, \frac{m_{\Gamma',i}(\lambda\tilde\lambda, \ell)}{\displaystyle \prod_{j\in P_{\Gamma'} / P_{\Gamma}} \rho_{j}(\lambda\tilde\lambda, \ell)}\Bigg|_{\text{cut}_\Gamma}
	     $$
	</div>
</div>

<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: 0mm;">
     <div style="font-size: 16pt; width:99%; text-align: left; display: inline-block; margin-top: 2mm; margin-left:10mm;">
          $\kern2mm$ The sum in the RHS is over all topologies <span style="font-size: 14pt;">$\Gamma'$</span> that have at least the cut propagators $\Gamma$, <br>
          $\kern2mm$ and the product is over propagators that have not been cut.
	</div>
</div>

<div style="font-size: 17pt; text-align: left; margin-bottom: 0mm; margin-top: 2mm;">
     $\circ$ Pentagons are reducible to linear combination of boxes, and we observe all bubbles vanish, leaving:
</div>
<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 15pt; text-align: left; display: inline-block; margin-top: 1mm;">
	     $$
	     A_5^{h_1h_2} = \sum_{a,b,c} d^{h_1h_2}_{p_a\times p_b \times p_c } D_0(p_a, p_b, p_c; m_t) + \sum_{a,b} c^{h_1h_2}_{p_a\times p_b} C_0(p_a, p_b; m_t)
	     $$
	</div>
</div>

<div style="font-size: 17pt; text-align: left; margin-bottom: 0mm; margin-top: -3mm;">
     $\circ$ This yields a few MBs of optimized <span style="font-variant: small-caps;">FORM</span> routines for the integral coefficients, which we simplify.
</div>

<div style="font-size: 17pt; text-align: left; margin-bottom: 0mm; margin-top: 3mm;">
     $\circ$ In principle, a numerical program for <span style="font-size: 15pt">$d^{h_1h_2}_{p_a\times p_b \times p_c }$</span> and <span style="font-size: 15pt">$c^{h_1h_2}_{p_a\times p_b}$</span> would suffice for what follows.
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Expanding Amplitudes in MRK and NMRK </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Goal is to obtain simple forms for <span style="font-size: 15pt">$d^{h_1h_2}_{p_a\times p_b \times p_c }$</span> and <span style="font-size: 15pt">$c^{h_1h_2}_{p_a\times p_b}$</span>
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     $\star$ We will use only numerical evaluations to study their analytic     structure <br>
     $\star$ We will parametrize the possible functional form (Ansatz) and solve for free coefficients
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     Think of this as a bootstrap approach, helped by additional numerical information.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 6mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The analytic structure should be clear with $p^\mu \in \mathbb{C}^{4}$ (good $\mathbb{R}^{4}$ behaviour will follow)
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     $\phantom{\star}$ In practice, take <span style="font-size: 15pt;">$p^{\mu=y}\in i\mathbb{Q} \; \Rightarrow \; E\pm p^z \text{ and } p^x\pm ip^y \in \mathbb{R} \; \Rightarrow \; \lambda_{\alpha} \in \mathbb{R} \text{ or } \mathbb{Q}$</span> <br>
     $\phantom{\star}$ This allows us to generate phase space points in a finite field (modular arithmetics)
</div>

<pre><code class="language-python">from syngular import Field
from lips import Particles
Particles(5, field=Field("finite field", 2 ** 31 - 1, 1), seed=0)  # Fp
Particles(5, field=Field("padic", 2 ** 31 - 1, 5), seed=0)  # Qp
Particles(5, field=Field("mpc", 0, 300), seed=0)  # C (examples for massless PSPs)
</code></pre>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$  Analytic manipulations are too complex, we bypass this complexity by letting cancellations <br>
     $\phantom{\circ}$ happen numerically. Modular arithmetic will ensure we do not lose precision.
</div>

</section>

---

<section >

{{< slide background-image="varieties-no-background.png" >}}

<br><br><br><br>

# NMRK Expansion

<br><br><br>

<span style="font-size: 18pt">algebro-geometric formulation for physicists in:<span> <br>
<span style="font-size: 18pt">[GDL, Page (JHEP 12 (2022) 140)](https://arxiv.org/abs/2203.04269)<span>

<span style="font-size: 18pt">see also Sturmfeld et al. "Spinor-Helicity Varieties":<span> <br>
<span style="font-size: 18pt">[arXiv:2406.17331](https://arxiv.org/abs/2406.17331)<span>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Challenge from Spurious Cancellations </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Consider polynomials <span style="font-size: 14pt;">$f, g, h$</span> in two variables <span style="font-size: 14pt;">$x, y$</span>. They live in a <b>polynomial ring</b>:
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle f(x,y), g(x, y), h(x, y) \in \mathbb{Q}[x, y] \, .
$$
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> $p$-adic numbers </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 14pt;">$n$</span>-point massless scattering, the quotient ring is
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2203.04269>
   GDL, Page ('22)
</a>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle \kern10mm R_{n} = \mathbb{F}\Big[|1⟩_{\alpha}, [1|_{\dot\alpha}, \dots, |n⟩_{\alpha}, [n|_{\dot\alpha} \Big] \Big/ \Big\langle {\textstyle \sum_{i=1}^n} |i\rangle[ i | \Big\rangle
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Recall the simple relation <span style="font-size: 14pt;">$p_i^\mu \sigma^\mu_{\alpha\dot\alpha} = |i\rangle_\alpha [i|_{\dot\alpha}$</span>.
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
\displaystyle \kern10mm R_{HHH} = \frac{\mathbb{F}\big[|1⟩_{\alpha}, [1|_{\dot\alpha}, |2⟩_{\alpha}, [2|_{\dot\alpha}, \boldsymbol{3}_{\alpha,\dot\alpha}, \boldsymbol{4}_{\alpha,\dot\alpha}, \boldsymbol{5}_{\alpha,\dot\alpha} \big]}{\big\langle |1\rangle[1|+|2\rangle[2| + \boldsymbol{3}_{\alpha,\dot\alpha} + \boldsymbol{4}_{\alpha,\dot\alpha} + \boldsymbol{5}_{\alpha,\dot\alpha}, \;\, \boldsymbol{3}_{\alpha,\dot\alpha} \boldsymbol{3}^{\dot\alpha,\alpha} - \boldsymbol{4}_{\alpha,\dot\alpha} \boldsymbol{4}^{\dot\alpha,\alpha}, \;\, \boldsymbol{4}_{\alpha,\dot\alpha} \boldsymbol{4}^{\dot\alpha,\alpha}- \boldsymbol{5}_{\alpha,\dot\alpha} \boldsymbol{5}^{\dot\alpha,\alpha} \big\rangle}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where <span style="font-size: 15pt;">$\boldsymbol{3}_{\alpha,\dot\alpha} \boldsymbol{3}^{\dot\alpha,\alpha} = \boldsymbol{4}_{\alpha,\dot\alpha} \boldsymbol{4}^{\dot\alpha,\alpha} = \boldsymbol{5}_{\alpha,\dot\alpha} \boldsymbol{5}^{\dot\alpha,\alpha} = 2 M_h^2$</span>, <span style="font-size: 15pt;">$\boldsymbol{3}_{\alpha,\dot\alpha},\boldsymbol{4}_{\alpha,\dot\alpha},\boldsymbol{5}_{\alpha,\dot\alpha}$</span> are full-rank (unfactorizable).
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
<div style="font-size: 14pt; margin-top: 4mm; margin-bottom: 3mm">
$$ 
\hat d^{++}_{12\times 3 \times 4}= \frac{\mathcal{N} \leftarrow 2794 \text{ free parameters }}{⟨12⟩²⟨1|𝟓|𝟒|𝟑|2]⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}}
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 8mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ We can prove <span style="font-size: 13pt">$⟨1|𝟓|𝟒|𝟑|2], ⟨2|𝟑|𝟒|𝟓|1]$</span> can be separated, their primary decomposition reads
</div>
<div style="font-size: 14pt; margin-top: 3mm; margin-bottom: 4mm">
$$ 
\big\langle ⟨1|𝟓|𝟒|𝟑|2], ⟨2|𝟑|𝟒|𝟓|1] \big\rangle = \big\langle ⟨1|𝟓|𝟒|𝟑|2], ⟨2|𝟑|𝟒|𝟓|1], \text{tr}_5 \big\rangle \cap \big\langle ⟨1|𝟓|𝟒|𝟑|2], ⟨2|𝟑|𝟒|𝟓|1], s_{2𝟑}, s_{1𝟓} \big\rangle
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Generate two phase space points, one for each branch, and verify the numerator vanishes.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 8mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Similarly, with four evaluations we can prove <span style="font-size: 13pt">$⟨1|𝟓|𝟒|𝟑|2], Δ_{12|𝟑|𝟒|𝟓}$</span> can be separated,
</div>
<div style="font-size: 14pt; margin-top: 3mm; margin-bottom: 4mm">
$$ 
\big\langle ⟨1|𝟓|𝟒|𝟑|2] , \, Δ_{12|𝟑|𝟒|𝟓} \big\rangle= \big\langle M_H, \; 𝟓_{\alpha\dot\alpha}𝟒^{\dot\alpha\beta} \big\rangle \cap \big\langle M_H, \; 𝟒^{\dot\alpha\alpha}𝟑_{\alpha\dot\beta} \big\rangle \cap \big\langle \langle 1 | 𝟑 | 2], \; \langle 1 | 𝟒 | 2], \; \langle 1 | 𝟑 | 𝟒 | 1 \rangle, [2 | 𝟑 | 𝟒 | 2] \big\rangle \cap \big\langle ??? \big\rangle
$$
</div><div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Although we don't have a complete set of generators for the last branch, we can still sample it.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 6mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Fit <span style="font-size: 13pt">$⟨1|𝟓|𝟒|𝟑|2]$</span> residue by sampling in limit <span style="font-size: 13pt">$⟨1|𝟓|𝟒|𝟑|2] \rightarrow 0$</span>
</div>
<div style="font-size: 14pt; margin-top: 4mm; margin-bottom: 10mm">
$$ 
\hat d^{++}_{12\times 3 \times 4} = \frac{\mathcal{N} \leftarrow 112 \text{ free parameters }}{⟨12⟩²⟨1|𝟓|𝟒|𝟑|2]} + \mathcal{O}(⟨1|𝟓|𝟒|𝟑|2]^0)
$$
</div>

</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# <br> Conclusions <br> & <br> Outlook

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Past and Upcoming Results </b>
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 4mm; margin-top: 2mm;">
     $\circ$ Analytic expressions implemented in <a href="https://mcfm.fnal.gov/">MCFM</a>, for phenomenology use this efficient Fortran implementation
</div>
<a href="https://arxiv.org/abs/1909.09117" style="font-size: 14pt; margin-top: -3mm; margin-right: 2mm; float: right; font-align: right;"> Campbell, Neumann</a>
<a href="https://arxiv.org/abs/1503.06182" style="font-size: 14pt; margin-top: -3mm; margin-right: 2mm; float: right; font-align: right;"> Campbell, Ellis, Giele;</a>
<a href="https://arxiv.org/abs/1105.0020" style="font-size: 14pt; margin-top: -3mm; margin-right: 2mm; float: right; font-align: right;"> Campbell, Ellis, Williams;</a>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 10mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/antares-results/" style="font-size: 20pt; font-variant: small-caps;">antares-results</a> (human readable exprs in <a href="https://gdelaurentis.github.io/antares-results/">docs</a>) with <a href="https://github.com/GDeLaurentis/antares-results/actions/">CI tests</a> for coefficients and/or full amplitudes
</div>
<div style="display: flex; justify-content: center; align-items: flex-start; margin-top: 2mm;">
     <img src="antares-results-transparent.png" 
          style="width: 100%; max-width: 700px; float: left; border: none; margin-top: 2mm; margin-bottom: 0mm;">
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
