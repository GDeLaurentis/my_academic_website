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

# Introduction

---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: -5mm;"> Overview </b>

<div style="display: flex; justify-content: center; margin-top: -3mm;">
    <div style="margin: 0 10px;">
        <img src="LHC_map.jpg" style="max-width:450px; border:none; margin-top: 8.5mm; margin-bottom: 0mm;">
    </div>
    <div style="margin: 0 10px;">
        <img src="ATLAS-XSections-transparent.png" style="max-width:430px; border:none; margin-top: 0mm; margin-bottom: 0mm;">
    </div>
</div>

<div style="text-align: left; font-size: 18pt; float: left; margin-top: -2mm; margin-bottom: 4mm;">
     $\circ\,$ LHC physics program possible also thanks to advancements on many fronts of the theory
</div>

<br>

<div style="display:block; width:100%; margin-top: -5mm;">
  <div style="width:43%; font-size: 14pt; float: left; display: inline-block; margin-left:-12mm;">
       Subtraction <br> <span style="font-size: 12pt; color: green;"> Pikelner, Pedron, Guadagni, Magnea, van Hameren, Vicini, $\dots$</span> <br>
       Renomalization / $\gamma^5$-schemes <br> <span style="font-size: 12pt; color: green;"> Gracey, Heinrich, Weißwange, Kühler, Stöckinger$\dots$</span> <br>
       Feynman Integrals <br> <span style="font-size: 12pt; color: green;"> Chaubey, Behring, Nega, Jones, Page, Broadhurst, $\dots$ <span>
  </div>
  <div style="width:33%; font-size: 14pt; float: right; display: inline-block; margin-right:-10mm;">
       Three / Four / Five Loops  <br> <span style="font-size: 12pt; color: green;"> Bluemlein, Yang, Moch, Schönwald, Maier, $\dots$ </span> <br>
       $\sigma$'s at N$^{(2-3)}$LO <br> <span style="font-size: 12pt; color: green;"> Sotnikov, Neumann, Chen, Mella, Savoini, $\dots$ </span> <br>
       Automation <br> <span style="font-size: 12pt; color: green;"> Lange, Shtabovenko, Zoller$\dots$ </span>
  </div>
  <div style="width:30%; font-size: 14pt; float: right; display: inline-block; margin-left:-8mm;">
       Higgses (<span style="font-size: 14pt">$2 \rightarrow 2$</span> w/ masses) <br> <span style="font-size: 12pt; color: green;"> Zhang, Davies, Kerner, $\dots$ </span> <br>
       Top-quark(s), internal or external<br> <span style="font-size: 12pt; color: green;"> Vitti, Coro, Wang, Magerya, $\dots$ </span> <br>
       Resummation <br> <span style="font-size: 12pt; color: green;"> Novikov, Andersen, Li, $\dots$ </span>
  </div>
</div>

<br><br><br><br>
<div style="text-align: center; float:center; font-size: 15pt; margin-top: -3mm; margin-bottom: 4mm;">
    And much more! Also, lines between various subfields often very blurry!
</div>
<div style="text-align: center; float:center; font-size: 15pt; margin-top: -3mm; margin-bottom: 4mm;">
    This talk: fixed order, 2 loops and 5 legs.
</div>

---

<b style="font-variant: small-caps; font-size: 32pt"> Precision Physics Requires NNLO Corrections </b>

<div style="text-align: left; font-size: 17pt; float: left; margin-top: 5mm; margin-bottom: 4mm;">
     $\circ\,$ K-factors at NNLO can still be large, especially if new channels open up beyond tree, e.g. $\sigma^{\text{NNLO}}_{pp\rightarrow \gamma\gamma\gamma}$
