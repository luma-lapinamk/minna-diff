# Differentiaaliyhtälöryhmät (KESKEN)

Differentiaaliyhtälöistä voidaan muodostaa yhtälöryhmiä samaan tapaan kuin muunkinlaisista yhtälöistä. Esimerkiksi kemianteollisuuden prosesseissa on mukana monta yhtä aikaa muuttuvaa osaa, kuten paine, lämpötila, aineiden konsentraatio ja muut olosuhteet. Jonkin tekijän muutos vaikuttaa muihin tekijöihin. Niinpä prosessin kuvaamiseen tarvitaan useampaa kuin yhtä differentiaaliyhtälöä.

## Yhtälöryhmän ratkaisu

Tarkastellaan yksinkertaisena esimerkkinä ilmiötä, johon liittyy ajasta $t$ riippuvat funktiot $y(t)$ ja $x(t)$. Tässä on tärkeää huomata, että $x$ on nyt funktion eikä muuttujan nimi. Funktiot vaikuttavat toisiinsa siten, että 

$\begin{equation} \begin{cases} y'=2y-2x \\ x'=-y+3x \end{cases} \end{equation} $

Yhtälöryhmän voi ratkaista eliminointimenetelmällä. Ratkaisun ideana on eliminoida yhtälöistä joko $x$ tai $y$ käyttäen apuna puolittain derivoimista. Erään mahdollisen ratkaisun yksityiskohdat ovat alla.

:::{admonition} Ratkaisu
:class: tip, dropdown

Ratkaisemalla alempi yhtälö funktion $y$ suhteen saadaan $y=-x'+3x$. Kun tämä yhtälö derivoidaan molemmin puolin, niin saadaan $y'=-x''+3x'$. Sijoittamalla nämä kaksi yhtälöä yhtälöparin ylempään yhtälöön päädytään sellaiseen differentiaaliyhtälöön, jossa on vain yksi tuntematon funktio: 

$-x''+3x'=2(-x'+3x)-2x $

$-x''+3x'=-2x'+6x-2x $

$-x''+5x'-4x=0 $

Nyt kyseessä on homogeeninen toisen kertaluvun differentiaaliyhtälö. Sitä vastaavan karakteristisen yhtälön $-m^2+5m-4=0$ juuret ovat $1$ ja $4$, joten differentiaaliyhtälön ratkaisuksi tulee $x(t)=C_1 e^t + C_2 e^{4t}$.

Yhtälö $y(t)$ saadaan ratkaistua sijoittamalla ratkaisu $x(t)$ ja sen derivaatta $x'(t)=C_1 e^t + 4 C_2 e^{4t}$ yhtälöön $y=-x'+3x$

$y(t)= -C_1 e^t -4 C_2 e^{4t} +3 C_1 e^t +3 C_2 e^{4t}$

$y(t)= 2C_1 e^t - C_2 e^{4t}$

:::


## Sovelluksia

**Saaliit ja pedot: Lotka-Volterra -malli**

Luonnossa samalla alueella voi elää sekä petoja että saaliita. Näiden eläinlajien määrät vaikuttavat toisiinsa: jos saaliita on paljon, pedoille riittää syötävää ja niiden poikaset menestyvät hyvin. Samalla kuitenkin saaliiden määrä pienenee ja sitä mukaa pedoille riittää vähemmän ravintoa. Kun petojen määrä pienenee, saaliiden määrä voi taas kasvaa. 

