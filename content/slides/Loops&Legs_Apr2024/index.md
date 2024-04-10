---
tile: Non-Planar Two-Loop Amplitudes for Five-Parton Scattering
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
	<b style="margin-top:15mm; font-size: 28pt;">
	   Non-Planar Two-Loop Amplitudes <br>
	   for Five-Parton Scattering
	</b>
</h3>

<div style="font-size: x-large; margin-top:10mm;">
Giuseppe De Laurentis
<br>
<div style="font-size: large;"> University of Edinburgh </div>
<br>
<a href="https://arxiv.org/abs/2311.10086">arXiv:2311.10086</a> <div style="font-size: large; margin-bottom: 10pt;"> (GDL, H. Ita, M. Klinkert, V. Sotnikov) </div>
<A href="https://arxiv.org/abs/2311.18752">arXiv:2311.18752</a> <div style="font-size: large;"> (GDL, H. Ita, V. Sotnikov) </div>

<!--- Amplitudes Meeting --->
Loops & Legs 2024
<br>
<p style="line-height: 0.05;"> <img src="UniEdinburghLogo-transparent.png"; style="max-width:120px;float:center;border:none;"> 
<br><br>
<span style="font-size: 11pt">Find these slides at  <a href="/slides/fivepartons_dec2023/#/">gdelaurentis.github.io/slides/loopslegs_apr2024</a> </span>
</div>

---

<section>

{{< slide background-image="LHCcern.jpg" >}}

# Introduction:
# (2) Loops & (5) Legs

---

{{< slide background-image="ATLAS2022.png" >}}

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 25mm;"> Status: Two-Loop Five-Point Massless Amplitudes </b>

<style>
    table {
        width: 100%;
        border-collapse: collapse;
    }
    th, td {
        border: 1px solid black;
        padding: 8px;
        text-align: center !important;
    }
    th {
        font-size: 20px; /* Adjust the font size for table headers */
    }
    td {
        font-size: 16px; /* Adjust the font size for table data */
    }
    tr:last-child td {
        border-bottom: 1px solid black; /* Add border to bottom of last row */
    }
</style>

<table>
    <thead>
        <tr>
            <th style="font-size: 24px;">Process</th>
            <th style="font-size: 24px;">Analytical Amplitudes</th>
            <th style="font-size: 24px;">Numerical Codes</th>
            <th style="font-size: 24px;">Cross Sections</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow \gamma\gamma\gamma$</td>
            <td style="font-size: 20px;">[3, 4, 5]</td>
            <td style="font-size: 20px;">[3, 5]</td>
            <td style="font-size: 20px;">[1, 2]</td>
        </tr>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow \gamma\gamma j$</td>
            <td style="font-size: 20px;">Row 1, Column 1</td>
            <td style="font-size: 20px;">Row 1, Column 2</td>
            <td style="font-size: 20px;">Row 1, Column 3</td>
        </tr>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow \gamma jj$</td>
            <td style="font-size: 20px;">Row 2, Column 1</td>
            <td style="font-size: 20px;">Row 2, Column 2</td>
            <td style="font-size: 20px;">Row 2, Column 3</td>
        </tr>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow jjj$</td>
            <td style="font-size: 20px;">Row 3, Column 1</td>
            <td style="font-size: 20px;">Row 3, Column 2</td>
            <td style="font-size: 20px;">Row 3, Column 3</td>
        </tr>
        <tr>
        </tr>
    </tbody>
</table>

<style>
    .two-col {
        display: flex;
        justify-content: center;
    }
    .column {
        flex: 1;
        padding: 10px;
        margin: 0 10px;
        text-align: left;
    }
</style>
<div class="two-col">
    <div class="column">
        <p style="margin-bottom:2mm; margin-top:2mm;"><a href="https://inspirehep.net/literature/1762583" style="font-size: 16pt;">[1] Chawdhry, Czakon, Mitov, Poncelet '19</a></p>
        <p style="margin-bottom:1mm; margin-top:1mm;"><a href="https://inspirehep.net/literature/1827330" style="font-size: 16pt;">[3] Abreu, Page, Pascual, Sotnikov '20</a></p>
        <p style="margin-bottom:1mm; margin-top:1mm;"><a href="https://inspirehep.net/literature/2663067" style="font-size: 16pt;">[5] Abreu, GDL, Ita, Klinkert, Page, Sotnikov '23</a></p>
    </div>
    <div class="column">
        <p style="margin-bottom:2mm; margin-top:2mm;"><a href="https://inspirehep.net/literature/1822188" style="font-size: 16pt;">[2] Kallweit, Sotnikov, Wiesemann '20</a></p>
        <p style="margin-bottom:2mm; margin-top:2mm;"><a href="https://inspirehep.net/literature/1838380" style="font-size: 16pt;">[4] Chawdhry, Czakon, Mitov, Poncelet '20</a></p>
    </div>
</div>

<div style="font-size: x-large; float: center; margin-bottom: -4mm;">
This talk: $pp\rightarrow jjj$, i.e. $\{0\rightarrow ggggg$, $0\rightarrow q\bar qggg$, $0\rightarrow q\bar qQ\bar Q g\}$
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: xxx-large; margin-bottom:0mm;"> Color Algebra </b>
     <p style="margin-top: -2mm; margin-bottom: 2mm; font-size: 16pt;">
     ($q\bar qQ\bar Q g$ example)
     </p>
</div>