</div>
<div style="display:block; width:100%;">
  <div style="width:50%; float: left; display: inline-block;">
       <img src="1911.00479.crosssection.png"; style="max-width:473px;float:center;border:none;margin-top:0px;margin-bottom:-5mm;">
       <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1911.00479>
       	  Chawdhry, Czakon, Mitov, Poncelet ('19)
       </a>
  </div>
  <div style="width:50%; float: center; display: inline-block;">
       <img src="2010.04681.crosssection.png"; style="max-width:450px;float:center;border:none;margin-top:0px;margin-bottom:-5mm;">
       <a style="font-size: large; text-align: center; float: center; margin-top: -10mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/2010.04681>
       	  Kallweit, Sotnikov, Wiesemann ('20)
       </a>
  </div>
</div>

<div style="text-align: left; font-size: 16pt; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ High-multiplicity two-loop amplitudes required because:
</div> <br>
<div style="display:block; width:100%;margin-top:0mm;">
  <div style="width:100%; font-size: 16pt; float: left; text-align: left; ">
       $\qquad\star$ At high energy, some radiation is more likely than no radiation (resummation disrupts naive $\alpha_s$ counting)
  </div>
  <div style="width:100%; font-size: 16pt; float: left; text-align: left; ">
       $\qquad\star$ As real-virtual(-virtual) contributions to emerging N$^3$LO computations (or N$^2$LO if loop-induced)
  </div>
  <div style="width:100%; font-size: 16pt; float: left; text-align: left; ">
       $\qquad\star$ Some interesting kinematic regions are only accessible with extra radiation (e.g. $p_T$ distributions)
  </div>
</div>


---

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 25mm;"> Status of Two-Loop Five-Point Amplitudes </b>

<style>
    table {
        width: 100%;
        border-collapse: collapse;
    }
    th, td {
        border: 1px solid black;
        padding: 3px;
        text-align: center !important;
    }
    th {
        font-size: 18px; /* Adjust the font size for table headers */
    }
    td {
        font-size: 15px; /* Adjust the font size for table data */
    }
    tr:last-child td {
        border-bottom: 1px solid black; /* Add border to bottom of last row */
    }
    .double-line { 
          border-bottom: 2px double black; /* Adjust the width and color as needed */
    }
</style>

<div style="max-width: 800px; margin: 0 auto;">
<table>
    <thead>
        <tr>
            <th>Process</th>
            <th>Analytical Amplitudes</th>
            <th>Numerical Codes</th>
            <th>Cross Sections</th>
        </tr>
    </thead>
    <tbody>
        <tr class="double-line">
        </tr>
        <tr>
            <td>$pp \rightarrow \gamma\gamma\gamma$</td>
            <td>[3$\kern-2.2mm\phantom{x}^\star$, 4$\kern-2.2mm\phantom{x}^\star$, <b>5</b>]</td>
            <td>[3$\kern-2.2mm\phantom{x}^\star$, <b>5</b>]</td>
            <td>[1$\kern-2.2mm\phantom{x}^\star$, 2$\kern-2.2mm\phantom{x}^\star$]</td>
        </tr>
        <tr>
            <td>$pp \rightarrow \gamma\gamma j$</td>
            <td>[6$\kern-2.2mm\phantom{x}^\dagger$, 7$\kern-2.2mm\phantom{x}^\dagger$, <b>9</b>]</td>
            <td>[6$\kern-2.2mm\phantom{x}^\dagger$]</td>
            <td>[8$\kern-2.2mm\phantom{x}^\dagger$]</td>
        </tr>
        <tr>
            <td>$pp \rightarrow \gamma jj$</td>
            <td>[<b>10</b>]</td>
            <td></td>
            <td>[<b>10</b>]</td>
        </tr>
        <tr>
            <td>$pp \rightarrow jjj$</td>
            <td>[11$^\dagger$, <b>12</b>, <b>13</b>, <b>14</b>]</td>
            <td>[11$^\dagger$,<b>14</b>]</td>
            <td>[15$\kern-2.2mm\phantom{x}^\dagger$]</td>
        </tr>
        <tr class="double-line">
        </tr>
        <tr>
            <td>$pp \rightarrow Wb\bar b$</td>
            <td>[16$\kern-2.2mm\phantom{x}^\dagger$, 17$\kern-2.2mm\phantom{x}^\dagger$]</td>
            <td></td>
            <td>[18$\kern-2.2mm\phantom{x}^\dagger$]</td>
        </tr>
        <tr>
            <td>$pp \rightarrow Hb\bar b$</td>
            <td>[19$^{\dagger\ast}$]</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>$pp \rightarrow Wj\gamma$</td>
            <td>[20$^\star$]</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>$pp \rightarrow Wjj$</td>
            <td>[16$\kern-2.2mm\phantom{x}^\dagger$]</td>
            <td></td>
            <td></td>
        </tr>
        <tr class="double-line">
        </tr>
        <tr>
            <td>$pp \rightarrow ttH$</td>
            <td></td>
            <td></td>
            <td>[21]</td>
        </tr>
        <tr>
        </tr>
    </tbody>
</table>
</div>
<div style="font-size: 14pt; float: center; margin-top: 2mm; margin-bottom: 4mm;">
Legend: <b>bold</b> = full color; $\star$ = planar $\neq$ leading color; $\dagger$ = planar = leading color; $\ast$ = ($y_b \neq 0$, $m_b = 0$)
</div><br>

<style>
    .two-col {
        display: flex;
        justify-content: center;
        margin: 0 auto;
    }
    .column {
        flex: 1;
        width: 50%;
        padding: 1px;
        margin: 0 1px;
        text-align: center;
    }
</style>
<div class="two-col" style="margin-top:-16mm; margin-left:-12mm;margin-right:-12mm;">
    <div class="column">
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1762583" style="font-size: 13pt;">[1] Chawdhry, Czakon, Mitov, Poncelet '19</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1827330" style="font-size: 13pt;">[3] Abreu, Page, Pascual, Sotnikov '20</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2663067" style="font-size: 13pt;">[5] Abreu, GDL, Ita, Klinkert, Page, Sotnikov '23</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1850624" style="font-size: 13pt;">[7] Chawdhry, Czakon, Mitov, Poncelet '21</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1862813" style="font-size: 13pt;">[9] Agarwal, Buccioni, von Manteuffel, Tancredi '21</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1849070" style="font-size: 13pt;">[11] Abreu, Febres Cordero, Ita, Page, Sotnikov</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2723256" style="font-size: 13pt;">[13] GDL, Ita, Klinkert, Sotnikov '23</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1868437" style="font-size: 13pt;">[15] Czakon, Mitov, Poncelet '21'</a></p> <!--- pp->jj - xsection LC --->
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1844767" style="font-size: 13pt;">[17] Badger, Hartanto, Zoia '21</a></p> <!--- pp->Wbb--->
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1896584" style="font-size: 13pt;">[19] Badger, Hartanto, Kryś, Zoia '21</a></p> <!--- pp->Hbb--->
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2165654" style="font-size: 13pt;">[21] Catani, Devoto, Grazzini, Kallweit, Mazzitelli, Savoini '22</a></p> <!--- pp->Hbb--->
    </div>
    <div class="column" style="margin-left:-5mm;">
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1822188" style="font-size: 13pt;">[2] Kallweit, Sotnikov, Wiesemann '20</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1838380" style="font-size: 13pt;">[4] Chawdhry, Czakon, Mitov, Poncelet '20</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1844579" style="font-size: 13pt;">[6] Agarwal, Buccioni, von Manteuffel, Tancredi '21</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1863379" style="font-size: 13pt;">[8] Chawdhry, Czakon, Mitov, Poncelet '21</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2651109" style="font-size: 13pt;">[10] Badger, Czakon, Hartanto, Moodie, Peraro, Poncelet, Zoia '23</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2723232" style="font-size: 13pt;">[12] Agarwal, Buccioni, Devoto, Gambuti, von Manteuffel, Tancredi '23</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2728739" style="font-size: 13pt;">[14] GDL, Ita, Sotnikov '23</a></p>
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/1944964" style="font-size: 13pt;">[16] Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov '21</a></p> <!--- pp->Wjj--->
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2077368" style="font-size: 13pt;">[18] Hartanto, Poncelet, Popescu, Zoia '22</a></p> <!--- pp->Wbb-xsection--->
        <p style="margin-bottom:-3mm; margin-top:-3mm;"><a href="https://inspirehep.net/literature/2008918" style="font-size: 13pt;">[20] Badger, Hartanto, Kryś, Zoia '22</a></p> <!--- pp->Wjy--->  
    </div>     
</div>

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

</section>

---

<section>

{{< slide background-image="Feynman-Diagrams-transparent.png" >}}

<h1 style="margin-top: -2mm;"> Numerical Computation </h1>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Color Algebra in the Trace Basis </b>

<div style="width:60%; float: left; display: inline-block;">
     <div style="font-size: 12pt; margin-top: 0mm; margin-bottom: 0mm">
          \[
          \require{color}
          \require{amsmath}
          \hspace{-5mm}
          \begin{align}
               \mathcal{A}_{\vec{a}}(1_g,2_g,3_g,4_g,5_g) & = \sum_{\sigma \in \mathcal{S}_5/\mathcal{Z}_5} \sigma\Big(\text{tr}(T^{a_1}T^{a_2}T^{a_3}T^{a_4}T^{a_5}) \; A_{1}(1,2,3,4,5)\Big) \; + \\[2mm]
               & \quad \sum_{\sigma\in \frac{\mathcal{S}_5}{\mathcal{Z}_2 \times \mathcal{Z}_3}} \sigma\Big(\text{tr}(T^{a_1}T^{a_2}) \text{tr}(T^{a_3}T^{a_4}T^{a_5}) \; A_{2}(1,2,3,4,5)\Big) + , \\[8mm]
               \mathcal{A}_{\vec{a}}(1_u,2_{\bar u},3_g,4_g,5_g) & =
               \sum_{\sigma \in \mathcal{S}_3(3,4,5)} \sigma\Big(
               (T^{a_3}T^{a_4}T^{a_5})^{\,\bar i_2}_{i_1} \; 
               A_{3}(1,2,3,4,5)\Big) \; + \\[2mm]
               & \quad \sum_{\sigma \in \frac{\mathcal{S}_3(3,4,5)}{\mathcal{Z}_2(3,4)}} 
               \sigma\Big(\text{tr}(T^{a_3}T^{a_4}) (T^{a_5})^{\,\bar i_2}_{i_1} 
               \; A_{4}(1,2,3,4,5)\Big) \; + \\[2mm]
               & \quad \sum_{\sigma \in \frac{\mathcal{S}_3(3,4,5)}{\mathcal{Z}_{3}(3,4,5)}} 
               \sigma\Big(\text{tr}(T^{a_3}T^{a_4}T^{a_5}) \delta^{\bar i_2}_{i_1}
               A_{5}(1,2,3,4,5)\Big) \; , \\[8mm]
               \mathcal{A}_{\vec{a}}(1_u,2_{\bar u},3_d,4_{\bar d},5_g) &= 
               \sum_{\sigma \in \mathcal{Z}_2(\{1,2\},\{3,4\})} \sigma\Big(
               \delta^{\bar i_4}_{i_1} (T^{a_5})^{\,\bar i_2}_{i_3} 
               \; A_{6}(1,2,3,4,5)\Big) \; + \\[2mm]
               & \quad \sum_{\sigma \in \mathcal{Z}_2(\{1,2\},\{3,4\})} \kern-2mm \sigma\Big(
               \delta^{\bar i_2}_{i_1} (T^{a_5})^{\,\bar i_4}_{i_3} 
               \; A_{7}(1,2,3,4,5)\Big)\,,\kern-1mm
          \end{align}
          \]
     </div>
</div>

<div style="width:40%; float: right; display: inline-block; margin-top: -5mm;">
     <img src="5g-diags-transparent.png"; style="max-width:270px; float:center; border:none; margin-top: 0mm; margin-bottom: -4mm; margin-left: 0mm;">
     <br>
     <img src="2q3g-diags-transparent.png"; style="max-width:270px; float:center; border:none; margin-top: 0mm; margin-bottom: -4mm; margin-left: 0mm;">
     <br>
     <img src="4q1g-diags-transparent.png"; style="max-width:270px; float:center; border:none; margin-top: 0mm; margin-bottom: -6mm; margin-left: 0mm;">
</div>

<br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<div style="font-size: x-large; float: center; margin-top:6mm; margin-bottom: 6mm;">
Each $A_{i}$ has an expansion in powers of $\alpha_s$. We consider the $\alpha_s^2$ corrections.
</div>

---

<div style="margin-top: 2mm; margin-bottom: 3mm">
     <b style="font-variant: small-caps; font-size: xxx-large; margin-bottom:0mm;"> Relations among Partials </b>
</div>

<br>

<div style="font-size: x-large; float: left; margin-bottom: 4mm; magin-top:-4mm;">
$\circ$ $N_c^{n_c}$ & $N_f^{n_f}$ expansion, notation $A^{(L),(n_c, n_f)}_{\text{partial}}$, <span style="color: red"> red </span> = new, $0\rightarrow q\bar q Q\bar Q g$ example
</div><br>
<div style="font-size: 14pt; margin-top: -2mm; margin-bottom: 0mm">
     \[
     \begin{gather}
          A_6^{(2)} = N_c^2 A_6^{(2),(2,0)} + {\color{red} A_6^{(2),(0,0)}} + \frac{1}{N_c^2} {\color{red} A_6^{(2),(-2,0)}}
               +  N_f N_c A_6^{(2),(1,1)} + \frac{N_f}{N_c} {\color{red} A_6^{(2),(-1,1)}} + N_f^2  A_6^{(2),(0,2)} \, , \\
          A_7^{(2)} = N_c {\color{red} A_7^{(2),(1,0)}}+\frac{1}{N_c}{\color{red} A_7^{(2),(-1,0)}}+\frac{1}{N_c^3}{\color{red} A_7^{(2),(-3,0)}}
               + N_f{\color{red} A_7^{(2),(0,1)}} + \frac{N_f}{N_c^2} {\color{red} A_7^{(2),(-2,1)}} + \frac{N_f^2}{N_c}{\color{red} A_7^{(2),(-1,2)}} \, .
     \end{gather}
     \]
</div>

<br>

<div style="font-size: x-large; float: left; margin-top:-2mm; margin-bottom: 8mm;">
$\circ$ New identities among partials (plus two more for the $n_f = 1$ partials) 
</div>
<div style="font-size: 14pt; margin-bottom: 4mm; magin-top: 6mm;">
     \[\\[2mm]
     \Big\{ \big[ 16 \, A^{(2),(2,0)}_6\, (1,2,3,4,5) 
          + 4 \, A^{(2),(0,0)}_6\, (1,2,3,4,5) + 
          A^{(2),(-2,0)}_6(1,2,3,4,5) \big]
          - \big[\dots \big]_{3 \leftrightarrow 4} \Big\}
          - \Big\{ \dots \Big\}_{1 \leftrightarrow 2} = 0 \, .
     \]
</div>
<div style="font-size: 14pt; margin-top: 8mm; margin-bottom: 0mm">
     \[
     \begin{gather}
          \big[  32 \, A^{(2),(2,0)}_6\, (1,2,3,4,5) + 8 \, A^{(2),(0,0)}_6\, (1,2,3,4,5) + 2 A^{(2),(-2,0)}_6(1,2,3,4,5) \\
               + 16 \, A^{(2),(1,0)}_7\, (1,2,3,4,5) \, + 4 A^{(2),(-1,0)}_7( 1,2,3,4,5) + A^{(2),(-3,0)}_7 (1,2,3,4,5) \big]
               - \big[ \dots \big]_{3 \leftrightarrow 4}=  0 \, .
     \end{gather}
     \]
</div>

<div style="font-size: 16pt; float: center; margin-top: 10mm; margin-bottom: 6mm;">
These redundancies do not affect the complexity of the calculation (see discussion on vector spaces).
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Partial Amplitudes & Finite Remainders </b>
 
<div style="font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ$ Amplitude (integrands) can be written as (for a suitable choice of master integrals)
</div>
<br>
<div style="font-size: 16pt; margin-top: 0mm;  margin-bottom: 2mm">
     $$
     \displaystyle A(\lambda, \tilde\lambda, \ell) =
\sum_{\substack{\Gamma,\\ i \in M_\Gamma \cup S_\Gamma}} \, c_{\,\Gamma,i}(\lambda, \tilde\lambda, \epsilon) \,		\frac{m_{\Gamma,i}(\lambda\tilde\lambda, \ell)}{\textstyle \prod_{j} \rho_{\,\Gamma,j}(\lambda\tilde\lambda, \ell)} \;\; \xrightarrow[]{\int d^D\ell} \;\; \sum_{\substack{\Gamma,\\ i \in M_\Gamma}} \frac{ \sum_{k=0}^{\text{finite}} \, {\color{red}c^{(k)}_{\,\Gamma, i}}(\lambda, \tilde\lambda) \, \epsilon^k}{\prod_j (\epsilon - a_{ij})} \, {\color{orange}I_{\Gamma, i}}(\lambda\tilde\lambda, \epsilon)
$$  
</div>
<div style="font-size: 15pt; float: center; margin-bottom: 5mm; margin-top: 5mm;">
     $\circ$  $\Gamma$: topologies $\quad\circ$ $M_\Gamma$: master integrands $\quad\circ$ $S_\Gamma$: surface terms 
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 0mm;">
     $\circ$ <u>All physical information</u> is contained in the <i>finite remainders</i>, at two loops
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -3mm; margin-bottom: -3mm;" href=https://inspirehep.net/literature/920274>
Weinzierl ('11)
</a>

<div style="font-size: 16pt; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\underbrace{\mathcal{R}^{(2)}}_{\text{finite remainder}} = \mathcal{A}^{(2)}_R \underbrace{- \quad I^{(1)}\mathcal{A}^{(1)}_R \quad - \quad I^{(2)}\mathcal{A}^{(0)}_R}_{\text{divergent + convention-dependent finite part}} + \mathcal{O}(\epsilon)
$$
</div>

<div style="text-align: left; font-size: 16pt; margin-bottom: 0mm;">
     $\phantom{\circ}$ $\mathcal{A}^{(1)}_R$ to order $\epsilon^2$ is still needed to build $\mathcal{R}^{(2)}$, but there is no real reason to reconstruct it.
</div>

<div style="text-align: left; font-size: x-large; margin-top: 5mm; margin-bottom: 5mm;">
     $\circ$ Finite remainder as a weighted sum of <i>pentagon functions</i> <a style="font-size: large; display: inline-block; text-align: right; float: right; margin-top: 2mm; margin-left: 4mm; " href=https://arxiv.org/abs/2009.07803> Chicherin, Sotnikov ('20);&nbsp; </a>
</div>

<div style="font-size: x-large; margin-top: 5mm; margin-bottom: 5mm">
$$ 
\textstyle \mathcal{R}(\lambda, \tilde\lambda) = \sum_i \color{orange}{r_{i}(\lambda,\tilde\lambda)} \, \color{red}{h_i(\lambda\tilde\lambda)}
$$
</div>

<div style="text-align: left; font-size: x-large; margin-top: 3mm; margin-bottom: 0mm;">
     $\circ$  Goal: reconstruct $\color{orange}{r_{i}(\lambda,\tilde\lambda)}$ from $\mathbb{F}_p$ samples
</div>
<a style="font-size: large; text-align: right; float: right; margin-top: -10mm; margin-bottom: -10mm;" href=https://arxiv.org/abs/1406.4513>
von Manteuffel, Schabinger ('14)
</a><br>
<a style="font-size: large; text-align: right; float: right; margin-top: -18mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1608.01902>
Peraro ('16)
</a>

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

<div style="font-size: x-large; float: left; margin-bottom: 4mm; margin-top: 8mm;">
$\circ$ The SLC cut-hierarchy is significantly larger than the LC one, e.g.
</div>
<div>
<img src="NbrOfDiagramsTable-transparent.png"; style="max-width:800px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
</div>

</section>

---

<section >

{{< slide background-image="varieties-no-background.png" >}}

<br><br><br><br>

# Analytic and Geometric Structure

<br><br><br><br>

based on: <br>
[GDL, Page (JHEP 12 (2022) 140)](https://arxiv.org/abs/2203.04269)

---

<b style="font-variant: small-caps; font-size: 33pt;"> Fieds of Fractions of Polynomial Quotient Rings  </b>

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: -4mm; margin-right: -4mm;">
     <div style="font-size: x-large; width:50%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     <div style="font-size: x-large; float: left; margin-top: 4mm; margin-bottom: 0mm;">
               $\circ$ Starting from polynomials, we have
          </div>
          <div style="font-size: x-large; float: left; margin-top: 0mm; margin-bottom: 1mm;">
               $\phantom{\circ}$ the covariant quotient ring of spinors
          </div>
          <br> 
          <div style="font-size:15pt; float: left; margin-top: 1mm; margin-bottom: 0mm">
               $$\displaystyle \kern10mm R_n = \mathbb{F}\big[|1⟩, [1|, \dots, |n⟩, [n|\big] \big/ \big\langle \sum_i |i⟩[i| \big\rangle$$
          </div>
          <div style="font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 1mm;">
               $\circ$ Lorentz invariants live in a sub-ring of $R_n$
          </div>
          <br>
          <div style="font-size:15pt; float: left; margin-top: 1mm; margin-bottom: 0mm">
               $$\displaystyle \kern4mm R_n \supset \mathcal{R}_n = \mathbb{F}\big[⟨1|2⟩, \dots, [n-1|n]\big] \big/ (\mathcal{J}_n + \mathcal{K}_n + \bar{\mathcal{K}}_n)$$
          </div>
          <div style="font-size:15pt; float: left; margin-top: 0mm; margin-bottom: 1mm;">
               $\phantom{\circ}$ where $\mathcal{J}_n$: momentum cons., $\;\stackrel{\tiny{(}\normalsize{-}\tiny{)}}{\mathcal{K}}_n$: shouten identities 
          </div>
	</div>
     <div style="width:50%; float: right; display: inline-block; margin-top: 0mm; margin-right: -4mm;">
          <img src="stability_mandel_spinor.png"; style="max-width:500px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
          <div style="width:100%; font-size: 14pt; margin-top: -2mm; margin-bottom: 1mm;">
               Plot from LC $pp\rightarrow \gamma\gamma\gamma$ remainder in Born kinematics.
          </div>
          <div style="width:100%; font-size: 14pt; margin-top: 1mm; margin-bottom: 1mm;">
               The slopes <i>flatten out</i> in soft/collinear configurations.
          </div>
     </div>
</div>

<div style="font-size: x-large; padding: 10px; display: inline-block; margin-top: 8mm;"> <!--- border: 2px solid black;  --->
    $r_i(\lambda, \tilde\lambda)$ at $n$-point belong to the field of fractions of $\mathcal{R}_{n>3}$
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
          <br><br>
          <div style="font-size:16pt; float: center; margin-top: -3mm; margin-bottom: 0mm">
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
          <br>
          <div style="font-size:16pt; float: center; margin-top: 1mm; margin-bottom: 0mm">
               $$
               \displaystyle \{\mathcal{D}_{\{1,\dots,35\}}\} = \bigcup_{\sigma \; \in \; \text{Aut}(R_5)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1] \big\}
               $$
          </div>
          <div style="font-size:15pt; float: right; margin-top: -10mm; margin-bottom: 1mm;">
               $\kern0mm\color{green}\text{Identical to 1-loop!}$
          </div>
	</div>
     <div style="width:40%; float: right; display: inline-block; margin-top: 0mm;">
          <img src="V2.png"; style="max-width:260px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
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
     <b style="font-variant: small-caps; font-size: 32pt"> Partial Fraction Decompositions </b>
     <p style="margin-top: -2mm; margin-bottom: -=mm; font-size: 16pt;">
     (i.e. what happens at codimension greater than one)
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

<div style="text-align: left; font-size:17pt; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ$ When is a partial fraction decomposition possible? (an example)
</div><br>
<div style="font-size:15pt; float: center; margin-top: -8mm; margin-bottom: 1mm;">
     $$\frac{\mathcal{N}}{(\prod_j \mathcal{D}_j^{q_j})\times\langle 4|1+3|4]\langle 5|1+4|5]} \stackrel{?}{=} \frac{\mathcal{N}_1}{(\prod_j \mathcal{D}_j^{q_j})\times\langle 4|1+3|4]} + \frac{\mathcal{N}_2}{(\prod_j \mathcal{D}_j^{q_j})\times\langle 5|1+4|5]}$$
</div>

<div style="text-align: left; font-size:17pt; float: left; margin-top: 2mm; margin-bottom: -4mm;">
     $\circ$ Compute primary decompositions
</div><br>
<div style="font-size:15pt; float: center; margin-top: -4mm; margin-bottom: 1mm;">
     $$
     J = \big\langle \langle 4|1+3|4], \langle 5|1+4|5] \big\rangle \qquad
     K = \big\langle \langle14\rangle,\langle15\rangle,\langle45\rangle,[23] \big\rangle \quad
     L = \big\langle \langle ij\rangle \; \forall \; i,j\in\{1,\dots 5\} \big\rangle \\[2mm]
     M = \big\langle \langle 4|1+3|4], \langle 5|1+4|5], |1+4|5\rangle\langle14\rangle + |5|4\rangle\langle15\rangle, \langle\rangle \leftrightarrow [] \big\rangle
     $$
