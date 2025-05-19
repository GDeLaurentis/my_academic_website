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
  theme: white
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula

---

{{< slide background-image="particle_tracks.jpg" >}}

<h3 style="margin-top:5mm; margin-left: -10mm; margin-right: -10mm;">
	<b style="margin-top:15mm; font-size: 32pt; text-transform: none;">
	   Analytic Structure and Reconstruction in QCD: Two-Loop $\boldsymbol{pp \to Vjj}$ and One-Loop $\boldsymbol{q\bar{q}\rightarrow t\bar{t}H}$
	</b>
</h3>

<div style="font-size: x-large; margin-top:8mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
Vjj: <a href="https://arxiv.org/abs/2503.10595">arXiv:2503.10595</a> <div style="font-size: large; margin-bottom:5mm;"> (GDL, H. Ita, B. Page, V. Sotnikov) </div>
ttH: <a href="https://arxiv.org/abs/2504.19909">arXiv:2504.19909</a> <div style="font-size: large;"> (J. Campbell, GDL, K. Ellis) </div>


LoopFest XXIII
<div style="font-size: large; margin-top:-5mm; margin-bottom:5mm"> Edmonton, CA </div>
<p style="line-height: 0.05;"> <img src="UniEdinburghLogo-transparent.png"; style="max-width:120px;float:center;border:none;margin-bottom:5mm;"> 
<br><br><br>
<span style="font-size: 11pt; margin-top: 10mm;">Find these slides at  <a href="/slides/sm@lhc_may2025/#/">gdelaurentis.github.io/slides/loopfest_may2025</a> </span>
</div>

---

<section>

{{< slide background-image="LHCcern.jpg" >}}

# Introduction

---

<b style="font-variant: small-caps; font-size: 32pt; margin-top: 2mm; margin-bottom: 0mm;">Phenomenological Motivation</b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 4mm; margin-top: 0mm;">
     $\circ\,$ <span style="font-size: 16pt">$pp\rightarrow Vjj$</span> (or similarly <span style="font-size: 16pt">$e^+e^-\rightarrow V \rightarrow 4j$</span>) is important for several EW precision measurements
</div>
<!-- Static background image (fades via fragment) -->
<div style="position: relative; width: 100%; min-height: 450px;">
     <!-- Fragment 1: full-opacity image -->
     <div class="fragment" data-fragment-index="1"
          style="position: absolute; top: 0; left: 0; z-index: 0; margin-top: 4mm;">
          <img src="ATLAS-XSections-transparent.png"
               style="max-width: 550px; opacity: 1; border: none; margin: 0;" />
     </div>
     <!-- Fragment 2: faded image and content -->
     <div class="fragment visible" data-fragment-index="2" 
          style="position: absolute; top: 0; left: 0; z-index: 0; margin-top: 4mm;">
          <img src="ATLAS-XSections-transparent-Vnj.png"
               style="max-width: 550px; opacity: 0.10; border: none; margin: 0;" />
     </div>
     <!-- Main text container (shown at same time as faded background) -->
     <div class="fragment visible" data-fragment-index="2"
          style="position: relative; z-index: 1; margin-left: 15%; padding: 10px;">
          <div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: -5mm;">
          $\rightarrow\,$ Theoretical uncertainties are already larger than experimental ones,
          <img src="cross-sections-transposed-transparent-v2.png"
               style="max-width:600px; border:none; margin-left:20mm; margin-top: 2mm;" />
          <a style="font-size: large; text-align: right; float: right; margin-top: -6mm;" href="https://inspirehep.net/literature/2808096">
          ATLAS Collab. '24
          </a>
          </div>
          <div style="clear: both; text-align: left; font-size: 18pt; margin-top: -10mm;">
          $\rightarrow\,$ NNLO is essential for agreement with experiment,
          <a style="font-size: large; text-align: right; float: right; margin-top: 5mm;" href="https://arxiv.org/abs/2404.08598">
          Mazzitelli, <div style="height: -10mm; margin-top: -1mm; margin-bottom: -1mm;"></div> Sotnikov, <div style="height: -10mm; margin-top: -1mm; margin-bottom: -1mm;"></div> Wiesemann '24
          </a>
          <img src="Z1jSotnikov-transparent-v2.png"
               style="max-width:500px; border:none; margin-left:24mm; margin-top: 0mm;" />
          <div style="text-align: right; font-size: 18pt; margin-top: -5mm; margin-bottom: 0mm; margin-left: -22mm;">
          Other studies at NNLO only for <span style="font-size: 16pt">$q\bar q'\rightarrow Wb\bar b, \; \text{e.g. no} \; gg\rightarrow Wq\bar q'$</span> despite available amps
          </div>
          <a style="font-size: large; text-align: right; float: right; margin-top: -1mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2212.04954">
          $\,$Buonocore, Devoto, Kallweit, Mazzitelli, Rottoli, Savoini '22;
          </a>
          <a style="font-size: large; text-align: right; float: right; margin-top: -1mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2205.01687">
          Hartanto, Poncelet, Popescu, Zoia '22;$\,$
          </a>
          </div>
     </div>
