---
tile: "Amplitude Reconstruction: Tools and Methods"
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
	   Analytic Structure and Reconstruction in QCD: Two-Loop $\boldsymbol{pp \to Vjj}$ and One-Loop $\boldsymbol{q\bar{q}\rightarrow t\bar{t}H}$
	</b>
</h3>

<div style="font-size: x-large; margin-top:8mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
Vjj: <a href="https://link.springer.com/article/10.1007/JHEP06(2025)093">JHEP 06 (2025) 093</a> <div style="font-size: large; margin-bottom:5mm;"> (GDL, H. Ita, B. Page, V. Sotnikov) </div>
ttH: <a href="https://arxiv.org/abs/2504.19909">arXiv:2504.19909</a> <div style="font-size: large;"> (J. Campbell, GDL, K. Ellis) </div>


Caravel Meeting 2025
<div style="font-size: large; margin-top:-5mm; margin-bottom:5mm"> UZH </div>
<p style="line-height: 0.05;"> <img src="UniEdinburghLogo-transparent.png"; style="max-width:120px;float:center;border:none;margin-bottom:5mm;"> 
<br><br><br>
<span style="font-size: 11pt; margin-top: 10mm;">Find these slides at  <a href="/slides/caravelmeeting2025/#/">gdelaurentis.github.io/slides/caravelmeeting2025</a> </span>
</div>

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