</div>

<div style="font-size:15pt; float: center; margin-top: 2mm; margin-bottom: 1mm;">
     $$
     J = K \cap \bar K \cap L \cap \bar L \cap M \quad \text{or} \quad V(J) = V(K) \cup V(\bar K) \cup V(L) \cup V(\bar L) \cap V(M)
     $$
</div>

<div style="text-align: center; float: center; font-size: x-large; margin-top: 2mm; margin-bottom: 0mm;">
     If $\mathcal{N}$ vanishes on all branches than the equality holds by Hilbert's Nullstellensatz.
</div>

<div style="text-align: center; float: center; font-size: 15pt; margin-top: 0mm; margin-bottom: 0mm;">
     For a fleshed out example with open-source code see <a href=https://inspirehep.net/literature/2661970> GDL (ACAT '22) </a>
</div>

</section>

---

<section>

{{< slide background-image="spinor_coeffs.png" >}}

<br><br><br><br><br><br>

# Analytic Reconstruction

<br><br><br><br>

also based on: <br>
GDL, Ita, Page, Sotnikov (to appear)

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
<img src="ReconstructionComplexity.png"; style="max-width:550px; float:center; border:none; margin-top: 0mm; margin-bottom: 0mm;">
</div>


<div style="text-align: left; font-size: x-large; float: left; margin-top: 1mm; margin-bottom: 0mm;">
     $\circ\,$ Change basis: 
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -10mm; margin-bottom: 5mm;">
     $$
     \kern-20mm \tilde{r}_i = O_{ii'}r_{i'\in\mathcal{B}} \; \longrightarrow \; R = \tilde{r}_{i} \, O_{ii'}^{-1}M_{i'j} \, h_j = \tilde{r}_{i}  \tilde{M}_{ij} h_j
     $$