</div>

<div class="fragment" data-fragment-index="2"
     style="text-align: left; font-size: 17pt; margin-bottom: 2mm; margin-top: -8mm;">
     $\circ\,$ <span style="font-size: 16pt">$pp\rightarrow ttH$</span> of interest primarily for direct access to top Yukawa <span style="font-size: 16pt">$y_t$</span> (but also CP, EFTs, 2HDM, etc.) <br>
     $\phantom{\circ}\,$ current N$^2$LO pheno. relies on approx. amplitudes
     <a style="font-size: large; text-align: right; float: right; margin-top: 0mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2210.07846">
     Catani, Devoto, Grazzini, Kallweit, Mazzitelli, Savoini '22;$\,$
     </a>
     <a style="font-size: large; text-align: right; float: right; margin-top: -3mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2411.15340">
     Devoto, Grazzini, Kallweit, Mazzitelli, Savoini '24;$\,$
     </a>
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> Theoretical Motivation </b>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ Status for Drell-Yan plus jets (Vjj)
</div>
<div style="display: flex; justify-content: center; margin-top: 0mm;">
     <div style="width: 55%; text-align: left; font-size: 17pt; margin: 0 10px; margin-left: -4mm;">
          $\;\star\,$ Limited knowledge at higher loops/points; <br>
          $\;\star\,$ All amplitudes in the lower triangle contribute  <br> 
          $\;\phantom{\star}\,$ at a given perturbatifve order; <br> 
          $\;\star\,$ Pheno can be hindered by complexity of results, <br> 
          $\;\phantom{\star}\,$ especially if IR cancellations are needed; <br> 
          $\;\star\,$ E.g. the two-loop amps of [5] were >1GB of files. <br><br>
          $\circ\,$ Goal: reduce complexity of [5] by manifesting the analytic structure to facilitate future computations
     </div>
     <div style="width: 55%; font-size: 14pt; margin: 0 10px; margin-left: -4mm; margin-right: -4mm;">
          <table style="border-collapse: collapse; text-align: center; margin-top: 1mm; font-size: 14pt;">
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


<div style="text-align: left; font-size: 18pt; margin-bottom: 1mm; margin-top: 2mm; margin-left: -4mm;">
     $\circ\,$ Status for $pp\rightarrow t\bar tH$
