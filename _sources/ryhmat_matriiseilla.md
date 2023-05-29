# Yhtälöryhmät matriisimuodossa

Matriisilaskenta on tehokas menetelmä ratkaista yhtälöryhmiä. Voit kerrata [Lineaarialgebran](https://luma-lapinamk.github.io/minna-lineaarialgebra/yhtaloryhmat.html) oppikirjasta, kuinka yhtälöryhmä muutetaan matriisiyhtälöksi ja ratkaistaan. Alta löytyy lyhyt tiivistelmä aiheesta.

:::{admonition} Lyhyt kertaus
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

- derivaatat sisältävä matriisi $X'=\begin{bmatrix} x_1' \\ x_2' \\ \vdots\end{bmatrix}$ 

- funktiot sisältävä matriisi $X=\begin{bmatrix} x_1 \\ x_2 \\ \vdots\end{bmatrix}$

Matriisimuodossa yhtälö on tällöin $X'=AX$.

::::{admonition} Esimerkki

Muodosta kerroinmatriisi $A$ yhtälöryhmälle

a) $\begin{equation} \begin{cases} x_1'=2x_1-2x_2 \\ x_2'=-x_1+3x_2 \end{cases} \end{equation}$

b) $\begin{equation} \begin{cases} 4 x_1 + 2x_1'+6 x_2=0 \\ x_2'+3x_1=x_2 \end{cases} \end{equation}$

:::{admonition} Ratkaisu
:class: tip, dropdown

a) Yhtälöryhmän $\begin{equation} \begin{cases} x_1'=2x_1-2x_2 \\ x_2'=-x_1+3x_2 \end{cases} \end{equation}$ kertoimista saadaan kerroinmatriisi $A$:

$A=\begin{bmatrix}2 & -2 \\ -1 & 3\end{bmatrix}$

b) Järjestetään yhtälön termejä uudelleen, jolloin yhtälöryhmäksi saadaan:

$\begin{equation} \begin{cases} 2x_1'=-4x_1-6x_2 \\ x_2'=-3x_1+x_2 \end{cases} \end{equation}$

Ylempi yhtälö pitää vielä jakaa puolittain luvulla 2, jotta vasemmalle puolelle saadaan pelkkä $x_1'$:

$\begin{equation} \begin{cases} x_1'=-2x_1-3x_2 \\ x_2'=-3x_1+x_2 \end{cases} \end{equation}$

Nyt kerroinmatriisiksi saadaan

$A=\begin{bmatrix}-2 & -3 \\ -3 & 1\end{bmatrix}$

:::

::::

## Ratkaisun periaate

Aiemmin on opittu, että yleisesti differentiaaliyhtälön $x'=ax$ ratkaisu on $x(t)=ce^{at}$. Tällöin voidaan olettaa, että matriisiyhtälöllä $X'=AX$ on ratkaisu $X=\vec{\eta} e^{\lambda t}$, missä vektori $\vec{\eta}$ sisältää kertoimet $c_1, c_2, \dots$ eli

$\vec{\eta}=\begin{bmatrix}c_1 \\ c_2 \\ \vdots\end{bmatrix}$

Huom! Voitaisiin merkitä myös $\eta$ ilman vektorimerkkinä, matriisina. Tässä tapauksessa kuitenkin kyseessä on olio nimeltä ominaisvektori, joten merkitään sitä vektorina.

Ratkaisun $X=\vec{\eta} e^{\lambda t}$ derivaatta on $X'=\vec{\eta}\lambda e^{\lambda t}$. Derivaattamatriisi on muodostettu ikään kuin laskettaisiin vektorin $\vec{\eta} e^{\lambda t}$ alkioiden derivaattoja normaalien derivointisääntöjen mukaan yksitellen.

Sijoittamalla edellä määritellyt $X'$ ja $X$ yhtälöön $X'=AX$ saadaan yhtälö: $\vec{\eta}\lambda e^{\lambda t}=A \vec{\eta}e^{\lambda t}$

Vaihdetaan puolet keskenään ja järjestellään termejä: $A \vec{\eta}e^{\lambda t}=\lambda \vec{\eta} e^{\lambda t}$

Jaetaan molemmat puolet lausekkeella $e^{\lambda t}$ (se ei koskaan saa arvoa nolla): $A \vec{\eta}=\lambda\vec{\eta}$

Kyseinen yhtälö on matriisin $A$ **ominaisarvoyhtälö**. Luku $\lambda$ on matriisin $A$ **ominaisarvo**, ja vektori $\vec{\eta}$ on matriisin $A$ **ominaisvektori**.

## Ratkaisujen muodostaminen