<div style="text-align: left; font-size: x-large; float: left; margin-top: 2mm; margin-bottom: 0mm;">
     $\circ\,$ Key insight to build a good $O_{ii'}:$
</div>
<br>
<div style="text-align: center; float: center; font-size: x-large; margin-top: -2mm; margin-bottom: 5mm;">
     $$
     \text{dim(span}(\lim_{\mathcal{D_j} \rightarrow  0 }r_{i})) \leq \text{dim(span}(r_{i}))
     $$
</div>
<div style="text-align: left; font-size: x-large; float: left; margin-top: -4mm; margin-bottom: 0mm;">
     $\phantom{\circ}\,$ i.e., the <span style="color: red">pole residues are correlated</span>, build linear combinations that <i> ''remove the overlap'' </i>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large; margin-bottom: -2mm;"> De-correlating the Residues </b>

<div style="text-align: left; font-size: 17pt; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\circ\,$ Build Laurent expansions around $t_{\mathcal{D}_k}$
</div>
<span style="font-size: 11pt; text-align: right; float: right; margin-top: 0mm; margin-bottom: 0mm;" >
See also: 
<a style="font-size: 11pt; " href=https://arxiv.org/abs/1608.01902>
Tiele interpolation - Peraro ('16); 
</a>
<a style="font-size: 11pt; " href=https://inspirehep.net/literature/1944964>
spinor slice - Abreu, Febres Cordero, Ita, Klinkert, Page, Sotnikov ('21); 
</a>
<a style="font-size: 11pt; " href=https://inspirehep.net/literature/2654774>
p(z)-adic expansion - Fontana, Peraro ('23)$\phantom{; }$
</a>
</span>
<br>
<div style="text-align: center; float: center; font-size: 17pt; margin-top: -13mm; margin-bottom: 5mm;">
     $$
     r_{i \in \mathcal{B}} = \sum_{m = 1}^{q_k = \text{max}_i(q_{ik})} \frac{e^k_{im}}{(t-t_{\mathcal{D}_k})^m} + \mathcal{O}((t-t_{\mathcal{D}_k})^0)
     $$
</div>
<div style="text-align: left; font-size: 17pt; float: left; margin-top: 0mm; margin-bottom: 0mm;">
     $\phantom{\circ}\,$ strictly formal over $\mathbb{F}_p$, but convergent over $\mathbb{Q}_p$ for $(t-t_{\mathcal{D}_k}) \propto p$
</div>

<div style="text-align: left; font-size: 17pt; float: left; margin-top: 5mm; margin-bottom: 0mm;">
     $\circ\,$ By Gaussian elimination, partition the space:
</div> <br><br>
<div style="text-align: center; font-size: 17pt; float: center; margin-top: -4mm; margin-bottom: 2mm;">
     $$
     \text{span}(r_{i \in \mathcal{B}}) = \underbrace{\text{column}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))}_{\text{functions with the singularity}} \;\;\; \oplus \, \underbrace{\text{null}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))}_{\text{functions without the singularity}}
     $$
