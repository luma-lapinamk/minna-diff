<!-- #region -->
# Separoituvat differentiaaliyhtälöt

Separoituvat differentiaaliyhtälöt ovat muotoa $y'=\frac{f(x)}{g(y)}$ tai $y'=f(x)g(y)$. Yhtälötyypin nimi johtuu siitä, että yhtälön muuttujista $x$ ja $y$ riippuvat osat on mahdollista erottaa eli separoida toisistaan. Ratkaisu hahmottuu helposti, kun kirjoitetaan derivaatta $y'(x)$ muodossa $\frac{\text{d}y}{\text{d}x}$. Tässä muodossa derivaattaa voi käsitellä kuten murtolukua.

**Osamäärämuotoinen separoituva differentiaaliyhtälö**

Kun kirjoitetaan derivaatta edellä kuvatulla tavala, muodossa $y'=\frac{f(x)}{g(y)}$ oleva yhtälö muuttuu seuraavasti:

$\frac{\text{d}y}{\text{d}x} = \frac{f(x)}{g(y)}$

Kerrotaan molemmat puolet luvuilla ${\text{d}x}$ ja ${g(y)}$:

$g(y) \text{d}y = f(x)\text{d}x$

Nyt ratkaisu saadaan integroimalla yhtälö puolittain, toisin sanoen

$\int g(y)~\text{d}y + C_1 = \int f(x)~\text{d}x + C_2$,

missä reaaliluvut $C_1$ ja $C_2$ ovat integroimisvakioita. Vakiot voidaan yhdistää yhdeksi vakioksi $C$. Tällöin ratkaisu voidaan kirjoittaa muodossa

$g(y) = \int f(x) \text{d}x + C$,

josta lopulta voidaan selvittää kysytty funktio $y$.

**Tulomuotoinen separoituva differentiaaliyhtälö**

Vastaavasti jos yhtälö on muotoa $y'=f(x)g(y)$, sitä voidaan muokata seuraavasti:

$\frac{\text{d}y}{\text{d}x} = f(x) g(y) $

$\frac{\text{d}y}{g(y)} = f(x) {\text{d}x}$

Integroimalla puolittain saadaan

$\int \frac{1}{g(y)}~\text{d}y + C_1 = \int f(x)~\text{d}x + C_2$

ja vastaavasti kuin edellä,

$\int \frac{1}{g(y)}~\text{d}y = \int f(x)~\text{d}x + C$

josta voidaan lopulta ratkaista $y$.

:::{admonition} Laskukaavan perustelu toisella tavalla
:class: tip, dropdown
Johdetaan yhtälötyypille $y'=\frac{f(x)}{g(y)}$ ratkaisumenetelmä seuraavasti. Olkoon funktion $f(x)$ integraalifunktio $F(x)$ ja funktion $g(y)$ integraalifunktio $G(y)$. Kumpikin voidaan laskea integroimalla:

$F(x)= \int f(x) \,dx +C, G(y) = \int g(y) \,dx + D$, missä $C \in \Re, D \in \Re$.

Funktioille pätee $F'(x)=f(x)$ ja $G'(x)=g(x)$.

Seuraavaksi lähestytään ratkaisua takaperin: kokeillaan, mitä tapahtuu, kun derivoidaan puolittain yhtälö $G(y)=F(x)$. Yhtälön vasen puoli täytyy derivoida yhdistetyn funktion derivointikaavalla, sillä funktiossa $G(y)$ muuttuja $y$ riippuu muuttujasta $x$, siis $G(y)=G(y(x))$.

Yhdistetyn funktion derivointikaava: $\frac{\text{d}}{\text{d}x} G(y(x)) = G'(y(x)) \cdot y'(x)$

Yhtälö $G(y)=F(x)$ muuttuu siis muotoon

$G'(y(x)) \cdot y'(x) = F'(x)$

Tästä saadaan ratkaistua

$y'(x) = \frac{F'(x)}{G'(y(x))}$

eli

$y'(x) = \frac{f(x)}{g(y)}$.

Päättelyketjua takaisinpäin lukemalla voidaan siis todeta, että $y'(x) = \frac{f(x)}{g(y)}$ on yhtäpitävä yhtälön $G'(y)=F'(x)$ kanssa ja siten ratkeaa puolittain integroimalla.
:::

**Esim.** Ratkaise yhtälö $y'=\frac{4x}{y}$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö voidaan muokata muotoon

$\frac{\text{d}y}{\text{d}x}=\frac{4x}{y}$

ja edelleen muotoon

$y~\text{d}y = 4x~\text{d}x$.

Integroimalla puolittain saadaan

$y = \int 4x~\text{d}x$

josta selviää, että

$y=2x^2 + C$.

:::

**Esim.** Ratkaise yhtälö $y'=4xy$.

:::{admonition} Ratkaisu
:class: tip, dropdown
Kirjoitetaan yhtälö muodossa 

$\frac{\text{d}y}{\text{d}x}=4xy$.

Kerrotaan molemmat puolet luvulla $\text{d}x$, jolloin yhtälö muuttuu muotoon

$\text{d}y=4xy~\text{d}x$.

Edelleen jakamalla tekijällä $y$ yhtälö saadaan muotoon

$\frac{\text{d}y}{y}=4x~\text{dx}$.

Puolittain integroimalla saadaan

$\int \frac{1}{y}~\text{d}y = \int 4x~\text{d}x$, josta ratkeaa

$\ln{y} = 2x^2 + C$.

Funktio $y$ ratkeaa ylläolevasta yhtälöstä potenssiinkorotuksella:

$e^{\ln{y}}=e^{2x^2+C}$ eli $y=e^{2x^2+C}$.



:::

## Onko differentiaaliyhtälö separoituva?

Kaikki separoituvat differentiaaliyhtälöt eivät aluksi ole muodossa $y'=\frac{f(x)}{g(y)}$ tai $y'=f(x) g(y)$. Kuitenkin oikea puoli voidaan muuttaa jompaan kumpaan näistä muodoista. Käytännössä siis differentiaaliyhtälö on separoituva, jos yhtälön toisella puolella on ainoastaan $y'$, ja toinen puoli voidaan esittää tulona tai osamääränä, jonka kummassakin osassa esiintyy vain yhtä muuttujaa.

**Esim.** 

:::{admonition} Ratkaisu
:class: tip, dropdown
hmm...
:::
<!-- #endregion -->
