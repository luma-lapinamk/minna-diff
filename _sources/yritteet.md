# Ratkaisu yritteellä

Lineaariselle ensimmäisen kertaluvun differentiaaliyhtälölle esitetyt ratkaisukaava sisältävät integraalifunktioita, jotka voivat olla hankalia laskea. Vakiokertoimiselle differentiaaliyhtälölle, joka siis on muotoa $y'=ay+g(x)$, on mahdollista löytää ratkaisu myös ikään kuin arvaamalla. Valitaan siis jokin funktio, jonka arvellaan toteuttavan yhtälön, ja hienosäädetään funktion parametrejä laskemalla. Arvattua funktiota kutsutaan yritteeksi.

## Ratkaisun periaate

Olkoon $y_h=Ce^{ax}$ homogeenisen yhtälön $y'= ay$ yleinen ratkaisu. Etsitään täydelliselle yhtälölle $y'=ay+g(x)$ yritteen avulla jokin yksittäisratkaisu $y_t$. Täydellisen yhtälön $y'=ay+g(x)$ ratkaisu saadaan muodossa $y_h+y_t$. 

## Yritteet

Yritettä ei tarvitse joka ongelmassa arvata erikseen. Yritteen valinta perustuu funktion $g(x)$ muotoon. Apua löytyy seuraavasta taulukosta:

| $g(x)$ | Yrite |
|--------|-------|
| vakio  | $A$   |
|polynomi $a+bx+cx^2+ \ldots$| saman asteluvun polynomi $A+Bx^2+Cx^2+\ldots$|
|$e^{ax}$  | $Ae^{ax}$ |
|$\sin{ax}$ tai $\cos{ax}$ | $A \sin{ax} + B \cos{ax}$|

Lisäksi jos funktio $g(x)$ muodostuu taulukossa mainittujen funktioiden summasta tai tulosta, niin vastaavasti yritefunktio on samoja funktioita vastaavien yritefunktioiden summa tai tulo.

Taulukossa tuntemattomia ovat kertoimet $A, B, \ldots$. Niille löydetään sopivat arvot sijoittamalla yritefunktio differentiaaliyhtälöön ja tutkimalla alkuehtoja.

**Esim.** Ratkaise differentiaaliyhtälö $y'-4y=5x$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Differentiaaliyhtälö voidaan muokata muotoon $y'=4y+5x$ eli kyseessä on epähomogeeninen, vakiokertoiminen differentiaaliyhtälö.

Ratkaistaan ensin vastaava homogeeninen differentiaaliyhtälö $y'=4y$. Ratkaisu tälle löytyy kaavalla $y(x)=Ce^{ax}$. Kyseessä on nyt ratkaisu $y_h$.

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

**Esim.** Ratkaise differentiaaliyhtälö $y'+4y=1+t+3e^{3t}$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Ratkaistaan ensin homogeeninen yhtälö $y'=-4y$. Kaavan mukaan ratkaisu tälle on $y_h=C_1e^{-4t}$.

Muodostetaan yrite funktion $g(t)=1+t+3e^{3t}$ avulla. Termit $1+t$ muodostavat ensimmäisen asteen polynomifunktion, joten yritteeseen tulee osa $A+Bt$. Viimeistä termiä vastaava yritefunktio on $Ce^{3t}$. Yritteeksi sopii siis $A+Bt+Ce^{3t}$. Funktion derivaatta on $B+3Ce^{3t}$. Sijoitetaan nämä alkuperäiseen yhtälöön:

$B+3Ce^{3t}+4(A+Bt+Ce^{3t})=1+t+3e^{3t}$

$B+3Ce^{3t}+4A+4Bt+4Ce^{3t}=1+t+3e^{3t}$

$B+4A + 4Bt + 7Ce^{3t} = 1+t+3e^{3t}$

Muodostetaan yhtälöryhmä:

$\begin{equation} \begin{cases} B+4A=1 \\ 4B=1 \\ 7C=3 \end{cases} \end{equation}$

Toisesta yhtälöstä saadaan heti $B=\frac{1}{4}$ ja kolmannesta yhtälöstä $C=\frac{3}{7}$. 

Ensimmäisestä yhtälöstä ratkeaa jo tiedossa olevan $B$:n avulla $A=\frac{1}{4}\left(1-\frac{1}{4}\right) = \frac{1}{4} \cdot \frac{3}{4} = \frac{3}{16}$.

Differentiaaliyhtälön ratkaisu on siis $y=y_h+y_t=Ce^{-4t}+\frac{3}{7}e^{3t}+\frac{1}{4}t+\frac{3}{16}$.

:::