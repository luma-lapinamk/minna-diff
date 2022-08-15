# Differentiaaliyhtälö

Differentiaaliyhtälöt ovat tärkeitä, kun tarkastellaan tilanteita, joissa jokin asia muuttuu. Esimerkkejä muuttuvista asioista ovat lämpötila (vaikkapa huonosti eristetyn talon sisällä kovalla pakkasella), väestön määrä (alueella, jonne pitäisi mahdollisesti kaavoittaa uusi asuinalue) ja kondensaattorista purkautuva sähköjännite (tietokoneen sisällä).

Aiemmin muutoksia ollaan tarkasteltu funktion derivaatan avulla. Differentiaaliyhtälöt ovatkin yhtälöitä, joissa esiintyy funktion derivaattoja. Esimerkiksi yhtälö $y'+6=4x$ on differentiaaliyhtälö, jossa esiintyy funktion $y(x)$ derivaatta. Differentiaaliyhtälöistä ei ole tarkoitus ratkaista muuttujaa $x$, vaan funktio $y(x)$. Funktio itse voi myös esiintyä differentiaaliyhtälössä, esimerkiksi $y^2=4y'-6y$.

## Differentiaaliyhtälön ratkaiseminen

Differentiaaliyhtälöiden ratkaisu perustuu integroimiseen. Integrointilaskuissa saadaan aina useampi kuin yksi ratkaisu. Esimerkiksi funktion $f(x)=2x+3$ integraalifunktioita ovat kaikki funktiot $F(x)=x^2+3x+C$, missä $C \in \Re$. Vastaavasti differentiaaliyhtälöille voidaan löytää tällainen ns. yleinen ratkaisu, jossa vakiolle $C$ ei ole määrätty tiettyä arvoa. Jokainen $C$:n arvo vastaa yhtä yksittäisratkaisua. Haluttu yksittäisratkaisu löydetään jonkin funktiolle määrätyn ehdon perusteella. Lisäksi differentiaaliyhtälöllä voi olla erikoisratkaisuja, jotka eivät löydy yleisen ratkaisun perusteella.

Yksinkertaisessa tapauksessa differentiaaliyhtälön ratkaisu tapahtuu aivan samalla tavalla kuin integrointi. Tämä onnistuu silloin, kun differentiaaliyhtälö on ns. perustyyppiä. Yhtälö on muotoa $y'=f(x)$. Yhtälössä esiintyy vain funktion $y(x)$ derivaatta, ei itse funktio $y(x)$. Yleinen ratkaisu löytyy laskemalla $y(x)=\int f(x) \, dx$.

**Esim.** Etsi differentiaaliyhtälölle $y'=4x$ 

a) yleinen ratkaisu, 

b) yksittäisratkaisu, joka toteuttaa ehdon $y(1)=8$.

:::{admonition} Ratkaisu
:class: tip, dropdown
a) Integroidaan: $y(x)=\int 4x \, dx = 2x^2 + C$

b) Ratkaistaan vakio $C$ yhtälöstä $2\cdot 1^2+C=8 \leftrightarrow C=8-6 \leftrightarrow C=6$. Kysytty yksittäisratkaisu on siis $y=2x^2+6$.

:::

## Differentiaaliyhtälön perustyypit

Differentiaaliyhtälöstä on edellisen perustapauksen lisäksi olemassa muutamaa erilaista perustyyppiä, jotka on helppo ratkaista itse laskemalla:
- separoituva yhtälö
- lineaarinen yhtälö
    - homogeeninen yhtälö
    - vakiokertoiminen yhtälö
    
Muun tyyppiset differentiaaliyhtälöt voidaan ratkaista numeerisin menetelmin. Tällöin funktiolle ei ole mahdollista johtaa lauseketta ja laskun lopputuloksena on likiarvo eikä tarkka arvo. Esimerkiksi [WolframAlpha](https://www.wolframalpha.com) osaa ratkaista differentiaaliyhtälöitä, joten sitäkin voi käyttää apuna.