<div style="font-size: x-large; float: left; margin-bottom: -4mm;">
$\circ$ Color decomposition (trace basis)
</div><br>
<div style="width:60%; float: left; display: inline-block;">
     <div style="font-size: 12pt; margin-top: -2mm; margin-bottom: 0mm">
          \[
          \require{color}
          \require{amsmath}
          \hspace{-5mm}
          \begin{align}
               \mathcal{A}_{\vec{a}}(1_u,2_{\bar u},3_d,4_{\bar d},5_g) &= 
               \sum_{\sigma \in \mathcal{Z}_2(\{1,2\},\{3,4\})} \sigma\Big(
               \delta^{\bar i_4}_{i_1} (T^{a_5})^{\,\bar i_2}_{i_3} 
               \; A_{d}(1,2,3,4,5)\Big) \; + \\[2mm]
               & \quad \sum_{\sigma \in \mathcal{Z}_2(\{1,2\},\{3,4\})} \kern-2mm \sigma\Big(
               \delta^{\bar i_2}_{i_1} (T^{a_5})^{\,\bar i_4}_{i_3} 
               \; A_{s}(1,2,3,4,5)\Big)\,,\kern-1mm
          \end{align}
          \]
     </div>
</div>

<div style="width:40%; float: right; display: inline-block; margin-top: -8mm;">
     <img src="4q1g-diags-transparent.png"; style="max-width:270px; float:center; border:none; margin-top: 0mm; margin-bottom: -6mm; margin-left: 0mm;">
</div>

<br><br>

<div style="font-size: x-large; float: left; margin-bottom: -4mm; magin-top:-4mm;">
$\circ$ $N_c^{n_c}$ & $N_f^{n_f}$ expansion, notation $A^{(L),(n_c, n_f)}_{\text{partial}}$, <span style="color: red"> red </span> = new
</div><br>
<div style="font-size: 14pt; margin-top: -2mm; margin-bottom: 0mm">
     \[
     \begin{gather}
          A_d^{(2)} = N_c^2 A_d^{(2),(2,0)} + {\color{red} A_d^{(2),(0,0)}} + \frac{1}{N_c^2} {\color{red} A_d^{(2),(-2,0)}}
               +  N_f N_c A_d^{(2),(1,1)} + \frac{N_f}{N_c} {\color{red} A_d^{(2),(-1,1)}} + N_f^2  A_d^{(2),(0,2)} \, , \\
          A_s^{(2)} = N_c {\color{red} A_s^{(2),(1,0)}}+\frac{1}{N_c}{\color{red} A_s^{(2),(-1,0)}}+\frac{1}{N_c^3}{\color{red} A_s^{(2),(-3,0)}}
               + N_f{\color{red} A_s^{(2),(0,1)}} + \frac{N_f}{N_c^2} {\color{red} A_s^{(2),(-2,1)}} + \frac{N_f^2}{N_c}{\color{red} A_s^{(2),(-1,2)}} \, .
     \end{gather}
     \]
</div>

<div style="font-size: x-large; float: left; margin-bottom: 6mm;">
$\circ$ New identities among partials (plus two more for the $n_f = 1$ partials) 
</div>
<div style="font-size: 14pt; margin-bottom: 4mm; magin-top: 6mm;">
     \[\\[2mm]
     \Big\{ \big[ 16 \, A^{(2),(2,0)}_d\, (1,2,3,4,5) 
          + 4 \, A^{(2),(0,0)}_d\, (1,2,3,4,5) + 
          A^{(2),(-2,0)}_d(1,2,3,4,5) \big]
          - \big[\dots \big]_{3 \leftrightarrow 4} \Big\}
          - \Big\{ \dots \Big\}_{1 \leftrightarrow 2} = 0 \, .
     \]
</div>
<div style="font-size: 14pt; margin-top: 8mm; margin-bottom: 0mm">
     \[
     \begin{gather}
          \big[  32 \, A^{(2),(2,0)}_d\, (1,2,3,4,5) + 8 \, A^{(2),(0,0)}_d\, (1,2,3,4,5) + 2 A^{(2),(-2,0)}_d(1,2,3,4,5) \\
               + 16 \, A^{(2),(1,0)}_s\, (1,2,3,4,5) \, + 4 A^{(2),(-1,0)}_s(1,2,3,4,5) + A^{(2),(-3,0)}_s (1,2,3,4,5) \big]
               - \big[ \dots \big]_{3 \leftrightarrow 4}=  0 \, .
     \end{gather}
     \]
</div>

---


<div style="display: flex; justify-content: center;">
    <div style="margin: 0 10px;">
        <div style="margin-top: 2mm; margin-bottom: 4mm">
          <b style="font-variant: small-caps; font-size: xxx-large"> Motivation</b>
        </div>
        <div style="font-size: 16pt;">
        3 is not that big! And certainly not close to $\infty$
        </div>
        <img src="correction_sizes_catani.png" style="max-width:600px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
        <div style="font-size: 16pt; margin-bottom: 2mm;">
        Slc contributions to $pp\rightarrow jjj$ should be similar to blue curve.
        </div>
        <div style="font-size: 16pt; margin-bottom: 2mm;">
        Expect $\mathcal{O}(10\%)$ effect on duble-virtual hard function.
        </div>
        <div style="font-size: 16pt;">
        Effect on $\sigma^{\text{NNLO}}$ depends on size of $\mathcal{H}^{(2)}$ in the chosen scheme!
        </div>
    </div>
    <div style="margin: 0 10px;">
        <div style="margin-top: 2mm; margin-bottom: 4mm">
          <b style="font-variant: small-caps; font-size: xxx-large"> Pheno. Goal</b>
        </div>
        <div style="font-size: 16pt; margin-bottom:2mm;">
        Stable and fast evaluations
        </div>
        <img src="h2_5g.png" style="max-width:590px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
        <div style="font-size: 16pt; margin-bottom:-4mm;">
        <code> C++ </code> Code available at
        </div>
        <a href="https://gitlab.com/five-point-amplitudes/FivePointAmplitudes-cpp" style="font-size: 16pt;">gitlab.com/five-point-amplitudes/FivePointAmplitudes-cpp</a>
        <div style="font-size: 16pt; margin-bottom:-4mm;">
        Analytics available at
        </div>
        <a href="https://zenodo.org/records/10142295" style="font-size: 16pt;">zenodo.org/records/10142295</a> <span style="font-size: 16pt">&</span>
        <a href="https://zenodo.org/records/10231547" style="font-size: 16pt;">zenodo.org/records/10231547</a>
    </div>