</div>

<!---
<div style="border: 1px solid black; font-size: 17pt; padding: 10px; display: inline-block; margin-top: 2mm;">
    $\text{null}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))$: functions that do <u>not</u> have a $D_k^m$ singularity
</div>
--->

<div style="display:block; width:100%; margin-top: 0mm; margin-bottom: 0mm; margin-left: 0mm;">
     <div style="font-size: 17pt; width:50%; float: left; text-align: center; display: inline-block; margin-top: 3mm;">
	     <div style="font-size: 17pt; float: left; margin-top: 4mm; margin-bottom: 1mm;">
               $\circ\,$ Search for linear combinations that remove as many singularities as possible
          </div>
          <br>
          <div style="font-size:16pt; float: left; margin-top: 0mm; margin-bottom: 0mm">
               $$
               \kern25mm \displaystyle O_{i'i} = \bigcap_{k, m} \, \text{nulls}(\text{Res}(r_{i \in \mathcal{B}}, \mathcal{D}_k^m))
               $$
          </div>
	</div>
     <div style="width:50%; float: right; display: inline-block; margin-top: 0mm;">
          <img src="search_tree.png"; style="max-width:400px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
     </div>
</div>

---

<b style="font-variant: small-caps; font-size: xxx-large"> Spinor-Helicity Results </b>
<br>

<div style="text-align: center; float:center; font-size: x-large; margin-bottom: 1mm; margin-top: -5mm;">
<img src="VSSizeTable-transparent.png"; style="max-width:350px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
<img src="quarks_vs_sizes.png"; style="max-width:340px; float:center; border:none; margin-top: 5mm; margin-bottom: 0mm;">
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The gluon MHV rational functions fit in 3 pages of the appendix
</div>

<div style="text-align: left; font-size: 14pt; margin-bottom: 1mm; margin-top: 5mm;">
     $$ \tilde{r}^{\text{MHV}}_{\text{first 5 of 115}} = \left\{ \frac{⟨45⟩^2}{⟨12⟩⟨13⟩⟨23⟩}, \frac{⟨45⟩^3}{⟨12⟩^2⟨34⟩⟨35⟩}, \frac{⟨45⟩^3}{⟨12⟩⟨15⟩⟨23⟩⟨34⟩}, \frac{[14][12][35]}{⟨23⟩[45]^3}, \frac{⟨45⟩^2⟨24⟩}{⟨12⟩^2⟨23⟩⟨34⟩}, \dots \right\} \text{+ symmetries}$$
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ All rational functions fitted in a single finite field. The matrices still required a few values of $p$.
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The size of the results is dominated by the rational matrices (explicitly given for all crossings).
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ The simplification of the basis change is <u>independent</u> of that from PFDs.
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
     $\circ$ The vector space has uniform mass dimension and phase weights, which depend on helicities
</div>
<div style="text-align: center; float: center; font-size: x-large; margin-top: 0mm; margin-bottom: 0mm;">
     $$
     |i⟩ \rightarrow t^{1/2}|i⟩, \; |i] \rightarrow t^{1/2}|i] \quad \forall \; i \quad \text{and} \quad
     |i⟩ \rightarrow t|i⟩, \; |i] \rightarrow \frac{1}{t}|i]
     $$
