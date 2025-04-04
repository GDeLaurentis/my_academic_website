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

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> $V+n\text{-jet}$ Cross Sections at the LHC </b>


<div style="text-align: left; font-size: 18pt; float: left; margin-top: -2mm; margin-bottom: 4mm;">
     $\circ\,$ Observations at the LHC are beautifully predicted by the Standard Model
</div>
<div style="font-size: 16pt; float: center; margin-top: 0mm; margin-bottom: 0mm;">
$$
\require{color}
\require{amsmath}
σ_{2 \rightarrow n - 2} = \sum_{a,b} \int dx_a dx_b f_{a/h_1}(x_a, \mu_F) \, f_{b/h_2}(x_b, \mu_F) \;\hat{\sigma}_{ab\rightarrow n-2}(x_a, x_b, \mu_F, \mu_R) \, , \\
\hat{σ}_{n}=\frac{1}{2\hat{s}}\int d\Pi_{n-2}\;(2π)^4δ^4\big(\sum_{i=1}^n p_i\big)\;|\overline{\mathcal{A}(p_i,h_i,a_i,μ_F, μ_R)}|^2 \, .
$$
</div>
<div style="text-align: left; float:center; font-size: 18pt; margin-top: -3mm; margin-bottom: 4mm;">
    $\phantom{\circ}\,$ at least to the extent with which we can compute <span style="font-size: 14pt"> $\mathcal{A} = \mathcal{A}^{(0)} + \alpha_{(s)}\mathcal{A}^{(1)} + \alpha^2_{(s)}\mathcal{A}^{(2)} + \dots$</span>
</div>

<div style="display: flex; justify-content: center; margin-top: 0mm;">
     <div style="margin: 0 10px; margin-left: -2mm;">
         <img src="ATLAS-XSections-transparent-Vnj.png" style="max-width:450px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
     </div>
     <div style="margin: 0 10px; margin-left: -2mm;">
          <table style="border-collapse: collapse; text-align: center; margin-top: 4mm; font-size: 14pt;">
               <tr>
                    <td style="border: 1px solid black; padding: 5px; text-align: center;">3</td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #FFD700; text-align: center;">
                    2023 <a href="https://arxiv.org/abs/example8">[6]</a>
                    </td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #FF7F7F; text-align: center;">
                    ?
                    </td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #FF7F7F; text-align: center;">
                    ?
                    </td>
               </tr>
               <tr>
                    <td style="border: 1px solid black; padding: 5px; text-align: center;">2</td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #90EE90; text-align: center;">
                    2007 <a href="https://arxiv.org/abs/example7">[4]</a>
                    </td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #FFD700; text-align: center;">
                    2021 <a href="https://arxiv.org/abs/2110.07541">[5]</a>
                    </td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #FF7F7F; text-align: center;">
                    ?
                    </td>
               </tr>
               <tr>
                    <td style="border: 1px solid black; padding: 5px; text-align: center;">1</td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #90EE90; text-align: center;">
                    1981 <a href="https://arxiv.org/abs/example6">[1]</a>
                    </td>
                    <td style="border: 1px solid black; padding: 5px; background-color: #90EE90; text-align: center;">
                    1997 <a href="https://arxiv.org/abs/example10">[2]</a>
                    </td>
                    <td style="border: 1px solid black; padding: 5px; background-color:rgb(250, 255, 0); text-align: center;">
                    2008 <a href="https://arxiv.org/abs/example11">[3]</a>
                    </td>
               </tr>
               <tr>
                    <th style="border: 1px solid black; padding: 5px; text-align: center;">Loops ↑<br>Jets →</th>
                    <th style="border: 1px solid black; padding: 5px; text-align: center;">$1$</th>
                    <th style="border: 1px solid black; padding: 5px; text-align: center;">$2$</th>
                    <th style="border: 1px solid black; padding: 5px; text-align: center;">$\geq3$</th>
               </tr>
          </table>
          <div style="margin-top: 5mm; margin-bottom: 2mm; font-size: 12pt;">
               <span style="background-color: #90EE90; padding: 5px; margin-right: 10px;">Analytic</span>
               <span style="background-color: rgb(250, 255, 0); padding: 5px; margin-right: 10px;"> Numeric</span>
               <span style="background-color: #FFD700; padding: 5px; margin-right: 10px;">Analytic (LCA)</span>
               <span style="background-color: #FF7F7F; padding: 5px; margin-right: 10px;">Unknown</span>
          </div>
          <div style="width: 105%; margin-left: -2mm;">
               <div style="font-size: 14pt; margin-top: 4mm; margin-bottom: -4mm;">
                    <a href="https://www.sciencedirect.com/science/article/abs/pii/0550321381901656?via%3Dihub">[1] Ellis, Ross, Terrano; </a>
                    <a href="https://arxiv.org/abs/hep-ph/9708239">[2] Bern, Dixon, Kosower;</a>
                    <a href="https://arxiv.org/abs/0803.4180">[3] BlackHat; </a><a href="https://arxiv.org/abs/1907.13071">OpenLoops; </a>
                    <a href="https://arxiv.org/abs/0711;.4711">[4] Gehrmann-De Ridder, Gehrmann, Glover, Heinrich; </a>
                    <a href="https://arxiv.org/abs/2110.07541">[5] Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov </a> 
                    <a href="https://arxiv.org/abs/2503.10595" style="color:rgb(255, 149, 0);">+ This talk; </a>
                    <a href="https://arxiv.org/abs/2307.15405">[6] Gehrmann, Jakubčík, Mella, Syrrakos, Tancredi</a>
               </div>
          </div>
     </div>
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> Precision Physics Requires Compact Amplitudes </b>

