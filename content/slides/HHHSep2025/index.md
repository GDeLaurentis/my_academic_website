---
tile: "Analytic One-Loop Amplitude for $gg \\rightarrow HHH$"
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
	   Analytic One-Loop Amplitudes for $gg \rightarrow HHH$
	</b>
</h3>

<div style="font-size: x-large; margin-top:8mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
<a href="https://arxiv.org/pdf/2507.19313">arXiv:2507.19313</a> 
<div style="font-size: large; margin-bottom:5mm;"> with J. M. Campbell and R. K. Ellis </div>

<div style="font-size: large; margin-top:10mm; margin-bottom:10mm;"> See also: <br>
<span style="font-size: 12pt;">$q\bar{q}\rightarrow t\bar{t}H$</span> (<a href="https://arxiv.org/abs/2504.19909">arXiv:2504.19909</a>,
<a href="https://link.springer.com/article/10.1007/JHEP07(2025)147">JHEP07(2025)147</a>) <br>
<span style="font-size: 12pt;">$pp\rightarrow HHj$</span> (<a href="https://arxiv.org/abs/2408.12686">arXiv:2408.12686</a>, 
<a href="https://link.springer.com/article/10.1007/JHEP10(2024)230">JHEP10(2024)230</a>) <br>
<span style="font-size: 12pt;">$pp\rightarrow Hjj$</span> (<a href="https://arxiv.org/abs/2002.04018">arXiv:2002.04018</a>,
<a href="https://link.springer.com/article/10.1007/JHEP05(2020)079">JHEP05(2020)079</a>)
</div>

HHH Workshop
<div style="font-size: large; margin-top:-5mm; margin-bottom:5mm"> Dubrovnik, HR </div>
<p style="line-height: 0.05;"> <img src="UniEdinburghLogo-transparent.png"; style="max-width:120px;float:center;border:none;margin-bottom:5mm;"> 
<br><br><br>
<span style="font-size: 11pt; margin-top: 10mm;">Find these slides at  <a href="/slides/hhhsep2025/#/">gdelaurentis.github.io/slides/hhhsep2025</a> </span>
</div>

---

<section>

{{< slide background-image="LHCcern.jpg" >}}

# Introduction

---

<b style="font-variant: small-caps; font-size: 32pt"> Theoretical Motivation </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 0mm; margin-left: -4mm;">
     $\circ\,$ Direct probe of triple and quartic Higgs self-couplings at current and future colliders. <br>
     $\phantom{\circ}\,$ We write the potential in the kappa framwork (SM: <span style="font-size: 15pt">$\kappa_3 = \kappa_4 = 1$</span>)
</div>

<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
V(H) = \frac{1}{2} m_h^2 H^2 + \kappa_3 \lambda v H^3 + \kappa_4 \frac{\lambda}{4}  H^4
$$
</div>
<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ There are contributions proportional to <span style="font-size: 15pt">$\kappa_4$, $\kappa_3^2$ ($A_3$), $\kappa_3$ ($A_4$)</span>, and no <span style="font-size: 15pt">$\kappa$ ($A_5$).</span>
</div>

<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
A_{\rm tot} = \delta^{AB} \frac{g_s^2}{16\pi^2} \, \frac{m_t^4}{v^3} \left(
A_3 + A_4 + A_5 \right)\, .
$$
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 5mm; margin-top: 5mm; margin-left: -4mm;">
     $\circ\,$ Facilitate phenomenological studies through faster and more stable evaluations: <br>
     $\phantom{\circ}\,$ we observe an order of magnitude speed up compared to <span style="font-variant: small-caps;">Recola2</span> and <span style="font-variant: small-caps;">OpenLoops2</span>.
</div>
<a href="https://arxiv.org/abs/1907.13071" style="font-size: 14pt; margin-top: 0mm; margin-bottom: -10mm; float: right; font-align: right;"> Buccioni, Lang, Lindert, Maierhöfer, Pozzorini, Zhang, Zoller</a>
<a href="https://arxiv.org/abs/1711.07388" style="font-size: 14pt; margin-top: -6mm; margin-bottom: 0mm; float: right; font-align: right;"> Denner, Lang, Uccirati</a>

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 14mm; margin-left: -4mm;">
     $\circ\,$ Improve understanding of the analytical structure:
     <div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
          $\qquad\star\,$ Stepping stone towards real-radiation processes and, eventually, multi-loop corrections.
     </div>
     <div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
          $\qquad\star\,$ Provide necessary input to understand cancellation of spurious kinematic singularities.
     </div>
     $\phantom{\circ}\,$ In this context full control over the leading order result is an essential baseline.
