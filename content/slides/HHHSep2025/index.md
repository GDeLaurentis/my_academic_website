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
	   Analytic One-Loop Amplitude for $gg \rightarrow HHH$
	</b>
</h3>

<div style="font-size: x-large; margin-top:8mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
<a href="https://arxiv.org/pdf/2507.19313">arXiv:2507.19313</a> 
<div style="font-size: large; margin-bottom:5mm;"> with J. Campbell and K. Ellis </div>

<div style="font-size: large; margin-top:10mm; margin-bottom:10mm;"> See also: <br>
<span style="font-size: 12pt;">$q\bar{q}\rightarrow t\bar{t}H$</span> (<a href="https://arxiv.org/abs/2504.19909">arXiv:2504.19909</a>) <br>
<span style="font-size: 12pt;">$pp\rightarrow HHj$</span> (<a href="https://arxiv.org/abs/2408.12686">arXiv:2408.12686</a>) <br>
<span style="font-size: 12pt;">$pp\rightarrow Hjj$</span> (<a href="https://arxiv.org/abs/2002.04018">arXiv:2002.04018</a>)
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

<b style="font-variant: small-caps; font-size: 32pt"> Subprocesses \& Feynman Diagrams: $\kappa_4$ \& $\kappa_3^2$</b>

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

<b style="font-variant: small-caps; font-size: 32pt"> Subprocesses \& Feynman Diagrams: $\kappa_3$ \& no $\kappa$ </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ The $\kappa_3$ diagrams are boxes (and triangle pinches, but no bubble contribution)
</div>
<img src="diagrams_self_coupling_k3_transparent.png" style="max-width:70%; height:auto; margin-top: 0mm; margin-bottom: 0mm;">
<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ Their contribution is also fairly simple, it can be written in 4 or 5 lines.
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 8mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ The background diagrams are by far the most complicated, for reasons we'll see shortly
</div>
<img src="diagrams_background_transparent.png" style="max-width:70%; height:auto; margin-top: 0mm; margin-bottom: 0mm;">
<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\phantom{\circ}\,$ We require a new approach to tackle them analytically.
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
     $\circ$ This results in a few MBs of optimized <span style="font-variant: small-caps;">FORM</span> routines for the box and triangle coefficients.
</div>

<div style="font-size: 17pt; text-align: left; margin-bottom: 0mm; margin-top: 3mm;">
     $\circ$ In principle, a numerical program for <span style="font-size: 15pt">$d^{h_1h_2}_{p_a\times p_b \times p_c }$</span> and <span style="font-size: 15pt">$c^{h_1h_2}_{p_a\times p_b}$</span> would suffice for what follows.
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Overview of the Approach </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Goal is to obtain simple forms for <span style="font-size: 15pt">$d^{h_1h_2}_{p_a\times p_b \times p_c }$</span> and <span style="font-size: 15pt">$c^{h_1h_2}_{p_a\times p_b}$</span>
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     $\star$ We will use only numerical evaluations to study their structure <br>
     $\star$ We will parametrize the possible functional form (Ansatz) and solve for free coefficients
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     Think of this as a bootstrap helped by additional numerical information.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The analytic structure should be clear with $p^\mu \in \mathbb{C}^{4}$ (good $\mathbb{R}^{4}$ behaviour will follow)
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     $\phantom{\star}$ In practice, take <span style="font-size: 16pt;">$P^{\mu=y}\in i\mathbb{Q}\Rightarrow \lambda_{\alpha} \in \mathbb{F}_p \text{ or } \mathbb{Q}_p$</span> <br>
     $\phantom{\star}$ This allows us to generate phase space points in a finite field (modular arithmetics)
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$  Analytic manipulations are too complex, we bypass this complexity by letting cancellations happen numerically
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
     $\circ$ For example, consider polynomials in two variables <span style="font-size: 14pt;">$x, y$</span>. They live in a <b>polynomial ring</b>:
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle f(x,y), g(x, y), h(x, y) \in \mathbb{Q}[x, y] \, .
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Now, localize them, e.g. on the unit circle <span style="font-size: 14pt;">$(x^2+y^2-1)$</span>
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle f(x,y) \approx g(x, y) + h(x, y) (x^2+y^2-1) \, ,
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ we should consider <span style="font-size: 14pt;">$f(x,y)$</span> and <span style="font-size: 14pt;">$g(x, y)$</span> as equivalent, for any <span style="font-size: 14pt;">$h(x,y)$</span>.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The structure is that of a polynomial <b>quotient</b> ring
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle \mathbb{Q}[x, y] \big/ \big\langle x^2+y^2-1 \big\rangle \\[2mm]
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ its elements are <b>equivalence classes</b> of polynomials.
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ <span style="font-size: 14pt;">$\big\langle x^2+y^2-1 \big\rangle \subset \mathbb{Q}[x, y]$</span> is an example of an <b>ideal</b>, the infinite set of polynomials <br> 
     $\phantom{\circ}$ <span style="font-size: 14pt;">$h(x, y) (x^2+y^2-1)$</span> that vanishes on the unit circle.
