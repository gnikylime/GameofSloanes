# Game of Sloanes
<p>A game to find putatively optimal packings in complex projective space with the goal of proving optimality of as many packings as possible.
Formerly hosted <a href="https://www.math.colostate.edu/~king/GameofSloanes.html">here.</a><br>

This project is licensed under the terms of the Creative Commons Attribution 4.0.
Please cite Game of Sloanes; https://github.com/gnikylime/GameofSloanes/; Authors: John Jasper, Emily J. King, and Dustin G. Mixon<br>

This repository concerns the problem of packing $`n`$ lines, represented by unit vectors, through the origin of $`C^d`$ such that the angles between the lines are as large as possible. The problem has applications in fields such as compressed sensing, digital fingerprinting, quantum state tomography, and multiple description coding.</br>

Let $`\Phi=\left(\varphi_j\right)_{j=1}^n`$ be a set of unit norm vectors. The <i>coherence</i> $`\mu`$ of $`\Phi`$ is defined to be\
$$\mu\left(\Phi\right) = \max_{1\leq  j < k\leq n} \vert\langle \varphi_j, \varphi_k \rangle\vert.$$<br>

We call $`\Phi`$ a <i>Grassmannian frame</i> or <i>(optimal) projective packing</i> if\
$$\Phi \in \text{argmin}\lbrace \mu(\Psi) \text{ } : \text{ }  \Psi \text{ } n \text{ unit norm vectors in }C^d \rbrace.$$<br>

For a review of results about complex Grassmannian frames, see the paper [JKM19].<br></p>

<h3>Submissions</h3>
<p>If you have a collection of $n$ vectors in $C^d$ which has a better coherence (to at least the eighth decimal point) than what is listed above, we welcome you to submit it.  We will accept sporadic packings for $d$ and $n$ not listed above if there is evidence that the packing is truly optimal. <br>
Submissions must be in the following format. A .txt file consisting of a newline-separated list of the $2 d n$ entries of the (unit-norm) vectors, starting with the real parts of the components of the first vector, then the real parts of the components of the second vector, and so on before working through the imaginary parts of each vector.<br>
The filenames must be of the form `dxn_init.txt`, where `d` is the dimension, `n` is the number of vectors and `init` is a three- or four-character (i.e., only alphabet characters) string to list in the Creator column.<br>
Please make a branch of the repository and put the new packings in the SubmittedPackings directory.  Then do a pull request.  If you would like to send additional information, write to our Gmail account asongofvectorsandangles.</p>

<h3>Open Problems</h3>
<p>
<ul>
<li><b>Conjecture</b>: The frames of $8$ vectors in $C^3$ that result from removing a single vector from any of the known equiangular tight frames of $9$ vectors in $C^3$ are Grassmannian frames.</br><b>Sources</b>: [JKM19]<br>(independently conjectured by Henry Cohn)</li>
<li><b>Conjecture</b>: Assume that an equiangular tight frame of $d^2$ vectors in $C^d$ exists. Then removing one vector from that equiangular tight frame results in a Grassmannian frame of $d^2-1$ vectors in $C^d$.</br><b>Source</b>: Conjectured by Henry Cohn.</li>
<li><b>Conjecture</b>: The following is a Grassmannian frame of $5$ vectors in $C^3$:
  
  $$\left(\matrix{ a & b & b & c & c \cr b & a & b & c w & cw^2 \cr b & b & a & cw^2 & cw}\right),$$
<br>
$$a = \frac{\sqrt{13}+\sqrt{2+\sqrt{13}}-1}{3\sqrt{3}}, \quad b = \sqrt{\frac{1-a^2}{2}}, \quad c = \frac{1}{\sqrt{3}},\quad w=e^{2\pi i/3}.$$
<b>Source</b>: [JKM19]</li>
<li><b>Conjecture</b>: The configuration of $85$ vectors in $C^5$ listed numerically in the leader board and explicitly constructed as the union of the root vectors corresponding to the $45$ $2$-reflections which generate the unitary reflection group $W(K_5)$ and $40$ vectors representing each antipodal pair of minimal vectors of the Coxeter-Todd lattice $O_{10}$ is a Grassmannian frame.</br><b>Source</b>: [BGM+22]</li>
<li><b>Open Problem</b>: Generalize the Levenstein and Bukh-Cox bounds to general subspace packings.</br><b>Source</b>: [JKM19]</li>
</ul>
</p>

<h3>Leader Board</h3>
      <p>Packings for all $2 \leq d \leq 7$ and $d+2 \leq n \leq 49$, plus sporadic packings.</p>

<h4>Legend and Further Notes</h4>
      <p>
        <ul>
          <li> The Grassmannian frames for $d = n$ are orthonormal bases and for $d+1 = n$ are regular simplices, hence we do not list them.</li>
          <li> <b>Best Coherence</b> gives the best coherence of the packings which have been submitted for that $d$ and $n$. A new packing is considered better if it beats the previous packing in at least the eighth decimal place.</li>
          <li> <b>Lower Bound</b> gives the maximum of whichever of the Bukh-Cox, Welch-Rankin, orthoplex, and/or Levenstein bounds are valid and largest for that $d$ and $n$.</li>
          <li> <b>Creator</b> gives a 3&ndash;4 character string indicating the creator of the packing.
            <ul>
              <li> etf: A known equiangular tight frame.  See, e.g., [FM16] and the references therein.</li>
              <li> orth: The maximal known set of vectors in $`C^d`$ which saturate the orthoplex bound.  When $`d`$ is a prime power, this collection is a maximal set of mutually unbiased bases consisting of $`d^2 + d`$ vectors.  See, e.g., [KlRo04] and the reference therein.</li>
              <li> Lev: A set of vectors which saturate the (second) Levenstein bound.</li>
              <li> B-C: A set of vectors which saturate the Bukh-Cox bound.</li>
              <li> AUTO: Removing a vector from the best known packing for $d$ and $n+1$ results in a better coherence than any of the submitted packings for $d$ and $n$.</li>
              <li> njas: Grassmannian frames in $C^2$ are equivalent to optimal spherical codes in $S^2$.  The configurations labeled with njas are best known spherical codes in $S^2$ downloaded from <a href="#Sloane1">[Sloane1]</a>.</li>
              <li> dgm, ejk, and JJ: Dustin G. Mixon, Emily J. King, and John Jasper, respectively.</li>
              <li> hlc: Henry Cohn.</li>
              <li> gKmR: Gene Kopp and Michael Ren.</li>
              <li> jrr: Juan Rom&aacute;n-Roche and Sebasti&aacute;n Roca-Jerat.</li>
              <li> bmem: Bastien Massion and Estelle Massart. </li>
              <li> BGM+22: From the paper [BGM+22].</li>
              <li> CID+21: From the paper [CID+21]. (Has since been knocked off the leader board.)</li>
            </ul>
          </li>
          <li> <b>Text File</b> contains a link to a .txt file with the best submitted packing formated as a newline-separated list of the $2 d n$ entries of the vectors, starting with the real parts of the first vector, then the real parts of the second vector, and so on until the imaginary parts of the last vector.</li>
          <li> <b>Notes</b> contain the following information:
            <ul>
              <li> &#9675; indicates that the configuration is provably optimal.</li>
              <li> &#9651; indicates that the configuration is conjectured to be optimal.</li>
              <li> When pertinent, a reference to a paper or website is listed.</li>
            </ul>
          </li>
          <li>For a listing of numerically approximated and explicitly defined optimal packings when $n=d^2$, see, e.g., [FSDH], [Grassl], and [Flamm].</li>
        </ul>
