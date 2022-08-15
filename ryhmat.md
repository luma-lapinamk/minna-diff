# Differentiaaliyhtälöryhmät

Differentiaaliyhtälöistä voidaan muodostaa yhtälöryhmiä samaan tapaan kuin muunkinlaisista yhtälöistä. Esimerkiksi kemianteollisuuden prosesseissa on mukana monta yhtä aikaa muuttuvaa osaa, kuten paine, lämpötila, aineiden konsentraatio ja muut olosuhteet. Jonkin tekijän muutos vaikuttaa muihin tekijöihin. Niinpä prosessin kuvaamiseen tarvitaan useampaa kuin yhtä differentiaaliyhtälöä.

## Yhtälöryhmän ratkaisu

Tarkastellaan yksinkertaisena esimerkkinä ilmiötä, johon liittyy ajasta $t$ riippuvat funktiot $y(t)$ ja $x(t)$. Tässä on tärkeää huomata, että $x$ on nyt funktion eikä muuttujan nimi. Funktiot vaikuttavat toisiinsa siten, että 

$\begin{equation} \begin{cases} y'=2y-2x \\ x'=-y+3x \end{cases} \end{equation} $

Yhtälöryhmän voi ratkaista eliminointimenetelmällä. Ratkaisun ideana on eliminoida yhtälöistä joko $x$ tai $y$ käyttäen apuna puolittain derivoimista. Erään mahdollisen ratkaisun yksityiskohdat ova alla.

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

Yksinkertaisia differentiaaliyhtälöryhmiä voidaan ratkaista tietokoneella samaan tapaan kuin tavallisiakin yhtälöryhmiä. Tehokas tapa on ilmaista yhtälöryhmä tietokoneelle matriisimuodossa. Ensimmäisen kertaluvun lineaariselle vakiokertoimiselle differentiaaliyhtälölle muodostetaan tällöin matriisiyhtälöt

$\mathbf{x}'(t)=\mathbf{A}\mathbf{x}(t)+\mathbf{f}(t), \mathbf{x}(0)=\mathbf{x_0}$,

missä $\mathbf{x}(t)$ sisältää tuntemattomien funktioiden derivaatat, $\mathbf{A}$ yhtälöissä olevat funktioiden kertoimet ja $\mathbf{f}(t)$ yhtälöiden epähomogeeniset termit. Mahdolliset alkuarvot ovat vektorissa $\mathbf{x_0}$.

**Esim.** Muunna matriisimuotoon yhtälöryhmä

$\begin{equation} \begin{cases} y'=2y-2x \\ x'=-y+3x \end{cases} \end{equation}$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Yhtälöryhmää $\begin{equation} \begin{cases} y'=2y-2x \\ x'=-y+3x \end{cases} \end{equation}$ vastaa matriisiyhtälö

$\begin{bmatrix} x_1' \\ x_2' \\\ x_3' \end{bmatrix} = \begin{bmatrix}-2 & 3 & 0 \\ 0 & -4 & 0 \\ 1 & 0 & 4 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} + \begin{bmatrix} t \\ 5t\\ t^2\end{bmatrix}$.


:::

## Sovelluksia


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