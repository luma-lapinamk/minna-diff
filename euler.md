# Eulerin menetelmä (KESKEN)

Tarkastellaan yhtälöä $y'=f(t,y), y(0)=y_0$. Eulerin menetelmä on algoritmi, jolla yhtälön arvolle voidaan löytää likiarvo, joka vastaa haluttua muuttujan $t$ arvoa, vaikka varsinaista funktion $y(t)$ lauseketta ei saataisi selville. Tiedossa on oltava jokin alkuarvo $y_0$, josta lähtien funktion muita arvoja aletaan arvioida.

Eulerin menetelmässä derivaatta ilmastaan erotusosamäärällä:

$y'(t)\approx\frac{y(t+h)-y(t)}{h}$

Tarkalleenhan derivaatta on erotusosamäärän raja-arvo, jossa $h \to 0$.

Sijoitetaan äskeinen derivaatan lauseke yhtälöön:

$\frac{y(t+h)-y(t)}{h}=f(t,y(t))$

Yhtälöstä on helppo ratkaista $y(t+h)$:

$y(t+h)=y(t)+hf(t,y(t))$.

Merkitään funktion arvoja eri ajan hetkillä seuraavasti: $y_0=y(0), y_1=y(h), y_2=y(2h), \ldots y_n=y(nh)$. Ajan arvoja merkitään vastaavasti $t_0=0, t_1=h, t_2=2h, \ldots t_n=nh$.

Tehtävä ratkaistaan laskemalla funktion arvoja perustuen aiempien hetkien arvoihin:

$y_1 = y_0 + hf(t_0, y_0)$

$y_2 = y_1 + hf(t_1, y_1)$

$\ldots$

$y_n = y_{n-1}+ hf(t_{n-1},y_{n-1})$

Askelpituuden $h$ valintaan ei ole mitään yleistä sääntöä. Usein pieni askelpituus on parempi kuin suurempi askelpituus.

**Esim.** Funktio $y=y(t)$ on differentiaaliyhtälön $y'=\sqrt{t+y}$ yksittäisratkaisu, joka toteuttaa ehdon $y(0)=1$. Selvitä, mikä on funktion $y(t)$ arvo, kun $t=2$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Funktiosta tiedetään alkuarvo $y_0 = 1$. Valitaan askelpituudeksi esim. $h=0.5$. Lasketaan funktion arvoja:

$y(0.5) = y_1 = y_0+h\sqrt{t_0 + y_0} = 1 + 0.5\cdot \sqrt{0+1} =1 + 0.5 = 1.5$

$y(1) = y_2 = y_1 + h\sqrt{t_1 + y_1} = 1.5 + 0.5\sqrt{0.5+1.5} = 1.5+0.5\sqrt{2} \approx 2.20711$

$y(1.5) = y_3 = 2.20711 + 0.5 \sqrt{1+2.20711} \approx 3.10253$

$y(2) = y_4 = 3.10253 + 0.5 \sqrt{1.5+3.10253} \approx 4.17521$.

:::

## Eulerin menetelmä ja derivaatta

Eulerin menetelmän avulla voi myös arvioida funktion kulkua sen derivaatan avulla. Differentiaaliyhtälössähän tuntematon $y'$ kertoo jokaisessa pisteessä funktion muutosnopeuden. Pienillä askelväleillä voidaan ajatella, että funktio hetkellisesti käyttäytyy kuten suora, jonka kulmakerroin on $y'$. Tällöin funktion arvon muutos saadaan laskemalla kulmakertoimen määritelmästä lähtien: $y'=\frac{\Delta y}{\Delta t}$, joten $\Delta y = y' \Delta t$.

Tarkastellaan edellistä esimerkkiä hieman toisella tavalla, välittämättä edellä esitellystä Eulerin algorismista, tarkastellen pelkästään funktion muutosnopeutta. 

**Esim.** Funktio $y=y(t)$ on differentiaaliyhtälön $y'=\sqrt{t+y}$ yksittäisratkaisu, joka toteuttaa ehdon $y(0)=1$. Selvitä, mikä on funktion $y(t)$ arvo, kun $t=2$.

Pisteessä $t=0$ funktion arvo on $y(0)=1$, ja funktion kasvunopeus on $y'(0)=\sqrt{0+1}=1$. Toisin sanoen kun siirrytään seuraavaan pisteeseen $t=0.5$, funktion arvon muutos $\Delta y$ on kasvunopeuden ja muutoksen $\Delta t$ tulo $1 \cdot 0.5=0.5$.

Näin ollen päästiin pisteeseen $y(0.5)=y(0)+\Delta y = 1+0.5 = 1.5$. Derivaatan arvo tässä pisteessä on $y'(0.5)=\sqrt{0.5+1.5}=\sqrt{2} \approx 1.414$. Funktion arvon muutos on siis seuraavaan pisteeseen siirryttäessä $\Delta y = 1.414\cdot 0.5 \approx 0.707$.

Seuraava piste on siis $y(1)=y(0.5)+y'(0.5)\cdot \Delta x = 1.5+0.707 = 2.207$. Tässä pisteessä derivaatta on $y'(1)=\sqrt{1+2.207} \approx 1.791$.

Seuraava piste on $y(1.5)=2.207+0.5\cdot 1.791 = 3.103$. Jälleen lasketaan derivaatta $y'(1.5) = \sqrt{1.5+3.103} \approx 2.145$. Viimeinen piste on $y(2)=3.103+0.5\cdot 2.145 \approx 4.176$.
