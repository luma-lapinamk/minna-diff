# Mikä on differentiaaliyhtälö?

Differentiaaliyhtälöt ovat tärkeitä, kun tarkastellaan tilanteita, joissa jokin asia muuttuu. Esimerkkejä muuttuvista asioista ovat lämpötila (vaikkapa huonosti eristetyn talon sisällä kovalla pakkasella), väestön määrä (alueella, jonne pitäisi mahdollisesti kaavoittaa uusi asuinalue) ja kondensaattorista purkautuva sähköjännite (tietokoneen sisällä).

Aiemmin muutoksia ollaan tarkasteltu funktion derivaatan avulla. Differentiaaliyhtälöt ovatkin yhtälöitä, joissa esiintyy funktion derivaattoja. Funktiota merkitään usein $y$ tai $y(x)$ ja sen derivaattaa $y'$ tai $y'(x)$. Differentiaaliyhtälöistä ei ole tarkoitus ratkaista muuttujaa $x$, vaan funktio $y(x)$.

Differentiaaliyhtälössä voi esiintyä funktion derivaatan lisäksi funktio itse, funktion muuttuja ja vielä vakioitakin. Esimerkiksi yhtälö $y'+6=4x$ on differentiaaliyhtälö, jossa esiintyy funktion $y$ derivaatta $y'$, muuttuja $x$ ja vakiotermi $6$.  Esimerkki differentiaaliyhtälöstä, jossa on mukana myös itse funktio $y$, on $y^2=4y'-6y$.

## Differentiaaliyhtälön yleinen muoto

Yleisesti differentiaaliyhtälöitä voidaan merkitä muodossa $y'=f(x)$ tai $y'=f(y)$ tai $y'=f(x,y)$ . Toisin sanoen derivaatta $y'$ esitetään funktiona $f$, jonka lausekkeessa voi esiintyä muuttujaa $x$, funktiota $y$ tai molempia. Lausekkeessa voi esiintyä muuttujien summia, tuloja ja muitakin laskutoimituksia. Kaikkiin näihin tapauksiin kelpaa myös sellainen differentiaaliyhtälö, jossa derivaatan $y'$ esiintyy pelkkiä vakioita.

::::{admonition} Esimerkki

Keksi kolme esimerkkiä differentiaaliyhtälöistä, jotka ovat muotoa

a) $y'=f(x)$, b) $y'=f(y)$, c) $y'=f(x,y)$

:::{admonition} Ratkaisu
:class: tip, dropdown

a) Esim. $y'=4x$, $y'=3$, $y'=4x^2+3$

b) Esim. $y'=3y$, $y'=4y+3$, $y'=3y^2+5$

c) Esim. $y'=3xy$, $y'=2x+5y$, $y'=3x+y^2$

:::

::::

## Differentiaaliyhtälön kertaluku

Differentiaaliyhtälön **kertaluku** on korkein differentiaaliyhtälössä esiintyvä $y$:n derivaatta. Ensimmäisen kertaluvun differentiaaliyhtälö sisältää siis derivaatan $y'$ ja mahdollisesti itse funktion $y$, jonka voi ajatella "nollantena derivaattana". Toisen kertaluvun differentiaaliyhtälö sisältää toisen derivaatan $y''$ ja lisäksi se voi sisältää tai olla sisältämättä derivaatan $y'$ ja funktion $y$.

On tärkeää erottaa kertaluku potenssiinkorotuksesta. Yhtälössä voi olla mukana $y^2, y^3$ jne. mutta nämä eivät vaikuta differentiaaliyhtälön kertalukuun. Myös derivaattaa voidaan korottaa potenssiin, esimerkiksi $(y')^2$.

Ensimmäisen kertaluvun differentiaaliyhtälöitä ovat esimerkiksi 

* $y'+2x=4$, 

* $y ^2+3y'=5x+4$ ja 

* $(y')^2+=2x+3y$.

Toisen kertaluvun differentiaaliyhtälöitä ovat esimerkiksi 

* $y''+2y'+3yx=6$, 

* $3y''+2y=4x$ ja 

* $y''=4$.


## Differentiaaliyhtälön ratkaisut

Differentiaaliyhtälöiden ratkaisu perustuu integroimiseen. Integrointilaskuissa saadaan aina useampi kuin yksi ratkaisu. Esimerkiksi funktion $f(x)=2x+3$ integraalifunktioita ovat kaikki funktiot $F(x)=x^2+3x+C$, missä $C \in \Re$.

Vastaavasti differentiaaliyhtälöille voidaan löytää tällainen ns. **yleinen ratkaisu**, jossa vakiolle $C$ ei ole määrätty tiettyä arvoa. Jokainen $C$:n arvo vastaa yhtä **yksittäisratkaisua**. Haluttu yksittäisratkaisu löydetään jonkin funktiolle määrätyn ehdon perusteella. Lisäksi differentiaaliyhtälöllä voi olla **erikoisratkaisuja**, jotka eivät löydy yleisen ratkaisun perusteella. Niitä tarkastellaan myöhemmin tässä materiaalissa.

Differentiaaliyhtälön ratkaisu yhtälön tyypistä, joita tarkastellaan seuraavalla sivulla. Seuraavissa esimerkeissä riittää todeta sijoittamalla, että annettu ratkaisu toteuttaa differentiaaliyhtälön.

::::{admonition} Esimerkki

Osoita, että funktio $y=2x^2-6x+3$ toteuttaa differentiaaliyhtälön $y'+6=4x$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Muodostetaan funktion derivaatta: $y'=4x-6$

Sijoitetaan derivaatta annettuun yhtälöön ja sievennetään:

$4x-6+6=4x \Leftrightarrow 4x=4x \Leftrightarrow 0 = 0 $

Yhtälö on tosi millä tahansa arvolla $x$, joten annettu funktio toteuttaa differentiaaliyhtälön.

:::

::::

::::{admonition} Esimerkki

Osoita, että funktio $y=Ce^{2x^2}-\frac{5}{4}$ on yleinen ratkaisu differentiaaliyhtälölle $y'=4xy+5x$. Selvitä lisäksi, mikä yksittäisratkaisu toteuttaa ehdon $y(0)=1$.

:::{admonitio} Ratkaisu
:class: tip, dropdown

Muodostetaan funktion $y$ derivaatta: $y'=4x C e^{2x^2}$ eli $y'=4Cx e^{2x^2}$

Sijoitetaan $y$ ja $y'$ annettuun differentiaaliyhtälöön:

$4Cx e^{2x^2}=4x(Ce^{2x^2}-\frac{5}{4})+5x$

$4Cx e^{2x^2}=4Cxe^{2x^2}-\frac{20x}{4}+5x$

$4Cx e^{2x^2}=4Cxe^{2x^2}-5x+5x$

$4Cx e^{2x^2}=4Cxe^{2x^2}$

$0=0$

Jälleen yhtälö on tosi kaikilla $x$:n arvoilla. Yksittäisratkaisu etsitään ratkaisemalla vakio $C$ yhtälöstä $y(0)=1$:

$Ce^{2\cdot ^2}-\frac{5}{4}=1$

$Ce^0-\frac{5}{4}=1$

$C\cdot 1 - \frac{5}{4}=1$

$C=1+\frac{5}{4}$

$C=\frac{9}{4}$

Kysytty yksittäisratkaisu on siis $y=\frac{9}{4}e^{2x^2}-\frac{5}{4}$
:::
:::::