Merkitään petojen määrää ajan $t$ funktiona $y(t)$ ja saaliiden määrää $x(t)$. Jos petoja ei olisi, niin saaliiden määrä kasvaisi eksponentiaalisesti yhtälön $x'=ax, a > 0$ mukaisesti. Jos taas saaliita ei olisi, niin petojen määrä vähenisi eksponentiaalisesti yhtälön $y'=-by, b > 0$ mukaisesti. Jos taas sekä petojen että saaliiden määrä on suurempi kuin nolla, niin ns. [Lotka-Volterra](https://fi.wikipedia.org/wiki/Lotkan%E2%80%93Volterran_yht%C3%A4l%C3%B6) -mallin mukaan yhtälöiksi muodostuvat

(1) $x'=ax-cxy$,

(2) $y'=-by+dxy$

joissa vakiot $c > 0, d > 0$ liittyvät petojen ja saaliiden välisiin kohtaamisiin. Tällaisessa kohtaamisessahan saalis saattaa tulla syödyksi ja peto taas voi saada populaation kasvuun tarpeellista ravintoa. Kohtaamisten lukumäärän oletetaan mallissa riippuvan petojen ja saaliiden määrän tulosta $xy$.

Kyseistä differentiaaliyhtälöä ei voi ratkaista analyyttisesti. Tietokoneella ratkaisu kyllä onnistuu.

**Virtausongelmat**

Kuvitellaan, että teollisuuden prosessissa on peräkkäin kolme vesisäiliötä. Säiliöissä on aluksi puhdasta vettä 100, 300 ja 20 litraa. Ensimmäisen säiliöön syötetään suolaa nopeudella 10 l/s. Suola sekoittuu tasaisesti veteen. Suolavettä virtaa ensimmäisestä seuraavaan säiliöön, edelleen siitä seuraavaan säiliöön ja lopulta ulos samalla nopeudella 10 l/s. 

Tällaista tilannetta voidaan kuvailla seuraavalla differentiaaliyhtälöryhmällä:

$\begin{equation} \begin{cases} m_1'=-\frac{1}{10}m_1 \\ m_2'=\frac{1}{10}m_1-\frac{1}{30} m_2 \\ m_3'=\frac{1}{30} m_2 -\frac{1}{2}m_3\end{cases}\end{equation}$

Suolan massan eri säiliöissä ajan funktiona voi ratkaista eliminoimalla tuntemattomia. Esimerkkiratkaisu on esitetty alla. Esimerkkiratkaisussa on käytetty alkuehtoja $m_1(0)=3~$ kg ja $m_2(0)=m_3(0)=0~$ kg.

:::{admonition} Ratkaisu
:class: tip, dropdown

Tuntematon $m_1$ saadaan selville keskimmäisestä yhtälöstä:

$m_1=10m_2'+\frac{1}{3}m_2$

Sijoitetaan oikean puolen lauseke ja sen derivaatta ensimmäiseen yhtälöön. Sieventämällä saadaan toisen kertaluvun differentiaaliyhtälö:

$10 m_2''+\frac{4}{3}m_2'+\frac{1}{30}m_2=0$

Tätä yhtälöä vastaavan karakteristisen yhtälön $10m^2+\frac{4}{3}m+\frac{1}{30}=0$ juuret ovat $-\frac{1}{10}$ ja $-\frac{1}{30}$, joten ensimmäisen säiliön suolamäärän yhtälöksi saadaan

$m_1(t)=C_1 e^{-\frac{1}{10}t}+C_2 e^{-\frac{1}{30}t}$

Alkuehdosta $m_1(0)=3$ saadaan vakioille ehto $C_1+C_2=3$.

Seuraavaksi ratkaisu $m_1$ voidaan sijoittaa yhtälöön $m_2'=\frac{1}{10}m_1-\frac{1}{30}m_2$. Tällöin saadaan lineaarinen epähomogeeninen yhtälö 

$m_2'+\frac{1}{30}m_2=\frac{1}{10} (C_1 e^{-\frac{1}{10}t}+C_2 e^{-\frac{1}{30}t})$.

Vastaavan homogeenisen yhtälön ratkaisu on $m_{2h}=C_3 e^{-\frac{1}{30}}t$, ja erikoisratkaisu saadaan yritteellä $m_{2y}=C_4 e^{-\frac{1}{10}t} + C_5 e^{-\frac{1}{30}t}$. Kun ratkaisu $m_2=m_{2h}+m_{2y}$ ja sen derivaatta sijoitetaan yhtälöön $m_2'=\frac{1}{10}m_1-\frac{1}{30}m_2$, saadaan pitkän mutta suoraviivaisen laskutoimituksen jälkeen yhtälöt muotoon

$m_1=3e^{-\frac{1}{10}t}, m_2=-\frac{9}{2}e^{-\frac{1}{30}t}+\frac{9}{2}e^{-\frac{1}{10}t}$.

Vastaavalla tavalla muokataan kolmas yhtälö muotoon $m_3'+\frac{1}{2}m_3=-\frac{9}{60}e^{-\frac{1}{30}t}+\frac{9}{60}e^{-\frac{1}{10}t}$, josta saadaan ratkaisu

$m_3=C_6 e^{-\frac{1}{2}t}+C_7 e^{-\frac{1}{30}t}+C_8 e^{-\frac{1}{10}t}$.

Sijoittamalla ratkaisu ja sen derivaatta kolmanteen yhtälöön sekä hyödyntämällä alkuehtoa $m_3(0)=0$ saadaan ratkaistua vakiot $C_6=\frac{3}{56}, C_7=-\frac{9}{28}$ ja $C_8=\frac{3}{8}$.

:::


## Korkeamman kertaluvun differentiaaliyhtälön ratkaisu

Laskentaohjelmat muuttavat korkeamman kertaluvun differentiaaliyhtälöt useaksi ensimmäisen kertaluvun differentiaaliyhtälöksi. Menetelmä tällaiseen muunnokseen on seuraava:

- Määrittele apumuuttujat $x_1, x_2, \ldots x_n$ siten, että $x_1=y, x_2=y', \ldots x_n=y^{(n-1)}$

- Muodosta apumuuttujien derivaatat: $x_1'=y', x_2'=y'', \ldots x_n' = y^{(n)}$

- Ratkaise alkuperäinen yhtälö derivaatan $y^{(n)}$ suhteen: $y^{(n)}=x_n=f(x_1, \ldots , x_n)$

- Muodosta differentiaaliyhtälöryhmä $x_1'=x_2, x_2'=x_3, \ldots x_n'=f(x_1, \ldots , x_n)$

Muodostunut differentiaaliyhtälöryhmä voidaan jälleen ratkaista eliminaatiomenetelmällä. Siten yhtälöryhmästä katoaa funktioita, kunnes jäljellä on vain yhden tuntemattoman funktion sisältävä differentiaaliyhtälö. 

**Esim.** Muunna differentiaaliyhtälö $y''+2y'-3y= 2\sin t$ ryhmäksi ensimmäisen kertaluvun differentiaaliyhtälöitä.

:::{admonition} Ratkaisu
:class: tip, dropdown

Määritellään apumuuttujat $x_1=y$ ja $x_2=y'$. Näiden derivaatat ovat $x_1'=y'$ ja $x_2'=y''$. Nyt alkuperäinen yhtälö muuttuu muotoon $x_2'=-2 x_2+x_1+\sin t$ ja lisäksi voidaan muodostaa yhtälö $x_1'=x_2$. Saadaan siis yhtälöpari

$\begin{equation} \begin{cases} x_1'=x_2 \\ x_2' = -2x_2 -3x_1 +2 \sin t\end{cases} \end{equation}$

:::