</div>


---

<b style="font-variant: small-caps; font-size: 32pt"> Feynman Diagrams for $A_3$: $\kappa_4$ \& $\kappa_3^2$</b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ The $\kappa_4$ and $\kappa_3^2$ diagrams are triangles (no contribution from pinch bubbles)
</div>

<img src="diagrams_self_coupling_k4_transparent.png" style="max-width:70%; height:auto;">

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ This sub-amplitude is easily stated as (for the two indep. helicity configurations)
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

<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ Where $C_0(p_1,p_2; \mt)$ is the scalar triangle Feynman integral: $\frac{1}{i \pi^{2}} \int \,  \frac{d^4 l}{d_0 \; d_1 \; d_2} $
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> Feynman Diagrams for $A_4$ and $A_5$: $\kappa_3$ \& no $\kappa$ </b>

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

<b style="font-variant: small-caps; font-size: 34pt; magin-bottom: -10mm;"> Setting up the Calculation </b> <br>

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

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Overview of the Approach </b>

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

# Analytic & Geometric Structure

<br><br><br>

<span style="font-size: 18pt">algebro-geometric formulation for physicists in:<span> <br>
<span style="font-size: 18pt">[GDL, Page (JHEP 12 (2022) 140)](https://arxiv.org/abs/2203.04269)<span>

<span style="font-size: 18pt">see also Sturmfeld et al. "Spinor-Helicity Varieties":<span> <br>
<span style="font-size: 18pt">[arXiv:2406.17331](https://arxiv.org/abs/2406.17331)<span>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Variables Subject to Constraints </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Consider polynomials <span style="font-size: 14pt;">$f, g, h$</span> in two variables <span style="font-size: 14pt;">$x, y$</span>. They live in a <b>polynomial ring</b>:
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle f(x,y), g(x, y), h(x, y) \in \mathbb{Q}[x, y] \, .
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ We may want to consider e.g. funcitons on the unit circle, <span style="font-size: 14pt;">$(x^2+y^2-1)$</span>. If we have
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle f(x,y) \approx g(x, y) + h(x, y) (x^2+y^2-1) \, ,
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ then we should consider <span style="font-size: 14pt;">$f(x,y)$</span> and <span style="font-size: 14pt;">$g(x, y)$</span> as equivalent, for any <span style="font-size: 14pt;">$h(x,y)$</span>.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ This structure is that of a polynomial <b>quotient</b> ring
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle \mathbb{Q}[x, y] \big/ \big\langle x^2+y^2-1 \big\rangle \\[2mm]
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ its elements are <b>equivalence classes</b> of polynomials.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ <span style="font-size: 14pt;">$\big\langle x^2+y^2-1 \big\rangle \subset \mathbb{Q}[x, y]$</span> is an example of an <b>ideal</b>, that is the infinite set of polynomials <br> 
     $\phantom{\circ}$ <span style="font-size: 14pt;">$h(x, y) (x^2+y^2-1)$</span>, for any <span style="font-size: 14pt;">$h(x,y)$</span>, that vanishes on the unit circle.
</div>


---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Massless Scattering </b>

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

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The "unit circle" is now the codimension <span style="font-size: 14pt;">$4$</span> "momentum conservation" <b>variety</b> within a <span style="font-size: 14pt;">$4n$</span> <br> $\phantom{\circ}$ dimensional space. On this variety we have equivalence relations such as 
</div>
<div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
     $$
     \displaystyle \langle 1|2+3|1]=\langle 1|-1-4-5|1]=-\langle 1|4+5|1] \quad \text{in} \quad R_5
     $$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Integral coefficients are rational functions <span style="font-size: 16pt">$r_i$</span> in the field of fractions of <span style="font-size: 16pt">$R_n$</span>,
