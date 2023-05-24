# Separoituvat differentiaaliyhtälöt

Separoituvat differentiaaliyhtälöt ovat differentiaaliyhtälöitä, joissa derivaatta $y'$ on mahdollista esittää pelkästään $x$:stä (ja vakioista) riippuvan lausekkeen $f(x)$ ja pelkästään $y$:stä (ja vakioista) riippuvan lausekkeen $g(y)$ tulona tai osamääränä. Yhtälötyypin nimi johtuu siitä, että yhtälön muuttujista $x$ ja $y$ riippuvat osat on mahdollista erottaa eli separoida toisistaan.

Differentiaaliyhtälö on siis separoituva, jos $y'=f(x)g(y)$ tai $y'=\frac{f(x)}{g(y)}$.

::::{admonition} Esimerkki

Ovatko seuraavat differentiaaliyhtälöt separoituvia? Mitkä ovat näissä differentiaaliyhtälöissä $f(x)$ ja $g(y)$?

a) $y'=x+2y$, b) $y'=2xy$, c) $y'=\frac{x}{2y}$, d) $y'=2x+6xy$

:::{admonition} Ratkaisu
:class: tip, dropdown

a) Ei ole separoituva. 

b) On separoituva. Voidaan valita $f(x)=2x$ ja $g(y)=y$. Myös funktiot $f(x)=x$ ja $g(x)=2y$ tuottavat saman differentiaaliyhtälön.

c) On separoituva. Funktiot ovat $f(x)=x$ ja $g(y)=2y$. Toisaalta differentiaaliyhtälön voi ajatella olevan myös muodossa $f(x)g(y)$, missä  $f(x)=x$ ja $g(x)=\frac{1}{2y}$ tuottavat saman differentiaaliyhtälön.

d) On separoituva. Yhtälö voidaan sieventää muotoon $y'=2x(1+3y)$, jolloin $f(x)=2x$ ja $g(y)=1+3y$.

:::

::::

Separoituvan differentiaaliyhtälön ratkaisu perustuu siihen, että derivaatta $y'$ kirjoitetaan muodossa $\frac{\,dy}{\,dx}$. Tässä muodossa derivaattaa voi käsitellä kuten murtolukua. Siirretään kumpaankin muuttujaan liittyvä differentiaali omalle puolelleen yhtälöä. Järjestellään yhtälön $y$:stä ja $x$:stä riippuvat termit omille puolilleen yhtälöä. Lopuksi integroidaan yhtälön molemmat puolet. 

Ratkaisun vaiheet ja lopputulos näyttävät hieman erilaiselta riippuen siitä, onko differentiaaliyhtälössä funktioiden $f(x)$ ja $g(y)$ tulo vai osamäärä. Valmista ratkaisukaavaa kumpaankaan tapaukseen ei kannata opetella ulkoa, sillä ratkaisuun päätyy tavallisella yhtälön muokkaamisella. Seuraavaksi kuitenkaan esitetään näiden kahden eri tapauksen ratkaisujen yleinen muoto.

**1. Osamäärämuotoinen differentiaaliyhtälö $f(x)/g(y)$**

Kun kirjoitetaan derivaatta edellä kuvatulla tavalla, yhtälö muuttuu seuraavasti:

$y'=\frac{f(x)}{g(y)} \leftrightarrow \frac{\,dy}{\,dx} = \frac{f(x)}{g(y)}$.

Kerrotaan molemmat puolet termeillä ${\,dx}$ ja ${g(y)}$, jolloin saadaan $g(y) \,dy = f(x) \,dx$

Nyt ratkaisu saadaan integroimalla yhtälö puolittain, toisin sanoen 

$\int g(y) \,dy + C_1 = \int f(x) \,dx + C_2$,

missä reaaliluvut $C_1$ ja $C_2$ ovat integroimisvakioita. Vakiot voidaan yhdistää yhdeksi vakioksi $C$. Tällöin ratkaisu voidaan kirjoittaa muodossa

$g(y) = \int f(x) \,dx + C$,

josta lopulta voidaan selvittää kysytty funktio $y$.

::::{admonition} Esimerkki

Ratkaise yhtälö $y'=\frac{4x}{y}$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö voidaan muokata muotoon $\frac{\,dy}{\,dx}=\frac{4x}{y}$

ja edelleen muotoon $y~\,dy = 4x \,dx$.

Integroimalla puolittain saadaan $\int y~\,dy = \int 4x \,dx +C$

eli $\frac{1}{2} y^2 = 2x^2 + C$.

Tästä voidaan ratkaista $y^2 = 2\cdot(2x^2+C)$ 

ja edelleen $y=\sqrt{2 \cdot(2x^2 + C)}$.

Myös ratkaisu $y=-\sqrt{2 \cdot (2x^2 + C)}$ toteuttaa alkuperäisen yhtälön.

:::

::::

**2. Tulomuotoinen differentiaaliyhtälö $f(x)g(y)$**

Vastaavasti jos yhtälö on muotoa $y'=f(x)g(y)$, sitä voidaan muokata seuraavasti:

