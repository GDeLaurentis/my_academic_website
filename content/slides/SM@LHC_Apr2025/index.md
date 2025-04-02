---
tile: Two-Loop Five-Point Amplitudes in the Spinor Helicity Formalism
summary: 
authors: ["Giuseppe De Laurentis"]
tags: [QCD, Scattering Amplitudes]
categories: []
date: "2023-05-15T30:00:00Z"
markup: blackfriday
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: sky
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula

---

{{< slide background-image="particle_tracks.jpg" >}}

<h3 style="margin-top:5mm; margin-left: -10mm; margin-right: -10mm;">
	<b style="margin-top:15mm; font-size: 28pt; text-transform: none;">
	   Compact Two-Loop QCD Corrections <br>
	   for $Vjj$ Production in $pp$ Collisions
	</b>
</h3>

<div style="font-size: x-large; margin-top:10mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
<a href="https://arxiv.org/abs/2503.10595">arXiv:2503.10595</a> <div style="font-size: large;"> (GDL, H. Ita, B. Page, V. Sotnikov) </div>

SM@LHC 2025
<div style="font-size: large; margin-top:-5mm; margin-bottom:10mm"> Durham </div>
<p style="line-height: 0.05;"> <img src="UniEdinburghLogo-transparent.png"; style="max-width:120px;float:center;border:none;margin-bottom:5mm;"> 
<br><br><br>
<span style="font-size: 11pt;">Find these slides at  <a href="/slides/sm@lhc_apr2025/#/">gdelaurentis.github.io/slides/sm@lhc_apr2025</a> </span>
</div>

---

<section>

{{< slide background-image="LHCcern.jpg" >}}

# Introduction

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Cross Sections at the Large Hadron Collider </b>

<div style="display: flex; justify-content: center; margin-top: 0mm;">
    <div style="margin: 0 10px;">
        <img src="LHC_map.jpg" style="max-width:480px; border:none; margin-top: 8.5mm; margin-bottom: 0mm;">
    </div>
    <div style="margin: 0 10px;">
        <img src="ATLAS-XSections-transparent.png" style="max-width:450px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
    </div>
</div>

<div style="text-align: left; font-size: 18pt; float: left; margin-top: -2mm; margin-bottom: 4mm;">
     $\circ\,$ Observations at the LHC are beautifully predicted by the Standard Model through,
</div>

<div style="font-size: 18pt; float: center; margin-top: 0mm; margin-bottom: 0mm;">
$$
\require{color}
\require{amsmath}
σ_{2 \rightarrow n - 2} = \sum_{a,b} \int dx_a dx_b f_{a/h_1}(x_a, \mu_F) \, f_{b/h_2}(x_b, \mu_F) \;\hat{\sigma}_{ab\rightarrow n-2}(x_a, x_b, \mu_F, \mu_R) \, , \\
\hat{σ}_{n}=\frac{1}{2\hat{s}}\int d\Pi_{n-2}\;(2π)^4δ^4\big(\sum_{i=1}^n p_i\big)\;|\overline{\mathcal{A}(p_i,h_i,a_i,μ_F, μ_R)}|^2 \, .
$$
</div>

<div style="text-align: left; float:center; font-size: 18pt; margin-top: -3mm; margin-bottom: 4mm;">
    $\phantom{\circ}\,$ At least to the extent with which we can compute <span style="font-size: 15pt"> $\mathcal{A} = \mathcal{A}^{(0)} + \alpha_{(s)}\mathcal{A}^{(1)} + \alpha^2_{(s)}\mathcal{A}^{(2)} + \dots$</span>
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> Precision Physics Requires NNLO Corrections </b>

<div style="text-align: left; font-size: 17pt; float: left; margin-top: -1mm; margin-bottom: 0mm;">
     $\circ\,$ Theoretical uncertainties already larger than experimental ones, especially at higher points
</div>
<div style="width:100%; float: left; display: inline-block;">
     <span style="width:100%; font-size: 14pt; float: left; text-align: left; margin-left:25mm; margin-top:12mm; margin-bottom:-10mm;">
          $\sigma^{\text{exp.}}_{pp \, \rightarrow \, Z \, + \, n\,j}:$
     </span><img src="cross-sections-transposed-transparent.png"; style="max-width:450px;float:center;border:none;margin-top:-5mm ;margin-bottom:2mm;">
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\phantom{\circ}\,$ 13 TeV data for W+jets appears to not be avaiable yet.
</div>

<div style="text-align: left; font-size: 17pt; margin-top: -1mm; margin-bottom: 0mm;">
     $\circ\,$ NNLO is essential for agreement with experiment, e.g.
</div>
<div style="width:100%; float: left; display: inline-block;">
     <span style="width:100%; font-size: 14pt; float: left; text-align: left; margin-left:25mm; margin-top:12mm; margin-bottom:-10mm;">
          $\sigma^{\text{exp.}}_{pp \, \rightarrow \, Z \, + \, n\,j}:$
     </span><img src="cross-sections-transposed-transparent.png"; style="max-width:450px;float:center;border:none;margin-top:-5mm ;margin-bottom:2mm;">
</div>

<div style="text-align: left; font-size: 16pt; fmargin-top: 4mm; margin-bottom: 4mm;">
     $\circ\,$ Phenomenology can be hindered by complexity of results
</div>

<div style="text-align: left; font-size: 16pt;margin-top: 4mm; margin-bottom: 4mm;">
     $\circ\,$ High-multiplicity two-loop amplitudes required also because:
</div>
<div style="display:block; width:100%;margin-top:-2mm;">
  <div style="width:100%; font-size: 16pt; float: left; text-align: left; ">
       $\qquad\star$ As real-virtual-virtual contributions to emerging N$^{3}$LO computations;
  </div>
  <div style="width:100%; font-size: 16pt; float: left; text-align: left; ">
       $\qquad\star$ Many interesting kinematic regions are only accessible with extra radiation (e.g. $p_T$ distributions).
  </div>
</div>


---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Guiding Principles </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Amplitude should be gauge and Lorentz invariant, and little group covariant
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{red} ✗}$ $\xi$-gauge dependence; reference vectors; open Lorentz indices (tensors)
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ $P^\mu\sigma_{\mu\alpha\dot\alpha} = \lambda_\alpha \tilde\lambda_{\dot\alpha}$; all $\alpha, \dot\alpha$ indices contracted
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The singularity structure should be manifest in $\mathbb{C}$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Rational reparametrisations of the kinematics change the denominator structure
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{red} ✗}$ If a function is neither even nor odd, forcing the split misses cancellations
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ Little-group dependend cancellations to obtain the true LCD
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ Work off the real slice: $P^\mu \in \mathbb{C}^4$, $\lambda_\alpha \neq \tilde\lambda_{\dot\alpha}^\dagger$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Focus only on final physical expressions
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Unphysical intermediate steps may be unnecessarily complicated
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ Bypass all intermediate steps with numerical evaluations
</div>

</section>

---

<section>

{{< slide background-image="Feynman-Diagrams-transparent.png" >}}

<h1 style="margin-top: -2mm;"> Numerical Computation </h1>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Partial Amplitudes & Finite Remainders </b>
 
<div style="font-size: 18pt; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ Amplitude (integrands) can be written as (for a suitable choice of master integrals)
</div>
<br>
<div style="font-size: 14.5pt; margin-top: 0mm;  margin-bottom: 2mm">
     $$
     \displaystyle A(\lambda, \tilde\lambda, \ell) =