</p>



<!--Start table-->

<div class="table-responsive my-table">
  <table class="table">
    <thead>
        <tr>
            <th scope="col">d</th>
            <th scope="col">n</th>
            <th scope="col">Best Coherence</th>
            <th scope="col">Lower Bound</th>
            <th scope="col">Creator</th>
            <th scope="col">Text File</th>
            <th scope="col">Notes</th>
        </tr>
    </thead>
    <tbody>
<tr><td>2</td><td>4</td><td>0.57735027</td><td>0.57735027</td><td>etf</td><td><a href="CurrentBestPackings/2x4_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>5</td><td>0.70710678</td><td>0.70710678</td><td>AUTO</td><td><a href="CurrentBestPackings/2x5_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>6</td><td>0.70710678</td><td>0.70710678</td><td>orth</td><td><a href="CurrentBestPackings/2x6_orth.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>7</td><td>0.77786191</td><td>0.73029674</td><td>njas</td><td><a href="CurrentBestPackings/2x7_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>8</td><td>0.79410449</td><td>0.75000000</td><td>njas</td><td><a href="CurrentBestPackings/2x8_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>9</td><td>0.81649658</td><td>0.77777778</td><td>njas</td><td><a href="CurrentBestPackings/2x9_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>10</td><td>0.83797205</td><td>0.80000000</td><td>njas</td><td><a href="CurrentBestPackings/2x10_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>11</td><td>0.85065081</td><td>0.81818182</td><td>njas</td><td><a href="CurrentBestPackings/2x11_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>12</td><td>0.85065081</td><td>0.83333333</td><td>njas</td><td><a href="CurrentBestPackings/2x12_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>13</td><td>0.87824726</td><td>0.84615385</td><td>njas</td><td><a href="CurrentBestPackings/2x13_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>14</td><td>0.88429359</td><td>0.85714286</td><td>njas</td><td><a href="CurrentBestPackings/2x14_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>15</td><td>0.89235808</td><td>0.86666667</td><td>njas</td><td><a href="CurrentBestPackings/2x15_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>16</td><td>0.89785706</td><td>0.87500000</td><td>njas</td><td><a href="CurrentBestPackings/2x16_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>17</td><td>0.90224565</td><td>0.88235294</td><td>njas</td><td><a href="CurrentBestPackings/2x17_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>18</td><td>0.90793607</td><td>0.88888889</td><td>njas</td><td><a href="CurrentBestPackings/2x18_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>19</td><td>0.91463569</td><td>0.89473684</td><td>njas</td><td><a href="CurrentBestPackings/2x19_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>20</td><td>0.91555370</td><td>0.90000000</td><td>njas</td><td><a href="CurrentBestPackings/2x20_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>21</td><td>0.92181843</td><td>0.90476190</td><td>njas</td><td><a href="CurrentBestPackings/2x21_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>22</td><td>0.92474490</td><td>0.90909091</td><td>njas</td><td><a href="CurrentBestPackings/2x22_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>23</td><td>0.92812903</td><td>0.91304348</td><td>njas</td><td><a href="CurrentBestPackings/2x23_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>24</td><td>0.92819138</td><td>0.91666667</td><td>njas</td><td><a href="CurrentBestPackings/2x24_njas.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>2</td><td>25</td><td>0.93471884</td><td>0.92000000</td><td>njas</td><td><a href="CurrentBestPackings/2x25_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>26</td><td>0.93655704</td><td>0.92307692</td><td>njas</td><td><a href="CurrentBestPackings/2x26_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>27</td><td>0.93765378</td><td>0.92592593</td><td>njas</td><td><a href="CurrentBestPackings/2x27_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>28</td><td>0.94160243</td><td>0.92857143</td><td>njas</td><td><a href="CurrentBestPackings/2x28_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>29</td><td>0.94347269</td><td>0.93103448</td><td>njas</td><td><a href="CurrentBestPackings/2x29_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>30</td><td>0.94380927</td><td>0.93333333</td><td>njas</td><td><a href="CurrentBestPackings/2x30_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>31</td><td>0.94633995</td><td>0.93548387</td><td>njas</td><td><a href="CurrentBestPackings/2x31_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>32</td><td>0.94699963</td><td>0.93750000</td><td>njas</td><td><a href="CurrentBestPackings/2x32_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>33</td><td>0.95036772</td><td>0.93939394</td><td>njas</td><td><a href="CurrentBestPackings/2x33_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>34</td><td>0.95157352</td><td>0.94117647</td><td>njas</td><td><a href="CurrentBestPackings/2x34_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>35</td><td>0.95287401</td><td>0.94285714</td><td>njas</td><td><a href="CurrentBestPackings/2x35_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>36</td><td>0.95321776</td><td>0.94444444</td><td>njas</td><td><a href="CurrentBestPackings/2x36_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>37</td><td>0.95522052</td><td>0.94594595</td><td>njas</td><td><a href="CurrentBestPackings/2x37_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>38</td><td>0.95566293</td><td>0.94736842</td><td>njas</td><td><a href="CurrentBestPackings/2x38_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>39</td><td>0.95759890</td><td>0.94871795</td><td>njas</td><td><a href="CurrentBestPackings/2x39_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>40</td><td>0.95842633</td><td>0.95000000</td><td>njas</td><td><a href="CurrentBestPackings/2x40_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>41</td><td>0.95948849</td><td>0.95121951</td><td>njas</td><td><a href="CurrentBestPackings/2x41_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>42</td><td>0.96003426</td><td>0.95238095</td><td>njas</td><td><a href="CurrentBestPackings/2x42_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>43</td><td>0.96104341</td><td>0.95348837</td><td>njas</td><td><a href="CurrentBestPackings/2x43_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>44</td><td>0.96130156</td><td>0.95454545</td><td>njas</td><td><a href="CurrentBestPackings/2x44_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>45</td><td>0.96287317</td><td>0.95555556</td><td>njas</td><td><a href="CurrentBestPackings/2x45_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>46</td><td>0.96372563</td><td>0.95652174</td><td>njas</td><td><a href="CurrentBestPackings/2x46_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>47</td><td>0.96413753</td><td>0.95744681</td><td>njas</td><td><a href="CurrentBestPackings/2x47_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>48</td><td>0.96418159</td><td>0.95833333</td><td>njas</td><td><a href="CurrentBestPackings/2x48_njas.txt">File</a></td><td></td></tr>
<tr><td>2</td><td>49</td><td>0.96609820</td><td>0.95918367</td><td>njas</td><td><a href="CurrentBestPackings/2x49_njas.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>5</td><td>0.43425855</td><td>0.41406779</td><td>dgm</td><td><a href="CurrentBestPackings/3x5_dgm.txt">File</a></td><td>&#9651;</td></tr>
<tr><td>3</td><td>6</td><td>0.44721360</td><td>0.44721360</td><td>etf</td><td><a href="CurrentBestPackings/3x6_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>3</td><td>7</td><td>0.47140452</td><td>0.47140452</td><td>etf</td><td><a href="CurrentBestPackings/3x7_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>3</td><td>8</td><td>0.50000000</td><td>0.48795004</td><td>AUTO</td><td><a href="CurrentBestPackings/3x8_AUTO.txt">File</a></td><td>&#9651;</td></tr>
<tr><td>3</td><td>9</td><td>0.50000000</td><td>0.50000000</td><td>etf</td><td><a href="CurrentBestPackings/3x9_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>3</td><td>10</td><td>0.57735027</td><td>0.57735027</td><td>AUTO</td><td><a href="CurrentBestPackings/3x10_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>3</td><td>11</td><td>0.57735027</td><td>0.57735027</td><td>AUTO</td><td><a href="CurrentBestPackings/3x11_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>3</td><td>12</td><td>0.57735027</td><td>0.57735027</td><td>orth</td><td><a href="CurrentBestPackings/3x12_orth.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>3</td><td>13</td><td>0.62214387</td><td>0.59160798</td><td>dgm</td><td><a href="CurrentBestPackings/3x13_dgm.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>14</td><td>0.63763052</td><td>0.60302269</td><td>dgm</td><td><a href="CurrentBestPackings/3x14_dgm.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>15</td><td>0.64038820</td><td>0.61237244</td><td>JJ</td><td><a href="CurrentBestPackings/3x15_JJ.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>16</td><td>0.64775448</td><td>0.62017367</td><td>hlc</td><td><a href="CurrentBestPackings/3x16_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>17</td><td>0.65436636</td><td>0.62678317</td><td>JJ</td><td><a href="CurrentBestPackings/3x17_JJ.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>18</td><td>0.66295789</td><td>0.63245553</td><td>hlc</td><td><a href="CurrentBestPackings/3x18_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>19</td><td>0.67647322</td><td>0.63737744</td><td>hlc</td><td><a href="CurrentBestPackings/3x19_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>20</td><td>0.68646389</td><td>0.64168895</td><td>hlc</td><td><a href="CurrentBestPackings/3x20_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>21</td><td>0.68797170</td><td>0.64549722</td><td>hlc</td><td><a href="CurrentBestPackings/3x21_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>22</td><td>0.70342497</td><td>0.64888568</td><td>bmem</td><td><a href="CurrentBestPackings/3x22_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>23</td><td>0.70936761</td><td>0.65192024</td><td>jrr</td><td><a href="CurrentBestPackings/3x23_jrr.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>24</td><td>0.71909565</td><td>0.65465367</td><td>hlc</td><td><a href="CurrentBestPackings/3x24_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>25</td><td>0.72545783</td><td>0.65712874</td><td>bmem</td><td><a href="CurrentBestPackings/3x25_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>26</td><td>0.72912181</td><td>0.65938047</td><td>bmem</td><td><a href="CurrentBestPackings/3x26_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>27</td><td>0.73395441</td><td>0.66143783</td><td>bmem</td><td><a href="CurrentBestPackings/3x27_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>28</td><td>0.73682183</td><td>0.66332496</td><td>hlc</td><td><a href="CurrentBestPackings/3x28_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>29</td><td>0.74075020</td><td>0.66506217</td><td>bmem</td><td><a href="CurrentBestPackings/3x29_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>30</td><td>0.74394268</td><td>0.66666667</td><td>bmem</td><td><a href="CurrentBestPackings/3x30_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>31</td><td>0.74532208</td><td>0.66815310</td><td>hlc</td><td><a href="CurrentBestPackings/3x31_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>32</td><td>0.74797328</td><td>0.66953406</td><td>bmem</td><td><a href="CurrentBestPackings/3x32_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>33</td><td>0.75301857</td><td>0.67082039</td><td>hlc</td><td><a href="CurrentBestPackings/3x33_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>34</td><td>0.75683480</td><td>0.67202151</td><td>jrr</td><td><a href="CurrentBestPackings/3x34_jrr.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>35</td><td>0.75932202</td><td>0.67314560</td><td>bmem</td><td><a href="CurrentBestPackings/3x35_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>36</td><td>0.76088362</td><td>0.67419986</td><td>hlc</td><td><a href="CurrentBestPackings/3x36_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>37</td><td>0.76619123</td><td>0.67519060</td><td>hlc</td><td><a href="CurrentBestPackings/3x37_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>38</td><td>0.77189089</td><td>0.67612340</td><td>bmem</td><td><a href="CurrentBestPackings/3x38_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>39</td><td>0.77507569</td><td>0.67974369</td><td>hlc</td><td><a href="CurrentBestPackings/3x39_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>40</td><td>0.77729266</td><td>0.68377223</td><td>bmem</td><td><a href="CurrentBestPackings/3x40_bmem.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>41</td><td>0.77848806</td><td>0.68765248</td><td>hlc</td><td><a href="CurrentBestPackings/3x41_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>42</td><td>0.77853167</td><td>0.69139330</td><td>hlc</td><td><a href="CurrentBestPackings/3x42_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>43</td><td>0.78370816</td><td>0.69500286</td><td>hlc</td><td><a href="CurrentBestPackings/3x43_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>44</td><td>0.78689372</td><td>0.69848866</td><td>hlc</td><td><a href="CurrentBestPackings/3x44_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>45</td><td>0.78689437</td><td>0.70185760</td><td>JJ</td><td><a href="CurrentBestPackings/3x45_JJ.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>46</td><td>0.79435710</td><td>0.70511609</td><td>hlc</td><td><a href="CurrentBestPackings/3x46_hlc.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>47</td><td>0.79684252</td><td>0.70827002</td><td>jrr</td><td><a href="CurrentBestPackings/3x47_jrr.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>48</td><td>0.79933457</td><td>0.71132487</td><td>jrr</td><td><a href="CurrentBestPackings/3x48_jrr.txt">File</a></td><td></td></tr>
<tr><td>3</td><td>49</td><td>0.80155093</td><td>0.71428571</td><td>hlc</td><td><a href="CurrentBestPackings/3x49_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>6</td><td>0.32732684</td><td>0.32278096</td><td>dgm</td><td><a href="CurrentBestPackings/4x6_dgm.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>7</td><td>0.35355339</td><td>0.35355339</td><td>etf</td><td><a href="CurrentBestPackings/4x7_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>8</td><td>0.37796447</td><td>0.37796447</td><td>etf</td><td><a href="CurrentBestPackings/4x8_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>9</td><td>0.40185012</td><td>0.39528471</td><td>hlc</td><td><a href="CurrentBestPackings/4x9_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>10</td><td>0.41077812</td><td>0.40824829</td><td>hlc</td><td><a href="CurrentBestPackings/4x10_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>11</td><td>0.42514727</td><td>0.41833001</td><td>bmem</td><td><a href="CurrentBestPackings/4x11_bmem.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>12</td><td>0.42774232</td><td>0.42640143</td><td>JJ</td><td><a href="CurrentBestPackings/4x12_JJ.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>13</td><td>0.43301270</td><td>0.43301270</td><td>etf</td><td><a href="CurrentBestPackings/4x13_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>14</td><td>0.44721360</td><td>0.43852901</td><td>AUTO</td><td><a href="CurrentBestPackings/4x14_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>15</td><td>0.44721360</td><td>0.44320263</td><td>AUTO</td><td><a href="CurrentBestPackings/4x15_AUTO.txt">File</a></td><td>&#9651;</td></tr>
<tr><td>4</td><td>16</td><td>0.44721360</td><td>0.44721360</td><td>etf</td><td><a href="CurrentBestPackings/4x16_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>17</td><td>0.50000000</td><td>0.50000000</td><td>AUTO</td><td><a href="CurrentBestPackings/4x17_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>18</td><td>0.50000000</td><td>0.50000000</td><td>AUTO</td><td><a href="CurrentBestPackings/4x18_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>19</td><td>0.50000000</td><td>0.50000000</td><td>AUTO</td><td><a href="CurrentBestPackings/4x19_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>20</td><td>0.50000000</td><td>0.50000000</td><td>orth</td><td><a href="CurrentBestPackings/4x20_orth.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>21</td><td>0.53721512</td><td>0.50874702</td><td>hlc</td><td><a href="CurrentBestPackings/4x21_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>22</td><td>0.54543658</td><td>0.51639778</td><td>hlc</td><td><a href="CurrentBestPackings/4x22_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>23</td><td>0.55046239</td><td>0.52314836</td><td>hlc</td><td><a href="CurrentBestPackings/4x23_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>24</td><td>0.55701604</td><td>0.52915026</td><td>hlc</td><td><a href="CurrentBestPackings/4x24_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>25</td><td>0.56649311</td><td>0.53452248</td><td>hlc</td><td><a href="CurrentBestPackings/4x25_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>26</td><td>0.57142744</td><td>0.53935989</td><td>jrr</td><td><a href="CurrentBestPackings/4x26_jrr.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>27</td><td>0.57499638</td><td>0.54373907</td><td>hlc</td><td><a href="CurrentBestPackings/4x27_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>28</td><td>0.57711826</td><td>0.54772256</td><td>jrr</td><td><a href="CurrentBestPackings/4x28_jrr.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>29</td><td>0.57733882</td><td>0.55136195</td><td>hlc</td><td><a href="CurrentBestPackings/4x29_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>30</td><td>0.57735006</td><td>0.55470020</td><td>hlc</td><td><a href="CurrentBestPackings/4x30_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>31</td><td>0.57735027</td><td>0.55777335</td><td>AUTO</td><td><a href="CurrentBestPackings/4x31_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>32</td><td>0.57735027</td><td>0.56061191</td><td>AUTO</td><td><a href="CurrentBestPackings/4x32_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>33</td><td>0.57735027</td><td>0.56324185</td><td>AUTO</td><td><a href="CurrentBestPackings/4x33_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>34</td><td>0.57735027</td><td>0.56568542</td><td>AUTO</td><td><a href="CurrentBestPackings/4x34_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>35</td><td>0.57735027</td><td>0.56796183</td><td>AUTO</td><td><a href="CurrentBestPackings/4x35_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>36</td><td>0.57735027</td><td>0.57008771</td><td>AUTO</td><td><a href="CurrentBestPackings/4x36_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>37</td><td>0.57735027</td><td>0.57207755</td><td>AUTO</td><td><a href="CurrentBestPackings/4x37_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>38</td><td>0.57735027</td><td>0.57394404</td><td>AUTO</td><td><a href="CurrentBestPackings/4x38_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>39</td><td>0.57735027</td><td>0.57569833</td><td>AUTO</td><td><a href="CurrentBestPackings/4x39_AUTO.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>40</td><td>0.57735027</td><td>0.57735027</td><td>Lev</td><td><a href="CurrentBestPackings/4x40_Lev.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>4</td><td>41</td><td>0.62179172</td><td>0.57890857</td><td>jrr</td><td><a href="CurrentBestPackings/4x41_jrr.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>42</td><td>0.62416041</td><td>0.58038100</td><td>hlc</td><td><a href="CurrentBestPackings/4x42_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>43</td><td>0.62689046</td><td>0.58177447</td><td>hlc</td><td><a href="CurrentBestPackings/4x43_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>44</td><td>0.63028266</td><td>0.58309519</td><td>hlc</td><td><a href="CurrentBestPackings/4x44_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>45</td><td>0.63206547</td><td>0.58434871</td><td>bmem</td><td><a href="CurrentBestPackings/4x45_bmem.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>46</td><td>0.63583204</td><td>0.58554004</td><td>hlc</td><td><a href="CurrentBestPackings/4x46_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>47</td><td>0.63981695</td><td>0.58667371</td><td>hlc</td><td><a href="CurrentBestPackings/4x47_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>48</td><td>0.64342772</td><td>0.58775381</td><td>hlc</td><td><a href="CurrentBestPackings/4x48_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>49</td><td>0.64632850</td><td>0.58878406</td><td>hlc</td><td><a href="CurrentBestPackings/4x49_hlc.txt">File</a></td><td></td></tr>
<tr><td>4</td><td>64</td><td>0.68716020</td><td>0.60000000</td><td>hlc</td><td><a href="CurrentBestPackings/4x64_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>7</td><td>0.26635681</td><td>0.26447408</td><td>dgm</td><td><a href="CurrentBestPackings/5x7_dgm.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>8</td><td>0.29520808</td><td>0.29277002</td><td>hlc</td><td><a href="CurrentBestPackings/5x8_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>9</td><td>0.32011714</td><td>0.31622777</td><td>hlc</td><td><a href="CurrentBestPackings/5x9_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>10</td><td>0.33333333</td><td>0.33333333</td><td>etf</td><td><a href="CurrentBestPackings/5x10_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>11</td><td>0.34641016</td><td>0.34641016</td><td>etf</td><td><a href="CurrentBestPackings/5x11_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>12</td><td>0.35738925</td><td>0.35675303</td><td>hlc</td><td><a href="CurrentBestPackings/5x12_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>13</td><td>0.36760232</td><td>0.36514837</td><td>JJ</td><td><a href="CurrentBestPackings/5x13_JJ.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>14</td><td>0.37567476</td><td>0.37210420</td><td>hlc</td><td><a href="CurrentBestPackings/5x14_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>15</td><td>0.37993678</td><td>0.37796447</td><td>hlc</td><td><a href="CurrentBestPackings/5x15_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>16</td><td>0.38809284</td><td>0.38297084</td><td>hlc</td><td><a href="CurrentBestPackings/5x16_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>17</td><td>0.39353551</td><td>0.38729833</td><td>hlc</td><td><a href="CurrentBestPackings/5x17_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>18</td><td>0.39763025</td><td>0.39107694</td><td>dgm</td><td><a href="CurrentBestPackings/5x18_dgm.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>19</td><td>0.39763025</td><td>0.39440532</td><td>AUTO</td><td><a href="CurrentBestPackings/5x19_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>20</td><td>0.39763025</td><td>0.39735971</td><td>JJ</td><td><a href="CurrentBestPackings/5x20_JJ.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>21</td><td>0.40000000</td><td>0.40000000</td><td>etf</td><td><a href="CurrentBestPackings/5x21_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>22</td><td>0.40824829</td><td>0.40237391</td><td>AUTO</td><td><a href="CurrentBestPackings/5x22_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>23</td><td>0.40824829</td><td>0.40451992</td><td>AUTO</td><td><a href="CurrentBestPackings/5x23_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>24</td><td>0.40824829</td><td>0.40646942</td><td>AUTO</td><td><a href="CurrentBestPackings/5x24_AUTO.txt">File</a></td><td>&#9651;</td></tr>
<tr><td>5</td><td>25</td><td>0.40824829</td><td>0.40824829</td><td>etf</td><td><a href="CurrentBestPackings/5x25_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>26</td><td>0.44721360</td><td>0.44721360</td><td>AUTO</td><td><a href="CurrentBestPackings/5x26_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>27</td><td>0.44721360</td><td>0.44721360</td><td>AUTO</td><td><a href="CurrentBestPackings/5x27_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>28</td><td>0.44721360</td><td>0.44721360</td><td>AUTO</td><td><a href="CurrentBestPackings/5x28_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>29</td><td>0.44721360</td><td>0.44721360</td><td>AUTO</td><td><a href="CurrentBestPackings/5x29_AUTO.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>30</td><td>0.44721360</td><td>0.44721360</td><td>orth</td><td><a href="CurrentBestPackings/5x30_orth.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>31</td><td>0.48159568</td><td>0.45291081</td><td>hlc</td><td><a href="CurrentBestPackings/5x31_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>32</td><td>0.48688165</td><td>0.45812285</td><td>hlc</td><td><a href="CurrentBestPackings/5x32_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>33</td><td>0.49101569</td><td>0.46291005</td><td>hlc</td><td><a href="CurrentBestPackings/5x33_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>34</td><td>0.49721217</td><td>0.46732302</td><td>jrr</td><td><a href="CurrentBestPackings/5x34_jrr.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>35</td><td>0.49998890</td><td>0.47140452</td><td>AUTO</td><td><a href="CurrentBestPackings/5x35_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>36</td><td>0.49998890</td><td>0.47519096</td><td>AUTO</td><td><a href="CurrentBestPackings/5x36_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>37</td><td>0.49998890</td><td>0.47871355</td><td>AUTO</td><td><a href="CurrentBestPackings/5x37_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>38</td><td>0.49998890</td><td>0.48199920</td><td>jrr</td><td><a href="CurrentBestPackings/5x38_jrr.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>39</td><td>0.50000000</td><td>0.48507125</td><td>AUTO</td><td><a href="CurrentBestPackings/5x39_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>40</td><td>0.50000000</td><td>0.48795004</td><td>AUTO</td><td><a href="CurrentBestPackings/5x40_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>41</td><td>0.50000000</td><td>0.49065338</td><td>AUTO</td><td><a href="CurrentBestPackings/5x41_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>42</td><td>0.50000000</td><td>0.49319696</td><td>AUTO</td><td><a href="CurrentBestPackings/5x42_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>43</td><td>0.50000000</td><td>0.49559463</td><td>AUTO</td><td><a href="CurrentBestPackings/5x43_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>44</td><td>0.50000000</td><td>0.49785866</td><td>AUTO</td><td><a href="CurrentBestPackings/5x44_AUTO.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>45</td><td>0.50000000</td><td>0.50000000</td><td>Lev</td><td><a href="CurrentBestPackings/5x45_Lev.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>5</td><td>46</td><td>0.52188522</td><td>0.50202841</td><td>jrr</td><td><a href="CurrentBestPackings/5x46_jrr.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>47</td><td>0.53699561</td><td>0.50395263</td><td>jrr</td><td><a href="CurrentBestPackings/5x47_jrr.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>48</td><td>0.54097140</td><td>0.50578054</td><td>hlc</td><td><a href="CurrentBestPackings/5x48_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>49</td><td>0.54276167</td><td>0.50751922</td><td>jrr</td><td><a href="CurrentBestPackings/5x49_jrr.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>50</td><td>0.55173030</td><td>0.50917508</td><td>hlc</td><td><a href="CurrentBestPackings/5x50_hlc.txt">File</a></td><td></td></tr>
<tr><td>5</td><td>85</td><td>0.57735027</td><td>0.54006172</td><td>BGMP</td><td><a href="CurrentBestPackings/5x85_BGMP.txt">File</a></td><td>&#9651;[BGM+22]</td></tr>
<tr><td>6</td><td>8</td><td>0.22400924</td><td>0.22400924</td><td>B-C</td><td><a href="CurrentBestPackings/6x8_B-C.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>9</td><td>0.25000000</td><td>0.25000000</td><td>etf</td><td><a href="CurrentBestPackings/6x9_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>10</td><td>0.27220315</td><td>0.27216553</td><td>hlc</td><td><a href="CurrentBestPackings/6x10_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>11</td><td>0.28867513</td><td>0.28867513</td><td>etf</td><td><a href="CurrentBestPackings/6x11_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>12</td><td>0.30151134</td><td>0.30151134</td><td>etf</td><td><a href="CurrentBestPackings/6x12_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>13</td><td>0.31182456</td><td>0.31180478</td><td>hlc</td><td><a href="CurrentBestPackings/6x13_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>14</td><td>0.32031664</td><td>0.32025631</td><td>hlc</td><td><a href="CurrentBestPackings/6x14_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>15</td><td>0.32739651</td><td>0.32732684</td><td>hlc</td><td><a href="CurrentBestPackings/6x15_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>16</td><td>0.33333333</td><td>0.33333333</td><td>etf</td><td><a href="CurrentBestPackings/6x16_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>17</td><td>0.33933198</td><td>0.33850160</td><td>jrr</td><td><a href="CurrentBestPackings/6x17_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>18</td><td>0.34498346</td><td>0.34299717</td><td>hlc</td><td><a href="CurrentBestPackings/6x18_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>19</td><td>0.34924778</td><td>0.34694433</td><td>bmem</td><td><a href="CurrentBestPackings/6x19_bmem.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>20</td><td>0.35203544</td><td>0.35043832</td><td>bmem</td><td><a href="CurrentBestPackings/6x20_bmem.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>21</td><td>0.35644714</td><td>0.35355339</td><td>hlc</td><td><a href="CurrentBestPackings/6x21_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>22</td><td>0.35955441</td><td>0.35634832</td><td>hlc</td><td><a href="CurrentBestPackings/6x22_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>23</td><td>0.36537169</td><td>0.35887028</td><td>hlc</td><td><a href="CurrentBestPackings/6x23_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>24</td><td>0.36998252</td><td>0.36115756</td><td>hlc</td><td><a href="CurrentBestPackings/6x24_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>25</td><td>0.37267800</td><td>0.36324158</td><td>AUTO</td><td><a href="CurrentBestPackings/6x25_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>26</td><td>0.37267800</td><td>0.36514837</td><td>AUTO</td><td><a href="CurrentBestPackings/6x26_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>27</td><td>0.37267800</td><td>0.36689969</td><td>AUTO</td><td><a href="CurrentBestPackings/6x27_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>28</td><td>0.37267800</td><td>0.36851387</td><td>AUTO</td><td><a href="CurrentBestPackings/6x28_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>29</td><td>0.37267800</td><td>0.37000643</td><td>AUTO</td><td><a href="CurrentBestPackings/6x29_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>30</td><td>0.37267800</td><td>0.37139068</td><td>AUTO</td><td><a href="CurrentBestPackings/6x30_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>31</td><td>0.37267800</td><td>0.37267800</td><td>etf</td><td><a href="CurrentBestPackings/6x31_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>32</td><td>0.37796447</td><td>0.37387825</td><td>AUTO</td><td><a href="CurrentBestPackings/6x32_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>33</td><td>0.37796447</td><td>0.37500000</td><td>AUTO</td><td><a href="CurrentBestPackings/6x33_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>34</td><td>0.37796447</td><td>0.37605072</td><td>AUTO</td><td><a href="CurrentBestPackings/6x34_AUTO.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>35</td><td>0.37796447</td><td>0.37703695</td><td>AUTO</td><td><a href="CurrentBestPackings/6x35_AUTO.txt">File</a></td><td>&#9651;</td></tr>
<tr><td>6</td><td>36</td><td>0.37796447</td><td>0.37796447</td><td>etf</td><td><a href="CurrentBestPackings/6x36_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>37</td><td>0.40824829</td><td>0.40824829</td><td>orth</td><td><a href="CurrentBestPackings/6x37_orth.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>6</td><td>38</td><td>0.41682055</td><td>0.40824829</td><td>hlc</td><td><a href="CurrentBestPackings/6x38_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>39</td><td>0.42274914</td><td>0.40824829</td><td>hlc</td><td><a href="CurrentBestPackings/6x39_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>40</td><td>0.42819149</td><td>0.40824829</td><td>jrr</td><td><a href="CurrentBestPackings/6x40_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>41</td><td>0.43077617</td><td>0.40824829</td><td>jrr</td><td><a href="CurrentBestPackings/6x41_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>42</td><td>0.43731047</td><td>0.40824829</td><td>hlc</td><td><a href="CurrentBestPackings/6x42_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>43</td><td>0.44190326</td><td>0.41217007</td><td>jrr</td><td><a href="CurrentBestPackings/6x43_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>44</td><td>0.44673518</td><td>0.41585133</td><td>jrr</td><td><a href="CurrentBestPackings/6x44_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>45</td><td>0.45132430</td><td>0.41931393</td><td>hlc</td><td><a href="CurrentBestPackings/6x45_hlc.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>46</td><td>0.45560317</td><td>0.42257713</td><td>jrr</td><td><a href="CurrentBestPackings/6x46_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>47</td><td>0.45924802</td><td>0.42565792</td><td>jrr</td><td><a href="CurrentBestPackings/6x47_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>48</td><td>0.46253866</td><td>0.42857143</td><td>jrr</td><td><a href="CurrentBestPackings/6x48_jrr.txt">File</a></td><td></td></tr>
<tr><td>6</td><td>49</td><td>0.46590261</td><td>0.43133109</td><td>jrr</td><td><a href="CurrentBestPackings/6x49_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>9</td><td>0.19601846</td><td>0.19428362</td><td>JJ</td><td><a href="CurrentBestPackings/7x9_JJ.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>10</td><td>0.22157245</td><td>0.21951220</td><td>hlc</td><td><a href="CurrentBestPackings/7x10_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>11</td><td>0.23931889</td><td>0.23904572</td><td>hlc</td><td><a href="CurrentBestPackings/7x11_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>12</td><td>0.25510428</td><td>0.25482360</td><td>hlc</td><td><a href="CurrentBestPackings/7x12_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>13</td><td>0.26727220</td><td>0.26726124</td><td>hlc</td><td><a href="CurrentBestPackings/7x13_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>14</td><td>0.27735010</td><td>0.27735010</td><td>etf</td><td><a href="CurrentBestPackings/7x14_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>7</td><td>15</td><td>0.28571429</td><td>0.28571429</td><td>etf</td><td><a href="CurrentBestPackings/7x15_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>7</td><td>16</td><td>0.29278206</td><td>0.29277002</td><td>jrr</td><td><a href="CurrentBestPackings/7x16_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>17</td><td>0.29883989</td><td>0.29880715</td><td>jrr</td><td><a href="CurrentBestPackings/7x17_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>18</td><td>0.30417036</td><td>0.30403450</td><td>hlc</td><td><a href="CurrentBestPackings/7x18_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>19</td><td>0.30884718</td><td>0.30860670</td><td>hlc</td><td><a href="CurrentBestPackings/7x19_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>20</td><td>0.31334596</td><td>0.31264095</td><td>hlc</td><td><a href="CurrentBestPackings/7x20_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>21</td><td>0.31729487</td><td>0.31622777</td><td>hlc</td><td><a href="CurrentBestPackings/7x21_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>22</td><td>0.32172806</td><td>0.31943828</td><td>hlc</td><td><a href="CurrentBestPackings/7x22_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>23</td><td>0.32539307</td><td>0.32232919</td><td>hlc</td><td><a href="CurrentBestPackings/7x23_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>24</td><td>0.32959971</td><td>0.32494624</td><td>hlc</td><td><a href="CurrentBestPackings/7x24_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>25</td><td>0.33247138</td><td>0.32732684</td><td>hlc</td><td><a href="CurrentBestPackings/7x25_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>26</td><td>0.33315439</td><td>0.32950179</td><td>hlc</td><td><a href="CurrentBestPackings/7x26_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>27</td><td>0.33331171</td><td>0.33149677</td><td>jrr</td><td><a href="CurrentBestPackings/7x27_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>28</td><td>0.33333333</td><td>0.33333333</td><td>etf</td><td><a href="CurrentBestPackings/7x28_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>7</td><td>29</td><td>0.34077885</td><td>0.33502970</td><td>jrr</td><td><a href="CurrentBestPackings/7x29_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>30</td><td>0.34639121</td><td>0.33660139</td><td>hlc</td><td><a href="CurrentBestPackings/7x30_hlc.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>31</td><td>0.34941560</td><td>0.33806170</td><td>jrr</td><td><a href="CurrentBestPackings/7x31_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>32</td><td>0.35229897</td><td>0.33942212</td><td>jrr</td><td><a href="CurrentBestPackings/7x32_jrr.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>33</td><td>0.35355339</td><td>0.34069257</td><td>AUTO</td><td><a href="CurrentBestPackings/7x33_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>34</td><td>0.35355339</td><td>0.34188173</td><td>AUTO</td><td><a href="CurrentBestPackings/7x34_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>35</td><td>0.35355339</td><td>0.34299717</td><td>AUTO</td><td><a href="CurrentBestPackings/7x35_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>36</td><td>0.35355339</td><td>0.34404556</td><td>AUTO</td><td><a href="CurrentBestPackings/7x36_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>37</td><td>0.35355339</td><td>0.34503278</td><td>AUTO</td><td><a href="CurrentBestPackings/7x37_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>38</td><td>0.35355339</td><td>0.34596404</td><td>AUTO</td><td><a href="CurrentBestPackings/7x38_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>39</td><td>0.35355339</td><td>0.34684399</td><td>AUTO</td><td><a href="CurrentBestPackings/7x39_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>40</td><td>0.35355339</td><td>0.34767675</td><td>AUTO</td><td><a href="CurrentBestPackings/7x40_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>41</td><td>0.35355339</td><td>0.34846603</td><td>AUTO</td><td><a href="CurrentBestPackings/7x41_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>42</td><td>0.35355339</td><td>0.34921515</td><td>AUTO</td><td><a href="CurrentBestPackings/7x42_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>43</td><td>0.35355339</td><td>0.34992711</td><td>AUTO</td><td><a href="CurrentBestPackings/7x43_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>44</td><td>0.35355339</td><td>0.35060460</td><td>AUTO</td><td><a href="CurrentBestPackings/7x44_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>45</td><td>0.35355339</td><td>0.35125009</td><td>AUTO</td><td><a href="CurrentBestPackings/7x45_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>46</td><td>0.35355339</td><td>0.35186578</td><td>AUTO</td><td><a href="CurrentBestPackings/7x46_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>47</td><td>0.35355339</td><td>0.35245369</td><td>AUTO</td><td><a href="CurrentBestPackings/7x47_AUTO.txt">File</a></td><td></td></tr>
<tr><td>7</td><td>48</td><td>0.35355339</td><td>0.35301567</td><td>AUTO</td><td><a href="CurrentBestPackings/7x48_AUTO.txt">File</a></td><td>&#9651;</td></tr>
<tr><td>7</td><td>49</td><td>0.35355339</td><td>0.35355339</td><td>etf</td><td><a href="CurrentBestPackings/7x49_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>8</td><td>15</td><td>0.25000000</td><td>0.25000000</td><td>etf</td><td><a href="CurrentBestPackings/8x15_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>8</td><td>16</td><td>0.25819889</td><td>0.25819889</td><td>etf</td><td><a href="CurrentBestPackings/8x16_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>8</td><td>57</td><td>0.33071891</td><td>0.33071891</td><td>etf</td><td><a href="CurrentBestPackings/8x57_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>8</td><td>64</td><td>0.33333333</td><td>0.33333333</td><td>etf</td><td><a href="CurrentBestPackings/8x64_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>9</td><td>13</td><td>0.19245009</td><td>0.19245009</td><td>etf</td><td><a href="CurrentBestPackings/9x13_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>9</td><td>19</td><td>0.24845200</td><td>0.24845200</td><td>etf</td><td><a href="CurrentBestPackings/9x19_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>9</td><td>37</td><td>0.29397237</td><td>0.29397237</td><td>etf</td><td><a href="CurrentBestPackings/9x37_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>9</td><td>73</td><td>0.31426968</td><td>0.31426968</td><td>etf</td><td><a href="CurrentBestPackings/9x73_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>9</td><td>81</td><td>0.31622777</td><td>0.31622777</td><td>etf</td><td><a href="CurrentBestPackings/9x81_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>10</td><td>12</td><td>0.13896315</td><td>0.13896315</td><td>B-C</td><td><a href="CurrentBestPackings/10x12_B-C.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>10</td><td>16</td><td>0.20000000</td><td>0.20000000</td><td>njas</td><td><a href="CurrentBestPackings/10x16_njas.txt">File</a></td><td></td></tr>
<tr><td>10</td><td>19</td><td>0.22360680</td><td>0.22360680</td><td>etf</td><td><a href="CurrentBestPackings/10x19_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>10</td><td>25</td><td>0.25000000</td><td>0.25000000</td><td>etf</td><td><a href="CurrentBestPackings/10x25_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>10</td><td>91</td><td>0.30000000</td><td>0.30000000</td><td>etf</td><td><a href="CurrentBestPackings/10x91_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>10</td><td>100</td><td>0.30151134</td><td>0.30151134</td><td>etf</td><td><a href="CurrentBestPackings/10x100_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>11</td><td>23</td><td>0.22268089</td><td>0.22268089</td><td>etf</td><td><a href="CurrentBestPackings/11x23_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>11</td><td>121</td><td>0.28867513</td><td>0.28867513</td><td>etf</td><td><a href="CurrentBestPackings/11x121_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>12</td><td>16</td><td>0.14907120</td><td>0.14907120</td><td>etf</td><td><a href="CurrentBestPackings/12x16_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>12</td><td>23</td><td>0.20412415</td><td>0.20412415</td><td>etf</td><td><a href="CurrentBestPackings/12x23_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>12</td><td>45</td><td>0.25000000</td><td>0.25000000</td><td>etf</td><td><a href="CurrentBestPackings/12x45_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>12</td><td>144</td><td>0.27735010</td><td>0.27735010</td><td>etf</td><td><a href="CurrentBestPackings/12x144_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>13</td><td>169</td><td>0.26726124</td><td>0.26726124</td><td>etf</td><td><a href="CurrentBestPackings/13x169_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>14</td><td>16</td><td>0.10072316</td><td>0.10072316</td><td>B-C</td><td><a href="CurrentBestPackings/14x16_B-C.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>14</td><td>196</td><td>0.25819889</td><td>0.25819889</td><td>etf</td><td><a href="CurrentBestPackings/14x196_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>15</td><td>18</td><td>0.11111111</td><td>0.11111111</td><td>B-C</td><td><a href="CurrentBestPackings/15x18_B-C.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>15</td><td>225</td><td>0.25000000</td><td>0.25000000</td><td>etf</td><td><a href="CurrentBestPackings/15x225_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>16</td><td>21</td><td>0.12500000</td><td>0.12500000</td><td>etf</td><td><a href="CurrentBestPackings/16x21_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>16</td><td>80</td><td>0.23462896</td><td>0.22501758</td><td>jrr</td><td><a href="CurrentBestPackings/16x80_jrr.txt">File</a></td><td></td></tr>
<tr><td>16</td><td>256</td><td>0.24253563</td><td>0.24253563</td><td>etf</td><td><a href="CurrentBestPackings/16x256_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>18</td><td>20</td><td>0.07898736</td><td>0.07898736</td><td>B-C</td><td><a href="CurrentBestPackings/18x20_B-C.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>18</td><td>324</td><td>0.22941573</td><td>0.22941573</td><td>etf</td><td><a href="CurrentBestPackings/18x324_etf.txt">File</a></td><td>&#9675;</td></tr>
<tr><td>19</td><td>361</td><td>0.22360680</td><td>0.22360680</td><td>etf</td><td><a href="CurrentBestPackings/19x361_etf.txt">File</a></td><td>&#9675;</td></tr>
    </tbody>
  </table>