$\frac{\text{d}y}{\text{d}x} = f(x) g(y) \leftrightarrow \frac{\,dy}{g(y)} = f(x) {\,dx}$

Integroimalla puolittain saadaan $\int \frac{1}{g(y)} \,dy+ C_1 = \int f(x) \,dx + C_2$

ja vastaavasti kuin edellä, $\int \frac{1}{g(y)} \,dy = \int f(x) \,dx + C$

josta voidaan lopulta ratkaista $y$.

:::{admonition} Laskukaavan perustelu toisella tavalla
:class: tip, dropdown
Johdetaan yhtälötyypille $y'=\frac{f(x)}{g(y)}$ ratkaisumenetelmä seuraavasti. Olkoon funktion $f(x)$ integraalifunktio $F(x)$ ja funktion $g(y)$ integraalifunktio $G(y)$. Kumpikin voidaan laskea integroimalla:

$F(x)= \int f(x) \,dx +C, G(y) = \int g(y) \,dx + D$, missä $C \in \Re, D \in \Re$.

Funktioille pätee $F'(x)=f(x)$ ja $G'(x)=g(x)$.

Seuraavaksi lähestytään ratkaisua takaperin: kokeillaan, mitä tapahtuu, kun derivoidaan puolittain yhtälö $G(y)=F(x)$. Yhtälön vasen puoli täytyy derivoida yhdistetyn funktion derivointikaavalla, sillä funktiossa $G(y)$ muuttuja $y$ riippuu muuttujasta $x$, siis $G(y)=G(y(x))$.

Yhdistetyn funktion derivointikaava: $\frac{\text{d}}{\text{d}x} G(y(x)) = G'(y(x)) \cdot y'(x)$

Yhtälö $G(y)=F(x)$ muuttuu siis muotoon $G'(y(x)) \cdot y'(x) = F'(x)$