\sum_{\substack{\Gamma,\\ i \in M_\Gamma \cup S_\Gamma}} \, c_{\,\Gamma,i}(\lambda, \tilde\lambda, \epsilon) \,		\frac{m_{\Gamma,i}(\lambda\tilde\lambda, \ell)}{\textstyle \prod_{j} \rho_{\,\Gamma,j}(\lambda\tilde\lambda, \ell)} \;\; \xrightarrow[]{\int d^D\ell} \;\; \sum_{\substack{\Gamma,\\ i \in M_\Gamma}} \frac{ \sum_{k=0}^{\text{finite}} \, {\color{red}c^{(k)}_{\,\Gamma, i}}(\lambda, \tilde\lambda) \, \epsilon^k}{\prod_j (\epsilon - a_{ij})} \, {\color{orange}I_{\Gamma, i}}(\lambda\tilde\lambda, \epsilon)
$$  
</div>
<div style="font-size: 14pt; float: center; margin-bottom: 5mm; margin-top: 5mm;">
     $\circ$  $\Gamma$: topologies $\quad\circ$ $M_\Gamma$: master integrands $\quad\circ$ $S_\Gamma$: surface terms 
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm;">
     $\circ$ <u>All physical information</u> is contained in the <i>finite remainders</i>, at two loops
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -3mm; margin-bottom: -3mm;" href=https://inspirehep.net/literature/920274>
Weinzierl ('11)
</a>

<div style="font-size: 14.5pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\underbrace{\mathcal{R}^{(2)}}_{\text{finite remainder}} = \mathcal{A}^{(2)}_R \underbrace{- \quad I^{(1)}\mathcal{A}^{(1)}_R \quad - \quad I^{(2)}\mathcal{A}^{(0)}_R}_{\text{divergent + convention-dependent finite part}} + \mathcal{O}(\epsilon)
$$
</div>
<a style="font-size: 13pt; float:right; text-align:right; margin-top:-14mm;" href=https://www.sciencedirect.com/science/article/abs/pii/S0370269398003323?via%3Dihub>
Catani ('98)
</a>
<a style="font-size: 13pt; float:right; margin-top:-9mm;" href=https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.102.162001>
Becher, Neubert ('09)
</a>
<a style="font-size: 13pt; float:right; text-align:right; margin-top:-4mm;" href=https://arxiv.org/abs/0901.1091>
Gardi, Magnea ('09)
</a>

<div style="text-align: left; font-size: 16pt; margin-bottom: 0mm; margin-top:0mm;">
     $\phantom{\circ}$ $\mathcal{A}^{(1)}_R$ to order $\epsilon^2$ is still needed to build $\mathcal{R}^{(2)}$, but there is no real reason to reconstruct it.
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 5mm; margin-bottom: 5mm;">
     $\circ$ Finite remainder as a weighted sum of <i>pentagon functions</i> <a style="font-size: large; display: inline-block; text-align: right; float: right; margin-top: 0mm; margin-left: 4mm; " href=https://arxiv.org/abs/2009.07803> Chicherin, Sotnikov ('20) </a> <a style="font-size: large; display: inline-block; text-align: right; float: right; margin-top: -3mm; margin-left: 4mm; " href=https://arxiv.org/abs/2110.10111> Chicherin, Sotnikov, Zoia ('21) </a>
</div>

<div style="font-size: 14.5pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\textstyle \mathcal{R}(\lambda, \tilde\lambda) = \sum_i \color{red}{r_{i}(\lambda,\tilde\lambda)} \, \color{orange}{h_i(\lambda\tilde\lambda)}
$$
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 3mm; margin-bottom: 0mm;">
     $\circ$  Goal: reconstruct <span style="font-size: 14pt">$\color{red}{r_{i}(\lambda,\tilde\lambda)}$</span> from numerical samples in a field $\mathbb{F}$
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -10mm; margin-bottom: -10mm; margin-right: 24mm;" href=https://arxiv.org/abs/1406.4513>
$\mathbb{F}_p$: von Manteuffel, Schabinger ('14); 
</a> <a style="font-size: large; text-align: right; float: right; margin-top: -10mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1608.01902>
$\phantom{\mathbb{F}_p}$ Peraro ('16)
</a><br>
<a style="font-size: large; text-align: right; float: right; margin-top: -17mm; margin-bottom: -10mm; margin-right: 43mm;" href=https://arxiv.org/abs/1406.4513>
$\mathbb{C}$: GDL, Maitre ('19);
</a> <a style="font-size: large; text-align: right; float: right; margin-top: -16.7mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/1406.4513>
$\mathbb{Q}_p$: GDL, Page ('22)
</a>

---

<b style="font-variant: small-caps; font-size: 34pt; magin-bottom: -5mm;"> Numerical Computation </b> <br>

<div style="font-size: 18pt; text-align:left; margin-bottom: 0mm; margin-top: 2mm;">
$\circ$ Original computation performed with Caravel
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 16pt; width:75%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     $$
	     \require{color}
	     \displaystyle \sum_{\text{states}} \, \prod_{\text{trees}} A^{\text{tree}}(\lambda, \tilde\lambda, \ell)\big|_{\text{cut}_{\Gamma}} = \sum_{\substack{\Gamma' \ge \Gamma, \\ i \in M_\Gamma' \cup S_\Gamma'}} \kern-2mm {\color{red}{c_{\,\Gamma',i}(\lambda, \tilde\lambda)}} \, \frac{m_{\Gamma',i}(\lambda\tilde\lambda, \ell)}{\displaystyle \prod_{j\in P_{\Gamma'} / P_{\Gamma}} \rho_{j}(\lambda\tilde\lambda, \ell)}\Bigg|_{\text{cut}_\Gamma}
	     $$
	</div>
     <div style="width:25%; float: right; display: inline-block; margin-top: -15mm;">
	     <div style="font-size: x-large; width:50%; float: center; text-align: center;  display: inline-block; margin-top: 0mm;">
	     	  <code> C++ code </code>
	     </div><br>
	     <img src="CaravelLogo.png"; style="max-width:150px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
	     <br>
	     <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 5mm;"
	     	href=https://arxiv.org/abs/2009.11957>
		<div style="margin-top:0mm"> Abreu, Dormans, </div>
		<div> Febres Cordero, Ita  </div>
		<div> Kraus, Page, Pascual, </div>
		<div> Ruf, Sotnikov ('20) </div>
	     </a>
	</div>
     <div style="font-size: 18pt; width:75%; float: left; text-align: center; display: inline-block; margin-top: 5mm;">
	     $\star$ Numerical Berends-Giele recursion for LHS, <span style= "color:red"> solve for coeffs. in RHS. </span>
	</div>
     <div style="font-size: 18pt; width:75%; float: left; text-align: center; display: inline-block; margin-top: 5mm;">
	     $\star$ IBP reduction = decomposition on RHS, $\; m_{\Gamma,i} \in M_\Gamma \cup S_\Gamma $
	</div>
</div>

<div style="font-size: 18pt; float: left; margin-bottom: 4mm; margin-top: 8mm;">
$\circ$ This computation used the ancillaries of ...
</div>


</section>

---

<section >

{{< slide background-image="varieties-no-background.png" >}}

<br><br><br><br>

# Analytic & Geometric Structure

<br><br><br><br>

<span style="font-size: 18pt">based on:<span> <br>
<span style="font-size: 18pt">[GDL, Page (JHEP 12 (2022) 140)](https://arxiv.org/abs/2203.04269)<span>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: xxx-large"> Least Common Denominator </b>
     <p style="margin-top: -2mm; margin-bottom: 2mm; font-size: 16pt;">
     (i.e. geometry at codimension one)
     </p>
</div>

<div style="font-size: 16pt; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ$ Polynomials belong to the the covariant quotient ring of spinors,
</div>
<br>
<div style="font-size:15pt; float: center; margin-top: -6mm; margin-bottom: -10mm">
     $$\displaystyle \kern10mm R_n = \mathbb{F}\big[|1⟩, [1|, \dots, |n⟩, [n|\big] \big/ \big\langle \sum_i |i⟩[i| \big\rangle$$
</div>

<div style="display:block; width:100%; margin-top: -6mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: x-large; width:60%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     <div style="font-size: 16pt; float: left; margin-top: 4mm; margin-bottom: 1mm;">
                $\circ\,$ The rational function <span style="font-size: 15pt">$r_i$</span> belong to the field of fractions of <span style="font-size: 14pt">$R_n$</span>,
          </div>
          <br><br>
          <div style="font-size:16pt; float: center; margin-top: -3mm; margin-bottom: 0mm">
               $$
               \displaystyle r_i(|i\rangle,[i|) = \frac{\mathcal{N}(|i\rangle,[i|)}{\prod_j \mathcal{D}_j^{q_{ij}}(|i\rangle,[i|)}
               $$
          </div>
          <div style="font-size: 16pt; float: left; margin-top: 0mm; margin-bottom: 1mm;">
               $\circ\,$ The <span style="font-size: 14pt">$\mathcal{D}_j$</span> are related to the letters of the symbol alphabet
          </div>
          <br>
          <a style="font-size: 13pt; text-align: right; float: right; margin-top: 0mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1812.04586>
          Abreu, Dormans, Febres Cordero, Ita, Page ('18)
          </a>
          <br>
          <div style="font-size:14pt; float: center; margin-top: 1mm; margin-bottom: 0mm">
               $$
               \displaystyle \{\mathcal{D}_{\{1,\dots,35\}}\} = \bigcup_{\sigma \; \in \; \text{Aut}(R_5)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1] \big\}
               $$
          </div>
          <div style="font-size:13pt; float: right; margin-top: -10mm; margin-bottom: 0mm;">
               $\kern0mm\color{green}\text{Identical to 1-loop!}$
          </div>
	</div>
     <div style="width:40%; float: right; display: inline-block; margin-top: 6mm;">
          <img src="V2.png"; style="max-width:260px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
          <div style="width:100%; font-size: 14pt; margin-top: -2mm; margin-bottom: 1mm;">
               The codimension one variety 
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 1mm; margin-bottom: 1mm;">
               $\langle x^3 + y^3 - z^2 \rangle$ in $\mathbb{R}[x,y,z]$
          </div>
     </div>
</div>

<div style="text-align: center; float: left; font-size: 14pt; margin-top: -5mm; margin-bottom: -2mm;">
     $$
     \displaystyle \kern5mm \{D_j\} \subset \kern-3mm \bigcup_{\sigma \; \in \; \text{Aut}(R_6)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1], \langle 1|2+3|4], s_{123}, \Delta_{12|34|56}, ⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2] \big\}
     $$
</div>
<div style="font-size:13pt; float: right; margin-top: -10mm; margin-bottom: 1mm;">
     $\kern0mm\color{green}\text{New letter! Can we get rid of it?}$
</div>

<div style="border: 2px solid black; font-size: 16pt; padding: 10px; display: inline-block; margin-top: 2mm;">
    Poles & Zeros $\;\Leftrightarrow\;$ Irreducible Varieties $\;\Leftrightarrow\;$ Prime Ideals <br>
    <i style="font-size: 14pt; border-top: -8mm; border-bottom: -2mm;"> Physics $\kern18mm$ Geometry $\kern18mm$ Algebra </i>
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Multivariate Partial Fraction Decompositions </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (i.e. geometry at codimension greater than one)
     </p>
</div>

<div style="display: flex; margin-top:-6mm;">
    <div style="flex: 1;">
        <img src="V1.png" style="max-width:60%; height:auto;">
        <div style="width:100%; font-size: 14pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\langle xy^2 + y^3 - z^2 \rangle$
        </div>
    </div>
    <div style="flex: 1; max-width:3%; margin-top:20mm;">
        $\cap$
    </div>
    <div style="flex: 1;">
        <img src="V2.png" style="max-width:60%; height:auto;">
        <div style="width:100%; font-size: 14pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\langle x^3 + y^3 - z^2 \rangle$
        </div>
    </div>
    <div style="flex: 1; max-width:3%; margin-top:20mm;">
        $=$
    </div>
    <div style="flex: 1;">
        <img src="V3.png" style="max-width:60%; height:auto;">
        <div style="width:100%; font-size: 14pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\begin{gather}\langle 2y^3-z^2, x-y \rangle \cap \langle y^3-z^2, x \rangle \\ \cap \langle z^2, x+y \rangle\end{gather}$ 
        </div>
    </div>
</div>

<div style="text-align: left; font-size:16pt; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ$ When is a partial fraction decomposition possible? (an example)
</div><br>
<div style="font-size:14pt; float: center; margin-top: -6mm; margin-bottom: 1mm;">
     $$
     \frac{\mathcal{N}}{(\prod_j \mathcal{D}_j^{q_j})\times\langle 4|1+3|4]\langle 5|1+4|5]} \stackrel{?}{=} \frac{\mathcal{N}_1}{(\prod_j \mathcal{D}_j^{q_j})\times\langle 4|1+3|4]} + \frac{\mathcal{N}_2}{(\prod_j \mathcal{D}_j^{q_j})\times\langle 5|1+4|5]}
     $$
</div>

<div style="text-align: left; font-size:16pt; float: left; margin-top: 2mm; margin-bottom: -4mm;">
     $\circ$ Compute primary decompositions and check if <span style="font-size: 14p">$\mathcal{N}$</span> vanishes on all branches (Hilbert's Nullstellensatz)
</div><br>
<div style="font-size:14pt; float: center; margin-top: -4mm; margin-bottom: 1mm;">
     $$
     J = K \cap \bar K \cap L \cap \bar L \cap M \quad \text{or} \quad V(J) = V(K) \cup V(\bar K) \cup V(L) \cup V(\bar L) \cap V(M)
     $$
</div>

<div style="font-size:14pt; float: center; margin-top: 1mm; margin-bottom: 1mm;">
     $$
     J = \big\langle \langle 4|1+3|4], \langle 5|1+4|5] \big\rangle \qquad
     K = \big\langle \langle14\rangle,\langle15\rangle,\langle45\rangle,[23] \big\rangle \quad
     L = \big\langle \langle ij\rangle \; \forall \; i,j\in\{1,\dots 5\} \big\rangle \\[2mm]
     M = \big\langle \langle 4|1+3|4], \langle 5|1+4|5], |1+4|5\rangle\langle14\rangle + |5|4\rangle\langle15\rangle, \langle\rangle \leftrightarrow [] \big\rangle
     $$
</div>

<div style="text-align: center; float: center; font-size: 16pt; margin-top: 0mm; margin-bottom: 0mm;">
     For a fleshed out example with open-source code see <a href=https://inspirehep.net/literature/2661970> GDL (ACAT '22) </a>
</div>

</section>

---

<section>

{{< slide background-image="spinor_coeffs.png" >}}

<br><br><br><br><br><br>

# Analytic Reconstruction

<br><br><br><br>

<p style="margin-top:13mm; font-size: 16pt;">
also based on: <br>
GDL, Ita, Page, Sotnikov (to appear)
</p>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Basis Change based on Pole Residues </b>

<div style="text-align: left; font-size: 16pt; float: left; margin-top: -2mm; margin-bottom: -2mm;">
     $\circ\,$ Change basis from a subset of the pentagon coefficients $r_{i \in \mathcal{B}}$ to <span style="font-size: 14pt">$\mathbb{Q}$</span>-linear combinations $\tilde r$,
</div><br>
<div style="text-align: center; float: center; font-size: 15pt; margin-top: -8mm; margin-bottom: 0mm;">
     $$
     R = r_j h_j = r_{i\in \mathcal{B}} M_{ij} h_j = \tilde{r}_{i} \, O_{ii'}M_{i'j} \, h_j \, , \qquad O_{ii'}, M_{ij}\in \mathbb{Q}
     $$
</div>

<div>
<img src="BasisChangeEffectWjj.png"; style="max-width:800px; float:center; border:none; margin-top: -2mm; margin-bottom: 0mm;">
</div>

<div style="text-align: center; font-size: 14pt; float: center; margin-top: -6mm; margin-bottom: 0mm;">
     $\phantom{\circ}\,$ Notation: [mass dimension], {Little-group weights}
</div>

<div style="text-align: left; font-size: 16pt; float: left; margin-top: 3mm; margin-bottom: -2mm;">
     $\circ\,$ By Gaussian elimination, partition the space:
</div> <br>
<div style="text-align: center; font-size: 15pt; float: center; margin-top: -2mm; margin-bottom: 2mm;">
     $$
     \text{span}(r_{i \in \mathcal{B}}) = \underbrace{\text{column}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))}_{\text{functions with the singularity}} \;\;\; \oplus \, \underbrace{\text{null}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))}_{\text{functions without the singularity}}
     $$
</div>

<div style="display:block; width:100%; margin-top: -4mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 17pt; width:50%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     <div style="font-size: 17pt; float: left; margin-top: 4mm; margin-bottom: 1mm;">
               $\circ\,$ Search for linear combinations that remove as many singularities as possible
          </div>
          <br>
          <div style="font-size:15pt; float: left; margin-top: 0mm; margin-bottom: 0mm">
               $$
               \kern12mm \displaystyle O_{i'i} = \bigcap_{k, m} \, \text{nulls}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))
               $$
          </div>
	</div>
     <div style="width:50%; float: right; display: inline-block; margin-top: 0mm;">
          <img src="search_tree.png"; style="max-width:400px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
     </div>
</div>

---

<b style="font-variant: small-caps; font-size: 36pt; margin-bottom: -6mm;"> Spinor-Helicity Results </b>
<br>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: -4mm;">
     $\circ$ The 5-gluon MHV rational functions fit in 3 pages of the appendix,
</div>

<div style="text-align: center; float:center; font-size: x-large; margin-bottom: 1mm; margin-top: -2mm;">
<img src="VSSizeTable-transparent.png"; style="max-width:350px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
<img src="quarks_vs_sizes.png"; style="max-width:340px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
</div>

<div style="text-align: left; font-size: 13pt; margin-bottom: 1mm; margin-top: 5mm;">
     $$ \tilde{r}^{\text{MHV}}_{\text{first 5 of 115}} = \left\{ \frac{⟨45⟩^2}{⟨12⟩⟨13⟩⟨23⟩}, \frac{⟨45⟩^3}{⟨12⟩^2⟨34⟩⟨35⟩}, \frac{⟨45⟩^3}{⟨12⟩⟨15⟩⟨23⟩⟨34⟩}, \frac{[14][12][35]}{⟨23⟩[45]^3}, \frac{⟨45⟩^2⟨24⟩}{⟨12⟩^2⟨23⟩⟨34⟩}, \dots \right\} \text{+ symmetries}$$
</div>


<div style="text-align: left; font-size: 16pt; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The <span style="font-size: 14pt;">$pp\rightarrow Wjj$</span> functions are now 1.9 MB (from 1.3 GB),
</div>

<div style="display: flex; justify-content: center; margin-top: -10mm;">
    <div style="margin: 0 10px;">
        <img src="W_vs_sizes.png"; style="max-width:400px; float:center; border:none; margin-top: 18mm; margin-bottom: 0mm;">
    </div>
    $\kern4mm$
    <div style="margin: 0 10px;">
        <img src="CoefficientSizes.png"; style="max-width:350px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
    </div>
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 1mm; margin-top: -4mm;">
     $\phantom{\circ}$ Since <code style="font-size: 14pt;">PentagonsFunction++</code> can take permutations of the 1-mass basis we only need one <span style="font-size: 14pt;">$M_{ij}$</span> per partial <br> $\phantom{\circ}$ (another 2 MB overall). We now have fast and stable floating-point evaluations in double precision!
</div>

</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# Outlook

---

<b style="font-variant: small-caps; font-size: 30pt; margin-bottom: 4mm;">
   Taming the Complexity Growth
</b>

<div style="display:block; width:100%; font-size: 16pt; margin-top: 4mm; margin-bottom: 4mm;">
     <div style="width:50%; text-align: left; float: left; display: font-size: x-large; margin-top:8mm;">
          $\circ$ For every leg or mass, the number of letters in the spinor alphabet grows, as well their mass dimension;  <br><br>
          $\circ$ The LCD Ansatz size also grows quickly with <br> multiplicity (m) and mass dimension (d): <br><br>
          <a style="font-size: 12pt; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: -12mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/2010.14525>
               GDL, Maître ('20)
          </a> <br>
          <div style="text-align: left; font-size: 14pt; margin-top: -12mm; margin-bottom: 1mm;">
               $$
               \displaystyle \kern2mm \text{Ansatz size} \geq \small \left(\mkern -9mu \begin{pmatrix}\, m(m-3)/2 \, \\ \, d/2 \, \end{pmatrix} \mkern -9mu \right)
               $$
          </div>
     </div>
     <div style="width:50%; float: right; display: inline-block; margin-top: 4mm;">
          <img src="AnsatzSizes.png"; style="max-width:430px;float:center;border:none;margin-top:-10pt;margin-bottom: 0mm;">
     </div>
</div>

<br><br><br><br><br><br><br><br>

<div style="text-align: left; font-size: 16pt; margin-top: -6mm; margin-bottom: -4mm;">
$\circ\,$ We can retain control by iterating surface by surface
</div>
<a style="font-size: 12pt; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: -3mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/fix>
     Campbell, GDL, Ellis, ('22)$\;$
</a>
<a style="font-size: 12pt; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: -3mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/2203.04269>
     GDL, Page ('22);$\;$
</a>
<a style="font-size: 12pt; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: -3mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1904.04067>
     GDL, Maître ('19);$\;$
</a>

<br>
<div style="text-align: left; font-size: 13pt; margin-top: -8mm; margin-bottom: 1mm;">
$$ 
\begin{alignedat}{2}
& r^{(139 \text{ of } 139)}_{\bar{u}^+g^+g^-d^-(V\rightarrow \ell^+ \ell^-)} = & \qquad\qquad & {\small \text{Variety (scheme?) to isolate term(s)}} \\[2mm]
& +\frac{7/4(s_{24}-s_{13})⟨6|1+4|5]s_{123}(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]^2 Δ_{14|23|56}} & \qquad\qquad & \Big\langle ⟨2|1+4|3]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
& -\frac{49/64⟨3|1+4|2]⟨6|1+4|5]s_{123}(s_{123}-s_{234})(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]Δ^2_{14|23|56}} + \dots & \qquad\qquad & \Big\langle Δ_{14|23|56} \Big\rangle
\end{alignedat}
$$
</div>
<!--- 
 \\[1mm]
& + {\small \dots \text{more than 30 other fractions} \dots } &&
& +\frac{1/4[12]^3⟨14⟩[45]⟨46⟩}{[13][23]⟨1|2+3|1]⟨4|5+6|4]^2} & \qquad\qquad & \Big\langle ⟨1|2+3|1], ⟨4|5+6|4]^2 \Big\rangle \\[1mm]
& -\frac{1/4[12]2⟨13⟩⟨24⟩[45]⟨46⟩}{⟨12⟩[13]⟨2|1+3|2]⟨4|5+6|4]^2}-\frac{3/4⟨34⟩2[45]⟨46⟩⟨3|1+2|4]}{⟨14⟩⟨23⟩⟨2|1+3|4]⟨4|5+6|4]^2} & \qquad\qquad & \Big\langle ⟨4|5+6|4] \Big\rangle \\[1mm]
& \frac{-7/8⟨16⟩⟨1|2+3|5]⟨3|1+4|2](s_{13}-s_{24} )(s_{123}-s_{234})}{⟨14⟩⟨1|2+3|4]^2⟨2|1+4|3]Δ_{14|23|56}} & \qquad\qquad & \Big\langle ⟨1|2+3|4]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
& +\frac{7/2⟨13⟩^3[15]⟨16⟩[23]}{⟨12⟩⟨14⟩⟨1|2+3|1]⟨1|2+3|4]^2}+\frac{7/2⟨13⟩^2⟨16⟩[25]}{⟨12⟩⟨14⟩⟨1|2+3|4]^2} & \qquad\qquad & \Big\langle ⟨1|2+3|4] \Big\rangle \\[1mm]
& -\frac{7⟨24⟩[25][35]s_{123}}{⟨12⟩[23][56]⟨2|1+4|3]^2} & \qquad\qquad & \Big\langle ⟨2|1+4|3] \Big\rangle \\[1mm]
--->