</div>
<div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
     $$
     \displaystyle r_i(|i\rangle,[i|) = \frac{\mathcal{N}(|i\rangle,[i|)}{\mathcal{D}(|i\rangle,[i|)} \, , \quad r_i(|i\rangle,[i|) \in \text{Frac}(R_n)
     $$
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Covariant Q-Ring for $\text{ggHHH}$ </b>

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

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 6mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ It is sometimes useful to map to a set of all massless momenta / spinors,
</div>
<a href="https://arxiv.org/abs/1601.08113" style="font-size: 14pt; margin-top: -3mm; margin-right: 2mm; float: right; font-align: right;"> Conde, Marzolla</a>
<a href="https://arxiv.org/abs/1605.07402" style="font-size: 14pt; margin-top: -3mm; margin-right: 2mm; float: right; font-align: right;"> Conde, Joung, Mkrtchyan;</a>
<div style="font-size: 15pt; margin-top: 8mm; margin-bottom: 5mm">
$$ 
\displaystyle 1 \rightarrow 1, 2 \rightarrow 2, \boldsymbol{3} \rightarrow 3+4, \boldsymbol{4} \rightarrow 5+6, \boldsymbol{5} \rightarrow 7+8
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ but if we want neat expressions we must be careful not to overparametrise the space!
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 6mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Our coefficients <span style="font-size: 15pt">$d^{h_1h_2}_{p_a\times p_b \times p_c }$</span> and <span style="font-size: 15pt">$c^{h_1h_2}_{p_a\times p_b}$</span> belong to the field of fractions over <span style="font-size: 15pt">$R_{HHH}$</span>.
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: xxx-large"> Least Common Denominator </b>
     <p style="margin-top: -2mm; margin-bottom: 2mm; font-size: 16pt;">
     (i.e. geometry at codimension one)
     </p>
</div>

<div style="display:block; width:100%; margin-top: 2mm; margin-bottom: -3mm; margin-left: 0mm;">
     <div style="font-size: x-large; width: 65%; text-align: left; display: inline-block; margin-top: 2mm;">
          <!---
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 2mm;">
               $\circ$ Polynomials belong to the the covariant quotient ring of spinors,
          </div>
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
               $$\displaystyle \kern10mm R_n = \mathbb{F}\big[|1⟩, [1|, \dots, |n⟩, [n|\big] \big/ \big\langle \sum_i |i⟩[i| \big\rangle$$
          </div>
          --->
	     <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
                $\circ\,$ We can now determine the least common denominators (LCDs),
          </div>
          <div style="font-size:15pt; text-align: center; margin-top: 2mm; margin-bottom: 0mm">
               $$
               \displaystyle \mathcal{D} = \prod_j \mathcal{D}_j^{q_{ij}} \in R_{HHH} \; , \; \mathcal{D}_j \text{ irreducible} \, ,
               $$
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: -3mm; margin-bottom: 1mm;">
               $\phantom{\circ}\,$ from a univariate slice <span style="font-size: 16pt">$\vec\lambda(t)$</span> giving us <span style="font-size: 16pt">$\mathcal{D}(t)$</span>, <br> 
               $\phantom{\circ}\,$ if we know the possible <span style="font-size: 16pt">$\mathcal{D}_j$</span>.
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 5mm; margin-bottom: 1mm;">
               $\circ$ The curve must intersect all varieties <span style="font-size: 16pt">$V(\langle \mathcal{D}_j \rangle)$</span>, e.g.
          </div>
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
               $$
               \displaystyle |i\rangle \rightarrow |i\rangle + t a_i |\eta\rangle, [i| \rightarrow [i| + t b_i [\eta|
               $$
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
               $\phantom{\circ}\,$ Solve for <span style="font-size: 16pt">$a_i, b_i$</span> such that constraints are satisfied. For <span style="font-size: 16pt">$HHH$</span>, <br>
               $\phantom{\circ}\,$ we can use the massless algorithm at 8 point (or shift the <span style="font-size: 16pt">$p_{\alpha,\dot\alpha}$</span>).
          </div>
	</div>
     <div style="width:35%; float: right; display: inline-block; margin-top: 6mm; ">
          <img src="variety_slice_v2-transparent.png"; style="max-width:360px; float:center; border:none; margin-top: -7mm; margin-bottom: -2mm;">
          <div style="width:100%; font-size: 14pt; margin-top: 0mm; margin-bottom: 1mm;">
               The space has dimension $20-6=14$,
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 0mm; margin-bottom: 1mm;">
               $\mathcal{D}_j = 0$ have dimension $14-1=13$,
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 0mm; margin-bottom: 1mm;">
               $\vec\lambda(t)$'s have dimension 1.
          </div>
     </div>
</div>

<div style="border: 2px solid black; font-size: 16pt; padding: 10px; display: inline-block; margin-top: 10mm;">
    Poles & Zeros $\;\Leftrightarrow\;$ Irreducible Varieties $\;\Leftrightarrow\;$ Prime Ideals <br>
    <i style="font-size: 14pt; border-top: -8mm; border-bottom: -2mm;"> Physics $\kern18mm$ Geometry $\kern18mm$ Algebra </i>
</div>

---


<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> $HHH$ LCD Factors </b>


<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\circ\,$ The irreducible denominator factors <span style="font-size: 14pt">$\mathcal{D}_j$</span> for <span style="font-size: 14pt">$HHH$</span> are
</div>

<div style="text-align: center; font-size: 14pt; margin-top: 2mm; margin-bottom: 2mm;">
     $$
     \begin{gathered}
     \mathcal{D}_{HHH} = \big\{ 
          ⟨1|2⟩, [1|2], ⟨2|𝟓|1], ⟨2|𝟒|1], ⟨2|𝟑|1], ⟨1|𝟑|2], [1|𝟑|𝟓|1], ⟨1|𝟑|𝟓|1⟩, ⟨1|𝟓|𝟒|2⟩, [2|𝟒|𝟓|1], Δ_{12|𝟑|𝟒|𝟓}, \\
          ⟨2|𝟑|𝟒|𝟓|1], ⟨1|𝟓|𝟒|𝟑|2], ⟨1|2⟩[1|2]⟨1|𝟓|𝟒|𝟑|2]⟨2|𝟑|𝟒|𝟓|1]+m_t^2\text{tr}_5(1|2|𝟑|𝟒)^2, \\
          ⟨1|𝟑|2]⟨2|𝟒|𝟓|1⟩[1|𝟑|2⟩[2|𝟒|𝟓|1]+m_t^2\text{tr}_5(1|2|𝟑|𝟒)^2
     \big\}
     \end{gathered}
     $$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ plus closure under permutations, where 
</div>
<div style="text-align: center; font-size: 14pt; margin-top: 2mm; margin-bottom: 2mm;">
     $$
     \Delta_{12|3|4|5} \;=\;
\det\begin{pmatrix}
p_{12}\!\cdot\! p_{12} & p_{12}\!\cdot\! p_{3} & p_{12}\!\cdot\! p_{4} \\
p_{3}\!\cdot\! p_{12} & p_{3}\!\cdot\! p_{3}   & p_{3}\!\cdot\! p_{4} \\
p_{4}\!\cdot\! p_{12} & p_{4}\!\cdot\! p_{3}   & p_{4}\!\cdot\! p_{4}
\end{pmatrix} \quad \text{ and } \quad\quad
   \begin{aligned}
       \text{tr}_5(1|2|3|4) &= \text{tr}(\gamma^5 p_1 p_2 p_3 p_4) \\
       &= [1|2|𝟑|𝟒|1⟩ - ⟨1|2|𝟑|𝟒|1]
     \end{aligned}
     $$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ The two poles mixing kinematics with the top mass are what is left overs of the pentagons.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For example, for an integral coefficient at this stage we see
</div>
<div style="font-size: 14pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\hat d^{++}_{12\times 3 \times 4}= \frac{\mathcal{N}}{⟨12⟩²⟨1|𝟓|𝟒|𝟑|2]⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ For some unknown <span style="font-size: 15pt">$\mathcal{N}$</span> which would be fairly complicated in this LCD form.
</div>


---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> A Concrete Example </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For instance, we aim to find a form like
</div>
<div style="font-size: 12pt; margin-top: 10mm; margin-bottom: 3mm">
$$ 
\begin{gathered}
\hat d^{++}_{12\times 3 \times 4}=\Bigg\{\frac{[2|𝟒|𝟑-𝟓|2]\text{tr}(𝟓|𝟒|𝟑|1-2)}{4⟨12⟩⟨1|𝟓|𝟒|𝟑|2]} -
\frac{(s_{𝟑𝟒}-2m_h²)(s_{𝟑𝟓}+m_h²-2s_{2𝟒})}{2⟨12⟩²} -
\frac{(\text{tr}(1-2|𝟑)m_h²+⟨1|𝟑|𝟒|2⟩[12])}{⟨12⟩²} +\\
-\frac{(s_{𝟒𝟓}-s_{𝟑𝟒})²(s_{1𝟑}-s_{2𝟑})(s_{1𝟑}+s_{2𝟑})(\text{tr}(1+2|𝟒)+4s_{𝟑𝟒}-8m_t²)}{32⟨12⟩²Δ_{12|𝟑|𝟒|𝟓}} +\\
-\frac{(s_{𝟒𝟓}-s_{𝟑𝟒})(s_{1𝟑}-s_{2𝟑})(s_{𝟑𝟒}-m_h²)((s_{𝟒𝟓}-s_{𝟑𝟒})\text{tr}(1+2|𝟒)+s_{𝟑4}(s_{1𝟑}+s_{2𝟑})-s_{𝟑4}(s_{𝟑𝟒}-2m_h²)-8s_{123}m_t²)}{8⟨12⟩²Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{Δ_{12|𝟒|𝟑5}(s_{1𝟑}-s_{2𝟑})(s_{1𝟑}+s_{2𝟑})(\text{tr}(1+2|𝟒)-8m_t²)}{8⟨12⟩²Δ_{12|𝟑|𝟒|𝟓}} \Bigg\} + \Bigg\{12𝟑𝟒𝟓\rightarrow21𝟓𝟒𝟑\Bigg\}
\end{gathered}
$$
</div>

<div style="font-size: 16pt; text-align: left; margin-top: 3mm; margin-bottom: 2mm;">
     $\circ\,$ Challenge 1: how do we parametrize the numerators?
</div>

<div style="font-size: 16pt; text-align: left; margin-top: 3mm; margin-bottom: 2mm;">
     $\circ\,$ Challenge 2: in LCD form the numerators are often too complicated. <br>
     $\kern18mm$ How do we identify allowed partial fraction decompositions?
</div>

</section>

---

<section>

{{< slide background-image="spinor_coeffs.png" >}}

<br><br><br><br><br><br>

# Analytic Reconstruction

<br><br><br><br><br><br><br>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Invariant Quotient Sub-Rings </b>
<p style="margin-top: -6mm; margin-bottom: 2mm; font-size: 15pt;">
(see also <a href=https://arxiv.org/abs/2509.14350>2509.14350</a>, <i>Some remarks on invariants</i>)
</p>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Helicity amplitudes are Lorentz invariant: minimal ansätze are build in the <b>invariant sub-ring</b>.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ General construction for Lorentz-invariant sub-rings through elimination theory
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\quad\star$ Build a ring with both covariant and invariant variables (here showing massless case)
</div>
<div style="font-size: 15pt; text-align: center; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\mathbb{F}\big[ |i\rangle, [i|, \langle i j\rangle , [ij] \big]
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\quad\star$ Define relations among variables (on top of existing constraints, e.g. <span style="font-size: 15pt">$p_3^2=p_4^2$</span>)
</div>
<div style="font-size: 15pt; text-align: center; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\big\{ \langle ij \rangle - \epsilon^{\beta\alpha} \lambda_{i\alpha}  \lambda_{j, \beta}, [ij] - \tilde\lambda_{i\dot\alpha} \epsilon^{\dot\alpha\dot\beta} \tilde\lambda_{j, \dot\beta} \big\}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\quad\star$ Compute a lexicographical Groebner basis with invariants > covariants
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For  <span style="font-size: 15pt">$HHH$</span>, this yields the following quotient ring for the invariants
</div>

<div style="font-size: 14pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle \mathcal{R}_{HHH} = \frac{\underbrace{\substack{\normalsize\kern-30mm\mathbb{F}\big[ ⟨1|2⟩, [1|2], ⟨1|𝟑|1], ⟨1|𝟑|2], ⟨2|𝟑|1], ⟨2|𝟑|2], ⟨1|𝟒|1], ⟨1|𝟒|2], ⟨2|𝟒|1], ⟨2|𝟒|2],\\[2mm] \normalsize \kern10mm ⟨1|𝟑|𝟒|1⟩, ⟨1|𝟑|𝟒|2⟩, ⟨2|𝟑|𝟒|2⟩, [1|𝟑|𝟒|1], [1|𝟑|𝟒|2], [2|𝟑|𝟒|2], \text{tr}(𝟑|𝟑), \text{tr}(𝟑|𝟒), \text{tr}(𝟒|𝟒), m_h^2
 \big]}}_{20 \text{ variables}}}{\big\langle \underbrace{\text{tr}(𝟒|𝟒)-2m_h^2, \text{tr}(𝟑|𝟑)-2m_h^2, ⟨2|\boldsymbol{3}|2]⟨2|\boldsymbol{4}|1]-⟨2|\boldsymbol{3}|1]⟨2|\boldsymbol{4}|2]-[1|2]⟨2|\boldsymbol{3}|\boldsymbol{4}|2⟩, ...}_{\text{subject to } 122 \; \text{redundancy relations / Schouten identities (only first 2 are trivial rewritings)}} \big\rangle}