</div>
<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 0mm; margin-left: -4mm;">
     $\;\star\,$ one-loop: <span style="font-size: 15pt">$q\bar q\rightarrow t\bar tH$</span> previously not known analytically; <br>
     $\kern15mm$ <span style="font-size: 15pt">$gg\rightarrow t\bar t H$</span> known to <span style="font-size: 15pt">$\mathcal{O}(\epsilon^2)$</span> in terms of form factors <br>
     <a style="font-size: large; text-align: right; float: right; margin-top: -5mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2312.10015">
     Buccioni, Kreer, Liu, Tancredi '23
     </a>
     $\;\star\,$ two-loop: <span style="font-size: 15pt">$q\bar q\rightarrow t\bar tH$</span> with quark-loop (<span style="font-size: 15pt">$n_f$</span> part), known numerically (<a href="https://secdec.readthedocs.io/en/stable/" style="font-variant: small-caps;">pySecDec</a>) <br>
     <a style="font-size: large; text-align: right; float: right; margin-top: -1mm; margin-bottom: -4mm;" href="https://arxiv.org/abs/2402.03301">
     Agarwal, Heinrich, Jones, Kerner, Klein, Lang, Magerya, Olsson '24
     </a>
     $\kern15mm$ <span style="font-size: 15pt; margin-top: 5mm;">$pp\rightarrow t\bar tH$</span> master integrals in LCA
     <a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -3mm;" href="https://arxiv.org/abs/2312.08131">
     Febres Cordero, Figueiredo, Kraus, Page, Reina '23
     </a>
     $\circ\,$ Goal: show how to reconstruct amplitudes in a manifestly spin- and little-group covariant form
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
<a style="font-size: 13pt; float:right; text-align:right; margin-top:-18mm;" href=https://www.sciencedirect.com/science/article/abs/pii/S0370269398003323?via%3Dihub>
Catani ('98)
</a>
<a style="font-size: 13pt; float:right; margin-top:-13mm;" href=https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.102.162001>
Becher, Neubert ('09)
</a>
<a style="font-size: 13pt; float:right; text-align:right; margin-top:-8mm;" href=https://arxiv.org/abs/0901.1091>
Gardi, Magnea ('09)
</a>

<div style="text-align: left; font-size: 16pt; margin-bottom: 0mm; margin-top:0mm;">
     $\phantom{\circ}$ <span style="font-size: 15pt">$\mathcal{A}^{(1)}_R$</span> to order <span style="font-size: 15pt">$\epsilon^2$</span> is still needed to build <span style="font-size: 15pt">$\mathcal{R}^{(2)}$</span>, but there is no real physical reason to reconstruct it.
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

<div style="font-size: 18pt; text-align:left; margin-bottom: 0mm; margin-top: 0mm;">
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
     <div style="font-size: 18pt; width:75%; text-align: left; display: inline-block; margin-top: 5mm; margin-bottom: -4mm;">
	     $\star$ Numerical Berends-Giele recursion for LHS, solve for coeffs. in RHS.<br>
	     $\star$ IBP reduction = decomposition on RHS, <span style="font-size: 16t">$\; m_{\Gamma,i} \in M_\Gamma \cup S_\Gamma$</span>
	</div>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 0mm; margin-top: 6mm;">
     $\circ$ This computation started from the ancillaries files of <a href="https://arxiv.org/abs/hep-ph/9708239" style="font-size: 14pt">[1] Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov</a>
     <div style="font-size: 18pt; width:99%; text-align: left; display: inline-block; margin-top: 2mm; margin-left:10mm;">
	     1. Wrote a Python script to split the 1.4 GB ancillaries into >10k files <br>
	     2. Compile into 18.2 GB of C++ binaries (for reference <code style="font-size: 17pt">Caravel</code> compiles into approx. 5 GB) <br>
          3. Obtain <span style="font-size: 16t">$\mathbb{F}_p$</span> evaluations of the form factors (each takes approx. 1 sec per point)<br>
          4. Recombine triplets of form factors into helicity amplitudes
	</div>
</div>

<div style="font-size: 18pt; text-align:left; margin-bottom: 0mm; margin-top: 4mm;">
$\rightarrow$ Assemble 5 helicity amplitudes into 3 categories: <span style="font-size: 15pt;">$\mathcal{R}_{\bar qQ\bar QqV}^{\text{NMHV}} ,\, \mathcal{R}_{\bar qggqV}^{\text{MHV}} ,\, \mathcal{R}_{\bar qggqV}^{\text{NMHV}}$</span>
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

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Guiding Principles </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Amplitude should be gauge and Lorentz invariant, and spin and little-group covariant
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{red} ✗}$ gauge dependence, e.g. through reference vectors <br>
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{red} ✗}$ tensor decompositions <span style="font-size: 16pt;">$\epsilon_\mu T^\mu$</span>, polarizations are needed for simplifications
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ <span style="font-size: 16pt;">$\epsilon_\mu \rightarrow \epsilon_{\alpha\dot\alpha}$, $P^\mu \rightarrow  \lambda_\alpha \tilde\lambda_{\dot\alpha}$</span>; all <span style="font-size: 16pt;">$\alpha, \dot\alpha$</span> indices contracted; all <span style="font-size: 16pt;">$\lambda, \tilde\lambda$</span> random (subject to mom cons)
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The singularity structure should be manifest in $\mathbb{C}$ (exprs will then be better behaved in $\mathbb{R}$ too)
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Rational reparametrisations of the kinematics change the denominator structure
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Forcing unphysical splits misses cancellations (e.g. even nor odd separation)
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ Chiral cancellations are required to obtain the true Least Common Denominator
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ Work off the real slice: <span style="font-size: 16pt;">$P^\mu \in \mathbb{C}^4$, $\lambda_\alpha \neq \tilde\lambda_{\dot\alpha}^\dagger$</span>. In practice, <span style="font-size: 16pt;">$P^{\mu=y}\in i\mathbb{Q}\Rightarrow \lambda_{\alpha} \in \mathbb{F}_p \text{ or } \mathbb{Q}_p$</span>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 4mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Focus only on final physical expressions
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Unphysical intermediate steps may be unnecessarily complicated
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 3mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Analytic manipulations at this complexity are unfeasible, even on "physical" results
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 6mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ Bypass all intermediate steps with numerical evaluations (cancellations happen numerically)
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Trade-offs and Challenges </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ We must work with <u>variables subject to constrains</u>; the language is that of algebraic geometry.
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ The covariant rings are
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle \kern10mm R_{Vjj} = \mathbb{F}\big[|1⟩_{\alpha}, [1|_{\dot\alpha}, |2⟩_{\alpha}, [2|_{\dot\alpha}, |3⟩_{\alpha}, [3|_{\dot\alpha},  |4⟩_{\alpha}, [4|_{\dot\alpha}, [5|_{\dot\alpha}, |6⟩_{\alpha} \big] \Big/ \big\langle {\textstyle \sum_{i=1}^4} [5|i]\langle i |6\rangle \big\rangle
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where we took the the <span style="font-size: 15pt;">$V$</span> current to be <span style="font-size: 15pt;">$[5|\gamma^\mu|6\rangle$</span> and removed $5_{\alpha\dot\alpha}$ by mom. cons.; and
</div>
<div style="font-size: 15pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle \kern10mm R_{ttH} = \frac{\mathbb{F}\big[|1⟩_{\alpha}, [1|_{\dot\alpha}, |2⟩_{\alpha}, [2|_{\dot\alpha}, |\boldsymbol{3}^I⟩_{\alpha}, [\boldsymbol{3}^I|_{\dot\alpha}, |\boldsymbol{4}_J⟩_{\alpha}, [\boldsymbol{4}_J|_{\dot\alpha}, \boldsymbol{5}_{\alpha\dot\alpha} \big]}{\big\langle \sum_{i=1}^5 |i\rangle[i|, \langle \boldsymbol{3}|\boldsymbol{3}⟩ +[\boldsymbol{3}|\boldsymbol{3}], \langle \boldsymbol{3}|\boldsymbol{3}⟩-\langle \boldsymbol{4}|\boldsymbol{4}⟩, \langle \boldsymbol{4}|\boldsymbol{4}⟩ +[\boldsymbol{4}|\boldsymbol{4}]\big\rangle}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where <span style="font-size: 15pt;">$\langle \boldsymbol{3}^I|\boldsymbol{3}^J⟩=m\epsilon^{JI} \text{ and } [\boldsymbol{3}^I|\boldsymbol{3}^J⟩=\bar{m}\epsilon^{IJ}$</span>; we are setting <span style="font-size: 15pt;">$m=\bar{m}$</span> and the tops on-shell. <br>
     $\phantom{\circ}$ <u>Note</u>: we need only reconstruct a single choice, say <span style="font-size: 15pt;">$I=J=1$</span>, the other follow by covariance.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Helicity amplitudes are Lorentz invariant; minimal ansätze are build in the invariant sub-rings
</div>
<div style="font-size: 15pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle \mathcal{R}_{Vjj} = \frac{\mathbb{F}\big[ \langle ij\rangle : \, 1\leq i< j\leq 6, i,j \neq 5, \; [ij] : 1\leq i< j\leq 5 \big]}{\big\langle {\textstyle \sum_{i=1}^4} [5|i]\langle i |6\rangle, 34 \text{ Schouten identities} \big\rangle}
$$
</div>
<div style="font-size: 15pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle \mathcal{R}_{ttH} = \mathbb{F}\big[ \underbrace{\langle 12\rangle, \langle \boldsymbol{3}1\rangle ... ⟨2|\boldsymbol{3}|2] ... ⟨2|\boldsymbol{3}|\boldsymbol{4}|2⟩}_{37\; \text{invariants}}
 \big]\Big/ \big\langle \underbrace{⟨2|\boldsymbol{3}|2]⟨2|\boldsymbol{4}1]-⟨2|\boldsymbol{3}|1]⟨2|\boldsymbol{4}|2]-[1|2]⟨2|\boldsymbol{3}|\boldsymbol{4}|2⟩, ...}_{\text{more than} \; 90 \; \text{generators}} \big\rangle
$$
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
                $\circ\,$ The rational functions <span style="font-size: 16pt">$r_i$</span> belong to the field of fractions of <span style="font-size: 16pt">$R_X$</span>,
          </div>
          <div style="font-size:16pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
               $$
               \displaystyle r_i(|i\rangle,[i|) = \frac{\mathcal{N}(|i\rangle,[i|)}{\prod_j \mathcal{D}_j^{q_{ij}}(|i\rangle,[i|)} % \, , \quad r_i(|i\rangle,[i|) \in \text{Frac}(R_n)
               $$
          </div>
          <div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 1mm;">
                $\phantom{\circ}\,$ we obtain  <span style="font-size: 16pt">$q_{ij}$</span> from a univariate slice  <span style="font-size: 16pt">$\vec\lambda(t)$</span>, which we can build <br>
                $\phantom{\circ}\,$ in any q-ring with<span style="font-variant: small-caps; font-size: 16pt;"> Syngular:</span> <code style="font-size: 14pt">Ring.univariate_slice</code>.
          </div>
          <div style="font-size: 16pt; float: left; margin-top: 2mm; margin-bottom: 2mm;">
               $\circ\,$ The <span style="font-size: 14pt">$\mathcal{D}_j$</span> are (mostly) related to the letters of the symbol alphabet
          </div>
          <a style="font-size: 13pt; text-align: right; float: right; margin-top: -3mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1812.04586>
          Abreu, Dormans, Febres Cordero, Ita, Page ('18)
          </a>
          <br>
          <div style="text-align: center; float: center; font-size: 14pt; margin-top: 10mm; margin-bottom: 4mm;">
               $
               \displaystyle \mathcal{D}_{Vjj} \subset \kern-3mm \bigcup_{\sigma \; \in \; \text{Aut}(R_6)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1], \langle 1|2+3|4], s_{123}, \\[-2mm] \kern30mm \Delta_{12|34|56}, ⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2] \big\}
               $
          </div>
          <div style="text-align: center; float: center; font-size: 14pt; margin-top: 4mm; margin-bottom: 4mm;">
               $
               \displaystyle \mathcal{D}_{ttH} = \big\{ \langle 12 \rangle, [12], s_{123}, \dots, (s_{123}-m^2), \langle 1|\boldsymbol{3}|1], \dots, \\[2mm] \kern10mm \langle 1|\boldsymbol{3}|\boldsymbol{4}| 2 \rangle, \dots, \langle 1|\boldsymbol{3}|1+2|\boldsymbol{4}| 2], \dots, \Delta_{12|34|5}, \dots \Delta_{12|3|4|5} \big\}
               $
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

<div style="border: 2px solid black; font-size: 16pt; padding: 10px; display: inline-block; margin-top: 0mm;">
    Poles & Zeros $\;\Leftrightarrow\;$ Irreducible Varieties $\;\Leftrightarrow\;$ Prime Ideals <br>
    <i style="font-size: 14pt; border-top: -8mm; border-bottom: -2mm;"> Physics $\kern18mm$ Geometry $\kern18mm$ Algebra </i>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Basis Change from Laurent Coefficients </b>

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
<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\qquad\star\,$ Any pairs of <span style="font-size: 14pt">$s_{ijk}$</span> or <span style="font-size: 14pt">$\Delta_{ij|kl|mn}$</span> or <span style="font-size: 16pt">$\langle i|j|p_V|k|i]-\langle j|l|p_V|k|j]$</span> <br>
     $\qquad\star\,$ Any conjugate pair <span style="font-size: 14pt">$\{\langle i|j+k|l], \langle l|j+k|i]\}$</span> or cyclic <span style="font-size: 14pt">$\{\langle i|j\rangle, [i|j]\}$</span> <br>
     $\qquad\star\,$ Pairs of the form <span style="font-size: 14pt">$\{\Delta_{ij|kl|mn}, \langle c|a+b|d] \text{ or } \langle ab \rangle \text{ or } [ab] \}$</span> unless <span style="font-size: 14pt">$\{ab\}$</span> are <span style="font-size: 14pt">$\{ij\}$</span> or <span style="font-size: 14pt">$\{kl\}$</span> or <span style="font-size: 14pt">$\{mn\}$</span>
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 4mm; margin-bottom: 2mm;">
     $\circ\,$ Other denominator pairs <span style="font-size: 15pt">$\{\mathcal{D}_i, \mathcal{D}_j\}$</span> can be <i>separated to order $\kappa$</i> 