<div style="font-size: 17pt; text-align:left; margin-bottom: 0mm; margin-top: 0mm;">
$\circ$ Original computation  <a href="https://arxiv.org/abs/hep-ph/9708239" style="font-size: 18pt">[1]</a> was performed with <span style="font-variant: small-caps;font-size: 17pt">Caravel</span>
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 15pt; width:75%; text-align: left; display: inline-block; margin-top: 1mm;">
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
		<div style="margin-top:-4mm; font-size: 11pt;"> Abreu, Dormans, </div>
		<div style="margin-top:0mm; font-size: 11pt;"> Febres Cordero, Ita  </div>
		<div style="margin-top:0mm; font-size: 11pt;"> Kraus, Page, Pascual, </div>
		<div style="margin-top:0mm; font-size: 11pt;"> Ruf, Sotnikov ('20) </div>
	     </a>
	</div>
     <div style="font-size: 16pt; width:75%; text-align: left; display: inline-block; margin-top: 2mm; margin-bottom: -4mm;">
	     $\rightarrow$ Numerical Berends-Giele recursion for LHS, solve for coeffs. in RHS.<br>
	     $\rightarrow$ IBP reduction = decomposition on RHS, <span style="font-size: 16t">$\; m_{\Gamma,i} \in M_\Gamma \cup S_\Gamma$</span>
	</div>
</div>

<div style="font-size: 17pt; text-align: left; margin-bottom: 0mm; margin-top: 6mm;">
     $\circ$ This computation started from the ancillaries files of <a href="https://arxiv.org/abs/hep-ph/9708239" style="font-size: 14pt">[1] Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov</a>
     <div style="font-size: 16pt; width:99%; text-align: left; display: inline-block; margin-top: 2mm; margin-left:10mm;">
	     1. Wrote a Python script to split the 1.4 GB ancillaries into >10k files <br>
	     2. Compile into 18.2 GB of C++ binaries (for reference <span style="font-variant: small-caps;font-size: 17pt">Caravel</span> compiles into approx. 5 GB) <br>
          3. Obtain <span style="font-size: 16t">$\mathbb{F}_p$</span> evaluations of the form factors (each takes approx. 1 sec per point)<br>
          4. Recombine triplets of form factors into six-point helicity amplitudes (incl. decays)
	</div>
</div>

<div style="font-size: 17pt; text-align:left; margin-bottom: 0mm; margin-top: 2mm;">
$\rightarrow$ Assemble 5 helicity amplitudes into 3 categories: <span style="font-size: 14pt;">$\mathcal{R}_{\bar qQ\bar QqV}^{\text{NMHV}} ,\, \mathcal{R}_{\bar qggqV}^{\text{MHV}} ,\, \mathcal{R}_{\bar qggqV}^{\text{NMHV}}$</span>
</div>

<div style="font-size: 17pt; text-align: left; margin-bottom: 0mm; margin-top: 3mm;">
     $\circ$ <span style="font-size: 15pt;">$t\bar{t}H$</span> computed analytically (<span style="font-variant: small-caps;">Form</span> optimized) with unitarity, standard Feynman diagrams techniques, <br> $\phantom{\circ}$ and cross checked with <span style="font-variant: small-caps;">Open-Loops</span>
</div>
<a href="https://arxiv.org/abs/1907.13071" style="font-size: 14pt; margin-top: -5mm; float: right; font-align: right;"> Buccioni, Lang, Lindert, Maierhöfer, Pozzorini, Zhang, Zoller</a>

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

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Interesting mathematical observations and open questions: <br>
     $\quad\star$ <span style="font-size: 16pt">$R_3$</span> is not an Integral Domain, i.e. it breaks <span style="font-size: 16pt">$ab=0 \Rightarrow a = 0 \text{ or } b = 0$</span> <br>
     $\quad\star$ <span style="font-size: 16pt">$R_4$</span> is not an Unique Factorization Domain (which is why MHV = anti-MHV) <br>
     $\quad\star$ Conjecture: <span style="font-size: 16pt">$R_{n\geq 5}$</span> is UFD. For instance, this would imply the  denominators $\mathcal{D}$ are unique <br>
     $\phantom{\circ}$ <u>Note</u>: all polynomial rings are UFD, so clearly <span style="font-size: 16pt">$R_4$</span> is not equivalent to one, e.g. <span style="font-size: 16pt">$\mathbb{F}[s,t]$</span>
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Choosing the Appropriate Covariant Q-Ring </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 15pt;">$pp \rightarrow V(\rightarrow \bar\ell\ell)jj$</span> the space is simpler than that of say <span style="font-size: 15pt;">$pp \rightarrow jjjj$</span>, we don't want to use <span style="font-size: 15pt;">$R_6$</span>. <br>
     $\phantom{\circ}$ Take the decay current to be <span style="font-size: 15pt;">$[5|\gamma^\mu|6\rangle$</span>, and remove <span style="font-size: 15pt;">$p_{V\alpha\dot\alpha}=(5+6)_{\alpha\dot\alpha}$</span> by mom. cons.
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle \kern10mm R_{Vjj} = \mathbb{F}\big[|1⟩_{\alpha}, [1|_{\dot\alpha}, |2⟩_{\alpha}, [2|_{\dot\alpha}, |3⟩_{\alpha}, [3|_{\dot\alpha},  |4⟩_{\alpha}, [4|_{\dot\alpha}, [5|_{\dot\alpha}, |6⟩_{\alpha} \big] \Big/ \big\langle {\textstyle \sum_{i=1}^4} [5|i]\langle i |6\rangle \big\rangle
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ This always holds for the numerator polynomials (and almost the denomiantors).
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 15pt;">$pp \rightarrow ttH$</span> we use the massive spinor-helicity (or spin-spinor) formalism
</div>
<a href="https://arxiv.org/abs/1809.09644" style="font-size: 14pt; margin-top: -3mm; float: right; font-align: right;"> Shadmi, Weiss </a>
<a href="https://arxiv.org/abs/1802.06730" style="font-size: 14pt; margin-top: -3mm;  margin-right: 2mm; float: right; font-align: right;"> Ochirov; </a>
<a href="https://arxiv.org/abs/1709.04891" style="font-size: 14pt; margin-top: -3mm; margin-right: 2mm; float: right; font-align: right;"> Arkani-Hamed, Huang, Huang;</a>

<div style="font-size: 15pt; margin-top: 8mm; margin-bottom: 5mm">
$$ 
\displaystyle \kern10mm R_{ttH} = \frac{\mathbb{F}\big[|1⟩_{\alpha}, [1|_{\dot\alpha}, |2⟩_{\alpha}, [2|_{\dot\alpha}, |\boldsymbol{3}^I⟩_{\alpha}, [\boldsymbol{3}^I|_{\dot\alpha}, |\boldsymbol{4}_J⟩_{\alpha}, [\boldsymbol{4}_J|_{\dot\alpha}, \boldsymbol{5}_{\alpha\dot\alpha} \big]}{\big\langle \sum_{i,I,J} |i\rangle[i|, \langle \boldsymbol{3}|\boldsymbol{3}⟩ +[\boldsymbol{3}|\boldsymbol{3}], \langle \boldsymbol{3}|\boldsymbol{3}⟩-\langle \boldsymbol{4}|\boldsymbol{4}⟩, \langle \boldsymbol{4}|\boldsymbol{4}⟩ +[\boldsymbol{4}|\boldsymbol{4}]\big\rangle}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where <span style="font-size: 15pt;">$\langle \boldsymbol{3}^I|\boldsymbol{3}^J⟩=m\epsilon^{JI} \text{ and } [\boldsymbol{3}^I|\boldsymbol{3}^J]=\bar{m}\epsilon^{IJ}$</span>; we are setting <span style="font-size: 15pt;">$m=\bar{m}$</span> and the tops on-shell.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ <span style="font-size: 15pt;">$|\boldsymbol{3}^I⟩_{\alpha}$</span> is basically two copies of a massless spinor, we can think of this through the map
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

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Examples of Trees </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: -2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ To not make this too abstract, we are after expressions like these, but for the MI coefficients.
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 15pt;">$Vjj$</span> there are 5 amplitudes (showing 3)
</div>
<div style="font-size: 15pt; margin-top: 0mm; margin-bottom: 3mm">
$$ 
{A}_g^{(0)}(1^{+}_\bar{q}, 2^{+}_g, 3^{+}_g, 4^{-}_q, 5^{+}_\bar{\ell}, 6^{-}_\ell) = \frac{⟨46⟩^2}{⟨12⟩⟨23⟩⟨34⟩⟨65⟩} \, , \\[6mm]
{A}_g^{(0)}(1^{+}_\bar{q}, 2^{+}_g, 3^{-}_g, 4^{-}_q, 5^{+}_\bar{\ell}, 6^{-}_\ell) = \frac{⟨13⟩⟨3|1+2|5]^2}{⟨12⟩⟨23⟩[65]⟨1|2+3|4]s_{123}} \; + \; (123456\rightarrow \overline{432165}) \, , \\[6mm]
{A}_q^{(0)}(1^{+}_\bar{q}, 2^{+}_{q'}, 3^{+}_{\bar{q}'}, 4^{-}_q, 5^{+}_\bar{\ell}, 6^{-}_\ell) = -\frac{[12]⟨46⟩⟨3|1+2|5]}{⟨23⟩[23]⟨56⟩[56]s_{123}}+(123456\rightarrow 156423)\phantom{+}
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ For <span style="font-size: 15pt;">$q\bar{q}\rightarrow t\bar{t}H$</span> there is only a single amplitude
</div>
<div style="font-size: 15pt; margin-top: 8mm; margin-bottom: 5mm">
$$ 
{A}_{ttH}^{(0)}(1^{+}_q, 2^{-}_\bar{q}, 3_t, 4_\bar{t}, 5_H)^I_J = \frac{⟨2|𝟑|1]⟨𝟑^I𝟒_J⟩-[𝟑^I1][1𝟒_J]⟨12⟩}{s_{12}(s_{12𝟑}-m_t²)} + 
(12345\rightarrow\overline{21345},12435,\overline{21435})
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ where for clarity I have not suppressed the spin indices. Symmetries are made manifest.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ <u>Note</u>: The amplitude is <b>spin covariant</b>, just like it is little group covariant! <br>
     $\phantom{\circ} \kern7.2mm$ We need only obtain a single choice, say <span style="font-size: 15pt;">$I=J=1$</span>, the other follows. 
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Spinor Alphabets </b>

<div style="font-size: 17pt; text-align: left; margin-top: 2mm; margin-bottom: 2          mm;">
     $\circ$ We can always factorize a polynomial into products of irreducible factors, to some powers
</div>
<div style="font-size:15pt; text-align: center; margin-top: 2mm; margin-bottom: 2mm">
     $$
     \displaystyle r_i(|i\rangle,[i|) = \frac{\mathcal{N}(|i\rangle,[i|)}{\prod_j \mathcal{D}_j^{q_{ij}}(|i\rangle,[i|)} % \, , \quad r_i(|i\rangle,[i|) \in \text{Frac}(R_n)
     $$
</div>
<div style="font-size: 16pt; text-align: left; margin-top: 0mm; margin-bottom: 2mm;">
     $\phantom{\circ}$ For the numerators this is generally not particularly useful (when in least common denominator form) <br>
     $\phantom{\circ}$ The denominator factors <span style="font-size: 14pt">$\mathcal{D}_j$</span> are conjectured to be (mostly) related to the letters of the symbol alphabet
</div>
<a style="font-size: 13pt; text-align: right; float: right; margin-top: -3mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1812.04586>
Abreu, Dormans, Febres Cordero, Ita, Page ('18)
</a>

<br>

<div style="font-size: 17pt; text-align: left; margin-top: -10mm; margin-bottom: 2mm;">
     $\circ$ Convert your alphabet from independent Mandelstam invariants to redudant spinors brackets
</div>
<a style="font-size: 13pt; text-align: right; float: right; margin-top: -3mm; margin-bottom: 2mm;" href="">
From work in progress with S. Abreu, X. Liu, P.F. Monni
</a>
<br>
<div style="display: flex; align-items: center; justify-content: space-between; font-size: 16pt; margin-top: -8mm;">
  <div style="width: 48%; text-align: center;">
    <b style="font-variant: small-caps;">Mandelstam letters</b><br>
    <span style="font-size: 14pt;">$s_{12}$</span><br>
    <span style="font-size: 14pt;">$s_{123}$</span><br>
    <span style="font-size: 14pt;">$s_{12} - s_{123} - s_{345} + s_{45}$</span><br>
    <span style="font-size: 14pt;">$-s_{12} + s_{123}$</span><br>
    <span style="font-size: 14pt;">$s_{12}(s_{123} - s_{56}) - s_{123}(s_{123} + s_{34} - s_{56})$</span><br>
    <span style="font-size: 14pt;">
      $\displaystyle\frac{
        s_{12}\left(s_{16}(s_{23} - s_{234})s_{34} + s_{23}^{2}(\cdots) + \cdots\right) + s_{123}(\cdots) + s_{23}(\cdots)
      }{
        \sqrt{(-s_{12} + s_{123} - s_{23})^2\cdots}
      }$
    </span><br>
  </div>
  <div style="width: 4%; text-align: center;">
    <b style="font-size: 20pt;">$\Rightarrow$</b>
  </div>
  <div style="width: 48%; text-align: center;">
    <b style="font-variant: small-caps;">Spinor letters</b><br>
    <span style="font-size: 14pt;">$\langle 1\,2\rangle[1\,2]$</span><br>
    <span style="font-size: 14pt;">$s_{123}$</span><br>
    <span style="font-size: 14pt;">$\langle 3\,|\,6\rangle[3\,|\,6]$</span><br>
    <span style="font-size: 14pt;">$\langle 3\,|\,1{+}2\,|\,3]$</span><br>
    <span style="font-size: 14pt;">$\langle 3\,|\,1{+}2\,|\,4]\langle 4\,|\,1{+}2\,|\,3]$</span><br>
    <div style="display: flex; align-items: center; justify-content: center; height: 2.8em;">
      <span style="font-size: 14pt;">$\operatorname{tr}_5(2,3,4,5)$</span>
    </div>
  </div>
</div>

<div style="font-size: 17pt; text-align: left; margin-top: 4mm; margin-bottom: 2mm;">
     $\circ$ Factorization and extra chiral cancellations are key for simplification in gauge amplitudes 
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
     $\circ\,$ By Gaussian elimination, partition the space (abusing notation for <i>residue</i>):
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

<b style="font-variant: small-caps; font-size: xxx-large"> Laurent Series or p(z)-adic expansion </b>

<div style="text-align: left; font-size: 16pt; margin-top: 3mm; margin-bottom: -2mm;">
     $\circ\,$ With <span style="font-size: 14pt">$p$</span>-adic numbers this would be straight forward, set <span style="font-size: 14pt">$\mathcal{D}_j\propto p$</span> and evaluate the function
</div>
<div style="text-align: center; font-size: 15pt; margin-top: -2mm; margin-bottom: 2mm;">
     $$
     r_{i\in \mathcal{B}} = \sum_{m = 1}^{\text{max}_i(q_{ik})} \frac{e^k_{im}}{p^m} + \mathcal{O}(p^0) \text{ is a number in } \mathbb{Q}_p
     $$
</div>
<div style="text-align: center; font-size: 16pt; margin-top: 3mm; margin-bottom: -2mm;">
     See <code style="font-size: 14pt;">Particles._singular_variety</code> or <code style="font-size: 14pt;">Ideal.point_on_variety</code> to generate the configuration
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: -2mm;">
     $\circ\,$ We can't do this with only finite fields. Instead, build Laurent expansions around $t_{\mathcal{D}_k}$ <span style="font-size: 12pt"> (use more slices) </span>
</div>
<div style="text-align: center; font-size: 15pt; margin-top: -2mm; margin-bottom: 2mm;">
     $$
     r_{i \in \mathcal{B}} = \sum_{m = 1}^{\text{max}_i(q_{ik})} \frac{e^k_{im}}{(t-t_{\mathcal{D}_k})^m} + \mathcal{O}((t-t_{\mathcal{D}_k})^0)
     $$
</div>
<div style="text-align: left; font-size: 16pt; margin-top: 3mm; margin-bottom: -2mm;">
     $\phantom{\circ}\,$ strictly formal over $\mathbb{F}_p$, but convergent over $\mathbb{Q}_p$ for $(t-t_{\mathcal{D}_k}) \propto p$
</div>

<div style="text-align: left; font-size: 16pt; margin-top: 4mm; margin-bottom: -2mm;">
     $\circ\,$ Issue what if the letter does not have a factor linear in <span style="font-size: 15pt">$t$</span>?
</div>
<div style="text-align: center; font-size: 15pt; margin-top: -2mm; margin-bottom: 2mm;">
     $$
     r_{i \in \mathcal{B}} = \sum_{m = 1}^{\text{max}_i(q_{ik})} \frac{c^k_{im} t + d^k_{im}}{(t^2+a_kt+b_k)^m} + \mathcal{O}((t^2+a_kt+b_k)^0)
     $$
</div>
<a style="font-size: 13pt; text-align: right; float: right; margin-top: -10mm; margin-bottom: 2mm;" href=https://arxiv.org/abs/2304.14336 >
see also Fontana, Peraro ('23)
</a>

<div style="text-align: left; font-size: 16pt; margin-top: 3mm; margin-bottom: -2mm;">
     $\circ\,$ From these coefficients, build null spaces used in the search for simple functions
</div>
<div style="text-align: center; font-size: 15pt; float: center; margin-top: -2mm; margin-bottom: 2mm;">
     $$
     \text{null}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))_{ij} \text{ from } \text{ rref }  (d^k_{m})_{i,\text{slice}_j}
     $$
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

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: 32pt"> Example </b>
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\circ\,$ Start from the function
</div>
<div style="font-size: 13pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle f^{\text{ex}} = \frac{\mathcal{N}^{\text{ex}}}{⟨14⟩^2[14]^2 s_{56} ⟨1|2+4|3]^2⟨2|1+4|3]^4⟨2|1+3|4]^2Δ_{14|23|56}^4}
$$
</div>
<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\phantom{\circ}\,$  The numerator Ansatz has size 104$\,$128
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\circ\,$ Clean up the <span style="font-size: 14pt">$Δ_{14|23|56}$</span> Gram residue
</div>
<div style="font-size: 13pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle f^{\text{ex}} = \frac{\mathcal{N}^{\text{ex}}_1}{⟨14⟩^2[14]^2s_{56}⟨2|1\!+\!4|3]^4Δ_{14|23|56}^4 \,} + \frac{\mathcal{N}^{\text{ex}}_2}{⟨14⟩^2[14]^2s_{56}⟨2|1+4|3]^4⟨1|2\!+\!4|3]^2⟨2|1\!+\!3|4]^2}
$$
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\circ\,$ Split <span style="font-size: 14pt">$s_{14}$</span> and impose symmetry
</div>
<div style="font-size: 13pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle f^{\text{ex}} =
  \frac{\mathcal{N}^{\text{ex}}_{3}}{⟨14⟩^2 s_{56} ⟨2|1+4|3]^4Δ_{14|23|56}^4}
  + \frac{\mathcal{N}^{\text{ex}}_{4}}{⟨14⟩^2 s_{56} ⟨1|2+4|3]^2⟨2|1+4|3]^4⟨2|1+3|4]^2} + (123456\rightarrow \overline{432165})
$$
</div>

<div style="text-align: left; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     $\circ\,$ Impose degree bound on poles at codimension two
</div>
<div style="font-size: 13pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\displaystyle f^{\text{ex}} = 
  \sum_{k=0}^3 \frac{\mathcal{N}^{\text{ex}}_{5,k}}{⟨14⟩^2 s_{56} ⟨2|1+4|3]^{1+k} Δ_{14|23|56}^{4-k}}
    + \frac{\mathcal{N}^{\text{ex}}_6}{⟨14⟩^2 s_{56}⟨1|2+4|3]^2⟨2|1+4|3]^4⟨2|1+3|4]^2} + (123456\rightarrow \overline{432165})
$$
</div>

<div style="text-align: center; font-size: 18pt; margin-top: 2mm; margin-bottom: 2mm;">
     The Ansatz now has size 13$\,$532, almost a factor of 10 simpler.
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
