# Toisen kertaluvun differentiaaliyhtälöt

Toisen kertaluvun differentiaaliyhtälö sisältää myös funktion $y$ toista derivaattaa $y''$. Vakiokertoiminen toisen kertaluvun differentiaaliyhtälö on muotoa $y''+ay'+by=f(t)$. Tässä tarkastelu rajoitetaan pelkästään homogeenisiin yhtälöihin, jotka ovat siis muotoa $y''+ay'+by=0$. Yleisesti toisen kertaluvun vakiokertoimisen differentiaaliyhtälön ratkaisu on homogeenisen ja epähomogeenisen yhtälön ratkaisujen summa, siis $y=y_h+y_t$. 

## Homogeeniset toisen kertaluvun yhtälöt

Homogeenisille yhtälölle $y''+ay'+by=0$ ratkaisu $y_h$ löytyy seuraavasti:

- valitaan yritteeksi ratkaisu $y_h=e^{mt}$

- lasketaan yritteelle derivaatat $y_h'=me^{mt}$ ja $y_h''=m^2 e^{mt}$

- kirjoitetaan alkuperäinen yhtälö yritteen avulla: $m^2 e^{mt} + am e^{mt} + be^{mt} = 0$

- sievennetään yhtälöä valitsemalla yhteiseksi tekijäksi $e^{mt}$: $e^{mt}(m^2 + am + b) =0$

- tulon nollasäännön perusteella riittää nyt ratkaista yhtälö $m^2 + am + b = 0$

Edellisen prosessin viimeistä yhtälöä $m^2 + am + b= 0$ kutsutaan differentiaaliyhtälön karakteristiseksi yhtälöksi. Koska kyseessä on toisen asteen yhtälö, sille voidaan löytää useampi kuin yksi ratkaisu. Reaaliluvuarvoisia ratkaisuja löytyy yksi kappale, $m$, tai kaksi kappaletta, $m_1$ ja $m_2$. Lisäksi kun otetaan käyttöön kompleksiluvut, voidaan saada ratkaisut $m=a\pm bi$. Kompleksiarvoisia ratkaisuja saadaan silloin, kun reaalilukujen matematiikassa "yhtälölle ei löyty ratkaisua".

:::{admonition} Toisen asteen yhtälön ratkaisu
:class: tip, dropdown

Toisen asteen yhtälön $ax^2+bx+c=0$ ratkaisukaavaksi voidaan johtaa $x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$.

Yksi juuri seuraa, kun $b^2-4ac=0$, esimerkiksi $x^2+6x+9=0$:

$x=\frac{-6\pm\sqrt{6^2-4\cdot 1 \cdot 9}}{2\cdot 1}=\frac{-6\pm 0}{2}=-3$

Kaksi reaaliarvoista juurta seuraa, kun $b^2-4ac > 0$, esimerkiksi $x^2+x-6=0$:

$x=\frac{-1\pm\sqrt{1^2-4\cdot 1 \cdot (-6)}}{2\cdot 1}=\frac{-1\pm 5}{2}$

$x_1=\frac{-1+5}{2}=2, x_2=\frac{-1-5}{2}=-3$

Kompleksiarvoiset juuret seuraavat, kun $b^2-4ac < 0$. Tällöin neliöjuuren sisälle jää negatiivinen luku. Se pitää esittää imaginaarilukuna huomioiden, että $i^2=-1$. Esimerkiksi luku $-4$ voidaan ilmaista muodossa $-1\cdot 4=i^2 \cdot 4$. Tällöin tästäkin luvusta voi laskea neliöjuuren: $\sqrt{-4}=\sqrt{4i^2 }=2i$.

Esimerkki toisen asteen yhtälöstä, josta tulee kompleksinen ratkaisu, on $x^2+2x+3=0$:

$x=\frac{-2\pm\sqrt{2^2-4\cdot 1 \cdot 3}}{2\cdot 1}=\frac{-2\pm\sqrt{-8}}{2}$

$x=\frac{-2\pm\sqrt{8i^2}}{2}=\frac{-2\pm \sqrt{8}i}{2} = \frac{-2\pm 2\sqrt{2}i}{2}= -1\pm \sqrt{2}i$

