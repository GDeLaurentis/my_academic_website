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
<div style="font-size: 15pt; margin-bottom:0mm;"> One Central Emission at Two Loops </div>
<div style="font-size: 15pt; margin-bottom:0mm;"><a href="https://arxiv.org/pdf/2412.20578">arXiv:2412.20578</a> <a href="https://link.springer.com/article/10.1007/JHEP04(2025)161">(10.1007/JHEP04(2025)161)</a></div>
<div style="font-size: 15pt; margin-bottom:0mm;"> with S. Abreu, G. Falcioni, E. Gardi, C. Milloy, L. Vernazza </div>
<br>
<div style="font-size: 15pt; margin-bottom:0mm;"> Two Central Emissions at One Loop </div>
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

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 0mm; margin-left: -5mm;">
     $\circ\,$ In the <b>forward limit</b> <span style="font-size: 15pt">$s \gg t$</span> (large CoM energy vs. momentum transfer), e.g. <span style="font-size: 15pt">$2\to 2$</span> scattering,
</div>
<img src="forward_diagram.png" style="max-width:100mm; margin-top:-4mm; margin-bottom:-7mm;">
<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 0mm; margin-left: -5mm;">
     $\phantom{\circ}\,$ final state emissions develop <b> large rapidity gaps</b>. The cross section grows as
</div>
<div style="font-size: 16pt; margin-top: 0mm; margin-bottom: -3mm">
$$
\sigma \approx \mathcal{O}\big(\alpha_s^n \log^n(s/|t|)\big )
$$
</div>
<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 0mm; margin-left: -5mm;">
     $\phantom{\circ}\,$ which is unphysically large (e.g. it violates the Froissart bound).
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 8mm; margin-left: -5mm;">
     $\circ\,$ The BFKL kernel captures the <b>exponentiation</b> of these <b>large logarithms</b>,<br>
     $\phantom{\circ}\,$ allowing us to <b>resum</b> their contribution to the cross section.
</div>
<span style="font-size: 14pt; margin-top: -8mm; margin-bottom: -8mm; margin-right:-5mm; float: right; font-align: right;"><a href="https://www.sciencedirect.com/science/article/abs/pii/0370269375905249"> Fadin, Kuraev, Lipatov `75</a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 0mm; margin-top: 8mm; margin-left: -5mm;">
     $\circ\,$ In this kinematic limit, known as <b>Multi-Regge Kinematics</b> (MRK), an effective particle is <br>
     $\phantom{\circ}\,$ exchanged in the t-channel, a Reggeon, from which more rapidity-gapped radiation can be emitted.
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> Expanding Amplitudes in MRK and NMRK </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 1mm; margin-top: 2mm; margin-left: -2mm;">
     $\circ\;$ In the (N)MRK we can picture the amplitude as follows
</div>
<img src="Emissions-transparent.png" style="max-width:225mm; margin-top: 2mm; margin-bottom: 0mm;">
<br>
<span style="font-size: 14pt; margin-top: -8mm; margin-bottom: -8mm; margin-right:-5mm; float: right; font-align: right;"> Images adapted from <a href="https://arxiv.org/abs/2312.15051"> Byrne `23</a></span>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: -2mm;">
     $\phantom{\circ}\;$ where: the ziggly line is a Reggeon <span style="font-size: 15pt">$\mathcal{R}$</span>, the green blobs are impact factors <span style="font-size: 15pt">$\mathcal{C}$</span>, the blue blob is <br>
     $\phantom{\circ}\;$ a one-emission central vertex <span style="font-size: 15pt">$\mathcal{V}_g$</span>, and the gray blob is a two-emission central vertex <span style="font-size: 15pt">$\mathcal{V}_{gg}$</span>.
</div>


<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: -2mm;">
     $\circ\;$ The amplitude factorise as follows (very schematically)