Ominaisarvoyhtälön ratkaisu on esitetty [Lineaarialgebran](https://luma-lapinamk.github.io/minna-lineaarialgebra/ominaisarvot.html) oppimateriaalissa. Lyhyesti sanottuna ominaisarvot lasketaan ratkaisemalla yhtälö $\det{(A-\lambda I)} = 0$ ja tämän jälkeen ominaisvektorit yhtälöstä $A \vec{\eta}=\lambda\vec{\eta}$. Jos olet parhaillaan differentiaaliyhtälöiden opintojaksolla, ei huolta - opettelemme menetelmän tunnilla sitten kun se on ajankohtaista. 

:::{admonition} Ratkaisu tietokoneella
:class: tip, dropdown

Ominaisarvot ja ominaisvektorit voi laskea myös tietokoneella. Octavella komento on seuraavaa muotoa:

[ov,oa]=eig(A)

- ov on matriisi, jonka sarakkeissa on ominaisvektorit 

- oa on matriisi, jonka lävistäjällä ovat ominaisarvot

Esimerkiksi komennolla [ov,ov]=eig([1,2;3,0]) saadaan seuraava tulos:

>ov = [0.7071  -0.5547;0.7071   0.8321]

>oa = [3   0;0  -2]

Tulos tarkoittaa seuraavaa:

- matriisilla on ominaisarvo $\lambda_1=3$ ja sitä vastaa ominaisvektori $\vec{\eta_1}=\begin{bmatrix} 0.707 \\ 0.707\end{bmatrix}$ 

- matriisilla on myös ominaisarvo $\lambda_2=-2$ ja sitä vastaa ominaisvektori $\vec{\eta_2}=\begin{bmatrix} -0.5547 \\ 0.8321\end{bmatrix}$ 

Ominaisvektorien luvut ovat pyöristettyjä eivätkä tarkkoja arvoja. Käsin laskemalla saataisiin tarkat arvot. Octave skaalaa ominaisvektorit siten, että niiden itseisarvo on yksi. Jokaista ominaisarvoa vastaa itse asiassa äärettömän monta ominaisvektoria; ne ovat yhdensuuntaisia, mutta eri pituisia vektoreita.

:::


Ominaisarvojen $\lambda_1, \lambda_2, \dots$ ja ominaisvektorien $\vec{\eta_1}, \vec{\eta_2}, \dots$ avulla voidaan nyt ilmaista differentiaaliyhtälöryhmän ratkaisu seuraavasti:

$\begin{bmatrix} x_1 \\ x_2 \\ \vdots\end{bmatrix} = c_1 e^{\lambda_1 t} \vec{\eta_1} + c_2 e^{\lambda_2t} \vec{\eta_2} + \dots$

Kyseessä ovat yleiset ratkaisut. Jos halutaan yksittäisratkaisuja, niin kertoimet $c_1, c_2, \dots$ pitää ratkaista joistakin annetuista alkuehdoista.

::::{admonition} Esimerkki

Ratkaistaan matriisimenetelmällä differentiaaliyhtälöpari

$\begin{equation}\begin{cases}x_1'=4x_1+7x_2 \\ x_2'=-2x_1-5x_2\end{cases}\end{equation}$

Muodostetaan ensin matriisiyhtälö. Sitten etsitään kerroinmatriisin ominaisarvot ja ominaisvektorit. Sitten kootaan tuloksista yhtälöparin ratkaisu. Ennen kuin katsot ratkaisun, mieti hieman, mitä tekisit näissä eri vaiheissa. 

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälöpari vastaa matriisiyhtälöä 

$\begin{bmatrix} x_1' \\ x_2' \end{bmatrix} = \begin{bmatrix} 4 & 7 \\ -2 & 5\end{bmatrix} \begin{bmatrix} x_1' \\ x_2' \end{bmatrix}$

Kerroinmatriisi on siis $\begin{bmatrix} 4 & 7 \\ -2 & 5\end{bmatrix}$. 

Tämän matriisin ominaisarvot ovat $\lambda_1 = -3$ ja $\lambda_2=2$. Ne voidaan selvittää esimerkiksi Octavella.

Ominaisvektorien laskeminen käsin on hieman haastavampaa. Todetaan, että tämän matriisin ominaisvektoreiksi voidaan valita esimerkiksi 

$\vec{\eta_1}=\begin{bmatrix} -1 \\ 1 \end{bmatrix}$ ja $\vec{\eta_2}=\begin{bmatrix} -\frac{7}{2} \\ 1 \end{bmatrix}$. 

Voit halutessasi tarkistaa, että yhtälö $A \vec{\eta}=\lambda\vec{\eta}$ on tosi, kun sijoitat sinne $\lambda_1$ ja $\vec{\eta_1}$ yhdessä, tai vaihtoehtoisesti $\lambda_2$ ja $\vec{\eta_2}$ yhdessä.

Tässä tapauksessa ratkaisuksi muodostuu siis

$\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = c_1 e^{-3 t} \begin{bmatrix} -1 \\ 1 \end{bmatrix} + c_2e^{2t} \begin{bmatrix} -\frac{7}{2} \\ 1 \end{bmatrix}$

Ratkaisun voi sieventää pois matriisimuodosta normaaleilla matriisien laskutoimituksella:

$\begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} - c_1 e^{-3 t} -\frac{7}{2} c_2e^{2t} \\ c_1 e^{3t} - c_2 e^{2t} \end{bmatrix}$

ja tästä päästään yhtälöparin muodossa esitettyyn ratkaisuun

$\begin{equation}\begin{cases}x_1=- c_1 e^{-3 t} -\frac{7}{2} c_2e^{2t}\\ x_2=c_1 e^{3t} - c_2 e^{2t}\end{cases}\end{equation}$

:::