</div>


---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Massless Scattering </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 14pt;">$n$</span>-point massless scattering, the quotient ring is
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle \kern10mm R_{n} = \mathbb{F}\Big[|1⟩_{\alpha}, [1|_{\dot\alpha}, \dots, |n⟩_{\alpha}, [n|_{\dot\alpha} \Big] \Big/ \Big\langle {\textstyle \sum_{i=1}^n} |i\rangle[ i | \Big\rangle
$$
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
     $\circ$ The rational functions <span style="font-size: 16pt">$r_i$</span> belong to the field of fractions of <span style="font-size: 16pt">$R_n$</span>,
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
     $\phantom{\circ}$ albeit in this case in a very simplified form since scalars have no states.
</div>
<a href="https://arxiv.org/abs/1809.09644" style="font-size: 14pt; margin-top: -2mm; float: right; font-align: right;"> Shadmi, Weiss </a>
<a href="https://arxiv.org/abs/1802.06730" style="font-size: 14pt; margin-top: -2mm;  margin-right: 2mm; float: right; font-align: right;"> Ochirov; </a>
<a href="https://arxiv.org/abs/1709.04891" style="font-size: 14pt; margin-top: -2mm; margin-right: 2mm; float: right; font-align: right;"> Arkani-Hamed, Huang, Huang;</a>

<div style="font-size: 15pt; margin-top: 12mm; margin-bottom: 5mm">
$$ 
\displaystyle \kern10mm R_{HHH} = \frac{\mathbb{F}\big[|1⟩_{\alpha}, [1|_{\dot\alpha}, |2⟩_{\alpha}, [2|_{\dot\alpha}, \boldsymbol{3}_{\alpha,\dot\alpha}, \boldsymbol{4}_{\alpha,\dot\alpha}, \boldsymbol{5}_{\alpha,\dot\alpha} \big]}{\big\langle |1\rangle[1|+|2\rangle[2| + \boldsymbol{3}_{\alpha,\dot\alpha} + \boldsymbol{4}_{\alpha,\dot\alpha} + \boldsymbol{5}_{\alpha,\dot\alpha}, \;\, \boldsymbol{3}_{\alpha,\dot\alpha} \boldsymbol{3}^{\dot\alpha,\alpha} - \boldsymbol{4}_{\alpha,\dot\alpha} \boldsymbol{4}^{\dot\alpha,\alpha}, \;\, \boldsymbol{4}_{\alpha,\dot\alpha} \boldsymbol{4}^{\dot\alpha,\alpha}- \boldsymbol{5}_{\alpha,\dot\alpha} \boldsymbol{5}^{\dot\alpha,\alpha} \big\rangle}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where <span style="font-size: 15pt;">$\boldsymbol{3}_{\alpha,\dot\alpha} \boldsymbol{3}^{\dot\alpha,\alpha} = \boldsymbol{4}_{\alpha,\dot\alpha} \boldsymbol{4}^{\dot\alpha,\alpha} = \boldsymbol{5}_{\alpha,\dot\alpha} \boldsymbol{5}^{\dot\alpha,\alpha} = 2 M_h^2$</span>.
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

<div style="display:block; width:100%; margin-top: 2mm; margin-bottom: 0mm; margin-left: 0mm;">
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
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 0mm">
               $$
               \displaystyle \mathcal{D} = \prod_j \mathcal{D}_j^{q_{ij}}(|i\rangle,[i|) \, .
               $$
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: -3mm; margin-bottom: 1mm;">
               $\phantom{\circ}\,$ Obtain the <span style="font-size: 16pt">$q_{ij}$</span> from a univariate slice  <span style="font-size: 16pt">$\vec\lambda(t)$</span>, i.e. a 1D curve.
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
               $\circ$ The curve must intersect all varieties <span style="font-size: 16pt">$V(\langle \mathcal{D}_j \rangle)$</span>, e.g.
          </div>
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
               $$
               \displaystyle |i\rangle \rightarrow |i\rangle + t a_i |\eta\rangle, [i| \rightarrow [i| + t b_i [\eta|
               $$
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
               $\phantom{\circ}\,$ Solve for <span style="font-size: 16pt">$a_i, b_i$</span> such that constraints are satisfied.
          </div>
	     <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
               $\circ\,$ Publicly impelemented, see <a href="https://github.com/GDeLaurentis/antares/" style="font-size: 20pt; font-variant: small-caps;">antares</a>, <a href="https://github.com/GDeLaurentis/lips/" style="font-size: 20pt; font-variant: small-caps;">lips</a>, <a href="https://github.com/GDeLaurentis/syngular/" style="font-size: 20pt; font-variant: small-caps;">syngular</a> 
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 1mm; margin-bottom: 1mm;">
               $\phantom{\circ}\,$ <code style="font-size: 15pt;">do_codimension_one_study(func, slice, denoms)</code> <br>
               $\phantom{\circ}\,$ <code style="font-size: 15pt;">Particles.univariate_slice</code> or 
               <code style="font-size: 15pt;">Ring.univariate_slice</code>
          </div>
	</div>
     <div style="width:35%; float: right; display: inline-block; margin-top: 6mm; ">
          <img src="variety_slice_v2-transparent.png"; style="max-width:360px; float:center; border:none; margin-top: -5mm; margin-bottom: -2mm;">
          <div style="width:100%; font-size: 14pt; margin-top: 0mm; margin-bottom: 1mm;">
               Space has dimension $4n-4$,
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 0mm; margin-bottom: 1mm;">
               $\mathcal{D}_j = 0$ have dimension $4n-5$,
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 0mm; margin-bottom: 1mm;">
               $\vec\lambda(t)$'s have dimension 1.
          </div>
     </div>
</div>

<div style="border: 2px solid black; font-size: 16pt; padding: 10px; display: inline-block; margin-top: 4mm;">
    Poles & Zeros $\;\Leftrightarrow\;$ Irreducible Varieties $\;\Leftrightarrow\;$ Prime Ideals <br>
    <i style="font-size: 14pt; border-top: -8mm; border-bottom: -2mm;"> Physics $\kern18mm$ Geometry $\kern18mm$ Algebra </i>
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> A Concrete Example </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For instance, <span style="font-size: 15pt">$\hat d^{+-}_{p_{12}\times p_3 \times p_4}=$</span>
</div>
<div style="font-size: 14pt; margin-top: 0mm; margin-bottom: 3mm">
$$ 
\begin{gathered}
\frac{-1/4⟨1|𝟒|𝟑-𝟓|1⟩⟨1|𝟑|𝟒|𝟓|2](s_{12}-3m_h²+8m_t²)}{⟨12⟩Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{(⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])⟨2|𝟑|𝟒|𝟓|2]⟨1|𝟑|𝟒|1⟩(-1/4(s_{12}-3m_h²+8m_t²)-1/8(s_{1𝟒}-s_{1𝟓}-2s_{12}+2s_{𝟑𝟒}-2m_h²))}{⟨12⟩⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{(⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])⟨1|𝟑|𝟒|𝟓|1]⟨1|𝟓|𝟒|1⟩(-1/4(s_{12}-3m_h²+8m_t²)-1/8(s_{1𝟒}-2s_{1𝟓}-2s_{12}+2s_{𝟑𝟒}))}{⟨12⟩⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{(⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])⟨1|𝟑|𝟒|𝟓|2]⟨1|𝟑|𝟓|2⟩(-1/8(m_h²-3s_{12}+2s_{1𝟒}-2s_{2𝟑}-s_{2𝟒})-1/4(s_{12}-3m_h²+8m_t²))}{⟨12⟩⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{(⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])⟨1|𝟑|𝟒|𝟓|2](3/16⟨1|𝟑|1]²+3/16⟨1|𝟒|1]²+1/8\text{tr}(𝟑|𝟒)⟨2|𝟑|2]+1/16⟨2|𝟑|2]²)}{⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{(⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])(-1/8⟨1|𝟑|2]⟨1|𝟑|𝟓|1⟩+1/4⟨1|𝟒|2]⟨1|𝟑|𝟒|1⟩)}{⟨12⟩Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{-1/4⟨1|𝟒|2]⟨1|𝟒|1](⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])⟨1|𝟑|𝟒|𝟓|1]}{⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}} +\\
\frac{(⟨1|𝟑|𝟒|𝟓|1]-⟨2|𝟑|𝟒|𝟓|2])⟨1|𝟑|𝟒|1⟩m_h²(-1/8m_h²⟨1|𝟒|1]-1/8(s_{𝟑𝟒}-m_h²)⟨2|𝟑|2])}{⟨12⟩⟨2|𝟑|𝟒|𝟓|1]Δ_{12|𝟑|𝟒|𝟓}} +\\
(21𝟓𝟒𝟑,\;\text{True}) \phantom{+}
\end{gathered}
$$
</div>