</div>
<div style="font-size:14pt; text-align: center; margin-top: 2mm; margin-bottom: 1mm;">
     $$
     \frac{\mathcal{N}}{\mathcal{D}_i^{q_i}\mathcal{D}_j^{q_j}\mathcal{D}_{\text{rest}}} \rightarrow \sum_{\kappa - q_j\leq m \leq q_i}\frac{\mathcal{N}_i}{\mathcal{D}_i^{m}\mathcal{D}_j^{\kappa - m}\mathcal{D}_{\text{rest}}}
     $$
</div><div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\qquad\star\,$ E.g. <span style="font-size: 14pt">$\Delta_{ij|kl|mn}^4, \langle i|k+l|j]^5$</span> are separable to order 5.
</div>

<div style="text-align: center; font-size: 18pt; margin-top: 3mm; margin-bottom: -2mm;">
     ${\color{greeN} ✓}$ Reconstruction only required 50k <span style="font-size: 16pt">$\mathbb{F}_p$</span> samples $\;{\color{greeN} ✓}$Already simpler than original ones (<span style="font-size: 14pt">$\sim$</span>20MB) <br>
     $\;{\color{red} ✗}$ Results are unstable and sub-optimal, e.g. numbers like this appeared
</div>
<span style="font-size: 14pt">127187555379407704220939486282289348327703498501718808908391691454242601886997968263623652083189652150273</span>