</div>
<div><p>Last updated: 2026-01-19.</p></div>



<!--End table-->


<h3>Code</h3>
<p>See the readme file in the Matlab directory.  We also encourage submission of code in other languages.  Please create a branch and add a directory named `LanguageTools` where `Language` is the language the code is written in.
<h3>Papers</h3>
<h4>Review Paper</h4>
<p>
[JKM19] John Jasper, Emily J. King, and Dustin G. Mixon: &ldquo;Game of Sloanes: Best known packings in complex projective space.&rdquo; <i>Wavelets and Sparsity XVIII</i>, <i>SPIE Proceedings</i> 11138, 416&ndash;425 <a href="http://arxiv.org/abs/1907.07848">[arXiv]</a></br>
</p>
<h4>Further Literature and Websites</h4>
<p>
[BGM+22] Dmitriy Bilyk, Alexey Glazyrin, Ryan Matzke, Josiah Park, and Oleksandr Vlasiuk: &ldquo;Optimal measures for $p$-frame energies on spheres.&rdquo; <i>Rev. Mat. Iberoam.</i> 38(4), 1129&ndash;1160 (2022)</br>
[CID+21] Diego Cuevas, Carlos Beltr&aacute;n, Ignacio Santamaria, V&iacute;t Tu&#269;ek, and Gunnar Peters: &ldquo;A Fast Algorithm for Designing Grassmannian Constellations.&rdquo; (2021) <a href="https://gtas.unican.es/files/pub/non_coherent_wsa21_full_paper.pdf">https://gtas.unican.es/files/pub/non_coherent_wsa21_full_paper.pdf</a>, <i>Conference: WSA 2021 - 25th International ITG Workshop on Smart Antennas</i></i></br>
[FM16] Matt Fickus and Dustin G. Mixon: &ldquo;Tables of the existence of equiangular tight frames.&rdquo; (2016) <a href="http://arxiv.org/abs/1504.00253">[arXiv]</a></br>
[Flamm] Steve Flammia: &ldquo;Exact SIC fiducial vectors.&rdquo; <a href="http://www.physics.usyd.edu.au/~sflammia/SIC/">http://www.physics.usyd.edu.au/~sflammia/SIC/</a></br>
[FrameOpt] Juan Rom&aacute;n-Roche: &ldquo;frameopt&rdquo; A suite of optimization algorithms and tools for the numerical construction of maximally orthogonal frames (MOFs) in complex space <a href="https://github.com/chuan97/frameopt">GitHub repository</a></br>
[FSDH] Christopher Fuchs, Blake Stacey, John DeBrota, and Michael Hoang: &ldquo;QBism: Quantum Theory as a Hero's Handbook: SIC-POVM Solutions.&rdquo; <a href="http://www.physics.umb.edu/Research/QBism/solutions.html">http://www.physics.umb.edu/Research/QBism/solutions.html</a></br>
[Grassl] Markus Grassl and Andrew J. Scott: &ldquo;SIC-POVMs&rdquo; <a href="http://sicpovm.markus-grassl.de/">http://sicpovm.markus-grassl.de/</a></br>
[KlRo04] Andreas Klappenecker and Martin R&ouml;tteler: &ldquo;Constructions of mutually unbiased bases.&rdquo; (2004) in <i>Finite fields and applications</i>, <i>Lecture Notes in Comput. Sci.</i> 2948, 137&ndash;144, Springer, Berlin. <a href="https://arxiv.org/abs/quant-ph/0309120">[arXiv]</a></br>
[MeDa14a] Ahmed Medra and Timothy N. Davidson: &ldquo;Flexible codebook design for limited feedback systems via sequential smooth optimization on the Grassmannian manifold.&rdquo; <i>IEEE Trans. Signal Process.</i> 62(5), 1305&ndash;1318 (2014)</br>
[MeDa14b] Ahmed Medra and Timothy N. Davidson: &ldquo;Flexible codebook design for limited feedback systems.&rdquo; <a href="http://www.ece.mcmaster.ca/~davidson/pubs/Flexible_codebook_design.html">http://www.ece.mcmaster.ca/~davidson/pubs/Flexible_codebook_design.html</a></br>
[Sloane1] Neil J. A. Sloane: &ldquo;Spherical codes.&rdquo; <a href="http://neilsloane.com/packings/">http://neilsloane.com/packings/</a></br>
[Sloane2] Neil J. A. Sloane: &ldquo;How to pack lines, planes, $3$-spaces, etc.&rdquo; <a href="http://neilsloane.com/grass/">http://neilsloane.com/grass/</a></br>
[TDHS05] Joel A. Tropp, Inderjit S. Dhillon, Robert W. Heath, Jr., and Thomas Strohmer: &ldquo;Designing structured tight frames via alternating projection.&rdquo; <i>IEEE Trans. Info. Theory</i> 51(1), 188&ndash;209 (2005)
</p>