---

<div style="margin-top: 2mm; margin-bottom: 4mm">
     <b style="font-variant: small-caps; font-size: xx-large">$\boldsymbol{Vjj}$</b> 
     <b style="font-variant: small-caps; font-size: xxx-large">and</b>
     <b style="font-variant: small-caps; font-size: xx-large">$\boldsymbol{t\bar{t}H}$</b>
     <b style="font-variant: small-caps; font-size: xxx-large">LCDs</b>
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\circ\,$ The irreducible denominator factors <span style="font-size: 14pt">$\mathcal{D}_j \text{ for } Vjj$</span> (modding out by permutation orbits) read
</div>
<div style="text-align: center; font-size: 14pt; margin-top: 2mm; margin-bottom: 2mm;">
     $$
     \displaystyle \mathcal{D}_{Vjj} \subset \kern-3mm \bigcup_{\sigma \; \in \; \text{Aut}(R_6)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1], \langle 1|2+3|4], s_{123}, \Delta_{12|34|56}, ⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2] \big\}
     $$
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\phantom{\circ}\,$ where only the last one is new at two loops.
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 3mm; margin-bottom: 2mm;">
     $\circ\,$ The <span style="font-size: 14pt">$\mathcal{D}_j \text{ for } t\bar{t}H$</span> read