$$
</div>


---

<b style="font-variant: small-caps; font-size: xxx-large"> The Numerator Ansatz </b>

<div style="text-align: left; font-size: x-large; margin-top: 1mm; margin-bottom: 2mm; ">
$\circ\,$ The numerator Ansatz takes the form (for the massless case)
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -6mm; margin-bottom: 4mm;" href=https://arxiv.org/abs/1904.04067>
   GDL, Maître ('19)
</a>
<div style="text-align: center; font-size: 15pt; margin-bottom: 5mm; margin-top: 1mm;">
$\displaystyle \text{Num. poly}(\lambda, \tilde\lambda) = \sum_{\vec \alpha, \vec \beta} c_{(\vec\alpha,\vec\beta)} \prod_{j=1}^n\prod_{i=1}^{j-1} \langle ij\rangle^{\alpha_{ij}} [ij]^{\beta_{ij}}$
</div>
<div style="text-align: left; font-size: x-large; float: left; margin-top: -2mm; margin-bottom: 4mm;">
     $\phantom{\circ}$ subject to constraints on $\vec\alpha,\vec\beta$ due to: 1) mass dimension; 2) little group; 3) linear independence. <br>
     $\phantom{\circ}$ For HHH we have polynomials in the 20 invariants from the previous slide.