</div>

</section>

---

<section>

{{< slide background-image="Feynman-Diagrams-transparent.png" >}}

<h1 style="margin-top: -2mm;"> Numerical Computation </h1>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Partial Amplitudes </b>
 
<div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 0mm;">
     $\circ$ Amplitude (integrands) can be written as (drop the extra sub- and super-scripts)
</div>
<br>
<div style="font-size: 16pt; margin-top: 0mm;  margin-bottom: 0mm">
     $$
     \displaystyle A(\lambda, \tilde\lambda, \ell) =
\sum_{\substack{\Gamma,\\ i \in M_\Gamma \cup S_\Gamma}} \, c_{\,\Gamma,i}(\lambda, \tilde\lambda, \epsilon) \,		\frac{m_{\Gamma,i}(\lambda\tilde\lambda, \ell)}{\textstyle \prod_{j} \rho_{\,\Gamma,j}(\lambda\tilde\lambda, \ell)} \;\; \xrightarrow[]{\int d^D\ell} \;\; \sum_{\substack{\Gamma,\\ i \in M_\Gamma}} {\color{red}c_{\,\Gamma, i}}(\lambda, \tilde\lambda, \epsilon) \, {\color{orange}I_{\Gamma, i}}(\lambda\tilde\lambda, \epsilon)
$$  
</div>

<br>

<div style="font-size: x-large; float: left; margin-top: -12mm; margin-bottom: 0mm;">
     $\circ$ For a suitable choice of integrands, we get:
</div>
<br>
<div style="font-size: 16pt; margin-top: -15mm; margin-bottom: 0mm">
     $$
     \displaystyle
     {\color{red}c_{\Gamma, i}}(\lambda, \tilde\lambda, \epsilon) = \frac{ \sum_{k=0}^{\text{finite}} \, {\color{red}c^{(k)}_{\,\Gamma, i}}(\lambda, \tilde\lambda) \, \epsilon^k}{\prod_j (\epsilon - a_{ij})} \;, \;\;\text{with} \quad a_{ij} \in \mathbb{Q} \, . 
     $$
</div>

<br>

<div style="font-size: x-large; float: left; margin-bottom: 0mm; margin-top: -10mm;">
     Some notation:
</div>
<br>
<div style="font-size: x-large; float: center; margin-bottom: 0mm; margin-top: -10mm;">
     $\circ$  $\Gamma$: topologies $\quad\circ$ $M_\Gamma$: master integrands $\quad\circ$ $S_\Gamma$: surface terms $\quad\circ$ $D = 4 - 2 \epsilon$