</div>
<div style="text-align: center; font-size: 14pt; margin-top: 2mm; margin-bottom: 2mm;">
     $$
     \displaystyle \kern-10mm \mathcal{D}_{ttH} = \big\{ \langle 12 \rangle, [12], s_{123}, \dots, (s_{123}-m^2), \langle 1|\boldsymbol{3}|1], \dots, \\[2mm] 
     \kern30mm \langle 1|\boldsymbol{3}|\boldsymbol{4}| 2 \rangle, \dots, \langle 1|\boldsymbol{3}|1+2|\boldsymbol{4}| 2], \dots, \Delta_{12|34|5}, \dots \Delta_{12|3|4|5} \big\}
     $$
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\phantom{\circ}\,$ note that there is no dependence on the top states (this looks like 3 massive scalars).
</div>

<div style="font-size: 16pt; text-align: left; margin-top: 3mm; margin-bottom: 2mm;">
     $\circ\,$ Challenge: in LCD form the numerators are intractably complicated. <br>
     $\phantom{\circ}\,$ For <span style="font-size: 15pt">$Vjj$</span> the most complicated <span style="font-size: 14pt">$\bar{q}^+g^-g^+q^-$</span> function had a mass dimension (<span style="font-size: 13pt">$\approx$</span> poly. degree) of 114, <br>
     $\phantom{\circ}\,$ and little group weights <span style="font-size: 14pt">$\{3, -12, 12, -3, -1, 1\}$</span>.  The ansatz size is approx. 25M. <br>
     $\phantom{\circ}\,$ Note how different from zero the little group weights are, chiral invariants are important!