---

<div style="margin-top: 2mm; margin-bottom: -2mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Iterated Pole Subtraction </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (i.e. geometry at codimension greater than one)
     </p>
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -18mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/1904.04067>
   GDL, Maître ('19)
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -13mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2203.04269>
   GDL, Page ('22)
</a>
<a style="font-size: large; text-align: right; float: right; margin-top: -8mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2312.03672>
   Chawdhry ('23)
</a>

<div style="text-align: left; font-size:16pt; margin-top: -2mm; margin-bottom: 0mm;">
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
        <div style="width:100%; font-size: 13pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\langle xy^2 + y^3 - z^2 \rangle$
        </div>
    </div>
    <div style="flex: 1; max-width:3%; margin-top:20mm;">
        $\cap$
    </div>
    <div style="flex: 1;">
        <img src="V2.png" style="max-width:60%; height:auto;">
        <div style="width:100%; font-size: 13pt; margin-top: -3mm; margin-bottom: 1mm;">
          $\langle x^3 + y^3 - z^2 \rangle$
        </div>
    </div>
    <div style="flex: 1; max-width:3%; margin-top:20mm;">
        $=$
    </div>
    <div style="flex: 1;">
        <img src="V3.png" style="max-width:53%; height:auto;">
        <div style="width:120%; font-size: 14pt; margin-left:-10mm; margin-top: -3mm; margin-bottom: 1mm;">
          $\begin{gather}\langle 2y^3-z^2, x-y \rangle \cap \langle y^3-z^2, x \rangle \cap \langle z^2, x+y \rangle\end{gather}$ 
        </div>
    </div>
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 0mm;">
$\circ\,$ Retain control by iteratively fitting residues on varieties (using <span style="text-size: 14pt">$p$</span>-adic numbers $\mathbb{Q}_p$, get $\mathbb{F}_p$ vals for nums)
</div>
<div style="text-align: left; font-size: 13pt; margin-top: 0mm; margin-bottom: 1mm;">
$$ 
\begin{alignedat}{2}
& r^{(139 \text{ of } 139)}_{\bar{u}^+g^+g^-d^-(V\rightarrow \ell^+ \ell^-)} = & \qquad\qquad & {\small \text{Variety (scheme?) to isolate term(s)}} \\[2mm]
& +\frac{7/4{\color{blue}(s_{24}-s_{13})}⟨6|1+4|5]s_{123}{\color{green}(s_{124}-s_{134})}}{⟨1|2+3|4]⟨2|1+4|3]^2 Δ_{14|23|56}} + ... & \qquad\qquad & \Big\langle ⟨2|1+4|3]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
% & -\frac{49/64⟨3|1+4|2]⟨6|1+4|5]s_{123}(s_{123}-s_{234})(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]Δ^2_{14|23|56}} + \dots & \qquad\qquad & \Big\langle Δ_{14|23|56} \Big\rangle
\end{alignedat}
$$
</div>