</div>
<div style="font-size: x-large; float: center; margin-bottom: 0mm; margin-top: 2mm;">
     $\circ$ Spinors: $\lambda_i = |i\rangle, \tilde\lambda_i =[i|$
     $\quad\circ$ External 4-momenta: $\lambda\tilde\lambda=p\kern-3mm/$
     $\quad\circ$ Loop $D$-momenta: $\ell $
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large; magin-bottom:-2mm;"> Numerical Generalized Unitarity @ 2 Loops </b>
<a style="font-size: large; text-align: center; float: center; margin-right: 0mm; margin-top: -2mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1510.05626>
     Ita ('15)
</a>
<a style="font-size: large; text-align: center; float: center; margin-left:2mm; margin-right: 0mm; margin-top: -2mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1712.03946>
     Abreu, Febres Cordero, Ita, Page, Zeng ('17)
</a>

<div style="font-size: x-large; float: left; margin-bottom: 0mm; margin-top: 2mm;">
$\circ$ The integrand Ansatz is matched to products of trees on cuts
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: x-large; width:75%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     $$
	     \require{color}
	     \displaystyle \sum_{\text{states}} \, \prod_{\text{trees}} A^{\text{tree}}(\lambda, \tilde\lambda, \ell)\big|_{\text{cut}_{\Gamma}} = \sum_{\substack{\Gamma' \ge \Gamma, \\ i \in M_\Gamma' \cup S_\Gamma'}} \kern-2mm c_{\,\Gamma',i}(\lambda, \tilde\lambda) \, \frac{m_{\Gamma',i}(\lambda\tilde\lambda, \ell)}{\displaystyle \prod_{j\in P_{\Gamma'} / P_{\Gamma}} \rho_{j}(\lambda\tilde\lambda, \ell)}\Bigg|_{\text{cut}_\Gamma}
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
     <div style="font-size: x-large; width:75%; float: left; text-align: center; display: inline-block; margin-top: 5mm;">
	     $\star$ Numerical Berends-Giele recursion for LHS, solve for coeffs. in RHS.
	</div>
     <div style="font-size: x-large; width:75%; float: left; text-align: center; display: inline-block; margin-top: 5mm;">
	     $\star$ IBP reduction = decomposition on RHS, $\; m_{\Gamma,i} \in M_\Gamma \cup S_\Gamma $
	</div>
</div>

<div style="font-size: x-large; float: left; margin-bottom: 0mm; margin-top: 8mm;">
$\circ$ The SLC cut-hierarchy is significantly larger than the LC one, e.g.
</div>
<div>
<img src="NbrOfDiagramsTable-transparent.png"; style="max-width:800px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Finite Remainders </b>

<!---
<div style="text-align: left; font-size: x-large; float: left; margin-bottom: 10mm; margin-top: 10mm">Decomposition in terms of <b> master integrals </b> </div>
<a style="font-size: large; text-align: right; float: right; margin-bottom: 5mm; margin-top: 10mm" href=https://arxiv.org/abs/0712.1851>Ellis, Zanderighi</a>
<a style="font-size: large; text-align: right; float: right; margin-bottom: 5mm; margin-top: 10mm" href=https://arxiv.org/abs/hep-ph/9212308>Bern, Dixon, Kosower;&nbsp</a>
<a style="font-size: large; text-align: right; float: right; margin-bottom: 5mm; margin-top: 10mm" href=https://www.sciencedirect.com/science/article/pii/0550321379906059?ref=pdf_download&fr=RR-2&rr=7c4afcac1f343b58>'t Hooft, Veltman;&nbsp</a>

<div style="font-size: x-large; margin-top: 10mm;">
$$A^{1-\text{loop},D=4}_{n} = \sum_i \color{orange}{d_i} \color{red}{I^i_{Box}} + \sum_i \color{orange}{c_i} \color{red}{I^i_{Triangle}} + \sum_i \color{orange}{b_i} \color{red}{I^i_{Bubble}} + \sum_i \color{orange}{a_i} \color{red}{I^i_{Tadpoles}} + \color{orange}{R}$$
</div>

<div style="width:90%; float: center; display: inline-block;">
       <img src="one-loop-decomposition-transparent.png"; style="max-width:750px;float:center;border:none;margin-top:-5px;">
</div>
--->

<div style="text-align: left; font-size: x-large; margin-bottom: 5mm;">
     $\circ$ Dim-reg is great, but it also introduces <b>a lot</b> of junk (see next slide).
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 5mm;">
     $\circ$ <u>All physical information</u> is contained in the <i>finite remainder</i>, at two loops
</div>

<div style="font-size: x-large; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\underbrace{\mathcal{R}^{(2)}}_{\text{finite remainder}} = \mathcal{A}^{(2)}_R \underbrace{- \quad I^{(1)}\mathcal{A}^{(1)}_R \quad - \quad I^{(2)}\mathcal{A}^{(0)}_R}_{\text{divergent + convention-dependent finite part}} + \mathcal{O}(\epsilon)
$$
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 0mm;">
     $\phantom{\circ}$ $\mathcal{A}^{(1)}_R$ to order $\epsilon^2$ is still needed to build $\mathcal{R}^{(2)}$, but there is no reason to reconstruct it
</div>
<div style="text-align: right; float: right; font-size: 11pt; margin-bottom: 1mm;">
     Although by the time I learned this, I had already reconstructed $\mathcal{A}^{(1)}_{5g}$ to $\epsilon^2$ $\qquad$
</div>

<br>

<div style="text-align: left; font-size: x-large; margin-bottom: 5mm;">
     $\circ$ Finite remainder as a weighted sum of <i>pentagon functions</i> <a style="font-size: large; display: inline-block; text-align: right; float: right; margin-top: 2mm; margin-left: 4mm; " href=https://arxiv.org/abs/2009.07803> Chicherin, Sotnikov ('20);&nbsp; </a>
</div>

<div style="font-size: x-large; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\textstyle \mathcal{R}(\lambda, \tilde\lambda) = \sum_i \color{orange}{r_{i}(\lambda,\tilde\lambda)} \, \color{red}{h_i(\lambda\tilde\lambda)}
$$
</div>

<div style="border: 2px solid black; font-size: x-large; padding: 10px; display: inline-block; margin-top: 0mm; margin-right: 10mm; margin-bottom: 7mm;">
    Goal: Reconstruct $\color{orange}{r_{i}(\lambda,\tilde\lambda)}$ from $\mathbb{F}_p$ samples
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: 0mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/1406.4513>
von Manteuffel, Schabinger ('14)
</a><br>
<a style="font-size: large; text-align: right; float: right; margin-top: -10mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1608.01902>
Peraro ('16)
</a>

<div style="text-align: left; font-size: x-large; margin-bottom: 5mm;">
     $\circ$ More precisely, we would like a basis of the vector space $\text{span}(r_i(\lambda,\tilde\lambda))$ <br>
     $\phantom{\circ}$ (given a basis, obtaining the full set is easy).
</div>

</section>

---

<section >

{{< slide background-image="varieties-no-background.png" >}}

<br><br><br><br>

# Analytic and Geometric Structure

<br><br><br><br>

based on: <br>
[GDL, Page (JHEP 12 (2022) 140)](https://arxiv.org/abs/2203.04269) <br>
GDL, Ita, Page, Sotnikov (to appear)

---

<b style="font-variant: small-caps; font-size: 33pt;"> Fieds of Fractions of Polynomial Quotient Rings  </b>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: x-large; width:50%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     <div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 1mm;">
               $\circ$ Covariant q-ring of spinors
          </div>
          <br>
          <div style="font-size:16pt; float: left; margin-top: 1mm; margin-bottom: 0mm">
               $$\displaystyle \kern10mm R_n = \mathbb{F}\big[|1⟩, [1|, \dots, |n⟩, [n|\big] \big/ \big\langle \sum_i |i⟩[i| \big\rangle$$
          </div>
          <div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 1mm;">
               $\circ$ Lorentz invariants live in a sub-ring of $R_n$
          </div>
          <br>
          <div style="font-size:16pt; float: left; margin-top: 1mm; margin-bottom: 0mm">
               $$\displaystyle \kern0mm R_n \supset \mathcal{R}_n = \mathbb{F}\big[⟨1|2⟩, \dots, [n-1|n]\big] \big/ (\mathcal{J}_n + \mathcal{K}_n + \bar{\mathcal{K}}_n)$$
          </div>
          <div style="font-size:15pt; float: left; margin-top: 0mm; margin-bottom: 1mm;">
               where $\mathcal{J}_n$: momentum cons., $\;\stackrel{\tiny{(}\normalsize{-}\tiny{)}}{\mathcal{K}}_n$: shouten identities 
          </div>
	</div>
     <div style="width:50%; float: right; display: inline-block; margin-top: 0mm;">
          <img src="stability_mandel_spinor.png"; style="max-width:500px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
          <div style="width:100%; font-size: 14pt; margin-top: -2mm; margin-bottom: 1mm;">
               Plot from LC $pp\rightarrow \gamma\gamma\gamma$ remainder in Born kinematics.
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 1mm; margin-bottom: 1mm;">
               The slopes <i>flatten out</i> in soft/collinear configurations.
          </div>
     </div>
</div>

<div style="border: 2px solid black; font-size: x-large; padding: 10px; display: inline-block; margin-top: 8mm;">
    $r_i(\lambda, \tilde\lambda)$ at $n$-point belong to the Field of Fractions of $\mathcal{R}_{n>3}$
</div>

<br>

<div style="float:left; font-size: x-large; margin-top: 8mm; margin-bottom: 1mm;">
     $\circ$ This allows to manifes:
</div>
<div style="float:left; font-size: 16pt; margin-top: 1mm; margin-bottom: 1mm;">
     $\kern8mm$ 1) that the singularities are $\approx \sqrt{s_{ij}}\kern10mm$ 2) the behaviour with $P^\mu \in \mathbb{C}$, i.e. away from $\langle ij \rangle = [ij]^{\ast}$
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: xxx-large"> Least Common Denominator </b>
     <p style="margin-top: -2mm; margin-bottom: 2mm; font-size: 18pt;">
     (i.e. what happens at codimension one)
     </p>
</div>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: x-large; width:60%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     <div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 1mm;">
                $\circ\,$ The rational coefficients take the form
          </div>
          <br>
          <div style="font-size:16pt; float: left; margin-top: 1mm; margin-bottom: 0mm">
               $$
               \displaystyle r_i(|i\rangle,[i|) = \frac{\mathcal{N}(|i\rangle,[i|)}{\prod_j D_j^{q_{ij}}(|i\rangle,[i|)}
               $$
          </div>
          <div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 1mm;">
               $\circ\,$ The $\mathcal{D}_j$ are related to the letters of the symbol alphabet
          </div>
          <br>
          <a style="font-size: large; text-align: right; float: right; margin-top: 0mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1812.04586>
          Abreu, Dormans, Febres Cordero, Ita, Page ('18)
          </a>
          <div style="font-size:16pt; float: left; margin-top: 1mm; margin-bottom: 0mm">
               $$
               \displaystyle \{\mathcal{D}_{\{1,\dots,35\}}\} = \bigcup_{\sigma \; \in \; \text{Aut}(R_5)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1] \big\}
               $$
          </div>
          <div style="font-size:15pt; float: left; margin-top: 0mm; margin-bottom: 1mm;">
               $\qquad\color{green}\text{Identical to 1-loop!}$
          </div>
	</div>
     <div style="width:40%; float: right; display: inline-block; margin-top: 0mm;">
          <img src="V2.png"; style="max-width:300px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
          <div style="width:100%; font-size: 14pt; margin-top: -2mm; margin-bottom: 1mm;">
               The codimension one variety 
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 1mm; margin-bottom: 1mm;">
               $\langle x^3 + y^3 - z^2 \rangle$ in $\mathbb{R}[x,y,z]$
          </div>
     </div>
</div>


<div style="text-align: left; font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\phantom{\circ}$ Non-trivial statement (not proven!): all irreducible polynomials generate prime ideals, @ 5-pt.
</div>


<div style="border: 2px solid black; font-size: x-large; padding: 10px; display: inline-block; margin-top: 5mm;">
    Poles & Zeros $\;\Leftrightarrow\;$ Irreducible Varieties $\;\Leftrightarrow\;$ Prime Ideals <br>
    <i style="font-size: 12pt; border-top: -8mm; border-bottom: -2mm;"> Physics $\kern38mm$ Geometry $\kern38mm$ Algebra </i>
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: xxx-large"> Partial Fraction Decompositions </b>
     <p style="margin-top: -2mm; margin-bottom: 2mm; font-size: 18pt;">
     (i.e. what happens at codimension greater than one)
     </p>
</div>

<div style="display: flex;">
    <div style="flex: 1;">
        <img src="V1.png" style="max-width:60%; height:auto;">
    </div>
    <div style="flex: 1; max-width:5%; margin-top:20mm;">
        $\cap$
    </div>
    <div style="flex: 1;">
        <img src="V2.png" style="max-width:60%; height:auto;">
    </div>
    <div style="flex: 1; max-width:5%; margin-top:20mm;">
        $=$
    </div>
    <div style="flex: 1;">
        <img src="V3.png" style="max-width:60%; height:auto;">
    </div>
</div>

</section>

---

<section>

{{< slide background-image="spinor_coeffs.png" >}}

# Analytic Reconstruction

---

<b style="font-variant: small-caps; font-size: xxx-large"> Vector Spaces of Rational Functions </b>


<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ\,$ Sort the $r_i$ by mass dimension of $\mathcal{N}$ ($\approx$ Ansatz size), pick simplest subset forming a basis $r_{i \in \mathcal{B}}$
</div><br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -8mm; margin-bottom: -2mm;">
     $$
     R = r_j h_j = r_{i\in \mathcal{B}} M_{ij} h_j \, , \qquad M_{ij} \in \mathbb{Q}
     $$
</div>
<div>
<img src="ReconstructionComplexity.png"; style="max-width:650px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
</div>


<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ Key insight: 
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -4mm; margin-bottom: 5mm;">
     $$
     \text{dim(span}_{FF(R_5), \mathbb{Q}}\left(\lim_{\mathcal{D_j} \rightarrow  0 }r_{i}\right)) \leq \text{dim(span}_{FF(R_5), \mathbb{Q}}(r_{i}))
     $$
</div>
<div style="text-align: left; font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\phantom{\circ}\,$ I.e., the <span style="color: red">pole residues are correlated</span>, build linear combinations that <i> ''remove the overlap'' </i>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Correlation of Residues </b>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ\,$ Build Laurent expansions around $t_{\mathcal{D}_k}$ <span style="font-size: 12pt"> Univariate Tiele Tiziano, Ben's Lecture Notes, p(z)-adic expansion</span>
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -5mm; margin-bottom: 5mm;">
     $$
     r_{i \in \mathcal{B}} = \sum_{m = 1}^{q_k = \text{max}_i(q_{ik})} \frac{e^k_{im}}{(t-t_{\mathcal{D}_k})^m} + \mathcal{O}((t-t_{\mathcal{D}_k})^0)
     $$
</div>
<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\phantom{\circ}\,$ strictly formal over $\mathbb{F}_p$, but convergent over $\mathbb{Q}_p$ for $(t-t_{\mathcal{D}_k}) \propto p$
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: -5mm;">
     $\circ\,$ Repeat for several (anti-)holomorphic slices, build vectors
</div>
<br><br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -5mm; margin-bottom: 0mm;">
     $$
     \vec{e}^k_{im} = (e^k_m)_{ij} = \{ e^k_{im}(\text{slice}_1), \dots, e^k_{im}(\text{slice}_n)  \}
     $$
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ By Gaussian elimination on the matrix $(e^k_m)_{ij}$ we can partition the space:
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 5mm;">
     $$
     \text{span}_{\vec{\mathbb{Q}},\mathbb{Q}}(r_{i \in \mathcal{B}}) = \text{column}_{\vec{\mathbb{Q}},\mathbb{Q}}(\text{Res}(r_{i \in \mathcal{B}}, D_k^m)) \oplus \text{null}_{\vec{\mathbb{Q}},\mathbb{Q}}(\text{Res}(r_{i \in \mathcal{B}}, D_k^m))
     $$
</div>

<div style="border: 2px solid black; font-size: x-large; padding: 10px; display: inline-block; margin-top: 0mm;">
    Interpretation of $\text{null}_{\vec{\mathbb{Q}},\mathbb{Q}}(\text{Res}(r_{i \in \mathcal{B}}, D_k^m)) \cdot r_{i \in \mathcal{B}}$: functions that do <u>not</u> have a $D_k^m$ singularity
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Breadth-First Search </b>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ If a function $\tilde{r}$ does not have poles $D_{k_1}^{m_1}$ and $D_{k_2}^{m_2}$, then
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 5mm;">
     $$
     \tilde{r} \in \text{span}_{FF(R_5),\mathbb{Q}}\Bigg[\Big(\text{null}_{\vec{\mathbb{Q}},\mathbb{Q}}(\text{Res}(r_{i \in \mathcal{B}}, D_{k_1}^{m_1})) \cap \text{null}_{\vec{\mathbb{Q}},\mathbb{Q}}(\text{Res}(r_{i \in \mathcal{B}}, D_{k_2}^{m_2}))\Big)_{i'i} \; \cdot \; r_{i\in \mathcal{B}}\Bigg]
     $$
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ Build linear combination that remove as many singularities as possible, without dropping rank
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 5mm;">
     $$
     \displaystyle O_{i'i} = \cap_{k, m} \, \text{nulls}_{\vec{\mathbb{Q}},\mathbb{Q}} \qquad \text{(schematically)}
     $$
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ This is done by searching a tree of possibilities of which pole gets dropped to which order. <br>
     $\phantom{\circ}\,$ Several optimizations required to search an otherwise proibitively large space, naively of size
</div>
<br><br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -5mm; margin-bottom: 5mm;">
     $$
     \prod_k (m_k + 1) \quad \text{with } \; k \;\text{ enumerating } \; D_k^{m_k}
     $$
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Least Least-Common-Denominator </b>
<br>

<div style="text-align: left; font-size: x-large; margin-bottom: 2mm; margin-top: 5mm;">
     $\circ$ In other words, we have reshuffled the $r_i$ by linear combinations of the others $r_{j\neq i}$
</div>
<div style="text-align: center; float:center; display: inline-block; font-size: x-large; margin-bottom: 2mm; margin-top: 2mm;">
     $\displaystyle \tilde{r}_i = \sum_{j\neq i} O_{ij} r_j + r_i$
</div>

<br>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ The rational functions now take the form
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -5mm; margin-bottom: 5mm;">
     $$
     \displaystyle \tilde{r}_i(|i\rangle,[i|) = \frac{\tilde{\mathcal{N}}(|i\rangle,[i|)}{\prod_j D_j^{\tilde{q}_{ij}}(|i\rangle,[i|)}
     $$
</div>
<div style="text-align: left; font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\phantom{\circ}\,$ where we have minimized $\sum_j \tilde{q}_{ij}$, compared to the $r_i$.
</div>

<br>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ This is the closest thing that I am aware of to a Gram–Schmidt procedure for vector spaces over fields that are not number fields, but in this case fields of fractions over polynomial quotient rings.
</div>

<div style="text-align: left; font-size: x-large; float: left; margin-top: 5mm; margin-bottom: 2mm;">
     $\circ\,$ Can we think of this as defining an inner product on the space of rational functions?
</div>
<br><br><br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -8mm; margin-bottom: 0mm;">
     $$
     O_{ij} \sim \langle r_i | r_j \rangle \qquad \text{(very schematically)}
     $$
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Spinor-Helicity Results </b>
<br>

<div>
<img src="VSSizeTable-transparent.png"; style="max-width:350px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ For the first time with an MHV two-loop five-point amplitude the results for the rational coefficients are compact enough to be present within a paper
</div>

https://arxiv.org/pdf/2311.10086.pdf#page=14

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The simplification of the basis change is <u>independent</u> of that obtained from partial fraction decompositions, as the latter can still be performed after the former.
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ Can now study propertities of the amplitude <br>
     $\phantom{\circ}$ e.g. no function has a $\text{tr}_5$ singularity, nor a pair of $\langle i | j + k | i]$ in the same denominator.
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Quarks from Gluons </b>
<br>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ Checking whether a rational function belongs to a given vector space
</div>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 0mm;">
     $$
     r_{\text{guess}} \stackrel{?}{\in} \text{span}_{FF(R_5), \mathbb{Q}}(r_{i})
     $$
</div>
<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\phantom{\circ}$ is much simpler problem than performing a rational reconstruction! <br>
     $\phantom{\circ}$ It only requires as many evaluations as the dimension of the vector space.
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The vector space has uniform mass dimension and phase weights
</div>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 0mm;">
     $$
     |i⟩ \rightarrow t^{1/2}|i⟩, \; |i] \rightarrow t^{1/2}|i] \quad \forall \; i \quad \text{and} \quad
     |i⟩ \rightarrow t|i⟩, \; |i] \rightarrow \frac{1}{t}|i]
     $$
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ Generate guesses for quark functions by re-scaling gluon functions
</div>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 0mm;">
     $$
     \tilde{r}^{-}_{73}(q^+,q^-,g^+,g^+,g^-) = \frac{[14]⟨25⟩⟨45⟩}{⟨24⟩[24]⟨34⟩^2} = \frac{⟨14⟩}{⟨24⟩} \underbrace{\frac{[14]⟨25⟩⟨45⟩}{⟨14⟩[24]⟨34⟩^2}}_{r^{--}_{18}(g^+,g^-,g^+,g^+,g^-)}
     $$
</div>
<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 2mm;">
     $\circ$ We obtain most (50% of 2q3g and 90% of 4q1g) quarks functions this way.
</div>


</section>

---

<section>

{{< slide background-image="Wjj_diagrams.png">}}

# Outlook

---

{{< slide background-image="ATLAS2022.png" >}}

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 25mm;"> Status: Two-Loop Five-Point One-Mass Amplitudes </b>

<style>
    table {
        width: 100%;
        border-collapse: collapse;
    }
    th, td {
        border: 1px solid black;
        padding: 8px;
        text-align: center !important;
    }
    th {
        font-size: 20px; /* Adjust the font size for table headers */
    }
    td {
        font-size: 16px; /* Adjust the font size for table data */
    }
    tr:last-child td {
        border-bottom: 1px solid black; /* Add border to bottom of last row */
    }
</style>

<table>
    <thead>
        <tr>
            <th style="font-size: 24px;">Process</th>
            <th style="font-size: 24px;">Analytical Amplitudes</th>
            <th style="font-size: 24px;">Numerical Codes</th>
            <th style="font-size: 24px;">Cross Sections</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow Wb\bar b$</td>
            <td style="font-size: 20px;">[3, 4, 5]</td>
            <td style="font-size: 20px;">[3, 5]</td>
            <td style="font-size: 20px;">[1, 2]</td>
        </tr>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow Hb\bar b$</td>
            <td style="font-size: 20px;">Row 1, Column 1</td>
            <td style="font-size: 20px;">Row 1, Column 2</td>
            <td style="font-size: 20px;">Row 1, Column 3</td>
        </tr>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow Wj\gamma$</td>
            <td style="font-size: 20px;">Row 2, Column 1</td>
            <td style="font-size: 20px;">Row 2, Column 2</td>
            <td style="font-size: 20px;">Row 2, Column 3</td>
        </tr>
        <tr>
            <td style="font-size: 20px;">$pp \rightarrow Wjj$</td>
            <td style="font-size: 20px;">Row 3, Column 1</td>
            <td style="font-size: 20px;">Row 3, Column 2</td>
            <td style="font-size: 20px;">Row 3, Column 3</td>
        </tr>
        <tr>
        </tr>
    </tbody>
</table>

<br><br>

<style>
    .two-col {
        display: flex;
        justify-content: center;
    }
    .column {
        flex: 1;
        padding: 10px;
        margin: 0 10px;
        text-align: left;
    }
</style>
<div class="two-col">
    <div class="column">
        <p style="margin-bottom:2mm; margin-top:2mm;"><a href="https://inspirehep.net/literature/1762583" style="font-size: 16pt;">[1] ... '19</a></p>
    </div>
    <div class="column">
        <p style="margin-bottom:2mm; margin-top:2mm;"><a href="https://inspirehep.net/literature/1822188" style="font-size: 16pt;">[2] ... '20</a></p>
    </div>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large; margin-bottom: 5mm;">
  5-point 1-mass Amplitudes: e.g. Wjj
</b>

<div style="text-align: left; font-size: x-large; margin-top: 5mm;">
     $0.\,$ Start from analytics of <a style="font-size: large"; href="https://arxiv.org/abs/2110.07541">Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov ('21) </a> - 1.2GB of <code>C++</code> source code.
</div>

<div style="text-align: left; font-size: x-large; margin-top: 5mm; margin-bottom: 5mm;">
     $1.\,$ Script to split up the expressions, and compile them ($\sim 20$GB binaries) for evaluation over $\mathbb{F}_p$;
</div>

<div style="text-align: left; font-size: x-large; margin-top: 5mm; margin-bottom: 5mm;">
$2.\,$ Recombine the 3 projections $p_V \parallel p_1, p_V \parallel p_2, p_V \parallel p_3$ and reintroduce the little group factors <br> 
to build 6-point spinor-helicity amplitudes (subject to degree bounds on $|5\rangle,[5|,|6\rangle,[6|$); <br>
</div>

<div style="text-align: left; font-size: x-large; margin-top: 5mm; margin-bottom: 0mm;">
$3.\,$ Perform (rough) PFDs based on expected structures and fit the Ansatze.
</div>

<br>

<div style="text-align: center; float:center; font-size: x-large; margin-top: -12mm; margin-bottom: 5mm;">
Comparison of $p\bar p \rightarrow jjj$ (in full color) to $pp \rightarrow Wjj$ (at leading color):  <br>
</div>

<table width=110% border="1" cellspacing="0" cellpadding="0" style="margin-left: -12mm; margin-bottom: 8mm; margin-top: 8mm; font-size: x-large;">
  <tr>
    <td><b>Kinematics</b></td>
    <td><b># Poles ($W$)</b></td>
    <td><b>LCD Ansatz</b></td>
    <td><b>Partial-Fraction Ansatz</b></td>
    <td><b>Rational Functions</b></td>
  </tr>
  <tr>
    <td style="text-align: center;">5-point massless</td>
    <td style="text-align: center;">35</td>
    <td style="text-align: center;">~200k</td>
    <td style="text-align: center;">~4k</td>
    <td style="text-align: center;">$\sim$200 KB</td>
  </tr>
  <tr>
    <td style="text-align: center;">5-point 1-mass</td>
    <td style="text-align: center;">>200</td>
    <td style="text-align: center;">>5M</td>
    <td style="text-align: center;">$\sim$40k</td>
    <td style="text-align: center; background-color: yellow;">$\sim$25 MB</td>
  </tr>
</table>

<div style="text-align: center; float: center; font-size: x-large; margin-top: 2mm; margin-bottom: 5mm;">
     $\displaystyle \kern-10mm \{W_j\} = \bigcup_{\sigma \; \in \; \text{Aut}(R_6)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1], \langle 1|2+3|4], s_{123}, \Delta_{12|34|56}, ⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2] \big\} $
</div>

---

<b style="font-variant: small-caps; font-size: xx-large; margin-bottom: 10mm;">
   Complexity of 2-loop 5-point 1-mass Amplitudes
</b>

<div style="display:block; width:100%; font-size: 16pt; margin-top: 5mm; margin-bottom: 4mm;">
     <div style="width:50%; float: left; display: inline-block; font-size: x-large;">
          $\circ$ The  Ansatz size grows quickly with <br> multiplicity (m) and mass dimension (d): <br><br>
          $\displaystyle \small \left(\mkern -9mu \begin{pmatrix}\, m(m-3)/2 \, \\ \, d/2 \, \end{pmatrix} \mkern -9mu \right)$ <br><br>
          is a lower bound. <a style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: -28mm; margin-top: 1mm; margin-bottom: 5mm;" href=https://arxiv.org/abs/2010.14525>
               GDL, Maître ('20)
          </a>
     </div>
     <div style="width:50%; float: center; display: inline-block;">
          <img src="AnsatzSizes.png"; style="max-width:320px;float:center;border:none;margin-top:0px;margin-bottom: 5mm;">
     </div>
</div>

<div style="text-align: left; font-size: x-large; margin-top: 1mm; margin-bottom: 2mm;">
$\circ\,$ Compact residues for the new 2-loop (spurious?) pole, $⟨k|j|p\mkern-7.5mu/_V|l|k]-⟨j|i|p\mkern-7.5mu/_V|l|j]$, e.g.:
$$r^{(5 \text{ of } 54)}_{\bar{u}^+g^+g^+d^-(V\rightarrow \ell^+ \ell^-)} = \frac{[12][23]⟨24⟩⟨46⟩^2⟨1|2+3|4]⟨2|1+3|4]}{⟨12⟩⟨23⟩⟨56⟩(⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2])^2}$$
</div>

<div style="text-align: left; font-size: x-large; margin-top: 8mm;">
$\circ\,$ The three mass Grams, $\Delta_{12|34|p_V}, \Delta_{14|23|p_V}$, behave analogously to one-loop amplitudes, e.g.:
</div>
<div style="text-align: left; font-size: large; margin-top: 2mm; margin-bottom: 1mm;">
$$ r^{(73 \text{ of } 120)}_{\bar{u}^+g^-g^+d^-(V\rightarrow \ell^+ \ell^-)} = \frac{105}{128}\frac{⟨2|1+4|3]⟨4|2+3|1]⟨6|1+4|5]s_{14}s_{23}s_{56}{\color{green}(s_{124}-s_{134})}(s_{123}-s_{234})(s_{25}+s_{26}+s_{35}+s_{36})}{{\color{orange}⟨3|1+4|2]}{\color{red}Δ_{23|14|56}^4}} + \\
\Bigg[-6\frac{[12]^2⟨13⟩[25]⟨34⟩⟨36⟩⟨56⟩[56]{\color{green}(s_{124}-s_{134})}}{{\color{orange}⟨3|1+4|2]^5}}\Bigg] + \Bigg[ \; \Bigg]_{1234\rightarrow \overline{4321}}+ \mathcal{O}\left(\frac{1}{⟨3|1+4|2]^{4}Δ_{23|14|56}^{3}}\right)$$
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


{{< slide background-image="EdiCastle.jpg" >}}

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