</div>

<br>

<div style="text-align: left; font-size: x-large; ">
$\circ\,$ Construct the Ansatz via the algorithm from Section 2.2 of <a href=https://arxiv.org/abs/2203.04269>GDL, Page ('22)</a>
</div>
<div style="text-align: center; display: inline-block; font-size: x-large;">
Linear independence = irreducibility by the Gröbner basis of the ideal of the redundancies.
</div>

<div style="text-align: left; font-size: x-large; margin-top: 5mm; margin-bottom: 0mm;">
$\circ\,$ Efficient implementation using open-source software only
</div>
<div style="display:block; width:100%; margin-left: -10mm; margin-top: 0mm;">
	<div style="width:50%; font-size: x-large; float: left; display: inline-block;">
	     <img src="SingularLogo.png"; style="max-width:300px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;"> <br>
	     Gröbner bases $\rightarrow$ constrain $\vec\alpha,\vec\beta$ <br>
	     <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 5mm;"
	     href=https://www.singular.uni-kl.de/index.php.html>
		Decker, Greuel, Pfister, Schönemann
	     </a>	    
	</div>
	<div style="width:50%; font-size: x-large; float: right; display: inline-block; ">
	     <img src="GoogleORToolsLogo.png"; style="max-width:300px; float:center; border:none; margin-top: 7mm; margin-bottom: 2mm;"> <br>
	     Integer programming $\rightarrow$ enumerate sols. $\vec\alpha,\vec\beta$ <br>
	     <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 5mm;"
	     href=https://www.singular.uni-kl.de/index.php.html>
		Perron and Furnon (Google optimization team)
	     </a>
	</div>