<div style="text-align: left; font-size: 16pt; margin-top: -2mm; margin-bottom: 0mm;">
$\circ\,$ Partial fraction decomposition and numerator insertions from e.g.:
</div>
<div style="text-align: left; font-size: 12pt; margin-top: 2mm; margin-bottom: 1mm;">
     $$
     \sqrt{\big\langle ⟨2|1+4|3], Δ_{14|23|56} \big\rangle} = \big\langle {\color{green}(s_{124}-s_{134})}, ⟨2|1+4|3] \big\rangle \, , \\[1mm] 
     \big\langle ⟨1|2+3|4], ⟨2|1+4|3] \big\rangle = \big\langle ⟨1|2+3|4], ⟨2|1+4|3], {\color{blue}(s_{13}-s_{24})}\big\rangle \cap \big\langle ⟨12⟩, [34] \big\rangle
     $$
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
     $\quad\rightarrow$ Finite fields $\mathbb{F}_p$ and $p$-adic number types $\mathbb{Q}_p$, including field extensions <br>
     $\quad\rightarrow$ rational number reconstruction (Wang's EEA, LGRR, MQRR) <br>
     $\quad\rightarrow$ univariate and multivariante Newthon & univariate Thiele interpolation algorithms in $\mathbb{F}_p$
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/syngular/" style="font-size: 20pt; font-variant: small-caps;">syngular</a> (in the backhand Singular is used for many operations)<br>
     $\quad\rightarrow$ object-oriented algebraic geometry (Field, Ring, Quotient Ring, Ideal) <br>
     $\quad\rightarrow$ ring-agnostic monomials and polynomials (with support for unicode characters, e.g. spinor brackets)<br>
     $\quad\rightarrow$ multivariate solver (Ideal.point_on_variety), under- and over-constrained systems OK <br>
     $\quad\rightarrow$ a semi-numerical prime and primary ideal test (assumes equi-dimensionality of ideal)
</div>

<div style="text-align: left; font-size:16pt; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/lips/" style="font-size: 20pt; font-variant: small-caps;">lips</a> (Lorentz invariant phase space)<br>
     $\quad\rightarrow$ phase space points over any field ($Q, Qi, R, C, Qp, Fp$), including internal and external masses <br>
     $\quad\rightarrow$ evaluate any Mandelstam or spinor expression (custom ast/regex parser) <br>
     $\quad\rightarrow$ generation of any special kinematic configuration (wrapper around Ideal.point_on_variety)
</div>

</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# Conclusion

---

<b style="font-variant: small-caps; font-size: 36pt; margin-bottom: -6mm;"> Spinor-Helicity Amplitudes Results </b>
<br>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 5mm;">
     $\circ$ The <span style="font-size: 14pt;">$pp\rightarrow Vjj$</span> coefficient functions are now 1.9 MB (from 1.4 GB), fast and stable. <br>
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

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ The complexity split is: quarks NMHV: 100 KB, gluons MHV: 200 KB, gluons NMHV: 1.6 MB.
</div>
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ The largest numbers are: quarks NMHV and gluons MHV: 3-digit, gluons NMHV: 12 digits.
</div>
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ Pheno ready results for the hard functions are available at <a href="https://gitlab.com/five-point-amplitudes/FivePointAmplitudes-cpp">FivePointAmplitudes</a>.
</div>
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ Amplitudes at <a href="https://github.com/GDeLaurentis/antares-results">antares-results</a>, with <a href="https://gdelaurentis.github.io/antares-results/index.html">human readable expr.</a>, and <a href="https://github.com/GDeLaurentis/antares-results/actions/">CI tests</a> for full amplitude in real kinematics
</div>

---

<b style="font-variant: small-caps; font-size: 34pt; margin-bottom: -6mm;"> A Numerical CAS for Computations in Q-Rings </b>
<br>
<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ Most operations do not require defining the variables, only being able to evaluate them.
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ Only need to define the quotient ring to build the Ansatz (and even then not having anlytic identities for the redundancies is not a big problem)
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 2mm; margin-top: 2mm;">
     $\circ$ <a href="https://github.com/GDeLaurentis/antares/" style="font-size: 20pt; font-variant: small-caps;">antares</a> (automated numerical to analytical reconstruction software), <a href="https://github.com/GDeLaurentis/antares-results/" style="font-size: 20pt; font-variant: small-caps;">antares-results</a>, <a href="https://gdelaurentis.github.io/antares-results/">documentation</a>
</div>
<div style="display: flex; justify-content: center; align-items: flex-start; margin-top: 2mm;">
    <div style="padding: 0 10px;">
        <img src="antares-results-transparent.png" style="width: 100%; max-width: 250px; border: none; margin-top: 2mm; margin-bottom: 0mm;">
    </div>
</div>

</section>

---

<section>

{{< slide background-image="edmonton.jpg" >}}

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