Tästä saadaan ratkaistua $y'(x) = \frac{F'(x)}{G'(y(x))}$

eli $y'(x) = \frac{f(x)}{g(y)}$.

Päättelyketjua takaisinpäin lukemalla voidaan siis todeta, että $y'(x) = \frac{f(x)}{g(y)}$ on yhtäpitävä yhtälön $G'(y)=F'(x)$ kanssa ja siten ratkeaa puolittain integroimalla.
:::

::::{admonition} Esimerkki

Ratkaise yhtälö $y'=4xy$.

:::{admonition} Ratkaisu
:class: tip, dropdown
Kirjoitetaan yhtälö muodossa $\frac{\,dy}{\,dx}=4xy$.

Kerrotaan molemmat puolet luvulla $\,dx$, jolloin yhtälö muuttuu muotoon $\,dy=4xy \,dx$.

Edelleen jakamalla tekijällä $y$ yhtälö saadaan muotoon $\frac{\,dy}{y}=4x \,dx$.

Puolittain integroimalla saadaan $\int \frac{1}{y} \,dy = \int 4x \,dx$, 

josta ratkeaa $\ln{y} = 2x^2 + C$.

Funktio $y$ ratkeaa ylläolevasta yhtälöstä potenssiinkorotuksella:

$e^{\ln{y}}=e^{2x^2+C}$ eli $y=e^{2x^2+C}$.

:::

::::

Separoituvia differentiaaliyhtälöitä esiintyy monenlaisissa fysiikan sovelluksissa. Tällöin hankalaa on differentiaaliyhtälön muodostaminen, ei niinkään ratkaiseminen.

::::{admonition} Esimerkki

Vene työnnetään liikkeelle alkunopeudella $v_0=5$ m/s. Ajassa $t_1=5$ s vene on siirtynyt matkan $x_1=12.5$ m. Kuinka pitkän matkan vene enintään liikkuu eli mikä on $\lim_{t\to \infty} x$, kun oletetaan ainoan liikkeen suuntaisen voiman, väliainevastuksen $F$, olevan suoraan verrannollinen nopeuteen? 

:::{admonition} Ratkaisu
:class: tip, dropdown

Newtonin 2. lain mukaan voima $F$ aiheuttaa kappaleelle, jonka massa on $m$, kiihtyvyyden $a$ siten, että $F=ma$, missä $a=\frac{\text{d}v}{\text{d}t}$. Siis $F=m \frac{\text{d}v}{\text{d}t}$. Lisäksi tehtävänannon perusteella tiedetään, että $F=-kv$.

Kirjoittamalla voimien määritelmät yhtä suuriksi saadaan yhtälö $m \frac{dv}{dt}=-kv$

Yhtälö on separoituva ja muokkaantuu muotoon $\frac{dv}{v}=-\frac{k}{m}~dt$

Integroimalla puolittain saadaan $\ln{v}=-\frac{k}{m} t + C_1$ ja edelleen $v(t)=Ce^{-\frac{k}{m}t}$.

Sijoittamalla $v(0)=v_0$ saadaan ratkaistua vakio $C=v_0$, siis  $v(t)=v_0 e^{-\frac{k}{m}t}$.

Veneen nopeus $v(t)$ kuvaa paikan $x$ muutosta ajan $t$ suhteen, siis $v(t)=\frac{dx}{dt}$.

Tästä saadaan ratkaistua $v(t)~\text{d}t=1~\text{d}x$ eli $x=\int v(t)~dt = \int v_0 e^{-\frac{kt}{m}}~dt$. 

Integroinnin jälkeen ratkaisu on $x(t)=-\frac{v_0 m}{k} (e^{-\frac{kt}{m}}+C_2)$.

Sijoittamalla alkuehto $x(0)=0$ saadaan $C_2=-1$, joten yhtälö muuttuu muotoon $x(t)=\frac{v_0 m}{k} (1-e^{-\frac{kt}{m}})$.

Massan $m$ ja vakion $k$ arvoja ei voida määrittää pelkästään tästä yhtälöstä, mutta voidaan merkitä $b=\frac{m}{k}$ ja laskea tälle arvo yhtälöstä $x(t)=v_0 b (1-e^{-\frac{t}{b}})$.

Sijoittamalla annetut lukuarvot saadaan yhtälö $12.5=5\cdot b (1-e^{-\frac{5}{b}})$ josta voidaan esim. WolframAlphalla selvittää $b=3.14$. 

Nyt voidaan laskea $\lim_{t\to \infty} x(t) = \lim_{t\to \infty} 5\cdot 3.14 (1-e^{-\frac{t}{3.14}}) = 5\cdot 3.14 = 15.7$.

:::

::::

::::{admonition} Esimerkki

Putoamisliikkeessä kappaleeseen vaikuttaa Maan vetovoima, josta kappale saa kiihtyvyyden $g\approx 9.81~\frac{\text{m}}{\text{s}
2}$. Jos ilmanvastusta ei huomioida, niin kappaleen nopeus sen pudotessa on $v(t)=\int g~dt+C=gt+C$, missä $C$ on kappaleen nopeus pudotuksen alussa.

Todellisuudessa kuitenkin moniin kappaleisiin vaikuttaa ilmanvastus, joka vähentää kiihtyvyyttä. Merkitään ilmanvastuksen aiheuttamaa kiihtyvyyttä $-kv$, missä $k > 0$ on kappaleen muodosta ja ilman ominaisuuksista riippuva vakio. (Oikeasti riippuvuus ei ole lineaarista, vaan muotoa $-kv^2$, mutta pienillä putoamismatkoilla tämä yksinkertaistus helpottaa laskemista huomattavasti.)

Kun ilmanvastus huomioidaan, kappaleen kokonaiskiihtyvyys on $v'(t)=g-kv$. Selvitä yleinen lauseke putoavan kappaleen nopeudelle $v(t)$. Selvitä myös yksittäisratkaisu erityistapauksessa, jossa $v(0)=0$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö $v'(t)=g-kv$ voidaan esittää tulomuodossa seuraavasti: $v'(t)=(g-kv)\cdot 1$. Nyt lauseke $g-kv$ riippuu nopeudesta $v$, ja lausekkeen $1$ voidaan ajatella liittyvän aikaan $t$, vaikka se ei lausekkeessa esiinnykään - tärkeintä on, että tässä lausekkeessa ei esiinny nopeutta $v$. 

Kirjoitetaan vielä $v'(t)$ toisin: $\frac{dv}{dt}=(g-kv)\cdot 1$

Yhtälö saadaan nyt muotoon $\frac{dv}{g-kv}=1~dt$

Yhtälön molemmat puolet voidaan nyt integroida, vasen puoli nopeuden suhteen ja oikea puoli ajan suhteen. Integraali on hieman hankala, mutta ratkaistavissa osamäärän integroinnin peruskaavoilla.

$\int \frac{dv}{g-kv}= \int 1~dt + C$

$-\frac{1}{k} \ln{(g-kv)}=t+C$

Ratkaistaan yhtälöstä aluksi $\ln{(g-kv)}:

$-\ln{(g-kv)}=kt+kC$

$\ln{(g-kv)}=-kt-kC$

Logaritmin "sisällä" oleva tuntematon ratkeaa potenssiinkorotuksella:

$e^{\ln{(g-kv)}}=e^{-kt-kC}$

Vasemmalla puolella Neperin luku ja eksponenttina oleva logaritmi kumoavat toisensa:

$g-kv=e^{-kt-kC}$

Yhtälöstä ratkeaa

$v=-\frac{1}{k}e^{-kt-kC}+\frac{g}{k}$

Yksittäisratkaisu on helpompi selvittää, kun sievennetään yhtälöä:

$v=-\frac{1}{k}e^{-kt}e^{-kC}+\frac{g}{k}$

Edelleen lyhennysmerkinnällä $e^{-kC}=D$ saadaan yhtälö muotoon

$v=-\frac{1}{k}De^{-kt}+\frac{g}{k}$

Sijoittamalla yhtälöön ehto $v(0)=0$ saadaan

$0=-\frac{1}{k}D+\frac{g}{k}$

josta ratkeaa $D=g$.

Kysytty yksittäisratkaisu on siis $v(t)=-\frac{1}{k}ge^{-kt}+\frac{g}{k}$, joka voidaan vielä sieventää muotoon $v(t)=\frac{g}{k}(1-e^{-kt})$.

:::

::::
