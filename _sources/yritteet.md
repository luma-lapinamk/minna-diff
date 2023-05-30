# Ratkaisu yritteellä

Lineaariselle ensimmäisen kertaluvun differentiaaliyhtälölle esitetyt ratkaisukaava sisältävät integraalifunktioita, jotka voivat olla hankalia laskea. Vakiokertoimiselle differentiaaliyhtälölle, joka siis on muotoa $y'=ay+g(x)$, on mahdollista löytää ratkaisu myös ikään kuin arvaamalla. Valitaan siis jokin funktio, jonka arvellaan toteuttavan yhtälön, ja hienosäädetään funktion parametrejä laskemalla. Arvattua funktiota kutsutaan yritteeksi.

## Ratkaisun periaate

Olkoon $y_h=Ce^{ax}$ homogeenisen yhtälön $y'= ay$ yleinen ratkaisu. Etsitään täydelliselle yhtälölle $y'=ay+g(x)$ yritteen avulla jokin yksittäisratkaisu $y_t$. Täydellisen yhtälön $y'=ay+g(x)$ ratkaisu saadaan muodossa $y_h+y_t$. Ratkaisun resepti on siis seuraava:

- Selvitä, mikä osa differentiaaliyhtälöstä muodostaa homogeenisen yhtälön

- Laske homogeenisen yhtälön ratkaisu $y_h$

- Muodosta yritefunktio $y_t$ alla olevien ohjeiden mukaan

- Sijoita funktio $y=y_h + y_t$ ja sen derivaatta $y'=y_h'+y_t'$ alkuperäiseen differentiaaliyhtälöön

## Yritteet

Yritettä ei tarvitse joka ongelmassa arvata erikseen. Yritteen valinta perustuu funktion $g(x)$ muotoon. Apua löytyy seuraavasta taulukosta:

| $g(x)$ | Yrite |
|--------|-------|
| vakio  | $A$   |
|polynomi $a+bx+cx^2+ \ldots$| saman asteluvun polynomi $A+Bx+Cx^2+\ldots$|
|$e^{ax}$  | $Ae^{ax}$ |
|$\sin{ax}$ tai $\cos{ax}$ | $A \sin{ax} + B \cos{ax}$|

Lisäksi jos funktio $g(x)$ muodostuu taulukossa mainittujen funktioiden summasta tai tulosta, niin vastaavasti yritefunktio on samoja funktioita vastaavien yritefunktioiden summa tai tulo.

Taulukossa tuntemattomia ovat kertoimet $A, B, \ldots$. Niille löydetään sopivat arvot sijoittamalla yritefunktio ja sen derivaatta differentiaaliyhtälöön ja tutkimalla alkuehtoja.

::::{admonition} Esimerkki

Ratkaise differentiaaliyhtälö $y'-4y=5x$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Differentiaaliyhtälö voidaan muokata muotoon $y'=4y+5x$ eli kyseessä on epähomogeeninen, vakiokertoiminen differentiaaliyhtälö.

Ratkaistaan ensin vastaava homogeeninen differentiaaliyhtälö $y'=4y$. Tälle löytyy ratkaisu $y(x)=Ce^{4x}$. Kyseessä on nyt ratkaisu $y_h$.

Etsitään sitten ratkaisu $y_t$ taulukon avulla. Nyt funktio $g(x)$ on polynomi $5x$, joten sopiva yrite on ensimmäisen asteen polynomi $y_t=A+Bx$. Huomaa, että vaikka funktiossa $g(x)$ ei ole vakiotermiä (se on siis muotoa $5x+0$), täytyy vakiotermi ottaa mukaan yritteeseen.

Sijoitetaan yritefunktio $y_t$ ja sen derivaatta $y_t'=B$ alkuperäiseen yhtälöön:

$y'-4y=5x$

$B-4(A+Bx)=5x$

$B-4A-4Bx=5x$

Sekä muuttujan $x$ kertoimen että vakiotermin tulee olla yhtälön molemmilla puolilla samat. Ratkaistaan siis yhtälöpari:

$\begin{equation} \begin{cases} B-4A = 0 \\ -4B=5 \end{cases} \end{equation}$

Jälkimmäisestä yhtälöstä saadaan suoraan $B=-\frac{5}{4}$. 

Sijoittamalla tämä ensimmäiseen yhtälöön saadaan $-\frac{5}{4}-4A=0$, josta ratkeaa $A=-\frac{5}{16}$.

Yritteen perusteella saatu ratkaisu on siis $y_t=-\frac{5}{16}-\frac{5}{4}x$. 

Yhtälön täydellinen ratkaisu on $y=y_h+y_t=Ce^{4x}-\frac{5}{4}x-\frac{5}{16}$.

:::

::::

::::{admonition} Esimerkki

Ratkaise differentiaaliyhtälö $y'+y=-2+t+5e^{3t}$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Ratkaistaan ensin homogeeninen yhtälö $y'=-y$. Ratkaisukaavan mukaan ratkaisu tälle on $y_h=C_1e^{-t}$.

Muodostetaan yrite funktion $g(t)=-2+t+5e^{3t}$ avulla. Termit $2+t$ muodostavat ensimmäisen asteen polynomifunktion, joten yritteeseen tulee osa $A+Bt$. Viimeistä termiä vastaava yritefunktio on $Ce^{3t}$. Yritteeksi sopii siis $A+Bt+Ce^{3t}$. Funktion derivaatta on $B+3Ce^{3t}$. Sijoitetaan nämä alkuperäiseen yhtälöön ja sievennetään:

$B+3Ce^{3t}+A+Bt+Ce^{3t}=-2+t+5e^{3t}$

$A+B + Bt + 4Ce^{3t} = -2+t+5e^{3t}$

Muodostetaan yhtälöryhmä:

$\begin{equation} \begin{cases} A+B=-2 \\ B=1 \\ 4C=5 \end{cases} \end{equation}$

Toisesta yhtälöstä saadaan heti $B=1$ ja kolmannesta yhtälöstä $C=\frac{5}{4}$. 

Ensimmäisestä yhtälöstä ratkeaa jo tiedossa olevan $B$:n avulla $A=-2-1=-3$.

Differentiaaliyhtälön ratkaisu on siis $y=y_h+y_t=C_1e^{-t}+\frac{5}{4}e^{3t}+t-3$.

:::

::::