<div style="text-align: left; font-size: 18pt; float: left; margin-top: -1mm; margin-bottom: -2mm;">
     $\circ\,$ Theoretical uncertainties already larger than experimental ones, especially at higher points
</div>
<div style="width:100%; float: left; display: inline-block;">
     <span style="width:100%; font-size: 16pt; float: left; text-align: left; margin-left:12mm; margin-top:16mm; margin-bottom:-10mm;">
          $\sigma^{\text{tot.}}_{pp \, \rightarrow \, Z \, + \, n\,j}:$
     </span><img src="cross-sections-transposed-transparent-v2.png"; style="max-width:600px;float:center;border:none; margin-top:-10mm ;margin-bottom:2mm; margin-left:25mm;">
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -8mm; margin-bottom: -4mm;" href=https://inspirehep.net/literature/2808096>
ATLAS Collab. '24
</a>

<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ\,$ NNLO is essential for agreement with experiment, e.g.
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -4mm;" href=https://arxiv.org/abs/2404.08598>
Mazzitelli, Sotnikov, Wiesemann '24
</a>
<div style="width:100%; display: inline-block;">
     <span style="width:100%; font-size: 18pt; float: left; text-align: left; margin-left:5mm; margin-top:15mm; margin-bottom:-10mm;">
          $\frac{d\sigma_{pp \, \rightarrow \, Z \, + \, \geq 1 \, b \text{ jet}}}{d |\eta|^{b-\text{jet}_1}}:$
     </span><img src="Z1jSotnikov-transparent-v2.png"; style="max-width:550px;text-align:center;border:none;margin-top:-15mm ;margin-bottom:2mm;">
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 0mm; margin-bottom: 2mm;">
     $\circ\,$ Besides this, only two other cross-section studies at NNLO, only for the process <span style="font-size: 16pt">$q\bar q'\rightarrow Wb\bar b$</span>
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -3mm; margin-bottom: -3mm;" href=https://arxiv.org/abs/2212.04954>
$\,$Buonocore, Devoto, Kallweit, Mazzitelli, Rottoli, Savoini '22;
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -3mm; margin-bottom: -3mm;" href=https://arxiv.org/abs/2205.01687>
Hartanto, Poncelet, Popescu, Zoia '22;$\,$
</a>

<div style="text-align: left; font-size: 18pt; margin-top: 10mm; margin-bottom: 4mm;">
     $\circ\,$ Phenomenology can be hindered by complexity of results. It's hard to do Monte Carlo integration <br> $\phantom{\circ}\,$ and verify IR cancellations when you have to evaluate >1GB of files in higher precision.
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

<b style="font-variant: small-caps; font-size: 34pt; magin-bottom: -5mm;"> Setting up the Calculation </b> <br>