<div style="text-align: left; font-size: 16pt; margin-top: -4mm; margin-bottom: -4mm;">
$\circ\,$ Partial fraction decomposition and numerator insertions from e.g.:
</div>
<div style="text-align: left; font-size: 12pt; margin-top: 0mm; margin-bottom: 1mm;">
     $$
     \sqrt{\big\langle ⟨2|1+4|3], Δ_{14|23|56} \big\rangle} = \big\langle s_{124}-s_{134}, ⟨2|1+4|3] \big\rangle \, , \\[1mm] 
     \big\langle ⟨1|2+3|4], ⟨2|1+4|3] \big\rangle = \big\langle ⟨1|2+3|4], ⟨2|1+4|3], (s_{13}-s_{24})\big\rangle \cap \big\langle ⟨12⟩, [34] \big\rangle
     $$
</div>

</section>

---

<section>

<!---
<b style="font-variant: small-caps; font-size: xxx-large; margin-bottom: 10mm;">
   Conclusions
</b>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ Full-color 5-point massless amplitudes are well within reach, 
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ Subleading color corrections can be fairly sizable
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ The reconstruction can be peformed in spinor-helicity variables, which yield compact results
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ Understanding the partial fraction structure of amplitudes is essential to tame their complexity
</div>

---
--->