</div>

<br><br><br><br>

<div style="text-align: left; font-size: x-large; margin-top: -2mm;">
$\circ\,$ Linear systems solved w/ CUDA over $\mathbb{F}_{2^{31}-1}$ ($t_{\text{solving}} \ll t_{\text{sampling}}$) w/ <a href=https://github.com/GDeLaurentis/linac-dev> linac </a> <span style="text-align: left; font-size: small;"> (coming soon) </span>
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
     <b style="font-variant: small-caps; font-size: 32pt"> Analytic Results for Theory and Phenomenology </b>
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


---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Challenges </b>
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 5mm; margin-bottom: 0mm;">
$\circ\,$ Can we always verify constraints numericaly? Alternatively, can we predict/guess them? <br>
$\phantom{\circ}\,$ <span style="font-size: 14pt">$p$</span>-adic evaluations can be costly (especially with multi-loop amplitudes).
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: 0mm;">
$\circ\,$ Imposing multiple constraints at ones means computing ideal intersections, which can be highly non-trivial:
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\mathcal{N} \in \langle q_1, q_2 \rangle \cap \langle q_3, q_4 \rangle \stackrel{?}{=} \langle q_1q_3, q_1q_4, q_2q_3, q_2 q_4\rangle 
$$
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\phantom{\circ}\,$ Unfortunately not always. This is called a <i>complete intersection</i> when it holds.
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: 0mm;">
$\phantom{\circ}\,$ Therefore, either: 
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\quad\star\,$ we compute the intersection explicitly (can be prohibitively hard),
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\quad\star\,$ or we have to make a choice of which constrain we manifest (trial and error).
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: 0mm;">
$\circ\,$ Computing primary decompositions with these many variables is hard, Singular can't do it on its own.
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: 0mm;">
$\circ\,$ Even constructing the ansatz requires a Groebner Basis, which in some cases Singular doesn't easily give. <br>
$\phantom{\circ}\,$ For <span style="font-size: 14pt">$pp\rightarrow HHHj$</span> we don't have the full GB, we need to remove redundancies through linear algebra.
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: 0mm;">
$\circ\,$ The reduction to master integrals of the amplitude is often not easy in the first place.
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