<div style="font-size: 18pt; text-align:left; margin-bottom: 0mm; margin-top: 2mm;">
$\circ$ Original computation  <a href="https://arxiv.org/abs/hep-ph/9708239" style="font-size: 18pt">[1]</a> was performed with <code style="font-size: 17pt">Caravel</code>
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 16pt; width:75%; text-align: left; display: inline-block; margin-top: 3mm;">
	     $$
	     \require{color}
	     \displaystyle \sum_{\text{states}} \, \prod_{\text{trees}} A^{\text{tree}}(\lambda, \tilde\lambda, \ell)\big|_{\text{cut}_{\Gamma}} = \sum_{\substack{\Gamma' \ge \Gamma, \\ i \in M_\Gamma' \cup S_\Gamma'}} \kern-2mm {\color{black}{c_{\,\Gamma',i}(\lambda, \tilde\lambda)}} \, \frac{m_{\Gamma',i}(\lambda\tilde\lambda, \ell)}{\displaystyle \prod_{j\in P_{\Gamma'} / P_{\Gamma}} \rho_{j}(\lambda\tilde\lambda, \ell)}\Bigg|_{\text{cut}_\Gamma}
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
     <div style="font-size: 18pt; width:75%; text-align: left; display: inline-block; margin-top: 5mm;">
	     $\star$ Numerical Berends-Giele recursion for LHS, solve for coeffs. in RHS.
	</div>
     <div style="font-size: 18pt; width:75%; text-align: left; display: inline-block; margin-top: 2mm;">
	     $\star$ IBP reduction = decomposition on RHS, <span style="font-size: 16t">$\; m_{\Gamma,i} \in M_\Gamma \cup S_\Gamma$</span>
	</div>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 0mm; margin-top: 8mm;">
     $\circ$ This computation started from the ancillaries files of <a href="https://arxiv.org/abs/hep-ph/9708239" style="font-size: 18pt">[1] </a>
     <div style="font-size: 18pt; width:99%; text-align: left; display: inline-block; margin-top: 5mm; margin-left:10mm;">
	     1. Wrote a Python script to split the 1.4 GB ancillaries into >10k files <br>
	     2. Compile into 18.2 GB of C++ binaries (for reference <code style="font-size: 17pt">Caravel</code> compiles into approx. 5 GB) <br>
          3. Obtain <span style="font-size: 16t">$\mathbb{F}_p$</span> evaluations of the form factors (each takes approx. 1 sec per point)<br>
          4. Recombine triplets of form factors into helicity amplitudes
	</div>
</div>

<a href="https://arxiv.org/abs/2110.07541" style="font-size: 18pt">[1] Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov '21</a>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Guiding Principles </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Amplitude should be gauge and Lorentz invariant, and little group covariant
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 10mm; margin-right: 2mm;">
     ${\color{red} ✗}$ gauge dependence; reference vector dependence; tensors decomposition $\epsilon_\mu T^\mu$
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
     ${\color{greeN} ✓}$ Chiral cancellations yield true Least Common Denominator
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