{{< slide background-image="Prague.jpeg" >}}

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

# Backup Slides

---

<div style="font-size: x-large; float: center; margin-top:4mm;">
</div>

<div style="display: flex; justify-content: center;">
    <div style="margin: 0 10px;">
        <div style="margin-top: 2mm; margin-bottom: 4mm">
          <b style="font-variant: small-caps; font-size: xxx-large"> Full $N_C $ motivation</b>
        </div>
        <div style="font-size: 16pt;">
        3 is not that big! And certainly not close to $\infty$
        </div>
        <img src="correction_sizes_catani.png" style="max-width:500px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
        <div style="font-size: 15pt; margin-bottom: 3mm;">
        Slc contributions to $pp\rightarrow jjj$ should be similar to blue curve.
        </div>
        <div style="font-size: 15pt; margin-bottom: 3mm;">
        Expect $\mathcal{O}(10\%)$ effect on duble-virtual hard function, <br> this is scheme dependant.
        </div>
        <div style="font-size: 15pt;">
        Effect on $\sigma^{\text{NNLO}}$ depends on size of $\mathcal{H}^{(2)}$.
        </div>
    </div>
    <div style="margin: 0 10px;">
        <div style="margin-top: 2mm; margin-bottom: 4mm">
          <b style="font-variant: small-caps; font-size: xxx-large"> Pheno. Goal</b>
        </div>
        <div style="font-size: 16pt; margin-bottom:2mm;">
        Stable and fast evaluations for cross sections
        </div>
        <img src="h2_5g.png" style="max-width:490px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
        <div style="font-size: 15pt; margin-bottom:-4mm;">
        <code> C++ </code> Code available at
        </div>
        <a href="https://gitlab.com/five-point-amplitudes/FivePointAmplitudes-cpp" style="font-size: 14pt;">gitlab.com/five-point-amplitudes/FivePointAmplitudes-cpp</a>
        <div style="font-size: 15pt; margin-bottom:-4mm;">
        Analytics available at
        </div>
        <a href="https://zenodo.org/records/10142295" style="font-size: 14pt;">zenodo.org/records/10142295</a> <span style="font-size: 16pt">&</span>
        <a href="https://zenodo.org/records/10231547" style="font-size: 14pt;">zenodo.org/records/10231547</a>
        <div style="font-size: 15pt; margin-bottom:-4mm;">
        with <code style="font-size: 14pt;">Mathematica</code>, <code style="font-size: 14pt;">Python</code> and <code style="font-size: 14pt;">C++</code> scripts.
        </div>
    </div>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large; margin-bottom: -5mm;"> Constraints from Poles </b>