</div>
<div style="font-size: 16pt; margin-top: 0mm; margin-bottom: -3mm">
$$
\mathcal{A}_4 \approx \mathcal{C}  \, \mathcal{R} \, \mathcal{C} \, , \qquad
\mathcal{A}_5 \approx \mathcal{C}  \, \mathcal{R} \, \mathcal{V}_g \, \mathcal{R} \, \mathcal{C} \, , \qquad
\mathcal{A}_6 \approx \mathcal{C}  \, \mathcal{R} \, \mathcal{V}_{gg} \, \mathcal{R} \, \mathcal{C}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: -2mm;">
     $\phantom{\circ}\;$ where each component admits an expansion in powers of <span style="font-size: 15pt">$\alpha_s$</span>, thus e.g. <span style="font-size: 15pt">$\mathcal{A}_4^{(1)}$</span> gives us <span style="font-size: 15pt">$\mathcal{C}^{(1)}$</span> and <span style="font-size: 15pt">$\mathcal{R}^{(1)}$</span>
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

<span style="font-size: 14pt; margin-top: -5mm; margin-bottom: 5mm; float: right; font-align: right;">Images from<a href="https://arxiv.org/abs/2204.12459"> Byrne, Del Duca, Dixon, Gardi, Smillie </a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 5mm; margin-top: 10mm;">
     $\phantom{\circ}\,$ (a) is a correction to the Regge trajectory <span style="font-size: 15pt">$\mathcal{R}^{(1)}$</span><br>
     $\phantom{\circ}\,$ (b) is the leading order central emission vertex (CEV) <span style="font-size: 15pt">$\mathcal{V}_g^{(0)}$</span> in MRK
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> NLO Kernel </b>
<div  style="text-align: left; font-size: 16pt; margin-bottom: 5mm; margin-top: -6mm; text-align: center;">
Next-To-Leading-Log (NLL) Resummation: <span style="font-size: 14pt;">$\mathcal{O}\big(\alpha_s^n \log^{n-1}(s/|t|)\big )$</span>
</div>

<img src="NLOKernel.png" style="max-width: 180mm; margin-top: 0mm; margin-bottom:0 mm;">

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (a) two-loop correction to the Regge trajectory, <span style="font-size: 15pt">$\mathcal{R}^{(2)}$</span>
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (b) one-loop correction to the one-emission CEV <span style="font-size: 15pt">$\mathcal{V}_g^{(1)}$</span> in MRK
</div>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 2mm; margin-left: 0mm;">
     $\phantom{\circ}\,$ (c) leading two-emission CEV <span style="font-size: 15pt">$\mathcal{V}_{gg}^{(0)}$</span>, this requires an next-to-MRK (NMRK) tree computation: <br>
     $\phantom{\circ}\,\kern4mm$ the two central gluons are <u>not</u> rapidity gapped
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> NNLO Kernel </b>
<div  style="text-align: left; font-size: 16pt; margin-bottom: 5mm; margin-top: -6mm; text-align: center;">
NNLL Resummation: <span style="font-size: 14pt;">$\mathcal{O}\big(\alpha_s^n \log^{n-2}(s/|t|)\big )$</span>
</div>

<img src="NNLOKernel.png" style="max-width: 280mm; margin-top: -5mm; margin-bottom: 2mm; margin-left: -16mm">

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: -3mm; margin-left: -7mm;">
     $\phantom{\circ}\,$ (a) Three loop <span style="font-size: 15pt">$2\to 2$</span> MRK, from three Reggeons to three-loop correction to the trajectory, <span style="font-size: 15pt">$\mathcal{R}^{(3)}$</span>
</div>
<span style="font-size: 14pt; margin-top: -3mm; margin-bottom: -5mm; float: right; font-align: right;"> <a href="https://arxiv.org/abs/2112.11098" > Falcioni, Gardi, Maher, Milloy, Vernazza `21</a>;$\;$<a href="https://arxiv.org/abs/2112.11097" > Caola, Chakraborty, Gambuti, von Manteuffel, Tancredi `21</a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 6mm; margin-left: -7mm;">
     $\phantom{\circ}\,$ (b) Two-loop correction to the central emission vertex <span style="font-size: 15pt">$\mathcal{V}_g^{(2)}$</span> for one gluon
</div>
<span style="font-size: 14pt; margin-top: -3mm; margin-bottom: -5mm; float: right; font-align: right;"> <a href="https://arxiv.org/abs/2412.20578"> Abreu, GDL, Falcioni, Gardi, Milloy, Vernazza `24</a>;$\;$<a href="https://arxiv.org/abs/2411.14050"> Buccioni, Caola, Devoto, Gambuti `24</a></span>
<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 5mm; margin-left: -7mm;">
     $\phantom{\circ}\,\kern9mm$ by expanding in the MRK limit the recently available two-loop five-parton amplitudes
