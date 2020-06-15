Analysis of dolphinfish catches in Pakistan
===========================================

Date: 6/14/2020

Motivation
----------

This document was prepared as a supplement to the review provided to A.
Baset, regarding the research article entitled “Maximum Sustainable
Yield of Dolphinfish, Coryphaena hippurus (Linnaeus, 1758) Fishery in
Pakistan”, available in
[Researchgate](https://www.researchgate.net/publication/342139244_Maximum_Sustainable_Yield_of_Dolphinfish_Coryphaena_hippurus_Linnaeus_1758_Fishery_in_Pakistan).
While the authors used the software CEDA (Catch Effort Data Analysis) to
fit three stock assessment models to dolphinfish catch-and-effort data
in Pakistan, here I use the `R` package
[`rcsurplus1d`](https://github.com/rtlemos/rcsurplus1d), by [Rankin and
Lemos
(2015)](https://www.researchgate.net/publication/279962333_An_alternative_surplus_production_model?_sg=VN8vMy1EvU8hSo7Fxzqaob_lVAwjzXROjHvcotff2oCFgmm3TVVVBGLz89dExHlwbt5gLlvtVOgihn8).

Data and models
---------------

The data are kindly provided by the authors, in Table 1. The models I
use are the same as Baset et al. (2020) – Schaeffer, Fox, and
Pella-Tomlinson –, plus the alternative model of Rankin and Lemos
(2015). For all models, I ran the MCMC for 100,000 iterations with 50%
burn-in and 1:10 thinning factor, resulting in 5,000 variates from the
posterior distribution.

Results
-------

Out of the four models, the Fox model provided the lowest value of DIC
(Table 1), which is why I will focus on it.

\*\*\* Table 1. Fox model summary
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Inference for Bugs model at “/tmp/RtmpZgSzFO/fox\_model.txt”,

Current: 1 chains, each with 10000 iterations (first 5000 discarded),
n.thin = 10

Cumulative: n.sims = 5000 iterations saved

<table>
<thead>
<tr class="header">
<th></th>
<th>mean</th>
<th>sd</th>
<th>2.50%</th>
<th>25.00%</th>
<th>50.00%</th>
<th>75.00%</th>
<th>97.50%</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>K</td>
<td>72510.1</td>
<td>18374.6</td>
<td>33289.5</td>
<td>59457.5</td>
<td>74965</td>
<td>87845</td>
<td>98650.2</td>
</tr>
<tr class="even">
<td>r</td>
<td>0.5</td>
<td>0.3</td>
<td>0</td>
<td>0.2</td>
<td>0.5</td>
<td>0.7</td>
<td>1</td>
</tr>
<tr class="odd">
<td>lq</td>
<td>-13</td>
<td>0.4</td>
<td>-13.6</td>
<td>-13.2</td>
<td>-13</td>
<td>-12.8</td>
<td>-12.1</td>
</tr>
<tr class="even">
<td>lsigma</td>
<td>-3.7</td>
<td>0.3</td>
<td>-4.3</td>
<td>-4</td>
<td>-3.8</td>
<td>-3.5</td>
<td>-3</td>
</tr>
<tr class="odd">
<td>MSY</td>
<td>1190.7</td>
<td>764.7</td>
<td>57.2</td>
<td>550.6</td>
<td>1107</td>
<td>1757.2</td>
<td>2747</td>
</tr>
<tr class="even">
<td>BMSY</td>
<td>26674.9</td>
<td>6759.7</td>
<td>12249.7</td>
<td>21870</td>
<td>27580</td>
<td>32320</td>
<td>36290</td>
</tr>
<tr class="odd">
<td>FMSY</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0.1</td>
<td>0.1</td>
</tr>
<tr class="even">
<td>mean[1]</td>
<td>-1.8</td>
<td>0.1</td>
<td>-2.1</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.8</td>
<td>-1.6</td>
</tr>
<tr class="odd">
<td>mean[2]</td>
<td>-1.8</td>
<td>0.1</td>
<td>-2</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.8</td>
<td>-1.6</td>
</tr>
<tr class="even">
<td>mean[3]</td>
<td>-1.7</td>
<td>0.1</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.7</td>
<td>-1.5</td>
</tr>
<tr class="odd">
<td>mean[4]</td>
<td>-1.7</td>
<td>0.1</td>
<td>-1.9</td>
<td>-1.7</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.4</td>
</tr>
<tr class="even">
<td>mean[5]</td>
<td>-1.6</td>
<td>0.1</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.6</td>
<td>-1.4</td>
</tr>
<tr class="odd">
<td>mean[6]</td>
<td>-1.6</td>
<td>0.1</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.5</td>
<td>-1.4</td>
</tr>
<tr class="even">
<td>mean[7]</td>
<td>-1.7</td>
<td>0.1</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.7</td>
<td>-1.5</td>
</tr>
<tr class="odd">
<td>mean[8]</td>
<td>-1.8</td>
<td>0.1</td>
<td>-2</td>
<td>-1.8</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
</tr>
<tr class="even">
<td>mean[9]</td>
<td>-1.7</td>
<td>0.1</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.5</td>
</tr>
<tr class="odd">
<td>mean[10]</td>
<td>-1.5</td>
<td>0.1</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.5</td>
<td>-1.5</td>
<td>-1.3</td>
</tr>
<tr class="even">
<td>mean[11]</td>
<td>-1.6</td>
<td>0.1</td>
<td>-1.8</td>
<td>-1.6</td>
<td>-1.6</td>
<td>-1.5</td>
<td>-1.3</td>
</tr>
<tr class="odd">
<td>mean[12]</td>
<td>-1.3</td>
<td>0.1</td>
<td>-1.5</td>
<td>-1.4</td>
<td>-1.3</td>
<td>-1.3</td>
<td>-1.1</td>
</tr>
<tr class="even">
<td>mean[13]</td>
<td>-1.3</td>
<td>0.1</td>
<td>-1.5</td>
<td>-1.3</td>
<td>-1.3</td>
<td>-1.2</td>
<td>-1.1</td>
</tr>
<tr class="odd">
<td>mean[14]</td>
<td>-1.3</td>
<td>0.1</td>
<td>-1.5</td>
<td>-1.4</td>
<td>-1.3</td>
<td>-1.2</td>
<td>-1.1</td>
</tr>
<tr class="even">
<td>mean[15]</td>
<td>-1.5</td>
<td>0.1</td>
<td>-1.7</td>
<td>-1.5</td>
<td>-1.5</td>
<td>-1.4</td>
<td>-1.2</td>
</tr>
<tr class="odd">
<td>mean[16]</td>
<td>-1.6</td>
<td>0.1</td>
<td>-1.8</td>
<td>-1.6</td>
<td>-1.6</td>
<td>-1.5</td>
<td>-1.3</td>
</tr>
<tr class="even">
<td>mean[17]</td>
<td>-1.6</td>
<td>0.1</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.6</td>
<td>-1.4</td>
</tr>
<tr class="odd">
<td>mean[18]</td>
<td>-1.7</td>
<td>0.1</td>
<td>-1.9</td>
<td>-1.7</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.5</td>
</tr>
<tr class="even">
<td>mean[19]</td>
<td>-1.7</td>
<td>0.1</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
<td>-1.5</td>
</tr>
<tr class="odd">
<td>mean[20]</td>
<td>-1.8</td>
<td>0.1</td>
<td>-2.1</td>
<td>-1.9</td>
<td>-1.8</td>
<td>-1.7</td>
<td>-1.6</td>
</tr>
<tr class="even">
<td>deviance</td>
<td>-18.3</td>
<td>6.1</td>
<td>-29.1</td>
<td>-22.7</td>
<td>-18.7</td>
<td>-14.5</td>
<td>-5.1</td>
</tr>
</tbody>
</table>

DIC info (using the rule, pD = Dbar-Dhat)

pD = 6.6 and DIC = -11.8

DIC is an estimate of expected predictive error (lower deviance is
better).

------------------------------------------------------------------------

All models struggled to provide a narrow distribution for the carrying
capacity parameter K (Figure 1).

![Figure 1. Posterior distribution of the carrying capacity parameter
K.](figures/K.png)

Figure 1. Posterior distribution of the carrying capacity parameter K.

With the exception of the Fox model, the posterior distribution of MSY
displayed a heavy right tail (Figures 2a and 2b), signalling
considerable uncertainty about this quantity.

![Figure 2a. Posterior distribution of MSY.](figures/MSY.png)

Figure 2a. Posterior distribution of MSY.

![Figure 2b. Posterior distribution of MSY for the Fox model
only.](figures/MSY2.png)

Figure 2b. Posterior distribution of MSY for the Fox model only.

Models differed in terms of their estimates of *B*<sub>*M**S**Y*</sub>,
with the Fox model providing higher density between 30 and 35 thousand
tonnes.

![Figure 3. Posterior distribution of the carrying capacity parameter
K.](figures/BMSY.png)

Figure 3. Posterior distribution of the carrying capacity parameter K.

The Fox model provided a slightly lower posterior mean for the
log-transformed measurement error variance parameter *σ* (Figure 4).

![Figure 4. Posterior distribution of the log-transformed value of
*σ*.](figures/log_sigma.png)

Figure 4. Posterior distribution of the log-transformed value of *σ*.

Models were mostly in good agreement regarding the log-catchability
parameter *χ*, although the Fox model provided slightly lower estimates
(Figure 5).

![Figure 5. Posterior distribution of log-catchability
*χ*.](figures/chi.png)

Figure 5. Posterior distribution of log-catchability *χ*.

Finally, in terms of fit, the Fox model is again the only model that
provides slightly different estimates, which appear to fit the data a
little better (Figure 6).

![Figure 6. Model fits.](figures/fit.png)

Figure 6. Model fits (lines) to observed CPUE (black circles).

With respect to initial (i.e., 1990) depletion, the Fox model estimates
it around 16.5%, with 95% credibility interval (13.5%, 22.3%). These
numbers were obtained by exponentiating the values of `mean[1]` in Table
1.

### Conclusion

In comparison to CEDA, package `rcsurplus1d` provides closer fits to the
data (compare Fig 7 above with Fig 1 of Baset et al., 2020). The Fox
model appears to provide slightly better estimates overall, and its 95%
CI for MSY is (57.2 t, 2747.0 t), with mean equal to 1190 tonnes. There
is some overlap with the MSY estimates provided by Baset et al. (2020),
although the mean provided by their models is higher. The initial
depletion estimated here (16.5%) is also lower than the 30% value
selected by Baset et al. (2020).