<br>
<b style="font-variant: small-caps; font-size: x-large; margin-top: -16mm;"> Bootstrapping trees (?) </b>

<div style="font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 8mm;">
     $\circ$ The degree of divergence / vanishing on various surfaces imposes strong constraints, e.g.
</div>

<div style="font-size: 20pt; float: center; margin-top: 5mm; margin-bottom: 5mm;">
     $ A^{\text{tree}}_{q^+g^+g^+\bar q^-g^-g^-} = \frac{\mathcal{N(\text{m.d.} = 6\,,\; \text{p.w.} = [-1, 0, 0, 1, 0, 0])}}{\langle 12\rangle\langle 23\rangle\langle 34\rangle [45][56][61]s_{345}}$
</div>

<div style="font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 5mm;">
     $\circ$ Pretend this is un unknown integral coefficient, $\mathcal{N}$ has 143 free parameters.
</div>

<div style="font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 5mm;">
     $\circ$ List the various prime ideal, such as
</div>

<br><br><br>

<div style="font-size: 20pt; float: center; margin-top: -2mm; margin-bottom: 0mm;">
     $ \big\langle \langle 12\rangle, \langle 23\rangle, \langle 13\rangle \big\rangle, \; \big\langle |1\rangle \big\rangle, \; \big\langle \langle 12\rangle, |1+2|3]\big\rangle, \dots$