</div>

<div style="text-align: left; font-size: x-large; margin-bottom: 1mm; margin-top: 5mm;">
     $\circ$ Rescale gluon amplitudes in a way reminiscent of supersymmetry Ward identities
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

<b style="font-variant: small-caps; font-size: 32pt; margin-bottom: 10mm;">
   Complexity of 2-loop 5-point 1-mass Amplitudes
</b>

<div style="text-align: left; font-size: 16pt; margin-top: 5mm; margin-bottom: 1mm;">
$\circ\,$ The number of letters in the spinor alphabet goes from 35 to more then 220:
</div>
<div style="text-align: center; float: left; font-size: 16pt; margin-top: 0mm; margin-bottom: -2mm;">
     $$
     \displaystyle \kern5mm \{W_j\} = \bigcup_{\sigma \; \in \; \text{Aut}(R_6)} \sigma \circ \big\{ \langle 12 \rangle, \langle 1|2+3|1], \langle 1|2+3|4], s_{123}, \Delta_{12|34|56}, ⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2] \big\}
     $$
</div> <br><br>
<div style="text-align: left; font-size: 16pt; margin-top: -15mm; margin-bottom: 0mm;">
$\phantom{\circ}\,$ from the point of view of the coefficients, this is closer to a massless 6-pt. computation than a 5-pt. one.
</div>

