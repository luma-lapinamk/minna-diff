# Lineaarinen differentiaaliyhtälö

Lineaariseksi differentiaaliyhtälöksi sanotaan yhtälöä, joka voidaan kirjoittaa muodossa $y'=fy+g$ missä $f=f(x)$ ja $g=g(x)$. Lineaarinen differentiaaliyhtälö on

- homogeeninen, jos $g(x)=0$,

- vakiokertoiminen, jos $f(x)$ on vakio.

Yhtälö voi olla joko homogeeninen tai vakiokertoiminen, molempia yhtä aikaa, tai ei kumpaakaan.

## Yleinen ratkaisu

Lineaariselle differentiaaliyhtälölle, jonka ei tarvitse olla homogeeninen eikä vakiokertoiminen (mutta se voi olla kumpaa tahansa tai molempia), voidaan johtaa suoraan ratkaisukaava:

$y(x)=e^{F(x)}\left(\int e^{-F(x)}g(x) ~\text{d}x + C \right)$, missä

$F(x) = \int f(x)~\text{d}x$ on funktion $f(x)$ integraalifunktio.

:::{admonition} Perustelu
:class: tip, dropdown

Derivoidaan edellä annettu laskukaava:

$y'(x)=D\left(e^{F(x)}\right)\cdot \left(\int e^{-F(x)}g(x) ~\text{d}x + C \right) + \left(e^{F(x)}\right) \cdot D\left(\int e^{-F(x)}g(x) ~\text{d}x + C \right)$

$= e^{F(x)} D\left(F(x)\right)\cdot \left(\int e^{-F(x)}g(x) ~\text{d}x + C \right) + e^{F(x)}\cdot e^{-F(x)} g(x)$

$= f(x)\cdot e^{F(x)} \left(\int e^{-F(x)}g(x) ~\text{d}x + C \right) + g(x)$

$=f(x)y(x)+g(x)$.

:::

**Esim.** Ratkaise yhtälö $y'=2xy+3x$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Tunnistetaan lausekkeesta funktiot $f(x)=2x$ ja $g(x)=3x$. Lasketaan ensin funktion $f(x)$ integraalifunktio

$F(x)=\int 2x~\text{d}x = x^2$

ja tehdään sitten tarvittavat sijoitukset ratkaisukaavaan:

$y(x)=e^{x^2}\left(\int e^{-x^2} 3x ~\text{d}x + C \right)$

Koska $\int e^{-x^2} 3x~\text{d}x = -\frac{3}{2}e^{-x^2}$, ratkaisuksi saadaan

$y(x)=-\frac{3}{2}e^{x^2}e^{-x^2}+Ce^{x^2}$ joka sievenee muotoon $-\frac{3}{2}+Ce^{x^2}$.

:::

## Homogeeninen lineaarinen yhtälö

Jos $g(x)=0$, niin lineaarinen differentiaaliyhtälö on muotoa $y'=fy$. Tällöin yhtälö voidaan ratkaista yllä esitetyllä ratkaisukaavalla, joka sievenee muotoon $y(x)=C e^{F(x)}$.

Ratkaisussa voi myös käyttää samoja menetelmiä kuin separoituvien differentiaaliyhtälöiden ratkaisussa. Yhtälöhän on mahdollista esittää myös muodossa $\frac{\text{d}y}{\text{d}x}=f(x) y$ eli $\frac{1}{y} ~\text{d}y = f(x)~\text{d}x$.

**Esim.** Ratkaise yhtälö $y'=3xy$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Tunnistetaan yhtälöstä $f(x)=3x$. Ratkaisukaavaan tarvittava integraalifunktio on $F(x)=\int 3x ~\text{d}x = \frac{3}{2}x^2$.

Ratkaisukaavaan sijoittamalla saadaan $y(x)=Ce^{\frac{3}{2}x^2}$.

:::

## Vakiokertoiminen lineaarinen yhtälö

Vakiokertoimisessa lineaarisessa differentiaaliyhtälössä kerroinfunktio $f(x)$ on vakio. Vakiofunktion $f(x)=a$ integraalifunktio on $F(x)=ax$ joten ratkaisukaava sievenee muotoon

$y(x)=e^{ax}\left(\int e^{-ax} g(x) ~\text{d}x + C \right)$.

**Esim.** Ratkaise yhtälö $y'=2y+3x$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Tässä yhtälössä $f(x)=2$, $a=2$ ja $g(x)=3x$, joten ratkaisuksi saadaan

$y(x)=e^{2x}\left(\int e^{-2x} 3x ~\text{d}x + C \right)$.

Integraalin $\int e^{-2x} 3x ~\text{d}x$ saadaan (WolframAlphalla) $-\frac{3}{4} e^{-2 x} (1 + 2 x)$, joten differentiaaliyhtälön ratkaisuksi muodostuu

$y(x)=e^{2x}\left(-\frac{3}{4} e^{-2x} (1 + 2 x) + C \right) = -\frac{3}{4}(1+2x)+Ce^{2x}$.

:::

**Esim.** Ratkaise yhtälö $y'=5y$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälö on sekä homogeeninen että vakiokertominen. Tunnistetaan yhtälöstä: $f(x)=5$, $F(x)=5x$, $g(x)=0$. Sijoitetaan nämä ratkaisukaavaan 

$y(x)=e^{F(x)}\left(\int e^{-F(x)}g(x) ~\text{d}x + C \right)$

$y(x)=e^{5x}\left(\int e^{-5x}\cdot 0 ~\text{d}x + C \right) = Ce^{5x}$.

Toisaalta yhtälö on myös separoituva: 

$\frac{\text{d}y}{text{d}x}=5y$

$\frac{1}{y}\text{d}y=5~\text{d}x$

$\int \frac{1}{y}~\text{d}y=\int 5~\text{d}x$

$\ln{y} = 5x+C$

$y=e^{5x+C}$

$y=e^C e^{5x}$

$y=C_1 e^{5x}$.

:::