</div>

</section>

---

<section>

{{< slide background-image="spinor_coeffs.png" >}}

<br><br><br><br><br><br>

# Analytic Reconstruction

<br><br><br><br><br><br><br>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Invariant Quotient Rings </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Helicity amplitudes are Lorentz invariant: minimal ansätze are build in the invariant sub-rings.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ General construction for Lorentz-Invariant sub-rings through elimination theory
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\quad\star$ Build a ring with both covariant and invariant variables
</div>
<div style="font-size: 15pt; text-align: center; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\mathbb{F}\big[ |i\rangle, [i|, \langle i j\rangle , [ij] \big]
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\quad\star$ Define relations among variables (on top of existing constraints)
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
     $\circ$ We obtain the following invariant rings
</div>
<div style="font-size: 15pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle \mathcal{R}_{Vjj} = \frac{\mathbb{F}\big[ \langle ij\rangle : \, 1\leq i< j\leq 6, i,j \neq 5, \; [ij] : 1\leq i< j\leq 5 \big]}{\big\langle {\textstyle \sum_{i=1}^4} [5|i]\langle i |6\rangle, 34 \text{ Schouten identities} \big\rangle}
$$
</div>
<div style="font-size: 15pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle \mathcal{R}_{ttH} = \mathbb{F}\big[ \underbrace{\langle 12\rangle, \langle \boldsymbol{3}1\rangle ... ⟨2|\boldsymbol{3}|2] ... ⟨2|\boldsymbol{3}|\boldsymbol{4}|2⟩}_{37\; \text{invariants}}
 \big]\Big/ \big\langle \underbrace{⟨2|\boldsymbol{3}|2]⟨2|\boldsymbol{4}|1]-⟨2|\boldsymbol{3}|1]⟨2|\boldsymbol{4}|2]-[1|2]⟨2|\boldsymbol{3}|\boldsymbol{4}|2⟩, ...}_{\text{more than} \; 90 \; \text{generators}} \big\rangle
$$
</div>


---

<b style="font-variant: small-caps; font-size: xxx-large"> The Numerator Ansatz </b>

<div style="text-align: left; font-size: x-large; margin-top: 1mm; margin-bottom: 2mm; ">
$\circ\,$ The numerator Ansatz takes the form
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -6mm; margin-bottom: 4mm;" href=https://arxiv.org/abs/1904.04067>
   GDL, Maître ('19)
</a>
<div style="text-align: center; font-size: x-large; margin-bottom: 5mm; margin-top: 1mm;">
$\displaystyle \text{Num. poly}(\lambda, \tilde\lambda) = \sum_{\vec \alpha, \vec \beta} c_{(\vec\alpha,\vec\beta)} \prod_{j=1}^n\prod_{i=1}^{j-1} \langle ij\rangle^{\alpha_{ij}} [ij]^{\beta_{ij}}$
</div>
<div style="text-align: left; font-size: x-large; float: left; margin-top: -2mm; margin-bottom: 0mm;">
     $\phantom{\circ}$ subject to constraints on $\vec\alpha,\vec\beta$ due to: 1) mass dimension; 2) little group; 3) linear independence.
</div>

<br>