---

<section>

<div style="margin-top: 50mm; margin-bottom: 30mm;">
<b style="font-variant: small-caps; font-size: xxx-large;"> Backup slides. </b>
</div>

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Effective Pentagons </b>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ As mentioned, pentagons can be reduced to a combination of boxes,
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$
\begin{eqnarray}
  &&E_0(p_1,p_2,p_3,p_4;\mt)=
  c^{(1)} D_0(p_2,p_3,p_4;\mt)
  +c^{(2)} D_0(p_{12},p_3,p_4;\mt) \\
  &+&c^{(3)} D_0(p_1,p_{23},p_4;\mt)
  +c^{(4)} D_0(p_1,p_2,p_{34};\mt)
  +c^{(5)} D_0(p_1,p_2,p_3;\mt)\, .
\end{eqnarray}
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ We find it useful to write the box coefficients in terms of effective pentagons <span style="font-size: 15pt;">$\hat e$</span> and boxes <span style="font-size: 15pt;">$\hat d$</span>
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$
d^{h_1h_2}_{p_a\times p_b \times p_c } =  \sum_{i=\{i_1,i_2\}} c^{(i)} \hat e_{p_x \times p_y \times p_z \times p_w}+ \hat d^{h_1h_2}_{p_a\times p_b \times p_c }
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where the sum involves the two pentagons that pinch to the given box.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The coefficients <span style="font-size: 15pt;">$\hat e$</span> and <span style="font-size: 15pt;">$\hat d$</span> are not uniquely defined, but <span style="font-size: 15pt;">$\hat e$</span> has the property of capturing <br>
     $\phantom{\circ}$ the residue of the poles that mix top-mass and kinematic dependence. <br>
     $\phantom{\circ}$ The non-uniqueness comes from, e.g.
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$
⟨1|2⟩[1|2]⟨1|𝟓|𝟒|𝟑|2]⟨2|𝟑|𝟒|𝟓|1]+m_t^2\text{tr}_5(1|2|𝟑|𝟒)^2=0
$$
</div>

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Example of Code Syntax </b>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ This is just a couple of pip install's aways
</div>
<pre><code class="language-python" style="font-size: 11pt">field = Field("padic", 2 ** 31 - 1, 5)
oPs8pt = Particles(8, field=field, seed=0)
oPs8pt._singular_variety(("s_34-s_56", "s_56-s_78", '⟨1|7+8|5+6|3+4|2]', '⟨2|3+4|5+6|7+8|1]'),
                         (field.digits, field.digits, 1, 1), seed=0,
                         generators=('s_34-s_56', 's_56-s_78', '⟨1|7+8|5+6|3+4|2]', 
                                     '⟨2|3+4|5+6|7+8|1]', 'tr5(1|2|3+4|5+6)'))
