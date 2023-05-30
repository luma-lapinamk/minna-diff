# Eulerin menetelmä

Funktion $y(x)$ lauseketta ei aina saada ratkaistua differentiaaliyhtälöstä. Tämä ei johdu siitä, että olisi huono matematiikassa, vaan siitä että lauseketta ei ole olemassa tai sitä ei mitenkään pysty selvittämään. Tällöin voidaan kuitenkin laskea funktion $y(x)$ arvoja eri muuttujan arvoilla. Tämä tieto voi hyvinkin riittää. Esimerkiksi jos differentiaaliyhtälö kuvastaa sekoitusongelman säiliössä olevan aineen määrää, riittää tietää lukuarvona, paljonko ainetta on tiettynä kellonaikana.

Funktion arvoja saadaan selville erilaisilla numeerisilla menetelmillä. Peruslähtökohta differentiaaliyhtälöissä on Eulerin menetelmä tai Eulerin algoritmi.

Eulerin menetelmässä derivaatta ilmastaan erotusosamäärällä: $y'(x)\approx\frac{y(x+h)-y(x)}{h}$

Tarkalleen määriteltynähän derivaatta on erotusosamäärän raja-arvo, jossa $h \to 0$.

Sijoitetaan äskeinen derivaatan lauseke yhtälöön: $\frac{y(x+h)-y(x)}{h}=y'(x)$

Yhtälöstä on helppo ratkaista $y(x+h)=y(x)+hy'(x)$

Yhtälön merkitys on se, että pienillä muuttujan muutoksilla $h$ voidaan ajatella, että funktio hetkellisesti käyttäytyy kuten suora, jonka kulmakerroin on $y'(x)$. Pisteestä $y(x)$ päästään seuraavaan pisteeseen $y(x+h)$ tätä suoraa pitkin. Derivaatta pitää laskea uudelleen jokaisessa pisteessä.

Eulerin algoritmia käytettäessä pitää tietää funktiolle jokin alkuarvo $y(x_0)$, josta lähteä liikkeelle. Lisäksi tietenkin pitää olla tiedossa funktion derivaatta $y'(x)$. Differentiaaliyhtälössä tämä derivaatta yleensä riippuu myös itse funktiosta $y(x)$. Siksi derivaattaa merkitään usein funktiona $f(x,y)$.

Askelpituuden $h$ valintaan ei ole mitään sääntöä. Yleensä pieni askelpituus tuottaa paremmin tuloksen. Haluttuun arvoon $x$ pitäisi päätyä kertomalla askelpituus jollakin kokonaisluvulla. Esimerkiksi jos lähtöpiste on $x_0=1$ ja funktion arvo halutaan tietää pisteessä $x=1.3$, niin askelpituudeksi ei kannata valita $h=0.2$ mutta sen sijaan esimerkiksi $h=0.1$ tai $h=0.05$ voi toimia. Pienellä askelpituudella laskutoimitus kannattaa tietenkin automatisoida ohjelmoimalla tai käyttämällä haluamansa ohjelmointikielen valmiita työkaluja.

::::{admonition} Esimerkki 

Tiedossa on differentiaaliyhtälö $y'=x+y$ ja eräs funktion arvo $y(0)=1$. Laske, ratkaisematta differentiaaliyhtälöä, mitä on $y(1.2)$.

:::{admonition} Ratkaisu
:class: tip, dropdown

Funktion derivaatta on $f(x,y)=x+y$. Valitaan askelpituudeksi nyt $h=0.4$, koska silloin päästään kolmella askeleella haluttuun pisteeseen. Lasketaan askel kerrallaan:


$y(0.4) = y(0)+0.4\cdot f(0,y(0)) = 1 + 0.4\cdot (0+1) = 1+0.4=1.4$

$y(0.8) = y(0.4)+0.4\cdot f(0.4,y(0.4)) $

$ \dots = 1.4 + 0.4\cdot (0.4+1.4) = 1.4+0.72=2.12$

$y(1.2) = y(0.8)+0.4\cdot f(0.8,y(0.8)) $

$ \dots = 2.12 + 0.4\cdot (0.8+2.12) = 2.12+1.168=3.38$

Funktion todellinen arvo kyseisessä pisteessä on noin 4.440, joka saadaan ratkaisemalla differentiaaliyhtälö ja sijoittamalla ratkaisuun annettu muuttujan arvo. Lähemmäs oikeaa arvoa päästäisiin pienentämällä askelpituutta. Tätä kokeillaan oppitunnilla.

:::
