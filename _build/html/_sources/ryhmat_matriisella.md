# Yhtälöryhmät matriisimuodossa

Matriisilaskenta on tehokas menetelmä ratkaista yhtälöryhmiä. Voit kerrata [Lineaarialgebran](https://luma-lapinamk.github.io/minna-lineaarialgebra/yhtaloryhmat.html) oppikirjasta, kuinka yhtälöryhmä muutetaan matriisiyhtälöksi ja ratkaistaan. Alta löytyy lyhyt tiivistelmä aiheesta.

{admonition} Lyhyt kertaus
:class: tip, dropdown

Yhtälöryhmää

$\begin{equation} \begin{cases}
a_{11} x_1+a_{12} x_2+ \ldots +a_{1n} x_n=b_1 \\
a_{21} x_1+a_{22} x_2+\ldots +a_{2n} x_n=b_2 \\
\vdots \\
a_{m1} x_1+a_{m2} x_2+ \ldots +a_{mn} x_n=b_m \end{cases} \end{equation}$

vastaavat matriisiyhtälössä $AX=B$ matriisit

$A=\begin{bmatrix} a_{11}&a_{12}& \ldots &a_{1n} \\ a_{21}&a_{22}& \ldots &a_{2n}\\ \vdots & \vdots & \ddots & \vdots \\ a_{m1}&a_{m2}& \ldots &a_{mn}\end{bmatrix}, X=\begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n\end{bmatrix}$ ja $B=\begin{bmatrix} b_1 \\ b_2 \\ \vdots \\ b_m\end{bmatrix}$

ja tuntemattomat sisältä matriisi $X$ saadaan tästä selville laskemalla $X=A^{-1}B$, mikäli käänteismatriisi $A^{-1}$ on olemassa.

:::

Differentiaaliyhtälöryhmissä on yhtälöitä, joissa tuntemattomina ovat funktiot $x_1(t), x_2(t), \dots$ ja lisäksi yhtälöissä esiintyy näiden funktioiden derivaattoja $x_1'(t), x_2'(t), \dots$. Oletaan, että derivaatat voidaan esittää funktioiden avulla, eli esimerkiksi $x_1'=f(x_1, x_2, \dots)$ ja tarkemmin lineaarikombinaationa $x_1'= a_1 x_1'+a_2 x_2' + \dots$, missä $a_1, a_2 \dots$ ovat reaalilukuja. Tietyn funktion derivaatta ei kuitenkaan riipu minkään muun funktion derivaatasta!

Tällöin voidaan muodostaa seuraavat matriisit:

- funktioiden kertoimia sisältävä matriisi $A$, johon kerätään 1. riville 1. yhtälön kertoimet, 2. riville 2. yhtälön kertoimet jne.

- derivaatat sisältävä matriisi $X'=\begin{matrix} x_1' \\ x_2' \\ \vdots\end{bmatrix}$ 

- funktiot sisältävä matriisi $X=\begin{matrix} x_1 \\ x_2 \\ \vdots\end{bmatrix}$

Matriisimuodossa yhtälö on tällöin $X'=AX$.

::::{admonition} Esimerkki

Muodosta kerroinmatriisi $A$ yhtälöryhmälle

a) $\begin{equation} \begin{cases} x_1'=2x_1-2x_2 \\ x_2'=-x_1+3x_2 \end{cases} \end{equation}$

b) $\begin{equation} \begin{cases} 4 x_1 + 2x_1'+6 x_2=0 \\ x_2'+3x_1=x_2 \end{cases} \end{equation}$

:::{admonition} Ratkaisu
:class: tip, dropdown

a) Yhtälöryhmän $\begin{equation} \begin{cases} x_1'=2x_1-2x_2 \\ x_2'=-x_1+3x_2 \end{cases} \end{equation}$ kertoimista saadaan kerroinmatriisi $A$:

$A=\begin{\bmatrix}2 & -2 \\ -1 & 3\end{bmatrix}$

b) Järjestetään yhtälön termejä uudelleen, jolloin yhtälöryhmäksi saadaan:

$\begin{equation} \begin{cases} 2x_1'=-4x_1-6x_2 \\ x_2'=-3x_1+x_2 \end{cases} \end{equation}$

Ylempi yhtälö pitää vielä jakaa puolittain luvulla 2, jotta vasemmalle puolelle saadaan pelkkä $x_1'$:

$\begin{equation} \begin{cases} x_1'=-2x_1-3x_2 \\ x_2'=-3x_1+x_2 \end{cases} \end{equation}$

Nyt kerroinmatriisiksi saadaan

$A=\begin{\bmatrix}-2 & -3 \\ -3 & 1\end{bmatrix}$

:::

::::