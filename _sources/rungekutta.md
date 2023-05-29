# Muita menetelmiä (KESKEN)

Eulerin algoritmi ei välttämättä toimi kovin tarkasti kaikkien differentiaaliyhtälöiden ratkaisuissa. Siitä on kehitetty erilaisia muunnoksia, joista tässä esitellään kaksi. Muunnokset onnistuvat esimerkiksi Pythonin valmiilla toiminnoilla. Algoritmit eivät tosin ole hankalia ohjelmoida itsekään.

## Muunneltu Eulerin menetelmä

Eulerin algoritmia voidaan käyttää myös siten, että käyrän tangentin kulmakerroin lasketaan välien alkupisteiden lisäksi myös pisteiden puolivälissä. Tangenteista lasketaan keskiarvo, ja siirtymän suuntana käytetään tätä keskiarvoa.

Muunnellun Eulerin menetelmän askel kohdasta $t_{n-1}$ kohtaan $t_n$ lasketaan seuraavasti: 

$y_n = y_{n-1}+hf(t_{n-1}+\frac{h}{2},y_{n-1}+\frac{h}{2}f(t_{n-1},y_{n-1}))$

Käytännössä laskukaava puretaan välivaiheisiin, joista saadut tulokset on helppo sijoittaa lopulliseen kaavaan.

**Esim.** Ratkaise alkuarvotehtävä $y'=-ty, y(0)=1$ muunnellulla Eulerin menetelmällä. Laske funktion $y(t)$ arvot, jotka vastaavat muuttujan $t$ arvoja $t_1=0.05$ ja $t_2=0.1$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö voidaan esittää muodossa $f(t,y)=-ty$. Lasketaan arvo $y(0.05)$ välivaiheiden kautta seuraavasti:

Aluksi lasketaan $\frac{h}{2}f(t_0,y_0)=\frac{0.05}{2}\cdot (-0 \cdot 1) = 0$.  

Seuraava vaihe on laskea $f(t_0+\frac{h}{2},y(t_0)+\frac{h}{2}\cdot 0) = -(0+\frac{0.05}{2})\cdot 1 = -0.025.$

Lopuksi lasketaan $y(0.05) = 1 + 0.05\cdot(-0.025) = 0.99875$.

Lasketaan vielä arvo seuraavassa pisteessä $t_2$:

Ensin lasketaan $\frac{h}{2} f(t_1,y_1)= \frac{0.05}{2} \cdot (-0.05 \cdot 0.99875) = -0.00125$.  

Sitten lasketaan $f(t_1+\frac{h}{2},y(t_1)+\frac{h}{2}\cdot (-0.00125))$  

$= -(0.05+\frac{0.05}{2})\cdot (0.99875-0.00125\cdot\frac{0.05}{2}) = -0.07490$.

Lopuksi lasketaan $y(0.1) = 0.99875 + 0.05\cdot(-0.07490) = 0.99501$.

Käytännössä tällainen tehtävä suoritettaisiin tietokoneella, ja välivaiheiden tulokset tallennettaisiin useampien desimaalien tarkkuudella kuin tässä.

:::

## Runge-Kutta -menetelmä

Runge-Kutta -menetelmä on muunnos Eulerin algoritmista. Menetelmästä on olemassa erilaisia muunnoksia. Tässä tarkastellaan menetelmän perusversiota. Idea on samanlainen kuin muunnellussa Eulerin menetelmässä, mutta jokaisella välillä lasketaankin nyt neljä tangentin kulmakerrointa $k_1, k_2, k_3$ ja $k_4$, ja siirtymän suunta on näiden kulmakertoimien painotettu keskiarvo. Laskukaavat voidaan esittää seuraavasti:

$k_1=f(t_{n-1},y_{n-1})$  

$k_2=f(t_{n-1}+h/2, y_{n-1}+(h/2) k_1)$  

$k_3=f(t_{n-1}+h/2, y_{n-1}+(h/2) k_2)$  

$k_4=f(t_{n-1}+h, y_{n-1}+h k_3)$  

$y_n = y_{n-1}+ (h/6)(k_1+2k_2+2k_3+k_4)$

**Esim.** Ratkaise alkuarvotehtävä $y'=-ty, y(0)=1$ Runge-Kutta -menetelmällä. Laske funktion $y(t)$ arvot, jotka vastaavat muuttujan $t$ arvoja $0.05$ ja $0.1$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö voidaan esittää muodossa $f(t,y)=-ty$. Tällöin Runge-Kutta -menetelmän laskukaavat ovat seuraavat:

$k_1=-t_{n-1}y_{n-1}$  

$k_2=-(t_{n-1}+h/2)(y_{n-1}+(h/2) k_1)$  

$k_3=-(t_{n-1}+h/2) (y_{n-1}+(h/2) k_2)$  

$k_4= -(t_{n-1}+h)(y_{n-1}+h k_3)$  

$y_n=y_{n-1}+(h/6)(k_1+2k_2+2k_3+k_4)$  

Lasketaan arvo $y(0.05)$:

$k_1=-0\cdot 1 = 0$  

$k_2=-(0+0.025)(1+0.025\cdot 0) = -0.025$  

$k_3=-(0+0.025) (1+0.025\cdot(-0.025)) = -0.024984375$  

$k_4=-(0+0.05)(1+0.05\cdot(-0.024984375)) = -0.0499375390625$  

$y_1=1+(0.05/6)(0+2\cdot(-0.025)+2\cdot(-0.024984375)-0.0499375390625) = 0.9987508$ 

Arvon $y(0.1)$ laskeminen jää vapaaehtoiseksi harjoitustehtäväksi!

:::