<br>

<div style="display:block; width:100%; font-size: 16pt; margin-top: -5mm; margin-bottom: 4mm;">
     <div style="width:50%; text-align: left; float: left; display: font-size: x-large;">
          $\circ$ The  Ansatz size grows quickly with <br> multiplicity (m) and mass dimension (d): <br><br>
          $\displaystyle \kern40mm \small \left(\mkern -9mu \begin{pmatrix}\, m(m-3)/2 \, \\ \, d/2 \, \end{pmatrix} \mkern -9mu \right)$ <br><br>
          is a lower bound. <br>
          <a style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: -5mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/2010.14525>
               GDL, Maître ('20)
          </a>
     </div>
     <div style="width:50%; float: right; display: inline-block;">
          <img src="AnsatzSizes.png"; style="max-width:440px;float:center;border:none;margin-top:-10pt;margin-bottom: 0mm;">
     </div>
</div>

<br><br><br><br><br><br><br>

<div style="text-align: left; font-size: 16pt; margin-top: 2mm; margin-bottom: 2mm;">
$\circ\,$ We can still achieve compact results, e.g. for the new 2-loop pole, $⟨k|j|p\mkern-7.5mu/_V|l|k]-⟨j|i|p\mkern-7.5mu/_V|l|j]$
$$r^{(5 \text{ of } 54)}_{\bar{u}^+g^+g^+d^-(V\rightarrow \ell^+ \ell^-)} = \frac{[12][23]⟨24⟩⟨46⟩^2⟨1|2+3|4]⟨2|1+3|4]}{⟨12⟩⟨23⟩⟨56⟩(⟨3|2|5+6|4|3]-⟨2|1|5+6|4|2])^2}$$
</div>