</div>
<span style="font-size: 14pt; margin-top: -3mm; margin-bottom: -5mm; float: right; font-align: right;"> <a href="https://arxiv.org/abs/2311.10086"> GDL, Ita, Klinkert, Sotnikov `23</a>;$\;$<a href="https://arxiv.org/abs/2311.18752"> GDL, Ita, Sotnikov `23</a>;$\;$<a href="https://arxiv.org/abs/2311.09870"> Agarwal, Buccioni, Devoto, Gambuti, von Manteuffel, Tancredi `23</a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 8mm; margin-left: -7mm;">
     $\phantom{\circ}\,$ (d) The last missing component is the next-to-maximally-helicity-violiating (NMHV) one-loop <br>
     $\phantom{\circ}\,\kern9mm$ two-gluon CEV <span style="font-size: 15pt">$\mathcal{V}_{g^{+}g^{-}}^{(0)}$</span>,
     this requires expanding in NMRK the one-loop six-gluon amplitude
</div>
<span style="font-size: 14pt; margin-top: -3mm; margin-bottom: -5mm; float: right; font-align: right;"> Byrne, GDL, Del Duca, Gardi, Smillie - in progress; <a href="https://arxiv.org/abs/1904.04067" >GDL, Maitre `19</a></span>

<div style="text-align: left; font-size: 18pt; margin-bottom: 2mm; margin-top: 8mm; margin-left: -7mm;">
     $\phantom{\circ}\,$ (e) The leading CEV for three emissions <span style="font-size: 15pt">$\mathcal{V}_{ggg}^{(0)}$</span> from an NNMRK limit at tree level