oPs8pt.m_t = field.random()
oPs8pt.m_h = "sqrt(s_34)"
oPs5pt = oPs.cluster([[1, ], [2, ], [3, 4], [5, 6], [7, 8]])

from antares_results.HHH.ggHHH.pp import coeffs as coeffs_pp
coeffs_pp\['d_12x3x4'\](oPsC)
</code></pre>
<pre><code class="language-python" style="margin-top:-5mm; font-size: 10pt">130808068*2147483647^-1 + 687356881 + 792807618*2147483647 + 696603492*2147483647^2 + O(2147483647^3)
</code></pre>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     The denominator goes like <span style="font-size: 13pt">$p^2$</span>, but the coefficient goes like <span style="font-size: 13pt">$p^{-1} \Rightarrow$</span> the numerator vanishes linearly.
</div>


<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 5mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The output is a <span style="font-size: 15pt">$p$</span>-adic number, i.e. a Laurent series in powers of the prime.<br> 
     $\phantom{\circ}$ With finite fields we cannot do this (with just one evaluation)! It would be dividing by zero.
</div>

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Core Tools - Fully Open Source </b>
</div>

<div style="text-align: center; float: center; font-size: 16pt; margin-top: 0mm; margin-bottom: 0mm;">
     For fleshed out examples see e.g. <a href=https://inspirehep.net/literature/2661970> GDL (ACAT '22)</a> or <a href="https://arxiv.org/abs/2504.19909">Appendix B of 2504.19909</a>
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 2mm;">
     Install from github (<code style="font-size:14pt;">git clone</code>) or PyPI (<code style="font-size:14pt;">pip install</code>); use of Jupyter is recommended.
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/pyadic/" style="font-size: 20pt; font-variant: small-caps;">pyadic</a><br>
     $\quad\rightarrow$ Finite field $\mathbb{F}_p$ and $p$-adic $\mathbb{Q}_p$ number types, including field extensions <br>
     $\quad\rightarrow$ rational number reconstruction (Wang's EEA, LGRR, MQRR) <br>
     $\quad\rightarrow$ univariate and multivariante Newthon & univariate Thiele interpolation algorithms in $\mathbb{F}_p$
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/syngular/" style="font-size: 20pt; font-variant: small-caps;">syngular</a> (in the backhand <a href="https://www.singular.uni-kl.de/index.php.html" style="font-size: 20pt; font-variant: small-caps;">Singular</a>  is used for many operations)<br>
     $\quad\rightarrow$ object-oriented algebraic geometry (Field, Ring, Quotient Ring, Ideal) <br>
     $\quad\rightarrow$ ring-agnostic monomials and polynomials (with support for unicode characters, e.g. spinor brackets)<br>
     $\quad\rightarrow$ multivariate solver (Ideal.point_on_variety), under- and over-constrained systems OK <br>
     $\quad\rightarrow$ a semi-numerical prime and primary ideal test (assumes equi-dimensionality of ideal)
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/lips/" style="font-size: 20pt; font-variant: small-caps;">lips</a> (Lorentz invariant phase space)<br>
     $\quad\rightarrow$ phase space points over any field ($\mathbb{Q}, \mathbb{Q}[i], \mathbb{R}, \mathbb{C}, \mathbb{Q}_p, \mathbb{F}_p$), including internal and external masses <br>
     $\quad\rightarrow$ evaluate any Mandelstam or spinor expression (custom ast/regex parser) <br>
     $\quad\rightarrow$ generation of any special kinematic configuration (wrapper around Ideal.point_on_variety)
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/antares/" style="font-size: 20pt; font-variant: small-caps;">antares</a> (automated numerical to analytical reconstruction software) - still under development <br>
     $\quad\rightarrow$ Univariate slicing, LCD determination, basis change, multivariate partial fractioning strategies, <br>
     $\phantom{\rightarrow}$ constraining of numerators, Ansatz generation and fitting strategies, etc.
</div>

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