---

<b style="font-variant: small-caps; font-size: 28pt; margin-bottom: 10mm;">
   Iterated Reconstruction by Sequentially Removing Poles
</b>

<div style="text-align: left; font-size: x-large; margin-top: 2mm;">
$\circ\,$ In general results are much more complicated, but we can retain control surface-by-surface
</div>
<a style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: 0mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/fix>
     Campbell, GDL, Ellis, ('22)
</a>
<p style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: 0mm; margin-bottom: 0mm">
     and $\;$
</p>
<a style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: 0mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/2203.04269>
     GDL, Page ('22) $\;$
</a>
<p style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: 0mm; margin-bottom: 0mm">
     see also: $\;$
</p>
<a style="font-size: large; display: inline-block; text-align: right; float: right; margin-left: 0mm; margin-top: 0mm; margin-bottom: 0mm;" href=https://arxiv.org/abs/1904.04067>
     GDL, Maître ('19) $\;$ 
</a>

<br>
<div style="text-align: left; font-size: 14pt; margin-top: -8mm; margin-bottom: 1mm;">
$$ 
\begin{alignedat}{2}
& r^{(139 \text{ of } 139)}_{\bar{u}^+g^+g^-d^-(V\rightarrow \ell^+ \ell^-)} = & \qquad\qquad & \text{Variety (scheme?) to isolate term(s)} \\[2mm]
& \frac{-7/8⟨16⟩⟨1|2+3|5]⟨3|1+4|2](s_{13}-s_{24} )(s_{123}-s_{234})}{⟨14⟩⟨1|2+3|4]^2⟨2|1+4|3]Δ_{14|23|56}} & \qquad\qquad & \Big\langle ⟨1|2+3|4]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
& +\frac{7/4(s_{24}-s_{13})⟨6|1+4|5]s_{123}(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]^2 Δ_{14|23|56}} & \qquad\qquad & \Big\langle ⟨2|1+4|3]^2, Δ_{14|23|56} \Big\rangle \\[1mm]
& -\frac{49/64⟨3|1+4|2]⟨6|1+4|5]s_{123}(s_{123}-s_{234})(s_{124}-s_{134})}{⟨1|2+3|4]⟨2|1+4|3]Δ^2_{14|23|56}} & \qquad\qquad & \Big\langle Δ_{14|23|56} \Big\rangle \\[1mm]
& +\frac{1/4[12]^3⟨14⟩[45]⟨46⟩}{[13][23]⟨1|2+3|1]⟨4|5+6|4]^2} & \qquad\qquad & \Big\langle ⟨1|2+3|1], ⟨4|5+6|4]^2 \Big\rangle \\[1mm]
& -\frac{1/4[12]2⟨13⟩⟨24⟩[45]⟨46⟩}{⟨12⟩[13]⟨2|1+3|2]⟨4|5+6|4]^2}-\frac{3/4⟨34⟩2[45]⟨46⟩⟨3|1+2|4]}{⟨14⟩⟨23⟩⟨2|1+3|4]⟨4|5+6|4]^2} & \qquad\qquad & \Big\langle ⟨4|5+6|4] \Big\rangle \\[1mm]
& + \dots \text{more than 30 other fractions} \dots &&
\end{alignedat}
$$
</div>
<!--- 
& +\frac{7/2⟨13⟩^3[15]⟨16⟩[23]}{⟨12⟩⟨14⟩⟨1|2+3|1]⟨1|2+3|4]^2}+\frac{7/2⟨13⟩^2⟨16⟩[25]}{⟨12⟩⟨14⟩⟨1|2+3|4]^2} & \qquad\qquad & \Big\langle ⟨1|2+3|4] \Big\rangle \\[1mm]
& -\frac{7⟨24⟩[25][35]s_{123}}{⟨12⟩[23][56]⟨2|1+4|3]^2} & \qquad\qquad & \Big\langle ⟨2|1+4|3] \Big\rangle \\[1mm]
--->

<div style="text-align: left; font-size: 16pt; margin-top: 2mm;">
$\circ\,$ Preliminary results (originally around 1.3GB of source code, compiled in almost 20GB of C++ binaries):
</div>
<div style="text-align: center; font-size: 16pt; margin-top: 2mm;">
$pp\rightarrow Vq\bar q : \; 120\text{KB} \; r_i, \; 500\text{KB} \; M_{ij} \qquad pp\rightarrow Vgg \text{(MHV)}: \; 170\text{KB} \; r_i, \; 33\text{KB} \; M_{ij}; $ <br>
$pp\rightarrow Vgg \text{(NMHV)}: \; 13\text{MB} \; r_i, \; 1\text{MB} \; M_{ij}.$
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