<div style="display:block; width:100%; margin-top: 2mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: x-large; width: 65%; text-align: left; display: inline-block; margin-top: 2mm;">
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 2mm;">
               $\circ$ Polynomials belong to the the covariant quotient ring of spinors,
          </div>
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
               $$\displaystyle \kern10mm R_n = \mathbb{F}\big[|1⟩, [1|, \dots, |n⟩, [n|\big] \big/ \big\langle \sum_i |i⟩[i| \big\rangle$$
          </div>
	     <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
                $\circ\,$ The rational function <span style="font-size: 16pt">$r_i$</span> belong to the field of fractions of <span style="font-size: 16pt">$R_n$</span>,
          </div>
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
               $$
               \displaystyle r_i(|i\rangle,[i|) = \frac{\mathcal{N}(|i\rangle,[i|)}{\prod_j \mathcal{D}_j^{q_{ij}}(|i\rangle,[i|)}
               $$
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
                $\phantom{\circ}\,$ we obtain  <span style="font-size: 16pt">$q_{ij}$</span> from a univariate slice  <span style="font-size: 16pt">$\vec\lambda(t)$</span>.
          </div>
          <div style="font-size: 16pt; float: left; margin-top: 2mm; margin-bottom: 2mm;">
               $\circ\,$ The <span style="font-size: 14pt">$\mathcal{D}_j$</span> are related to the letters of the symbol alphabet
          </div>
          <a style="font-size: 13pt; text-align: center; float: left; margin-left:40mm; margin-top: 0mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1812.04586>
          Abreu, Dormans, Febres Cordero, Ita, Page ('18)
          </a>
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

<div style="text-align: center; float: center; font-size: 14pt; margin-top: 10mm; margin-bottom: 4mm;">
     $
     \displaystyle \kern5mm \{D_j\} \subset \kern-3mm \bigcup_{\sigma \; \in \; \text{Aut}(R_6)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1], \langle 1|2+3|4], s_{123}, \Delta_{12|34|56}, ⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2] \big\}
     $
</div>
<div style="font-size:13pt; float: right; margin-top: -9mm; margin-bottom: 1mm;">
     $\kern0mm\color{green}\text{New letter!}$
</div>
<div style="border: 2px solid black; font-size: 16pt; padding: 10px; display: inline-block; margin-top: 0mm;">
    Poles & Zeros $\;\Leftrightarrow\;$ Irreducible Varieties $\;\Leftrightarrow\;$ Prime Ideals <br>
    <i style="font-size: 14pt; border-top: -8mm; border-bottom: -2mm;"> Physics $\kern18mm$ Geometry $\kern18mm$ Algebra </i>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Basis Change from Pole Residues </b>

<div style="text-align: left; font-size: 16pt; float: left; margin-top: -2mm; margin-bottom: -2mm;">
     $\circ\,$ Change basis from a subset of the pentagon coefficients $r_{i \in \mathcal{B}}$ to <span style="font-size: 14pt">$\mathbb{Q}$</span>-linear combinations $\tilde r$,
</div><br>
<div style="text-align: center; float: center; font-size: 15pt; margin-top: -8mm; margin-bottom: 0mm;">
     $$
     R = r_j h_j = r_{i\in \mathcal{B}} M_{ij} h_j = \tilde{r}_{i} \, O_{ii'}M_{i'j} \, h_j \, , \qquad O_{ii'}, M_{i'j}\in \mathbb{Q}
     $$
</div>

<div>
<img src="BasisChangeEffectWjj.png"; style="max-width:900px; float:center; border:none; margin-top: -2mm; margin-bottom: 0mm;">
</div>
<div style="text-align: center; font-size: 14pt; float: center; margin-top: -3mm; margin-bottom: 0mm;">
     [<a href="https://arxiv.org/abs/hep-ph/9708239" style="font-size: 14pt">6</a>] Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov '21
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

</section>

---

<section>

{{< slide background-image="spinor_coeffs.png" >}}

<br><br><br><br><br><br>

# Analytic Reconstruction

<br><br><br><br><br><br><br>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Reconstruction from Conjectured Properties </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (for planar five-point one-mass amplitudes - all properties checked a posteriori)
     </p>
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 3mm; margin-bottom: 2mm;">
     $\circ\,$ Denominator pairs <span style="font-size: 16pt">$\{\mathcal{D}_i, \mathcal{D}_j\}$</span> can be <i>cleanly separated</i>:
</div>
<div style="font-size:14pt; text-align: center; margin-top: 2mm; margin-bottom: 1mm;">
     $$
     \frac{\mathcal{N}}{\mathcal{D}_i^{q_i}\mathcal{D}_j^{q_j}\mathcal{D}_{\text{rest}}} \rightarrow \frac{\mathcal{N}_i}{\mathcal{D}_i^{q_i}\mathcal{D}_{\text{rest}}} + \frac{\mathcal{N}_j}{\mathcal{D}_j^{q_j}\mathcal{D}_{\text{rest}}}
     $$
</div>
<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\phantom{\circ}\,$ Examples of <span style="font-size: 16pt">$\{\mathcal{D}_i, \mathcal{D}_j\}$</span> are:
</div>
<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\qquad\star\,$ Any pairs of <span style="font-size: 16pt">$s_{ijk}$</span> or <span style="font-size: 16pt">$\Delta_{ij|kl|mn}$</span> or <span style="font-size: 16pt">$\langle i|j|p_V|k|i]-\langle j|l|p_V|k|j]$</span> <br>
     $\qquad\star\,$ Any conjugate pair <span style="font-size: 16pt">$\{\langle i|j+k|l], \langle l|j+k|i]\}$</span> or cyclic <span style="font-size: 16pt">$\{\langle i|j\rangle, [i|j]\}$</span> <br>
     $\qquad\star\,$ Pairs of the form <span style="font-size: 16pt">$\{\Delta_{ij|kl|mn}, \langle a|b+c|d]\}$</span> and <span style="font-size: 16pt">$\{\Delta_{ij|kl|mn}, \langle ab \rangle\}$</span> and <span style="font-size: 16pt">$\{\Delta_{ij|kl|mn}, [ab]\}$</span> <br>
     $\qquad\phantom{\star}\,$ unless <span style="font-size: 16pt">$\{bc\}$</span> are <span style="font-size: 16pt">$\{ij\}$</span> or <span style="font-size: 16pt">$\{kl\}$</span> or <span style="font-size: 16pt">$\{mn\}$</span>
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 8mm; margin-bottom: 2mm;">
     $\circ\,$ Denominator pairs <span style="font-size: 16pt">$\{\mathcal{D}_i, \mathcal{D}_j\}$</span> can be <i>separated to order $\kappa$</i>:
</div>

<div style="text-align: center; font-size: 18pt; margin-top: 3mm; margin-bottom: -2mm;">
     ${\color{greeN} ✓}$ Reconstruction only requires <span style="font-size: 16pt">$\mathbb{F}_p$</span> samples $\;{\color{greeN} ✓}$Already simpler than original ones (<span style="font-size: 14pt">$\sim$</span>20MB) <br>
     $\;{\color{red} ✗}$ Results are unstable and sub-optimal, e.g. numbers of this size appeared
</div>
<span style="font-size: 14pt">127187555379407704220939486282289348327703498501718808908391691454242601886997968263623652083189652150273</span>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Iterated Pole Subtraction </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (i.e. geometry at codimension greater than one)
     </p>
</div>

<div style="text-align: left; font-size:16pt; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ$ Multivariate Partial Fraction Decompositions
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

<div style="text-align: left; font-size: 16pt; margin-top: -4mm; margin-bottom: 0mm;">
$\circ\,$ Retain control iterating surface by surface
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\begin{alignedat}{2}
& r^{(139 \text{ of } 139)}_{\bar{u}^+g^+g^-d^-(V\rightarrow \ell^+ \ell^-)} = & \qquad\qquad & {\small \text{Variety (scheme?) to isolate term(s)}} \\[2mm]
& +\frac{7/4(s_{24}-s_{13})⟨6|1+4|5]s_{123}(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]^2 Δ_{14|23|56}} & \qquad\qquad & \Big\langle ⟨2|1+4|3]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
& -\frac{49/64⟨3|1+4|2]⟨6|1+4|5]s_{123}(s_{123}-s_{234})(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]Δ^2_{14|23|56}} + \dots & \qquad\qquad & \Big\langle Δ_{14|23|56} \Big\rangle
\end{alignedat}
$$
</div>

<div style="text-align: left; font-size: 16pt; margin-top: -4mm; margin-bottom: -4mm;">
$\circ\,$ Partial fraction decomposition and numerator insertions from e.g.:
</div>
<div style="text-align: left; font-size: 12pt; margin-top: 0mm; margin-bottom: 1mm;">
     $$
     \sqrt{\big\langle ⟨2|1+4|3], Δ_{14|23|56} \big\rangle} = \big\langle s_{124}-s_{134}, ⟨2|1+4|3] \big\rangle \, , \\[1mm] 
     \big\langle ⟨1|2+3|4], ⟨2|1+4|3] \big\rangle = \big\langle ⟨1|2+3|4], ⟨2|1+4|3], (s_{13}-s_{24})\big\rangle \cap \big\langle ⟨12⟩, [34] \big\rangle
     $$
</div>

<div style="text-align: center; float: center; font-size: 16pt; margin-top: 0mm; margin-bottom: 0mm;">
     For a fleshed out example with open-source code see <a href=https://inspirehep.net/literature/2661970> GDL (ACAT '22) </a>
</div>

</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# Outlook

---

<b style="font-variant: small-caps; font-size: 36pt; margin-bottom: -6mm;"> Spinor-Helicity Results </b>
<br>

<div style="text-align: left; font-size: 16pt; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The <span style="font-size: 14pt;">$pp\rightarrow Wjj$</span> functions are now 1.9 MB (from 1.4 GB),
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

1.6MB 200KB 100KB

<div style="text-align: left; font-size: 16pt; margin-bottom: 1mm; margin-top: -4mm;">
     $\phantom{\circ}$ Since <code style="font-size: 14pt;">PentagonsFunction++</code> can take permutations of the 1-mass basis we only need one <span style="font-size: 14pt;">$M_{ij}$</span> per partial <br> $\phantom{\circ}$ (another 2 MB overall). We now have fast and stable floating-point evaluations in double precision!
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ quarks nmhv and gluons mhv largest number has 3-digit, gluons nmhv 12 digits
</div>

</section>

---

<section>

{{< slide background-image="durham.jpeg" >}}

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