</div>
<span style="font-size: 14pt; margin-top: -3mm; margin-bottom: -5mm; float: right; font-align: right;"> <a href="https://arxiv.org/abs/2506.10644"> Byrne, Del Duca, Gardi, Mo, Smillie `25</a></span>

</section>

---

<section>

{{< slide background-image="varieties-no-background.png" >}}

# NMRK Numerical Expansion

---

<b style="font-variant: small-caps; font-size: 34pt; magin-bottom: -10mm;"> Minimal Variables for (N)MRK </b> <br>

<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: -4mm;">
$\circ$ The problem is most easily formulated in terms of lightcone momenta
</div>
<div style="font-size: 16pt; margin-top: 0mm; margin-bottom: 0mm">
$$
\begin{array}{rllll}
p \; = & (p^+, & p^-, & p_\perp , & \bar p_\perp ) \\
  = & (E + p_z, & E - p_z, & p_x + i p_y, & p_x - i p_y)
\end{array}
$$
</div>

<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: 2mm;">
$\circ$ We can picture the MRK limit as follows
</div>
<div style="display: flex; justify-content: space-between; align-items: flex-start; margin-top: 2mm; margin-bottom: 0mm;">
     <!-- Left column: image -->
     <div style="flex: 1; margin-right: 10mm;">
     <img src="mrk-variables.png" style="max-width:100mm; margin-top: 2mm; margin-bottom: 0mm;">
     </div>
     <!-- Right column: table -->
     <div style="font-size: 16pt; margin-top: 10mm; margin-bottom: 0mm; margin-right: 20mm;">
     $$
     p_{i}^{\;j} = \left(
     \begin{array}{cccc}
     0 & \text{mc} & 0 & 0 \\
     \text{mc} & 0 & 0 & 0 \\
     p_4^{+} X_{34} & \text{mc} & \text{mc} & \text{mc} \\
     p_4^{+}  & \text{mc} & \frac{-q_1}{z − 1} & \frac{-\bar q_1}{\bar z − 1} \\
     p_4^{+} / X_{45} & \text{mc} & \frac{q_1 z}{z − 1} & \frac{\bar q_1\bar z }{\bar z − 1} 
     \end{array}\right)
     $$
     </div>
</div>
<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: 2mm;">
$\circ\,$ The MRK limit is a two-variable problem <span style="font-size: 16pt;">$z, \bar z$</span>; <br>
$\phantom{\circ}\,$ <span style="font-size: 16pt;">$q_1, \bar q_1, p_4^+$</span> drop out by normalizing by the tree and <span style="font-size: 16pt;">$X_{34} \sim X_{45} \sim 1/x \gg 1$</span>
</div>

<div style="font-size: 17pt; text-align:left; margin-bottom: 2mm; margin-top: 2mm;">
$\circ$ The NMRK limit is a five-variable problem <span style="font-size: 15pt;">$z, \bar z, w, \bar w, X=X_{(45)}$</span>
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Challenge from Spurious Cancellations </b>

<div style="font-size: 16pt; margin-top: 10mm; margin-bottom: 0mm; margin-right: 20mm;">
$$
\mathcal{A}^{(\ell)} = \sum_i c_i \, I_i
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ\,$ For the MRK limit of the two-loop five-point amplitude we had to expand to second order in <span style="font-size: 16pt;">$x$</span>, because of one order of spurious singularity between the <span style="font-size: 16pt;">$c_i$</span> and <span style="font-size: 16pt;">$I_i$</span>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ\,$ NMRK six point
</div>
<pre><code class="language-python" style="font-size: 11pt">> from antares_results.jjjj.gggggg.pmpmpm import coeffs  # import integral coefficients
> coeffs['box(1)']
</code></pre>
<pre><code class="language-python" style="margin-top:-5mm; font-size: 10pt">< Terms("""+(-1/2j⟨1|2⟩⁴[1|2][2|3]⟨3|1+2|5]⁴)/(⟨1|3⟩⁴[4|5][5|6]⟨1|2+3|4]⟨3|1+2|6]s_123)""")
</code></pre>
<pre><code class="language-python" style="font-size: 11pt">> len(str(coeffs['box(1)'])), len(str(coeffs['triangle(19)']))
</code></pre>
<pre><code class="language-python" style="margin-top:-5mm; font-size: 10pt">< 76, 168150
</code></pre>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}\,$ Some coefficients (three mass triangles and bubbles) are very complicated!
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ\,$ Problem: we observe up to 8 orders of spurious cancellations in the MRK parameter $x\rightarrow 0$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     ${\color{red} ✗}$ Analytic expansion is a no go. Run out of memory and time after 3 or 4 orders! <br>
     ${\color{red} ✗}$ Numerical expansion with floating-point numbers is also too complicated. <br>
     $\phantom{{\color{red} ✗}}$ Say we input $x\approx 10^{-10}$ to have 10 good digits to work with, we would lose 80 digits!
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 0mm;"> <span style="font-size: 27pt;">$p\kern2mm$</span>-adic numbers </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ You may be familiar with finite field (integers modulo a prime)
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/FIXME>
   Heller, von Manteuffel; Peraro
</a>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle a \in \mathbb{F}_p : a \in \{0, \dots, p -1\} \; \text{ with } \; \{+, -, \times, \div\}
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Limits (and calculus) are not well defined in $\mathbb{F}_p$. We can make things zero, but not small:
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle |a|_0 = 0 \; \text{if} \; a = 0 \; \text{else} \; 1 \quad \text{a.k.a. the trivial absolute value.}
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ There exists just one more absolute value on the rationals, the $p$-adic absolute value.
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/FIXME>
   Ostrowoski theorem
</a>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Let's start from $p$-adic integers, instead of working modulo p, expand in powers of p
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle a \in \mathbb{Z}_p : a_0 p^0 + a_1 p^1 + a_2 p^2 + \dots + \mathcal{O}(p^n)
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ In some sense we are correcting the finite field result with more (subleading) information.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ $p$-adic numbers $\mathbb{Q}_p$ allow for negative powers of $p$, (would be division by zero in $\mathbb{F}_p$!)
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle a \in \mathbb{Q}_p : a_{-\nu} p^{-\nu} + \dots + a_0 + a_1 p^1 + \dots + \mathcal{O}(p^n)
$$
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -4mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/2203.04269>
   GDL, Page ('22)
</a>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The $p$-adic absolute value is defined as $|a|_p = p^\nu$.
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ Think of $p$ as a small quantity, $\epsilon$, even if it is a large prime (by the real absolute value, $|\,|_\infty$).
</div>

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> The <span style="font-size: 27pt;">$p\kern2mm$</span>-adic (N)MRK Limit </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The space of $p$-adic numbers is an <b>ultrametric</b> space, the triangle inequality is strengthened to:
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle d(x,z)\leq \max \left\{d(x,y),d(y,z)\right\} 
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ This leads to better stability properties: adding two numbers can never result is a larger number!
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ With general kinematic
</div>
<pre><code class="language-python" style="font-size: 11pt">from syngular import Field
oPs = Particles(6, field=Field("padic", 2 ** 31 - 1, 9), seed=0)  # create psp
(1j * coeffs['bubble(1)'])(oPs)  # evaluate the coefficient(s)
</code></pre>
<pre><code class="language-python" style="margin-top:-5mm; font-size: 10pt">490010355 + 1085079429*2147483647 + 1676653899*2147483647^2 + 726358851*2147483647^3 + 1074867770*2147483647^4 + 133781189*2147483647^5 + 892424664*2147483647^6 + 1457115085*2147483647^7 + 2127645140*2147483647^8 + O(2147483647^9)
</code></pre>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Manipulate phase space: set the (N)MRK parameter controlling the rapidity gap to be $x\approx p$
</div>
<div style="font-size: 15pt; margin-top: 3mm; margin-bottom: 3mm">
$$ 
\displaystyle 0 \leq \text{leading NMRK behavior} \leq p-1 + \mathcal{O}(2147483647^1)
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 0mm; margin-left: 2mm; margin-right: 2mm;">
     ${\color{greeN} ✓}$ We still lose 1 digit per spurious pole, but the result is now <u>exact</u>.
</div>

</section>

---

<section>

{{< slide background-image="varieties-no-background.png" >}}

# NMRK Analytic Reconstruction

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 2mm;"> Variables Ring \& Least Common Denomiantors </b>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ We have 5 independent variables
</div>
<div style="font-size: 15pt; margin-top: 2mm; margin-bottom: 5mm">
$$ 
\displaystyle \kern10mm R_{NRMK} = \mathbb{F}\big[ z, \bar z, w, \bar w, X(=X_{45}) \big]
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ We are after rational functions in these five variables
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ The complexity is not just because of the number of variables, but also because of the possible sigularities
</div>
<div style="font-size: 15pt; margin-top: 2mm; margin-bottom: 5mm">
$$ 
\displaystyle \mathcal{D}_{\Delta_{3m}} = -4(-1+w)w(-1+\bar w)\bar w X^2 (-1+z) z (-1+\bar z) \bar z+ \\ (X z (\bar w+\bar z-\bar w \bar z+X\bar z)+w(\bar w-X (-1+z) \bar z+\bar w X(1-\bar z+z(-1+2\bar z))))^2
$$
</div>
<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\phantom{\circ}$ alone has degreee 10. It appears up to cubic pole, making denominators exceed degree 30.
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ By comparison the most complicated singularity at 5-point was <span style="font-size: 15pt;">$(z - \bar{z})$</span>
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ Obtain least common denominators from a unviariate slice (think BCFW shift)
</div>
<div style="font-size: 15pt; margin-top: 2mm; margin-bottom: 5mm">
$$ 
\displaystyle z \rightarrow z + c_z t, \; \bar z \rightarrow \bar z + c_{\bar z} t, \; w \rightarrow w + c_{\bar w} t, \; \bar w \rightarrow \bar w + c_{\bar w} t, \; X \rightarrow X + c_X t
$$
</div>

<div style="font-size: 18pt; text-align: left; margin-bottom: 2mm; margin-top: 2mm; margin-left: 2mm; margin-right: 2mm;">
     $\circ$ In Least Common Denominator form the numberators are too complex, we would need hundred of thousands to millions of evaluations to determine them.
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
     $\circ\;$ Nesting the $p$-adic limit: set $x \propto p^5$, get 5 digits for the leading NMRK behaviour <br>
     $\phantom{\circ}\;$ Set $\mathcal{D}_i \propto p$, as long as it's pole degree is less than 5, get a value for the residue
</div>


</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# <br> Summary <br> & <br> Outlook

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