<div style="text-align: left; font-size: x-large; ">
$\circ\,$ Construct the Ansatz via the algorithm from Section 2.2 of <a href=https://arxiv.org/abs/2203.04269>GDL, Page ('22)</a>
</div>
<div style="text-align: center; display: inline-block; font-size: x-large;">
Linear independence = irreducibility by the Gröbner basis of a specific ideal.
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
$\circ\,$ Linear systems solved w/ CUDA over $\mathbb{F}_{2^{31}-1}$ ($t_{\text{solving}} \ll t_{\text{sampling}}$) w/ <a href=https://github.com/GDeLaurentis/linac-dev> linac </a> <span style="text-align: left; font-size: small;"> (coming soon-ish) </span>
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
     $\phantom{\circ}$ The complexity will depend on <span style="font-size: 15pt">$\mathcal{D}_1, \mathcal{D}_2$</span>
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
\langle xy^2 + y^3 - z^2 \rangle + \langle x^3 + y^3 - z^2 \rangle = \langle xy^2 + y^3 - z^2, x^3 + y^3 - z^2 \rangle = \langle 2y^3-z^2, x-y \rangle \cap \langle y^3-z^2, x \rangle \cap \langle z^2, x+y \rangle
$$
</div>
<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\phantom{\circ}$ This is a primary decomposition. If <span style="font-size: 14pt">$\mathcal{N}$</span> vanishes on all branches, than the partial fraction decomposition exists.

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

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Iteratively reconstruct a residues at a time using <span style="text-size: 13pt">$p$</span>-adic numbers to get <span style="text-size: 13pt">$\mathbb{F}_p$</span> samples for the residues
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\begin{alignedat}{2}
& r^{(139 \text{ of } 139)}_{\bar{u}^+g^+g^-d^-(V\rightarrow \ell^+ \ell^-)} = & \qquad\qquad & {\small \text{Variety (scheme?) to isolate term(s)}} \\[2mm]
& +\frac{7/4{\color{blue}(s_{24}-s_{13})}⟨6|1+4|5]s_{123}{\color{green}(s_{124}-s_{134})}}{⟨1|2+3|4]⟨2|1+4|3]^2 Δ_{14|23|56}} +  & \qquad\qquad & \Big\langle ⟨2|1+4|3]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
& -\frac{49/64⟨3|1+4|2]⟨6|1+4|5]s_{123}(s_{123}-s_{234})(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]Δ^2_{14|23|56}} + \dots & \qquad\qquad & \Big\langle Δ_{14|23|56} \Big\rangle
\end{alignedat}
$$
</div>

<div style="text-align: left; font-size: 16pt; margin-top: -2mm; margin-bottom: 0mm;">
$\circ\,$ We get more than just partial fraction decomposition, we cna identify numerator insertions from e.g.:
</div>
<div style="text-align: left; font-size: 12pt; margin-top: 2mm; margin-bottom: 1mm;">
     $$
     \sqrt{\big\langle ⟨2|1+4|3], Δ_{14|23|56} \big\rangle} = \big\langle {\color{green}(s_{124}-s_{134})}, ⟨2|1+4|3] \big\rangle \, , \\[1mm] 
     \big\langle ⟨1|2+3|4], ⟨2|1+4|3] \big\rangle = \big\langle ⟨1|2+3|4], ⟨2|1+4|3], {\color{blue}(s_{13}-s_{24})}\big\rangle \cap \big\langle ⟨12⟩, [34] \big\rangle
     $$
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: 0mm;">
$\circ\,$ Interesting and non-trivial bevhavior also at 5-point 3-mass
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\def\spa#1.#2{\left\langle#1\,#2\right\rangle}
\def\spb#1.#2{\left[#1\,#2\right]}
\def\spaa#1.#2.#3{\langle\mskip-1mu{#1} 
                  | #2 | {#3}\mskip-1mu\rangle}
\def\spbb#1.#2.#3{[\mskip-1mu{#1}
                  | #2 | {#3}\mskip-1mu]}
\def\spab#1.#2.#3{\langle\mskip-1mu{#1} 
                  | #2 | {#3}\mskip-1mu]}