</div>

<div style="font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 2mm;">
     $\phantom{\circ}$ and impose that $\mathcal{N}$ vanishes to the correct order. We determine it up to an overall constant.
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -2mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/2207.10125>
     GDL, Page ('22)
</a>

<div style="font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 5mm;">
     $\circ$ Likewise, the ansatz for $A^{\text{tree}}_{g^+g^+g^+ g^-g^-g^-}$ shrinks $1326 \rightarrow 1$, etc..
</div>

<br><br><br>

<div style="font-size: x-large; float: center; margin-top: -2mm; margin-bottom: 0mm;">
     <i> Effectively, we can <b> compute </b> trees, just from their <u>poles orders</u>. <br> Note: compared to BCFW there is <u>no</u> information about <u>residues</u>. </i>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Partial Fraction Decompositions </b>

<div style="font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ$ For integral coefficients, we can't rely on the Ansatz to shrinks to an overall constant.
</div>

<div style="font-size: x-large; float: left; margin-top: 3mm; margin-bottom: 0mm;">
     $\circ$ Partial fraction decompositions (PFDs) are a popular method to tame algebraic complexity.
</div>

<div style="font-size: x-large; float: left; margin-top: 3mm; margin-bottom: 0mm;">
     $\circ$ In my opinion, a PFD algorithm needs
</div>
<br><br><br>
<div style="font-size: x-large; float: center; margin-top: -3mm; margin-bottom: 5mm;">
     $1.$ to say if two poles $W_a$ and $W_b$ are separable into different fractions; <br>
     $2.$ ideally, to answer $(1.)$ without having access to an analytic expression. 
</div>

<div style="font-size: x-large; float: left; margin-top: 1mm; margin-bottom: 0mm;">
     $\circ$ <span style="color: green">Hilbert's nullstellensatz</span>: if $\mathcal{N}$ vanishes on all branches of $\langle W_a, W_b \rangle$, then the PFD is possible$\kern-3mm\phantom{x}^\dagger$.
</div>
<div style="font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ Generalizing to powers $>\kern-1mm 1$ can be done via <span style="color: green">symbolic powers</span> and the <span style="color: green">Zariski-Nagata Theorem</span>.
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: 1mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/.>
   GDL, Page ('22)
</a>
<div style="font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ Similarly, generalizing to non-radical ideals requires <span style="color: green">ring extensions</span>.
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: 0mm; margin-bottom: 0mm; margin-right: 33mm;" href=https://arxiv.org/abs/.>
   Campbell, GDL, Ellis ('22)
</a>

<div style="font-size: x-large; float: left; margin-top: 7mm; margin-bottom: 0mm;">
     <b> Issue: </b>evaluations on singular surfaces are expensive, but are not always needed!
</div>
<div style="font-size: x-large; float: left; margin-top: 1mm; margin-bottom: 0mm;">
     <b> Opportunity: </b>we get more than partial fraction decompositions.
</div>

<br><br><br><br><br><br>

<div style="font-size: large; float: center; margin-top: 5mm; margin-bottom: 5mm;">
     $\kern-4mm\phantom{x}^\dagger$ $\langle W_a, W_b\rangle$ needs to be radical.
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Beyond Partial Fractions </b>

<div style="font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ$ $\color{red}\text{Case 0}$: the ideal does $\color{green}\text{not involve denominator factors}$.
</div>
<div style="font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     E.g. a 6-point function $c_i$ has a pole at $⟨1|2+3|4]$ but not at $⟨4|2+3|1]$,
</div>
<div style="font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     yet it is regular on the irreducible surface $V(\big\langle ⟨1|2+3|4], ⟨4|2+3|1] \big\rangle)$. Then
</div>
<br><br>
<div style="font-size: x-large; float: center; margin-top: 5mm; margin-bottom: 0mm;">
     $\displaystyle c_i \sim \frac{⟨4|2+3|1]}{⟨1|2+3|4]} + \mathcal{O}(⟨1|2+3|4]^0) \; \text{ instead of } \; c_i \sim \frac{1}{⟨1|2+3|4]}  + \mathcal{O}(⟨1|2+3|4]^0)$