Kompleksiarvoinen juuri, jossa ei ole ollenkaan reaaliosaa, saadaan esimerkiksi tapauksessa $x^2+5=0$:

$x=\frac{-0\pm\sqrt{0^2-4\cdot 1 \cdot 5}}{2\cdot 1}=\frac{\sqrt{-20}}{2}=\frac{\sqrt{20 i^2}}{2} = \frac{\sqrt{4\cdot 5 i^2}}{2} = \frac{2 \sqrt{5} i}{2} = \sqrt{5}i$

:::

Ratkaisujen lukumäärän perusteella differentiaaliyhtälölle saadaan seuraavat ratkaisut:

- Yksi reaaliarvoinen juuri $m$: $y=(C_1 t + C_2) e^{mt}$

- Kaksi reaaliarvoista juurta $m_1$ ja $m_2$: $y=C_1 e^{m_1 t} + C_2 e^{m_2} t$

- Kompleksiset juuret $m=a+ bi$: $y=e^{at}(C_1 \cos(bt) + C_2 \sin(bt))$

Juurten lukumäärä ja laatu vaikuttavat siihen, millainen funktio ratkaisusta muodostuu. Tarkastellaan aluksi reaaliarvoisia juuria. Jos ainoa reaalinen juuri $m$ tai molemmat reaaliset juuret $m_1, m_2$ ovat negatiivisia, niin funktiosta tulee vähenevä, eli sen arvot pienenevät kun muuttujat arvot kasvavat. Jos taas ainoa juuri $m$ tai vähintään toinen juurista $m_1, m_2$ on positiivinen, funktio on kasvava.

Kompleksiarvoiset juuret aiheuttavat sen, että funktion arvo ei lähesty mitään tiettyä arvoa sitä mukaa kun muuttujan $t$ arvo kasvaa, vaan arvot heilahtelevat edestakaisin. Tällöin kyseessä on värähtely. Se voi olla vaimenevaa tai kasvavaa tai pysyä samanlaisena. Jos kompleksiluvun reaaliosa on positiivinen, niin värähtely on voimistuvaa, ja jos reaaliosa on negatiivinen, niin vaimeneminen on värähtelevää. Jos juuri on kuitenkin kokonaan imaginaarinen, värähtelyn amplitudi ei muutu. Värähtelyä tapahtuu esimerkiksi kulkuneuvojen jousituksessa, heilureissa ja virtapiireissä.

**Esim.** Ratkaise differentiaaliyhtälöt

a) $y''-2y'-3y=0$, b) $y''-4y'+4y=0$, c) $y''-y'+\frac{5}{4}y=0$.

:::{admonition} Ratkaisu
:class: tip, dropdown

a) Ratkaistaan karakteristinen yhtälö $m^2 -2m-3=0$:

$m=\frac{-(-2)\pm\sqrt{(-2)^2-4\cdot 1 \cdot (-3)}}{2\cdot 1} = \frac{2\pm\sqrt{16}}{2} = \frac{2\pm 4}{2}$

$m_1 = \frac{2+4}{2}=3, m_2= \frac{2-4}{2}=-1$

Ratkaisu on siis $y(t)=C_1 e^{-t}+C_2 e^{3t}$.

b) Ratkaistaan karakteristinen yhtälö $m^2-4m+4=0$:

$m=\frac{-(-4)\pm\sqrt{(-4)^2-4\cdot 1 \cdot 4}}{2\cdot 1} = \frac{4\pm 0}{2} = 2$

Ratkaisu on siis $y(t)=(C_1 t+C_2)e^{2t}$.

c) Ratkaistaan karakteristinen yhtälö $m^2-m+\frac{5}{4}=0$:

$m=\frac{-(-1)\pm\sqrt{(-1)^2-4\cdot 1 \cdot \left(\frac{5}{4}\right)}}{2\cdot 1} = \frac{1\pm\sqrt{-4}}{2} = \frac{1\pm\sqrt{4i^2 }}{2} = \frac{1\pm 2i}{2} = \frac{1}{2}\pm i$.

Ratkaisu on siis $y(t)=e^{\frac{1}{2}t}(C_1 \cos{t}+C_2 \sin{t})$.

:::