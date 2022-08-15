<!-- #region -->
# Separoituvat differentiaaliyhtälöt

Separoituvat differentiaaliyhtälöt ovat muotoa $y'=\frac{f(x)}{g(y)}$ tai $y'=f(x)g(y)$. Yhtälötyypin nimi johtuu siitä, että yhtälön muuttujista $x$ ja $y$ riippuvat osat on mahdollista erottaa eli separoida toisistaan.

Ratkaisu hahmottuu helposti, kun kirjoitetaan derivaatta $y'(x)$ muodossa $\frac{\text{d}y}{\text{d}x}$. Tässä muodossa derivaattaa voi käsitellä kuten murtolukua.


## Osamäärämuotoinen separoituva differentiaaliyhtälö

Kun kirjoitetaan derivaatta edellä kuvatulla tavalla, yhtälö muuttuu seuraavasti:

$y'=\frac{f(x)}{g(y)} \leftrightarrow \frac{\text{d}y}{\text{d}x} = \frac{f(x)}{g(y)}$.

Kerrotaan molemmat puolet luvuilla ${\text{d}x}$ ja ${g(y)}$, jolloin saadaan $g(y) \text{d}y = f(x)\text{d}x$

Nyt ratkaisu saadaan integroimalla yhtälö puolittain, toisin sanoen 

$\int g(y)~\text{d}y + C_1 = \int f(x)~\text{d}x + C_2$,

missä reaaliluvut $C_1$ ja $C_2$ ovat integroimisvakioita. Vakiot voidaan yhdistää yhdeksi vakioksi $C$. Tällöin ratkaisu voidaan kirjoittaa muodossa

$g(y) = \int f(x) \text{d}x + C$,

josta lopulta voidaan selvittää kysytty funktio $y$.

**Esim.** Ratkaise yhtälö $y'=\frac{4x}{y}$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö voidaan muokata muotoon

$\frac{\text{d}y}{\text{d}x}=\frac{4x}{y}$

ja edelleen muotoon

$y~\text{d}y = 4x~\text{d}x$.

Integroimalla puolittain saadaan

$\frac{1}{2} y^2 = \int 4x~\text{d}x$

josta selviää, että

$y=\sqrt{2 \cdot(2x^2 + C)}$.

Myös ratkaisu $y=-\sqrt{2 \cdot (2x^2 + C)}$ toteuttaa alkuperäisen yhtälön.

:::

## Tulomuotoinen separoituva differentiaaliyhtälö

Vastaavasti jos yhtälö on muotoa $y'=f(x)g(y)$, sitä voidaan muokata seuraavasti:

$\frac{\text{d}y}{\text{d}x} = f(x) g(y) \leftrightarrow \frac{\text{d}y}{g(y)} = f(x) {\text{d}x}$

Integroimalla puolittain saadaan $\int \frac{1}{g(y)}~\text{d}y + C_1 = \int f(x)~\text{d}x + C_2$

ja vastaavasti kuin edellä, $\int \frac{1}{g(y)}~\text{d}y = \int f(x)~\text{d}x + C$

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

**Esim.** Ratkaise yhtälö $y'=4xy$.

:::{admonition} Ratkaisu
:class: tip, dropdown
Kirjoitetaan yhtälö muodossa $\frac{\text{d}y}{\text{d}x}=4xy$.

Kerrotaan molemmat puolet luvulla $\text{d}x$, jolloin yhtälö muuttuu muotoon $\text{d}y=4xy~\text{d}x$.

Edelleen jakamalla tekijällä $y$ yhtälö saadaan muotoon $\frac{\text{d}y}{y}=4x~\text{dx}$.

Puolittain integroimalla saadaan 

$\int \frac{1}{y}~\text{d}y = \int 4x~\text{d}x$, 

josta ratkeaa $\ln{y} = 2x^2 + C$.

Funktio $y$ ratkeaa ylläolevasta yhtälöstä potenssiinkorotuksella:

$e^{\ln{y}}=e^{2x^2+C}$ eli $y=e^{2x^2+C}$.

:::

Separoituvia differentiaaliyhtälöitä esiintyy monenlaisissa fysiikan sovelluksissa. Tällöin hankalaa on differentiaaliyhtälön muodostaminen, ei niinkään ratkaiseminen.

**Esim.** Vene työnnetään liikkeelle alkunopeudella $v_0=5$ m/s. Ajassa $t_1=5$ s vene on siirtynyt matkan $x_1=12.5$ m. Kuinka pitkän matkan vene enintään liikkuu eli mikä on $\lim_{t\to \infty} x$, kun oletetaan ainoan liikkeen suuntaisen voiman, väliainevastuksen $F$, olevan suoraan verrannollinen nopeuteen? 

:::{admonition} Ratkaisu
:class: tip, dropdown

Newtonin 2. lain mukaan voima $F$ aiheuttaa kappaleelle, jonka massa on $m$, kiihtyvyyden $a$ siten, että $F=ma$, missä $a=\frac{\text{d}v}{\text{d}t}$. Siis $F=m \frac{\text{d}v}{\text{d}t}$. Lisäksi tehtävänannon perusteella tiedetään, että $F=-kv$.

Kirjoittamalla voimien määritelmät yhtä suuriksi saadaan yhtälö $m \frac{\text{d}v}{\text{d}t}=-kv$

Yhtälö on separoituva ja muokkaantuu muotoon $\frac{\text{d}v}{v}=-\frac{k}{m}~\text{d}t$

Integroimalla puolittain saadaan $\ln{v}=-\frac{k}{m} t + C_1$ ja edelleen $v(t)=Ce^{-\frac{k}{m}t}$.

Sijoittamalla $v(0)=v_0$ saadaan ratkaistua vakio $C=v_0$, siis  $v(t)=v_0 e^{-\frac{k}{m}t}$.

Veneen nopeus $v(t)$ kuvaa paikan $x$ muutosta ajan $t$ suhteen, siis $v(t)=\frac{\text{d}x}{\text{d}t}$.

Tästä saadaan ratkaistua $v(t)~\text{d}t=1~\text{d}x$ eli $x=\int v(t)~\text{d}t = \int v_0 e^{-\frac{kt}{m}}~\text{d}t$. 

Integroinnin jälkeen ratkaisu on $x(t)=-\frac{v_0 m}{k} (e^{-\frac{kt}{m}}+C_2)$.

Sijoittamalla alkuehto $x(0)=0$ saadaan $C_2=-1$, joten yhtälö muuttuu muotoon $x(t)=\frac{v_0 m}{k} (1-e^{-\frac{kt}{m}})$.

Massan $m$ ja vakion $k$ arvoja ei voida määrittää pelkästään tästä yhtälöstä, mutta voidaan merkitä $b=\frac{m}{k}$ ja laskea tälle arvo yhtälöstä $x(t)=v_0 b (1-e^{-\frac{t}{b}})$.

Sijoittamalla annetut lukuarvot saadaan yhtälö $12.5=5\cdot b (1-e^{-\frac{5}{b}})$ josta voidaan esim. WolframAlphalla selvittää $b=3.14$. 

Nyt voidaan laskea $\lim_{t\to \infty} x(t) = \lim_{t\to \infty} 5\cdot 3.14 (1-e^{-\frac{t}{3.14}}) = 5\cdot 3.14 = 15.7$.

:::