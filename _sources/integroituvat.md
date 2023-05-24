# Eri tyyppiset differentiaaliyhtälöt


Differentiaaliyhtälöistä on olemassa muutamaa erilaista tyyppiä, jotka on helppoa tai ainakin mahdollista ratkaista itse laskemalla:
- "perustyyppi" eli integroituva differentiaaliyhtälö
- separoituva differentiaaliyhtälö
- lineaarinen differentiaaliyhtälö
    - homogeeninen differentiaaliyhtälö
    - vakiokertoiminen differentiaaliyhtälö

Erityyppisten yhtälöiden ratkaisumenetelmiin perehdytään seuraavissa luvuissa. On olemassa sellaisiakin differentiaaliyhtälöitä, joita ei voi ratkaista analyyttisesti. Tällöin funktiolle $y(x)$ ei ole mahdollista johtaa lauseketta, ja laskun lopputuloksena on likiarvo eikä tarkka arvo. Opintojaksolla perehdytään erilaisiin numeerisiin menetelmiin, joilla tällaisia ratkaisuja voi etsiä.

## Perustyyppi ratkeaa integroimalla

Yksinkertaisimmillaan differentiaaliyhtälön toisella puolella on etsittävän funktion $y(x)$ derivaatta $y'(x)$ ja toisella puolella pelkästään muuttujasta ja vakioista koostuva lauseke, jota voidaan merkitä $f(x)$. Tällöin funktio $y(x)$ saadaan selville integroimalla, siis $y(x)=\int f(x) \,dx +C$.

Tällaista yhtälöä kutsutaan differentiaaliyhtälön perustapaukseksi. Toinen nimitys on **integroituva** differentiaaliyhtälö. Yhtälössä esiintyy siis vain funktion $y(x)$ derivaatta, ei itse funktiota $y(x)$. 

Integroimalla saadaan differentiaaliyhtälön yleinen ratkaisu. Jos halutaan yksittäinen ratkaisu, pitää tietää jokin ehto $y(x_0)=y_0$.

::::{admonition} Esimerkki

Etsi differentiaaliyhtälölle $y'=4x$ 

a) yleinen ratkaisu, 

b) yksittäisratkaisu, joka toteuttaa ehdon $y(1)=8$.

:::{admonition} Ratkaisu
:class: tip, dropdown
a) Integroidaan: $y(x)=\int 4x \,dx +C = 2x^2 + C$

b) Ratkaistaan vakio $C$ yhtälöstä $2\cdot 1^2+C=8 \leftrightarrow C=8-6 \leftrightarrow C=6$. Kysytty yksittäisratkaisu on siis $y=2x^2+6$.

:::

::::

::::{admonition} Esimerkki

Kappaleen nopeus $v$ noudattaa ajan $t$ suhteen yhtälöä $v(t)=5~\frac{\text{m}}{\text{s}}+0.1 ~\frac{\text{m}}{\text{s}^2} t$. Hetkellä $t=0$ s kappaleen sijainti oli $x=10$ m. Nopeus on sijainnin derivaatta. Millä funktiolla kappaleen sijaintia ajan funktiona voidaan yleisesti kuvata?

:::{admonition} Ratkaisu
:class: tip, dropdown

Tiedetään, että $x'(t)=v(t)$. Näin ollen $x(t)=\int v(t)~dt + C$. Suoritaan integrointi (suureiden yksiköt on jätetty pois yksinkertaisuuden vuoksi):

$x(t)=\int 5+0.1t \,dt + C$

$x(t)=5t+0.05t^2+C$

Vakion $C$ arvo saadaan selville ehdosta $x(0)=10$, siis

$5\cdot 0 + 0.05\cdot 0^2+C=10 \Leftrightarrow C=10$.

Kappaleen sijaintia kuvaa siis funktio $x(t)=5t+0.05t^2+10$.

:::

::::

Integroituvassa differentiaaliyhtälössä voi esiintyä myös toista derivaattaa $y''$. Jos tällöin halutaan selville yksittäisratkaisu, pitää tietää ehdon $y(x_0)=y_0$ lisäksi jokin toinen ehto $y'(x_1)=y_1'$. Kaksi ehtoa tarvitaan, koska ratkaisu tapahtuu kaksi kertaa peräkkäin integroimalla. Ensimmäisellä integroinnilla saadaan toisesta derivaatasta $y''$ selville derivaatta $y'$, ja toisella integroinnilla funktio $y'$. Kummastakin integroinnista tulee mukaan oma vakionsa.

Toista derivaattaa sisältävän differentiaaliyhtälön ratkaisu onnistuu suoraviivaisesti integroimalla kahteen kertaan vain, jos yhtälössä ei esiinny derivaattaa $y'$ eikä itse funktiota $y$. Muulloin kyseessä ei ole integroituva differentiaaliyhtälö, vaan yleisempi toisen kertaluvun differentiaaliyhtälö. Näitä hankalampia tapauksia käsitellään luvussa "Toisen kertaluvun differentiaaliyhtälöt".

::::{admonition} Esimerkki

Ratkaise differentiaaliyhtälö $y'=2x+3$ ehdolla $y(1)=6$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Integroimalla saadaan yleinen ratkaisu:

$y=\int 2x+3 \,dx+C=x^2+3x+C$

Selvitetään vakio $C$ yhtälöstä $y(1)=6$:

$1^2+3\cdot 1 + C = 6 \Leftrightarrow C=6-1-3 \Leftrightarrow C=2$

Yksittäisratkaisu on siis $y=x^2+3x+2$.

:::

::::

::::{admonition} Esimerkki

Ratkaise yhtälö $y''=x^3+x$, kun tiedetään, että $y(1)=3$ ja $y'(0)=4$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Derivaatta $y'$ saadaan selville integroimalla $y''$. Merkitään tästä integroinnista saatavaa vakiota $C_1$.

$y'=\int x^3 + x \,dx+C_1$

$y'=\frac{1}{4}x^4+\frac{1}{2}x^2 + C_1$

Selvitetään vakion $C_1$ arvo ehdosta $y'(0)=4$:

$\frac{1}{4}\cdot 0^4+\frac{1}{2}\cdot 0^2 + C_1 = 4 \Leftrightarrow C_1=4$

Derivaatta on siis $y'=\frac{1}{4}x^4+\frac{1}{2}x^2 + 4$. Näin muodostunut ensimmäisen kertaluvun differentiaaliyhtälöä ratkeaa jälleen integroimalla. Vakiota on nyt merkitty $C_2$.

$y=\int \frac{1}{4}x^4+\frac{1}{2}x^2 + 4 \,dx + C_2$

$y=\frac{1}{4\cdot 5} x^5 + \frac{1}{2\cdot 3} x^3 + 4x + C_2$

$y=\frac{1}{20} x^5 + \frac{1}{6} x^3 + 4x + C_2$

Ratkaistaan vielä vakio $C_2$ yhtälöstä $y(1)=3$:

$\frac{1}{20} \cdot 1^5 + \frac{1}{6} \cdot 1^3 + 4\cdot 1 + C_2 = 3$

$\frac{1}{20} + \frac{1}{6} + 4+ C_2 = 3$

$C_2=3-4-\frac{1}{20}-\frac{1}{6}$

$C_2=-\frac{73}{60}$

Ehdot toteuttava yksittäisratkaisu on siis $y=\frac{1}{20} x^5 + \frac{1}{6} x^3 + 4x-\frac{73}{60}$.

:::

::::