\def\spba#1.#2.#3{[\mskip-1mu{#1} 
                  | #2 | {#3}\mskip-1mu\rangle}
\def\spaba#1.#2.#3.#4{\langle\mskip-1mu{#1} 
                  | #2 | #3 | {#4}\mskip-1mu\rangle}
\def\spbab#1.#2.#3.#4{[\mskip-1mu{#1} 
                  | #2 | #3 | {#4}\mskip-1mu]}
\def\spabab#1.#2.#3.#4.#5{\langle\mskip-1mu{#1}
                  | #2 | #3 | {#4}| {#5} \mskip-1mu]}
\def\spbaba#1.#2.#3.#4.#5{[\mskip-1mu{#1} 
                  | #2 | #3 | {#4}| {#5}\mskip-1mu\rangle}
\def\tr#1.#2{\text{tr}(#1|#2)}
\def\qb{\bar{q}}
\def\Qb{\bar{Q}}
\def\cA{{\cal A}}
\def\slsh{\rlap{$\;\!\!\not$}}     \def\three{{\bf 3}}
\def\four{{\bf 4}}
\def\five{{\bf 5}}
\begin{align}\label{eq:decomp_spaba1351_spbab2542}
\big\langle \spaba1.\three.\five.1,\, \spbab2.\five.\four.2 \big\rangle = \; &\big\langle \,  \spab1.\three.2,\, \spab1.\four.2,\, \spaba1.\three.\five.1,\, \spbab2.\five.\four.2
\, \big\rangle\; \cap \\
&\big\langle \, \spaba1.\three.\five.1,\, \spbab2.\five.\four.2, |\five|2]\langle1|\three| - |1+\three|2]\langle1|\five| \, \big\rangle \;, \nonumber
\end{align} \\
\text{because: } |\five|2]\spaba1.\three.\five.1[2| + |1\rangle\spbab2.\five.\four.2\langle1|\five| = \spab1.\five.2 \Big( |\five|2]\langle1|\three| - |1+\three|2]\langle1|\five| \Big) \, ,
$$
</div>
<div style="text-align: left; font-size: 16pt; margin-top: -2mm; margin-bottom: 0mm;">
$\phantom{\circ}\,$ or between the triangle and box Grams
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\begin{gather}\label{eq:decomp_delta12_34_5_and_delta_12_3_4_5}
  \big\langle \Delta_{12|34|5},\,\Delta_{12|3|4|5} \big\rangle =
  \big\langle
  s_{34},\, \tr1+2.{\three+\four}^2
  \big\rangle \cap
  \big\langle
  \Delta_{12|34|5},\, \tr1+2.{\three-\four}^2 
  \big\rangle \, .
\end{gather}
$$
</div>

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Challenges </b>
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Can we guess the constraints? If not, can we verify them with numerical evaluations? <br>
$\phantom{\circ}\,$ <span style="text-size: 13pt">$\mathbb{Q}_p$</span> evaluations can be costly (probably depending on implementation). <a href=https://arxiv.org/abs/2506.08452> Xia, Yang ('25) </a> say they are not!
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Ideal intersection can be highly non-trivial:
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\mathcal{N} \in \langle q_1, q_2 \rangle \cap \langle q_3, q_4 \rangle \stackrel{?}{=} \langle q_1q_3, q_1q_4, q_2q_3, q_2 q_4\rangle 
$$
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\phantom{\circ}\,$ Unfortunately not always. This is called a <i>complete intersection</i> when it holds.
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Therefore, either: 
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\quad\star\,$ we compute the intersection explicitly (can be prohibitively hard)
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\quad\star\,$ or we have to make a choice of which constrain we manifest
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Computing primary decompositions with these many variables is hard, Singular can't do it on its own
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Even constructing the ansatz requires a GB, which in some cases Singular doesn't easily give
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ And of course computing the reduction to MIs of the amplitude is not easy in the first place.
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

</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# <br> Conclusions <br> & <br> Outlook

---

