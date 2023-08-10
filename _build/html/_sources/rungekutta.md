# Muita menetelmiä

Eulerin algoritmi ei välttämättä toimi kovin tarkasti kaikkien differentiaaliyhtälöiden ratkaisuissa. Siitä on kehitetty erilaisia muunnoksia, joista tässä esitellään kaksi. Muunnokset onnistuvat esimerkiksi Pythonin valmiilla toiminnoilla. Algoritmit eivät tosin ole hankalia ohjelmoida itsekään.

## Muunneltu Eulerin menetelmä

Eulerin algoritmia voidaan käyttää myös siten, että funktion derivaatta lasketaan välien alkupisteiden lisäksi myös pisteiden puolivälissä. Derivaatasta lasketaan keskiarvo, ja siirtymän suuntana käytetään tätä keskiarvoa. Menetelmä onnistuu seuraavien välivaiheiden avulla:

- Arvioi, mikä on funktion $y(x)$ pisteiden $x$ ja $x+h$ puolivälissä. Tämä tapahtuu laskutoimituksella 

$y(x+\frac{h}{2})\approx y(x)+\frac{h}{2} f(x,y)$

- Laske edellisen perusteella derivaatta, jota tässä lyhennetään $k$, kyseisessä pisteessä: 

$k=f'(x+\frac{h}{2},y(x+\frac{h}{2})$

- Etene pisteeseen $y(x+h)$ laskemalla $y(x+h)=y(x)+kh$

::::{admonition} Esimerkki

Eräs differentiaaliyhtälö on $y'=-2x-y$ ja lisäksi tiedetään alkuarvo $y(0)=-1$. Selvitä muunnellulla Eulerin menetelmällä funktion arvo $y(0.1)$ askelpituudella $h=0.1$.

:::{admonition} Ratkaisu
:class: tip, dropdown

- Funktion derivaatta on nyt $f(x,y)=-2x-y$. Arvioidaan tämän avulla ensin $y(0.05)$:

$y(0.05) \approx y(0) + 0.05 \cdot f(0,y(0))$

$y(0.05) \approx y(0) + 0.05 \cdot (-2\cdot 0-y(0))$

$y(0.05) \approx -1 + 0.05 \cdot (-2\cdot 0-(-1))$

$y(0.05) \approx -1 + 0.05\cdot 1 = -0.95$

- Seuraavaksi lasketaan funktion derivaatta pisteessä $x=0.05$:

$k=f(0.05,y(0.05)=-2\cdot 0.05-(-0.95)=0.85$

- Seuraavaksi lasketaan $y(0.1)=y(0)+k\cdot 0.05$:

$y(0.1)=-1+0.1\cdot 0.855=-0.915$

:::

## Runge-Kutta -menetelmä

Runge-Kutta -menetelmä on muunnos Eulerin algoritmista. Menetelmästä on olemassa erilaisia muunnoksia. Tässä tarkastellaan menetelmän perusversiota. Idea on samanlainen kuin muunnellussa Eulerin menetelmässä, mutta jokaisella välillä lasketaankin nyt neljä tangentin kulmakerrointa $k_1, k_2, k_3$ ja $k_4$, ja siirtymän suunta on näiden kulmakertoimien painotettu keskiarvo. Menetelmään voi perehtyä halutessaan tarkemmin esimerkiksi opintojaksolla laadittavan seminaarityön yhteydessä.