</div>

<div style="font-size: x-large; float: left; margin-top: 8mm; margin-bottom: 0mm;">
     $\circ$ $\color{red}\text{Case 1}$: the $\color{green}\text{degree of vanishing is non-uniform}$ across branches, for example:
</div>
<br>
<div style="font-size: x-large; float: center; margin-top: 0mm; margin-bottom: 0mm;">
     $\displaystyle \frac{s_{14}-s_{23}}{⟨1|3+4|2]⟨3|1+2|4]}$
</div>
<div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 0mm;">
     has a double pole on the first branch, and a simple pole on the second branch of
</div>
<br>
<div style="font-size: x-large; float: center; margin-top: 3mm; margin-bottom: 0mm;">
     $\big\langle⟨1|3+4|2], ⟨3|1+2|4]\big\rangle_{R_6} = \big\langle ⟨13⟩, [24] \big\rangle_{R_6} \cap \big\langle ⟨1|3+4|2], ⟨3|1+2|4], (s_{14}-s_{23})\big\rangle_{R_6}$
</div>

<div style="font-size: x-large; float: left; margin-top: 10mm; margin-bottom: 0mm;">
     $\circ$ $\color{red}\text{Case 2}$: ideal is $\color{green}\text{non-radical}$ (example on last slide)
</div>
<br><br>
<div style="font-size: x-large; float: center; margin-top: -3mm; margin-bottom: 0mm;">
     $\displaystyle \small \kern0mm \sqrt{\big\langle {\color{black}⟨3|1+4|2]}, {\color{black}Δ_{23|14|56}} \big\rangle_{R_6}} = \big\langle {\color{black}⟨3|1+4|2]}, {\color{black}s_{124}-s_{134}} \big\rangle_{R_6} $
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