<b style="font-variant: small-caps; font-size: 36pt; margin-bottom: -6mm;"> Spinor-Helicity Amplitudes Results </b>
<br>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 5mm;">
     $\circ$ The <span style="font-size: 15pt;">$pp\rightarrow Vjj$</span> coefficient functions are now 1.9 MB (down from 1.4 GB), fast and stable. <br>
     $\phantom{\circ}$ Matrices <span style="font-size: 15pt;">$M_{ij}$</span> account for another 2 MB overall. Transcendental basis at <a href="https://gitlab.com/pentagon-functions/PentagonFunctions-cpp">PentagonFunctions++</a>.
</div>
<div style="display: flex; justify-content: center; align-items: flex-start; margin-top: 2mm;">
    <div style="padding: 0 10px;">
        <img src="CoefficientSizes.png" style="width: 100%; max-width: 450px; border: none; margin-top: 2mm; margin-bottom: 0mm;">
    </div>
    <div style="padding: 0 10px; ">
        <img src="h2__g_g__Z_d_d.stability.png" style="width: 100%; max-width: 550px; border: none; margin-top: 3mm; margin-bottom: 0mm;">
    </div>
</div>
<!---
<div style="display: flex; justify-content: center; align-items: flex-start; margin-top: 2mm;">
    <div style="padding: 0 10px;">
        <img src="CoefficientSizes.png" style="width: 100%; max-width: 450px; border: none; margin-top: 2mm; margin-bottom: 0mm;">
    </div>
    <div style="padding: 0 10px; ">
        <img src="h2__g_g__Z_b_b.stability.png" style="width: 100%; max-width: 550px; border: none; margin-top: 4mm; margin-bottom: 0mm;">
    </div>
</div>
<a style="font-size: 11pt; text-align: right; float: right; margin-top: -10mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2404.08598">
Courtesy of V. Sotnikov, <br>see also Mazzitelli, Sotnikov, Wiesemann ('24)
</a>
--->

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ The complexity split is: quarks NMHV: 100 KB, gluons MHV: 200 KB, gluons NMHV: 1.6 MB.
</div>
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ The largest numbers are: quarks NMHV and gluons MHV: 3-digit, gluons NMHV: 12 digits.
</div>
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ Pheno ready results for the hard functions are available at <a href="https://gitlab.com/five-point-amplitudes/FivePointAmplitudes-cpp">FivePointAmplitudes</a>.
</div>
<!---
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ Amplitudes at <a href="https://github.com/GDeLaurentis/antares-results">antares-results</a>, with <a href="https://gdelaurentis.github.io/antares-results/index.html">human readable expr.</a>, and <a href="https://github.com/GDeLaurentis/antares-results/actions/">CI tests</a> for full amplitude in real kinematics
</div>
--->

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> A Numerical CAS for Computations in Q-Rings </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (partially work in progress)
     </p>
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/antares/" style="font-size: 20pt; font-variant: small-caps;">antares</a> (automated numerical to analytical reconstruction software) <br>
     $\rightarrow$ Univariate slicing, LCD determination, basis change, multivariate partial fractioning strategies, <br>
     $\phantom{\rightarrow}$ constraining of numerators, Ansatz generation and fitting strategies <br>
     $\rightarrow$ Most operations do not require defining the variables (or redundancies), only being able to evaluate them.
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/antares-results/" style="font-size: 20pt; font-variant: small-caps;">antares-results</a> (human readable exprs in <a href="https://gdelaurentis.github.io/antares-results/">docs</a>) with <a href="https://github.com/GDeLaurentis/antares-results/actions/">CI tests</a> for coefficients and/or full amplitudes
</div>
<div style="display: flex; justify-content: center; align-items: flex-start; margin-top: 2mm;">
     <img src="antares-results-transparent-combined-v2.png" 
          style="width: 100%; max-width: 850px; float: left; border: none; margin-top: 2mm; margin-bottom: 0mm;">
</div>

</section>

---

<section>

<!--- {{< slide background-image="edmonton.jpg" >}} --->

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
