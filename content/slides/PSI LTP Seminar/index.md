---
title: Modern Methods for the Computation of Scattering Amplitudes
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
<html>
	<head>
		<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Indie+Flower">
		<link rel="stylesheet" href="../reveal_custom.css">
	</head>
</html>

{{< slide background-image="PSI-aerialview.jpg" >}}

<br><br>

### <b> Modern Methods for the Computation of Scattering Amplitudes </b>

<br>

Giuseppe De Laurentis

LTP Seminar \
\
<p style="line-height: 0.05;"> <img src="paul-scherrer-institute-psi-logo-vector-transparent.png"; style="max-width:280px;float:center;border:none;">\
\
<font size=2> These slides at [gdelaurentis.github.io/slides/psi-ltp-seminar](/slides/psi-ltp-seminar/#/) </font size> </p>

{{< speaker_note >}}
- Only speaker can read these.
- Press S to view.
{{< /speaker_note >}}

---

<section>

{{< slide background-image="LHCXSection.jpg" >}}

# What are <br> Scattering Amplitudes?

---

<b style="font-variant: small-caps; font-size: xxx-large"> Amplitudes and the $\boldsymbol{S}$-Matrix </b>


<div style="font-size: x-large">
$$\langle \text{final state} | S | \text{initial state} \rangle = \underbrace{\delta_{fi}}_{\text{no scattering}} + \underbrace{i(2\pi)^4\delta(p_f-p_i)}_{\text{4-momentum conservation}} \quad \times \; \underbrace{\mathcal{A}_{fi}}_{\text{scattering amplitude}}$$

Or simply: $\; S = 1 + i \, T$<br><br>

In practice, we want <span style="background-color: #FFFF007F">fully-connected, amputated Feynman diagrams</span>
</div>

<img src="ScatteringAmplitudeFeynmanDiagramTransparent.png"; style="max-width:300px;float:center;border:none;margin-top:-5px;">

---

<b style="font-variant: small-caps; font-size: xxx-large"> Amplitudes and Cross Sections </b>
<br>

<div style="text-align: left; font-size: x-large">
Cross sections at hadron colliders take the form:

$$\displaystyle σ_{2 \rightarrow n - 2} = \sum_{a,b} ∫ dx_a dx_b f_{a/h_1}(x_a, μ_F) \, f_{b/h_2}(x_b, μ_F) \;\hat{σ}_{ab→n-2}(μ_F, μ_R) \\[2mm]
\displaystyle \hat{σ}_{n}=\frac{1}{2\hat{s}}\int d\text{LIPS} \prod_{n-2}\;(2π)^4δ^4\big(\sum_{i=1}^n p_i\big)\;|\overline{\mathcal{A}(p_i,μ_F, μ_R)}|^2$$
</div>

<div style="display:block; width:100%;">
  <div style="width:50%; float: left; display: inline-block;">
       <img src="HiggsDiscoveryPlotTransparent.png"; style="max-width:430px; float:center; border:none; margin-top: 1mm; margin-bottom: -5mm;">
       <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1207.7214>
       	  ATLAS Collaboration ('12)
       </a>
  </div>
  <div style="width:50%; float: center; display: inline-block; font-size: x-large;">
       <img src="HiggsDiagramTransparent.png"; style="max-width:200px;float:center;border:none;margin-top:5mm;margin-bottom:0mm">
       $$\mathcal{A}_{pp\rightarrow h \rightarrow \gamma\gamma} \sim \frac{1}{m_{\gamma\gamma}^2 - m^2_h + i m_h \Gamma_h}$$
       $$\Rightarrow\; \text{Breit–Wigner distribution}$$
  </div>
</div>


---

<b style="font-variant: small-caps; font-size: xxx-large"> Perturbation Theroy </b>

<div style="text-align: left; font-size: x-large">
$$\displaystyle \mathcal{A}_n = \underbrace{\mathcal{A}_n^{\text{tree}}}_{\kern-40mm \text{comulative error:} \quad \sim 30\%} + \left(\frac{\alpha_S}{2\pi}\right) \underbrace{\mathcal{A}_n^{1-\text{loop}}}_{\sim 10\%} + \left(\frac{\alpha_S}{2\pi}\right)^2 \underbrace{\mathcal{A}_n^{2-\text{loop}}}_{\sim 1\%} + \dots$$

Better predictions require both <span style="background-color: #FFFF007F">more loops</span> and <span style="background-color: #FFFF007F">higher multiplicity</span>.

<table width=50% border="1" cellspacing="0" cellpadding="0" style="margin-bottom: 8mm; margin-top: 8mm">
  <tr class="greenline">
    <td colspan="2", rowspan="2"> <div id="rot90"> <center> <b> $\mathcal{A}_{n-gluons}^{\ell-loops} \propto g_s^{n-2+2\ell} $ </b> </center> </div> </td>
    <td colspan="4"> <center> multiplicity $(n)$ </center> </td>
  </tr>
  <tr>
    <td><b>4</b></td>
    <td><b>5</b></td>
    <td><b>6</b></td>
    <td><b>7</b></td>
  </tr>
  <tr>
    <td rowspan="3"> <center> loops ($\ell$) </center> </td>
    <td><b>0</b></td>
    <td>2</td>
    <td>3</td>
    <td>4</td>
    <td>5</td>
  </tr>
  <tr>
    <td><b>1</b></td>
    <td>4</td>
    <td>5</td>
    <td>6</td>
    <td>7</td>
  </tr>
  <tr>
    <td><b>2</b></td>
    <td>6</td>
    <td>7</td>
    <td>8</td>
    <td>9</td>
  </tr>
</table>

IR singularities have to be cancelled between real and virtual corrections. 
</div>

<div style="text-align: center; font-size: x-large; margin-top: 8mm;">
More loops $\rightarrow$ analytical complexity; &nbsp more legs $\rightarrow$ algebraic complexity.
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> State-of-the-Art </b>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 7mm;">
     $\circ\,$ Four-point three-loop <br>
     $\circ\,$ Five-point two-loop <br>
     $\circ\,$ Six-point one-loop (analytics); Solved to all multiplicities (numerics) <br>
     $\circ\,$ Tree (solved)
</div>

</section>
---

---
<section>

{{< slide background-image="Feynman-Diagrams-transparent.png" >}}

# The structure of <br> Scattering Amplitudes

---

<b style="font-variant: small-caps; font-size: xxx-large; margin-bottom: 30mm;"> <span style="color: green">Dynamics</span> and <span style="color: red">Kinematics</span> </b>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 10mm;">Color ordering at tree level ($T$'s are $SU(N_c)$ generators)</div>
<a style="font-size: large; text-align: right; float: right; margin-top: 5mm; margin-bottom: 5mm;" href=https://www.sciencedirect.com/science/article/pii/0550321387906043?ref=pdf_download&fr=RR-2&rr=7c49373aad8e3b51>Berends, Giele ('80s)</a>

<div style="font-size: x-large; margin-top: 10mm;">
$$\displaystyle \mathcal{A}^{tree}_{n}({p_i, λ_i, a_i}) = \; g^{n-2} \sum_{σ\in S_n/Z_n} \color{green}{\text{Tr}(T^{a_σ(1)}\dots T^{a_σ(n)})} \; \color{red}{A^{tree}_n(σ(p_1^{λ_1}),\dots ,σ(p_n^{λ_n}))}\\[8mm]$$
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 10mm;">and one loop</div>
<a style="font-size: large; text-align: right; float: right; margin-top: 5mm; margin-bottom: 5mm;" href=https://www.sciencedirect.com/science/article/pii/055032139190567H?ref=pdf_download&fr=RR-2&rr=7c4937405f2d3b51>Bern, Kosower ('91)</a>

<div style="font-size: x-large; margin-top: 10mm;">
$$\displaystyle\mathcal{A}^{1-loop}_{n}({p_i, λ_i, a_i}) = \; g^{n} \sum_{σ\in S_n/Z_n} \color{green}{N_{c}\text{Tr}(T^{a_σ(1)}\dots T^{a_σ(n)})} \; \color{red}{A^1_{n;1}(σ(p_1^{λ_1}),\dots ,σ(p_n^{λ_n}))} \\
\displaystyle + \sum_{c = 2}^{\lfloor n/2 \rfloor + 1}\sum_{σ\in S_n/Z_{n;c}} \color{green}{\text{Tr}(T^{a_σ(1)}\dots T^{a_σ(c-1)})\text{Tr}(T^{a_σ( c)}\dots T^{a_σ(n)})} \;  \color{red}{A^1_{n;c}(σ(p_1^{λ_1}),\dots ,σ(p_n^{λ_n}))}$$
</div>

<div style="text-align: center; font-size: x-large; margin-top: 10mm;">We will focus on <span style="background-color: #FFFF007F"><i>color-ordered</i> amplitudes</span> $A^\ell_n$</div>

---

<b style="font-variant: small-caps; font-size: xxx-large; margin-bottom: 20mm;"> <span style="color: orange">Rational</span> and <span style="color: red">Transcendental</span> </b>

<div style="text-align: left; font-size: x-large; float: left; margin-bottom: 10mm; margin-top: 10mm">Decomposition in terms of master integrals</div>
<a style="font-size: large; text-align: right; float: right; margin-bottom: 5mm; margin-top: 10mm" href=https://arxiv.org/abs/0712.1851>Ellis, Zanderighi</a>
<a style="font-size: large; text-align: right; float: right; margin-bottom: 5mm; margin-top: 10mm" href=https://arxiv.org/abs/hep-ph/9212308>Bern, Dixon, Kosower;&nbsp</a>
<a style="font-size: large; text-align: right; float: right; margin-bottom: 5mm; margin-top: 10mm" href=https://www.sciencedirect.com/science/article/pii/0550321379906059?ref=pdf_download&fr=RR-2&rr=7c4afcac1f343b58>'t Hooft, Veltman;&nbsp</a>

<div style="font-size: x-large; margin-top: 10mm;">
$$A^{1-\text{loop}}_{n} = \sum_i \color{orange}{d_i} \color{red}{I^i_{Box}} + \sum_i \color{orange}{c_i} \color{red}{I^i_{Triangle}} + \sum_i \color{orange}{b_i} \color{red}{I^i_{Bubble}} + \sum_i \color{orange}{a_i} \color{red}{I^i_{Tadpoles}} + \color{orange}{R}$$
</div>

<div style="width:90%; float: center; display: inline-block;">
       <img src="one-loop-decomposition-transparent.png"; style="max-width:750px;float:center;border:none;margin-top:-5px;">
  </div>

<div style="text-align: left; font-size: x-large; float: left; margin-bottom: 10mm;">
     In general, in $D= 4- 2 \epsilon$, for a suitable choice of master integrals
</div>

<div style="font-size: x-large; margin-top: 10mm; margin-bottom:10mm">
$$A^{\ell-loop}_n = \sum_{i \in \text{masters}} \frac{\color{orange}{c_i}(\vec p, \vec \lambda, \epsilon) \, \color{red}{I_i}(\vec p, \epsilon)}{\prod_j (\epsilon - a_{ij})}\;, \quad \text{with} \quad a_{ij} \in \mathbb{Q}$$
</div>

<!---
<div style="text-align: left; font-size: x-large; float: left; margin-bottom: 10mm;">
    $\kern30mm \cdot$ the coefficients $c_i$ are <span style="color: orange">rational</span> in $p_i$ and polynomial in $\epsilon$, <br>
    $\kern30mm \cdot$ the master integrals $I_i$ are <span style="color: red">transcendental</span>, <br>
    $\kern30mm \cdot$ the $a_{ij}$ are rational numbers ($a_{ij} \in \mathbb{Q}$)
</div>
--->

</font size>

---

{{< slide background-image="Five_gluons_mess-transparent-background.png" >}}

<b style="font-variant: small-caps; font-size: xxx-large"> Feynman diagram by Feynman diagram </b>
<br>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 5mm;">     
     $\circ\,$ Analytic computations get very complicated very quickly, even at tree level. <br>
     $\phantom{\circ}\,$ But this doesn't mean final results can't be compact. <br><br>

     $\circ\,$ Each term in the expression in the background reads something like:
</div>

<br><br><br><br>

<div style="text-align: center; font-size: x-large; float: center; margin-top: 5mm; margin-bottom: 5mm;">     
     $(k_1 \cdot k_4) (\varepsilon_2 \cdot k_2) (\varepsilon_1 \cdot \varepsilon_3) (\varepsilon_4 \cdot \varepsilon_5)$
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 5mm;">
     $\phantom{\circ}\,$ with $k_i$ 4-momenta, and $\varepsilon_i$ polarization tensors. <br><br>
     $\circ\,$ This is for a tree-level 5-gluon amplitude, which can be simplified to
</div>

<div style="text-align: center; font-size: 22pt; margin-top: 0mm; margin-bottom: 5mm;">
$A^{tree}(1^{+}_{g}2^{+}_{g}3^{+}_{g}4^{-}_{g}5^{-}_{g}) = \frac{i\,⟨45⟩^{4}}{⟨12⟩⟨23⟩⟨34⟩⟨45⟩⟨51⟩}$
</div>

<font size=5>
      [S.J.Parke, T.R.Taylor](https://journals.aps.org/prl/pdf/10.1103/PhysRevLett.56.2459);
      [F.A.Berends, W.T.Giele](https://www.sciencedirect.com/science/article/pii/0550321388904427)
</font size>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Spinor Helicity </b>
<br>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 7mm;">
     $\circ\,$ The spinors $\lambda, \bar\lambda$ can be expressed in terms of 4-momentum components as:
</div>

<font size=5>$$
\lambda\_\alpha=\frac{1}{\sqrt{p^0+p^3}}\begin{pmatrix}p^0+p^3 \\\ p^1+ip^2\end{pmatrix} \, , \;\;
\bar\lambda\_{\dot\alpha}=\frac{1}{\sqrt{p^0+p^3}}\begin{pmatrix}p^0+p^3 \\\ p^1-ip^2\end{pmatrix} 
$$</font size>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 7mm;">
     $\circ\,$ Indices are raised with the metrix $\epsilon^{\alpha\beta}=\epsilon^{\dot\alpha\dot\beta}$, which is the Levi-Civita symbol.
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 7mm;">
     $\circ\,$ Lorentz-invariant <i> spinor brackets </i> are built from spinor contractions
</div>

<font size=5>
$$
⟨ij⟩ = λ_iλ_j = (λ_i)^α(λ_j)_α \quad \quad \quad [ij] = \barλ_i\barλ_j = (\barλ_i)\_\dotα(\barλ_j)^\dotα
$$
</font size>

</section>
---

---
<section>

{{< slide background-image="ComputingClusterImage.jpg" >}}

# How do we compute Scattering Amplitudes efficiently?

---


<b style="font-variant: small-caps; font-size: xxx-large"> Recursion Relations for Trees </b>


<div style="font-size: x-large; float: left;">
$\circ$ Off-mass-shell recursion for tree (Berends-Giele)
</div>

<div style="font-size: x-large; float: left;">
$\circ$ On-mass-shell recursion for tree (Britto-Chacazo-Feng-Witten)
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Multi-Loop Amplitudes from Trees </b>

<div style="font-size: x-large; float: left; margin-bottom: 0mm;">
$\circ$ Generalized unitarity relates products of tree amplitudes to loop amplitudes
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: -5mm; margin-left: 5mm;">
	<div style="font-size: x-large; width:50%; float: left; text-align: center; display: inline-block; margin-top: 0mm;">
	     $$
	     \displaystyle \prod_{\text{trees}} A^{\text{tree}}(\vec k, \vec\ell) = \sum_{\substack{\text{topologies}\, \Gamma, \\ i \in M_\Gamma \cup S_\Gamma}} c_{i,\Gamma}(\vec k) \frac{m_{i,\Gamma}(\vec k, \vec\ell)}{\displaystyle \prod_{\text{props}\,j} \rho_{j}(\vec k, \vec\ell)}
	     $$
	     $$
	     \left. \begin{aligned}
	     \text{Master integrals:} \; & \int d^{D}\vec \ell \; m_{i\in M_\Gamma} \neq 0 \\
	     \text{Surface terms:} \; & \int d^{D}\vec \ell \; m_{i\in S_\Gamma} = 0 \\
	     \end{aligned} \right\} \; \begin{aligned} & \text{Complex} \\ & \text{problem!} \end{aligned}
	     $$
	</div>
	<div style="width:50%; float: right; display: inline-block;">
	     <div style="font-size: x-large; width:50%; float: center; text-align: center; display: inline-block; margin-top: 5mm;">
	     	  <tt> C++ code </tt>
	     </div><br>
	     <img src="CaravelLogo.png"; style="max-width:150px; float:center; border:none; margin-top: 0mm; margin-bottom: -5mm;">
	     <br>
	     <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 5mm;"
	     	href=https://www.sciencedirect.com/science/article/pii/0550321387906043?ref=pdf_download&fr=RR-2&rr=7c49373aad8e3b51>
		H. Ita (PSI) et al. ('20)
	     </a>
	</div>
</div>

<br><br><br><br><br><br><br><br>

<div style="display:block; width:100%; margin-top: 5mm; margin-bottom: 0mm;">
	<div style="font-size: x-large; width:50%; float: left; text-align: left; display: inline-block; margin-top: 10mm;">
	     $\circ$ The diagram on the right shows as example a one-loop box coefficient. <br><br>
     	     $\circ$ In general, need to solve linear systems for the coefficients $c_{i,\Gamma}$. <br>
	</div>
	<div style="width:50%; float: right; display: inline-block;">
	     <img src="BoxCoefficient.png"; style="max-width:350px; float:center; border:none; margin-top: 0mm; margin-left: 0mm; margin-bottom: 0mm;">
	</div>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Choosing a Number Field </b>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 5mm;">     
     $\circ\,$ Double-precision floating-point evaluations ($\mathbb{R}$ or $\mathbb{C}$) are too unstable, <br>
     $\phantom{\circ}\,$ and arbitrary precision evaluations are <b> very </b> slow. <br><br>

     $\circ\,$ Could try rational inputs ($\mathbb{Q}$), but integers grow way too large at intermediate stages. <br><br>

     $\circ\,$ Finite fields ($\mathbb{F}_p$) come to the rescue. These are integers modulo a prime number $p$: <br>
     <div style="text-align: center; float: center; margin-top: 5mm;">
     	  $\phantom{\circ}\,$ $\mathbb{F}_p = \{0, 1, 2, \dots, p-1, p\} \cup \{+, -, \times, \div \}$
     </div>
     <br>
     $\phantom{\circ}\,$ The prime $p$ needs to be large, to avoid accidental <tt> DivisionByZero </tt>. <br><br>
     
     $\circ\,$ But we can't do phenomenology with $\mathbb{F}_p$ ! <br><br>

</div>

</section>
---
---

<section>

{{< slide background-image="matrix.png" >}}

# Analytic Reconstruction

---

<b style="font-variant: small-caps; font-size: xxx-large"> Common-Denominator Ansatz </b>
<br>

<div style="text-align: left; font-size: x-large">
$\circ\,$ Denominators, Thiele interpolation
</div>

<div style="text-align: left; font-size: x-large">
$\circ\,$ The numerator Ansatz

</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Obtaining and Fitting the Ansatz </b>
<br>

<div style="text-align: left; font-size: x-large">
$\circ\,$ Enumerating all possible spinor monomials
</div>

<div style="display:block; width:100%; margin-top: 5mm;">
	<div style="width:50%; font-size: x-large; float: left; display: inline-block;">
	     Gröbner bases computations
	     <img src="SingularLogo.png"; style="max-width:350px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;"> <br>
	     <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 5mm;"
	     href=https://www.singular.uni-kl.de/index.php.html>
		Decker, Greuel, Pfister, Schönemann
	     </a>	    
	</div>
	<div style="width:50%; font-size: x-large; float: right; display: inline-block;">
	     Integer programming problem <br>
	     <img src="GoogleORToolsLogo.png"; style="max-width:350px; float:center; border:none; margin-top: 7mm; margin-bottom: 0mm;"> <br>
	     <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 5mm;"
	     href=https://www.singular.uni-kl.de/index.php.html>
		Perron and Furnon (Google optimization team)
	     </a>
	</div>
</div>

<br><br><br><br><br>

<div style="text-align: left; font-size: x-large; margin-top: 1mm;">
$\circ\,$ Solving linear systems with CUDA in $\mathbb{C}$ or $\mathbb{F}_{p\leq 2^{31}-1}$
</div>

<div style="display:block; width:100%; margin-top: 5mm;">
	<div style="width:50%; font-size: x-large; float: left; display: inline-block;">
	     Currently private code <br><br>
	     <table>
	     <tr>
	     <th style="text-align:center">System Size</th>
	     <th style="text-align:center">Timing</th>
	     </tr>
	     <tr>
	     <td style="text-align:center">8192</td>
	     <td style="text-align:center">8 s</td>
	     </tr>
	     <tr>
	     <td style="text-align:center">16384</td>
	     <td style="text-align:center">51 s</td>
	     </tr>
	     <tr>
	     <td style="text-align:center">32768</td>
	     <td style="text-align:center">6m 30s</td>
	     </tr>
	     </table>
	</div>
	<div style="width:50%; font-size: x-large; float: right; display: inline-block;">
	     RTX 2080ti on the gMerlin cluster <br>
	     <img src="2080ti.png"; style="max-width:200px; float:center; border:none; margin-top: 7mm; margin-bottom: 0mm;">
	</div>
</div>


---

<b style="font-variant: small-caps; font-size: xxx-large"> Complexity Scaling </b>
<br>

<div style="text-align: left; font-size: x-large">
Common-denominator is BAD
</div>

</section>
---

---
<section>

{{< slide background-image="varieties-no-background.png" >}}

# The Geometry of Phase Space

---

<b style="font-variant: small-caps; font-size: xxx-large"> Common Denominator Redoux </b>

<div style="text-align: left; font-size: x-large">
Singular surfaces
</div>

<div style="display:block; width:100%; margin-top: 5mm;">
	<div style="width:50%; float: left; display: inline-block;">
	     <img src="V1.png"; style="max-width:250px; float:center; border:none; margin-top: 5px;">
	</div>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Multivariate Partial Fractions </b>

<div style="text-align: left; font-size: x-large">
Singular surfaces
</div>

<div style="display:block; width:100%; margin-top: 5mm;">
	<div style="width:50%; float: left; display: inline-block;">
	     <img src="V1.png"; style="max-width:250px; float:center; border:none; margin-top: 5px;">
	</div>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Beyond Partial Fractions </b>

<div style="text-align: left; font-size: x-large">
Singular surfaces
</div>

<div style="display:block; width:100%; margin-top: 5mm;">
	<div style="width:50%; float: left; display: inline-block;">
	     <img src="V1.png"; style="max-width:250px; float:center; border:none; margin-top: 5px;">
	</div>
</div>	

</section>
---

---
<section>


<b style="font-variant: small-caps; font-size: xxx-large"> Upcoming Results </b>

<div style="text-align: left; font-size: x-large">
$pp \rightarrow \gamma \gamma \gamma$
</div>

<div style="text-align: left; font-size: x-large">
$pp \rightarrow Wjj$
</div>

---

<b style="font-size: xx-large"> Thank you! </b>

<br>

<b> Questions? </b>

</section>
---

---
<section data-visibility="uncounted">

# Backup Slides

</section>
---

---
<section data-visibility="uncounted">
# More Spinor Helicity

---

<b style="font-variant: small-caps; font-size: xxx-large">  Representations of the Lorentz group </b>

<font size=5>
(Recall: $\mathfrak{so}(1, 3)_\mathbb{C} \sim \mathfrak{su}(2) \times \mathfrak{su}(2)$)
</font size> 

<font size=5>

| $\boldsymbol{(j\_{-},j\_{+})}$ | dim. | name | quantum field | kinematic variable |
| :-------------: | :-------------: | :------------- | :-------------: | :-------------: |
| (0,0) | 1 | scalar | $h$ | m |
| (0,1/2) | 2 | right-handed Weyl spinor | $\chi_{R\,\alpha}$ | $\lambda_\alpha$ |
| (1/2,0) | 2 | left-handed Weyl spinor | $\chi_L^{\,\dot\alpha}$ | $\bar{\lambda}^{\dot\alpha}$ |
| (1/2,1/2) | 4 | rank-two spinor/four vector | $A^\mu/A^{\dot\alpha\alpha}$ | $P^\mu/P^{\dot\alpha\alpha}$ |
| (1/2,0)$\oplus$(0,1/2) | 4 | bispinor (Dirac spinor) | $\Psi$ | $u, v$ |

</font size>

---

<b style="font-variant: small-caps; font-size: xxx-large">  Spinor Covariants </b>
<br>

Weyl spinors are sufficient for massless particles:

<font size=5>$\text{det}(P^{\dot\alpha\alpha})=m^2 \rightarrow 0 \quad \Longrightarrow \quad P^{\dot\alpha\alpha} = \bar\lambda^{\dot\alpha}\lambda^\alpha$.</font size>

<br>
In terms of 4-momentum components we have:

<font size=5>$$
\lambda\_\alpha=\frac{1}{\sqrt{p^0+p^3}}\begin{pmatrix}p^0+p^3 \\\ p^1+ip^2\end{pmatrix} \, , \;\;\; \lambda^\alpha=\epsilon^{\alpha\beta} \lambda_\beta =\frac{1}{\sqrt{p^0+p^3}}\begin{pmatrix}p^1+ip^2 \\\ -p^0+p^3\end{pmatrix}
$$</font size>

<font size=5>$\bar\lambda\_{\dot\alpha}=\frac{1}{\sqrt{p^0+p^3}}\begin{pmatrix}p^0+p^3 \\\ p^1-ip^2\end{pmatrix} \, , \;\;\; \bar\lambda^{\dot\alpha}=\epsilon^{\dot\alpha\dot\beta}\bar\lambda_{\dot\beta}=\frac{1}{\sqrt{p^0+p^3}}\begin{pmatrix}p^1-ip^2 \\\ \-p^0+p^3\end{pmatrix}$</font size>

<br>

<font size=5>$$
\bar\lambda\_{\dot\alpha} = (\lambda\_\alpha)^* \quad if \quad p^i \in \mathbb{R}; \quad \quad \bar\lambda\_{\dot\alpha} \neq (\lambda\_\alpha)^* \quad if \quad p^i \in \mathbb{C}
$$</font size>

---

<b style="font-variant: small-caps; font-size: xxx-large">  Spinor Invariants </b>
<br>

<font size=5>
$$
⟨ij⟩ = λ_iλ_j = (λ_i)^α(λ_j)_α \quad \quad \quad [ij] = \barλ_i\barλ_j = (\barλ_i)\_\dotα(\barλ_j)^\dotα
$$


$$
s_{ij} = ⟨ij⟩[ji]
$$


$$
⟨i\;|\;(j+k)\;|\;l] = (λ_i)^α (\not P_j + \not P_k )\_{α\dotα} \barλ_l^\dotα
$$


$$
⟨i\;|\;(j+k)\;|\;(l+m)\;|\;n⟩ = (λ_i)^α (\not P_j + \not P_k )\_{α \dot α} (\bar{\not P_l} + \bar{\not P_m} )^{\dot α α} (λ_n)_α
$$


$$
tr_5(ijkl) = tr(\gamma^5 \not P_i \not P_j \not P_k \not P_l) =  [i\,|\,j\,|\,k\,|\,l\,|\,i⟩ - ⟨i\,|\,j\,|\,k\,|\,l\,|\,i]
$$

</font size>

</section>
---

---
<section data-visibility="uncounted">
# Five-Parton Two-Loop <br> Finite Remainders

<br>

Example Simplifications

---

<b> uubggg pmpmp Nf1 #3 </b>

<img src="uubggg_pmpmp_nf1_nb3.png"; style="max-width:1024px;float:center;border:none;">

<font size=5> is equal to </font size>

<font size=5>
$
-\frac{[32]^3 [41]^3}{2 [31]^3 [42]^3}
$
</font size>

---

<b> ggggg mpmpp Nf1 # 9 </b>

<img src="ggggg_mpmpp_nf1_9.png"; style="max-width:512px;float:center;border:none;">

<font size=5> is equal to </font size>

<font size=5>
$-1\frac{[12]³[15][23]⟨25⟩³[35]³}{[13]⁴[25]⟨5|1+2|5]³}+\frac{97}{12}\frac{[12]⁴⟨25⟩[35]⁴}{[13]⁴[25]³⟨5|1+2|5]}$
$+\frac{13}{3}\frac{[12]⁴⟨15⟩[15][35]⁴}{[13]⁴[25]⁴⟨5|1+2|5]}+\frac{1}{4}\frac{[12]⁴⟨15⟩[15]⟨25⟩[35]⁴}{[13]⁴[25]³⟨5|1+2|5]²}$
$-\frac{3}{2}\frac{[12]²⟨25⟩²[25][35]²}{[13]²[25]⟨5|1+2|5]²}+\frac{7}{4}\frac{[12]³⟨25⟩²[35]³}{[13]³[25]⟨5|1+2|5]²}$
$-\frac{43}{3}\frac{[12]³⟨25⟩[35]³}{[13]³[25]²⟨5|1+2|5]}$
$-\frac{25}{3}\frac{[12]³⟨15⟩[15][35]³}{[13]³[25]³⟨5|1+2|5]}$
$-\frac{3}{2}\frac{[12]⟨25⟩[25][35]}{[13][25]⟨5|1+2|5]}$
$+4\frac{[12]²⟨25⟩[35]²}{[13]²[25]⟨5|1+2|5]}$
$-\frac{15}{2}\frac{[12]²[35]²}{[13]²[25]²}$
$+\frac{7}{2}\frac{[12][35]}{[13][25]}$
$-\frac{2}{3}$
</font size>

</section>
---

---
<section data-visibility="uncounted">
# Higgs + 4-Parton Amplitude <br> (@ finite top-mass) 

---

<b> Example of cut diagram </b>

<img src="HiggsBox.png"; style="max-width:300px;float:center;border:none;">

Only singularity involving $m_{top}$ (from pentagon contributions)

$16 |S\_{1×2×3×4}| = −s\_{12} \, s\_{23} \, s\_{34} \, \langle 1 |2 + 3|4] \, \langle 4|2 + 3|1] + m^2\_{top} \, tr_5(1234)^2$

We can generate point near this singularity in a similar fashion.

---

<b> Structure of the coefficients </b>

The massive external leg (the Higgs) is easily accomodated by considering it as a pair of massless particles (think decay products). <br>
In the end all dependance on $P_{Higgs}$ is removed by using momentum conservation.

The coefficients are Taylor expasions in $m_{top}$:

$C^{(0)} + m^2_{top} C^{(2)}$.

with $C^{(0)}$ and $C^{(2)}$ resabling the six-gluon coefficients.
</section>
---