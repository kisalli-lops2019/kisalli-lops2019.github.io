---
layout: module-page
title: Tilastolliset tunnusluvut
chapter: 1
module: Tilastot ja todennäköisyys (MAA8)
---

* content
{:toc}

## Luvun tavoitteet
Tämän luvun tavoitteena on, että pystyt xxxx. Osaat
* xxxxx
* xxxxx
* xxxxx
* xxxxx
* xxxxx
* xxxxx
* xxxxx

## Frekvenssi
Kiinnistava aloitus tilastojen merkityksestä yhteiskunnassa esim. korona.

Tässä luvussa tutkitaan Suomessa asuvia lapsiperheitä, joissa on alle 18-vuotiaita lapsia. Lapsiperheitä koskevat tiedot on poimittu [Tilastokeskuksen sivulta](href="https://www.stat.fi/). Tämä lähestyminen seuraa [kevään 2020 lyhyen matematiikan ylioppilaskokeen tehtävää 6](http://yle.fi/plus/abitreenit/2020/kevat/2020-03-18_N_fi/index.html#6>).

Tutkimista varten määritellään muutamia tilastotieteen keskeisiä käsitteitä.


{% include box.html 
type="definition"
header="Havaintoyksikkö ja havaintoarvo" 
content="
Tutkittavan joukon alkioita kutsutaan *havaintoyksiköiksi*. Havaintoyksikköön liittyvää arvoa tai suuretta kutsutaan *havaintoarvoksi*.
" %}

Tässä tutkittava joukko on Suomessa asuvat lapsiperheet, joissa on alle 18-vuotiaita lapsia. Jokainen perhe on havaintoyksikkö ja perheen alle 18-vuotiaiden lasten lukumäärä on havaintoarvo. 
  
{% include box.html  
type="exercise"
header="Havaintoyksikkö ja havaintoarvo: kotipihan linnut" 
content="
Aleksanteri tutkii kotipihallaan pesivien lintujen linnunpönttöjen asukkaat. Niissä pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen.
1. Mikä Aleksanterin tutkimuksessa on havaintoyksikkö? 
1. Mikä Aleksanterin tutkimuksessa on havaintoarvo?
" 
dropdown="
1. Linnunpöntöt ovat havaintoyksiköitä, niitä on kuusi kappaletta. 
1. Jokaiseen havaintoyksikköön liittyy suure, joka on linnun laji. Linnun laji on siis havaintoarvo.
" %}
  
{% include box.html 
header="Lisätieto: Tilastollinen muuttuja" 
content="
*Tilastolliseksi muuttujaksi* kutsutaan funktiota, joka kuvaa jokaisen havaintoyksikön sitä vastaavalle havaintoarvolle.
" %}  

Tässä moduulissa tutustutaan vain tilanteisiin, joissa havaintoarvoja on äärellinen määrä tai joissa havaintoarvot voidaan numeroida luonnollisilla luvuilla. Tällaisia tilanteita kutsutaan *diskreeteiksi*. Jos tutkittava ominaisuus voi saada mitä tahansa reaalilukuarvoja jollakin välillä, kuten koulun oppilaiden pituudet, ei kyse ole diskreetistä tilanteesta. Näitä tilanteita tutkitaan moduulissa MAA12.
               
Jos joukossa on vähän havaintoyksiköitä, niin havaintoarvot voi esittää luettelemalle ne peräkkäin. Jos havaintoyksiköitä on paljon, niin havaintoarvojen luetteleminen on epäkäytännöllistä ja epähavainnollista. Tällöin havaintoyksiköt pitää *luokitella*. Luokittelussa lasketaan, kuinka moni havaintoyksikkö vastaa kutakin havaintoarvoa. Jos havaintoarvoja on hyvin paljon, täytyy ne ensin luokitella sopiviin luokkiin ennen havaintoyksikköjen laskemista.

Lapsiperheiden luokittelussa lasketaan, kuinka monessa perheessä, eli havaintoyksikössä, on yksi lapsi (havaintoarvo 1), kuinka monessa on kaksi lasta (havaintoarvo 2), jne. Tiedot on koottu alla olevaan taulukoon:
                
| Lasten lkm| $f$ 	|
| ---		| ---	|
| 1			| 241709|
| 2			| 220116| 			
| 3			| 75326	| 
| 4			| 18409	| 
| 5			| 5493	| 
| 6			| 2289	| 
| 7			| 1235	| 
| 8			| 751	| 
| 9			| 476	| 
| 10		| 262	| 
| 11		| 117	| 
| 12		| 41	| 
| 13		| 12	| 
| 14		| 3		| 
| 15		| 0		| 
| 16		| 3		| 
| **Yhteensä**	| **566242**| 
			
Yllä olevassa taulukossa ensimmäinen sarake "Lasten lkm" vastaa aineiston eri havaintoarvoja. Toinen sarake $f$ taas kertoo perheiden lukumäärän. Luku 15 ei ole havaintoarvo, koska missään perheessä ei ole 15 lasta. Se vaikuttaa mahdolliselta havainnolta, koska suurempiakin perheitä on olemassa. Sanotaan, että luku 15 on *mahdollinen havaintoarvo*, ja se otetaan tämän takia mukaan.

Lasten lukumääränä  17 myös on mahdollinen havaintoarvo; huomaa, että nolla ei ole mahdollinen havaintoarvo, koska tutkitaan perheitä, joissa on lapsia. Luokittelussa lapsiperheisiin liittyvät mahdolliset havaintoarvot rajataan ottamalla mukaan vain kaikki mahdollisuudet pienimmän havaintoarvon ja suurimman havaintoarvon väliltä.
				
{% include box.html  
type="definition"
header="Mahdollinen havaintoarvo" 
content="
*Mahdollinen havaintoarvo* on arvo tai suure, johon jokin havaintoyksikkö voisi liittyä.
" %}	

{% include box.html  
type="exercise"
header="Mahdollinen havaintoarvo: kotipihan linnut (jatkoa)" 
content="
Aleksanteri jatkaa linnunpönttöjen tutkimista tutkimalla myös naapurien linnunpöntöt.
1. Anna esimerkki lintulajista, joka on mielekäs mahdollinen havaintoarvo.
1. Anna esimerkki lintulajista, joka ei ole mielekäs mahdollinen havaintoarvo.
" 
dropdown="
1. Kaikki havaintoarvot ovat mahdollisia havaintoarvoja, joten Aleksanterin pihan lintulajit (havaintoarvot) kelpaavat vastaukseksi. Myös esimerkiksi talitiainen on mielekäs mahdollinen havaintoarvo.                                
1. Strutsi, koska se ei pesi pöntössä.
" %}
						
Luku, joka kertoo, kuinka moni havaintoyksikkö liittyy havaintoarvoon, on *frekvenssi*. 

Yllä olevasta taulukosta nähdään esimerkiksi, että havaintoarvon 10 frekvenssi on 262, eli kymmenlapsisia perheitä on Suomessa 262 kappaletta. Jos mahdollinen havaintoarvo ei ole havaintoarvo, niin siihen ei liity yhtään havaintoyksikköä, joten sen frekvenssi on nolla.
					
{% include box.html  
type="definition"
header="Frekvenssi ja suhteellinen frekvenssi" 
content="
Mahdollisen havaintoarvon *frekvenssi* on  sitä vastaavien havaintoyksiköiden lukumäärä. Frekvenssiä merkitään yleensä kirjaimella $f$.

Mahdollisen havaintoarvon *suhteellinen frekvenssi* on sen havaintoyksiköiden osuus kaikista havaintoyksiköistä.	Suhteellista frekvenssiä merkitään yleensä symbolilla $f$ %. 
" %}	

Esimerkiksi voidaan laskea, että kolmilapsisia perheitä on Suomessa $\frac{75326}{566242}=0{,}1330\ldots\approx 13{,}3$ %, joten havaintoarvon 3 suhteellinen frekvenssi on $13{,}3$ %.
	
{% include box.html  
type="exercise"
header="Suhteellinen frekvenssi ja teknisen apuvälineen käyttö: Suomen lapsiperheet" 
content="
Tehtävänä on täydentää taulukkoon suhteelliset frekvenssit.

| Lasten lkm| $f$ 	|
| ---		| ---	|
| 1			| 241709|
| 2			| 220116| 			
| 3			| 75326	| 
| 4			| 18409	| 
| 5			| 5493	| 
| 6			| 2289	| 
| 7			| 1235	| 
| 8			| 751	| 
| 9			| 476	| 
| 10		| 262	| 
| 11		| 117	| 
| 12		| 41	| 
| 13		| 12	| 
| 14		| 3		| 
| 15		| 0		| 
| 16		| 3		| 
| **Yhteensä**	| **566242**|

1. Laske yksilapsisten perheiden osuus kaikista perheistä, eli havaintoarvon 1 suhteellinen frekvenssi.
1. Kopioi taulukko  maalaamalla solut ja liitä tiedot taulukkolaskentaohjelmaan, esimerkiksi LibreOffice Calc- ohjelmaan. 
1. Syötä suhteellisen frekvenssin sarakkeeseen havaintoarvoa 1 vastaavalle riville a-kohdan lausekkeesi kaavana. Jos luku 241709 on solussa B1, niin kirjoita viereiseen soluun `=B1/566242*100` ja paina enter. 		
1. Kopioi kaava jokaiseen havaintoarvoon tarttumalla edellisen kohdan solun oikeasta alakulmasta kiinni ja maalaamalla sarake Yhteensä-riville asti. 	
1. Tarkista vastauksesta, saitko tehtyä samanlaisen taulukon.										
" 
dropdown="
1. Koska tilastossa on lapsiperheitä yhteensä 566242 kappaletta, niin yksilapsisten perheiden osuus kaikista aineiston perheistä on 
					$$\frac{241709}{566242}\approx 42,7\ \%.$$                
1. Taulukkolaskentaohjelman avulla saadaan seuraava taulukko:

| Lasten lkm| $f$ 	| $f$ %	|	 
| ---		| ---	| ---	|
| 1			| 241709| 42,7 %|
| 2			| 220116| 38,9 %|		
| 3			| 75326	| 13,3 %|
| 4			| 18409	| 3,3 %	|
| 5			| 5493	| 1,0 %	|
| 6			| 2289	| 0,4 %	|
| 7			| 1235	| 0,2 %	|
| 8			| 751	| 0,1 %	|
| 9			| 476	| 0,08 %|
| 10		| 262	| 0,05 %|
| 11		| 117	| 0,03 %|
| 12		| 41	| 0,007 %|
| 13		| 12	| 0,002 %|
| 14		| 3		| 0,0005 %|
| 15		| 0		| 0 %	|
| 16		| 3		| 0,0005 %|
| **Yhteensä**	| **566242**| 100 % |
" %}	

Mahdollisten havaintoarvojen ja suhteellisten frekvenssien muodostamaa kokonaisuutta kutsutaan *jakaumaksi*. Jakaumiin tutustutaan tarkemmin luvussa [jakaumat]. 

{% include box.html  
type="exercise"
header="Frekvenssi ja suhteellinen frekvenssi: kotipihan linnut (jatkoa)" 
content="
Aleksin kotipihalla pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen. Kerää lintulajien frekvenssit ja suhteelliset frekvenssit taulukkoon.
" 
dropdown="
| Havaintoarvo	| $f$ 	| $f$ %	|	 
| ---			| ---	| ---	|
| punarinta		| 1		| $\frac{1}{6}\approx 16,7\ \%$|
| kirjosieppo	| 2		| $\frac{2}{6}\approx 33,3\ \%$|		
| sinitiainen	| 3		| $\frac{3}{6}=50\ \%$|
| **Yhteensä**	| 6		| 100 %	|
" %}

## Keskiluvut

Aineistoja tutkittaessa mielenkiinnon kohteena on usein löytää aineiston "tyypillisin" tai "keskimmäisin" tapaus. Tätä kuvaamaan käytetään erilaisia keskilukuja. Niiden määrittämisen mielekkyys riippuu havaintoarvojen luonteesta, eli siitä mitä on mielekästä kutsua "tyypilliseksi" kyseisessä aineistossa.

Yksi keskiluku on aineiston yleisin havaintoarvo. Lapsiperheitä tutkiessa huomattiin, että  yksilapsisia perheitä on havaintoyksiköistä kaikkein eniten. Tilastotieteessä yleisintä havaintoarvoa kutsutaan *moodiksi*.

{% include box.html  
type="definition"
header="Mahdollinen havaintoarvo" 
content="
*Moodi* on havaintoarvo, jolla on suurin frekvenssi. Jos useammalla havaintoarvolla on suurin frekvenssi, niin ne kaikki ovat moodeja.
" %}

Havaintoarvot noudattavat *luokitteluasteikkoa*, jos  arvot voidaan ainoastaan luokitella, mutta niitä ei voi asettaa suuruusjärjestykseen. Tällaisia  ovat esimerkiksi silmien väri, sukupuoli, asuinkunta jne.
				
{% include box.html  
type="exercise"
header="Luokitteluasteikko ja moodi: kotipihan linnut (jatkoa)" 
content="
Aleksanterin kotipihalla pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen.
1. Noudattavatko arvot luokitteluasteikkoa?
1. Mikä on niiden moodi?

" 
dropdown="
1. Lintulajeija ei voi laittaa suuruusjärjestykseen, mutta ne voidaan luokitella. Eli kyseessä on luokitteluasteikko.						                               
1. Moodi on \"sinitiainen\".
" %}

Havaintoarvot noudattavat *järjestysasteikkoa*, jos  arvot voidaan asettaa suuruusjärjestykseen. Tälläisiä ovat esimerkiksi sotilasarvo tai ylioppilastutkinnon arvosanat (I, A, ..., E, L). Peruslaskutoimitukset eivät ole sallittuja (numeerisella) järjestysasteikolla, koska luokkien väliset etäisyydet voivat olla erisuuria.

{% include box.html  
type="exercise"
header="Järjestysasteikko" 
content="
Ylioppilastutkinnossa arvosanat rinnastetaan lukuihin seuraavasti: I vastaa lukua 0, A vastaa lukua 2, B vastaa lukua 3, ...,  E vastaa lukua 6 ja L vastaa lukua 7.  Ajatellaan seuraavaa tilannetta:
1. \"Maija ja Matti kävivät uusimassa matematiikan ylioppilaskokeen. Maija sai korotettua arvosanasta I arvosanaan B ja Matti arvosanasta M arvosanaan L.\"
1. Voidaanko tästä päätellä, että Maijan parannus on suurempi kuin Matin? Perustele.
" 
dropdown="
Ei voida, koska emme tunne eri havaintoarvojen välisiä etäisyyksiä. Maijan arvosanan parannus 3 ei kuvaa arvosanojen I ja B välistä etäisyyttää, kuten ei myöskään Matin arvosanan parannus 2 arvosanojen M ja L välistä etäisyyttä. Koska luvut eivät kuvaa etäisyyksiä, niin niitä ei voi verrata. 						
" %}	

Järjestysasteikolla havaintoarvoille voidaan määrittää moodin lisäksi mediaani.

{% include box.html  
type="definition"
header="Mediaani" 
content="
*Mediaani* on suuruusjärjestykseen järjestettyjen havaintoarvojen keskimmäinen havaintoarvo, jos havaintoarvoja on pariton määrä tai jos parillisessa tapauksessa kaksi keskimmäistä arvoa ovat samat. Jos parillisessa tapauksessa kaksi keskimmäistä havaintoarvoa ovat erisuuret, niin silloin mediaan on nämä molemmat arvot.			
" %}		

{% include box.html  
header="Lisätieto" 
content="
Välimatka-asteikolla parillisessa tapauksessa  mediaani voi  vaihtoehtoisesti olla keskimmäisten lukujen keskiarvon.
" %}	

Kirjoittamalla lapsiperhe-esimerkissä kaikki havaintoarvot eli kaikkien perheiden lasten lukumäärät peräkkäin suuruusjärjestykseen saamme:

$${\tiny
					
\underbrace{1, \ldots, 1}_{241\,709\text{kpl}}, \underbrace{2, \ldots, 2}_{220\,116\text{kpl}},
\underbrace{3, \ldots, 3}_{75\,326\text{kpl}}, \underbrace{4, \ldots, 4}_{18\,409\text{kpl}},
\underbrace{5, \ldots, 5}_{5\,493\text{kpl}}, \underbrace{6, \ldots, 6}_{2\,289\text{kpl}},
\underbrace{7, \ldots, 7}_{1\,235\text{kpl}}, \underbrace{8, \ldots, 8}_{751\text{kpl}},
\underbrace{9, \ldots, 9}_{476\text{kpl}}, \underbrace{10, \ldots, 10}_{262\text{kpl}},
\underbrace{11, \ldots, 11}_{117\text{kpl}}, \underbrace{12, \ldots, 12}_{41\text{kpl}},
\underbrace{13, \ldots, 13}_{12\text{kpl}}, 14, 14, 14, 16, 16, 16.					
}$$

Tässä on yhteensä 566242 lukua, joka on parillinen määrä. Näin ollen keskimmäistä lukua ei ole. Ensimmäisen puolikkaan viimeinen luku on 2, kuten myös toisen puolikkaan ensimmäinen luku. Mediaani on siis 2.
					
{% include box.html  
type="exercise"
header="Suhteellinen frekvenssi ja mediaani" 
content="
Laske alla olevaan taulukkoon suhteelliset frekvenssit. Pystyykö pelkistä suhteellisista frekvensseistä määrittämään mediaanin?


| **Arvosana**	| 4	| 5	| 6	| 7	| 8	| 9	| 10	|
| **Lkm**		| 1	| 0	| 3	| 1	| 2	| 1	| 2		|
|	$f$ %		|	|	|	|	|	|	|		|							

" 
dropdown="
" %}

Havaintoarvot noudattavat *välimatka-asteikkoa*, jos arvojen erotus on mielekkäästi tulkittavissa. Tällaisia  ovat esimerkiksi kouluarvosana, vuosiluku, jne. 
				
Esimerkiksi mineraalien luokittelussa ja tunnistamisessa käytetään kovuutta kuvaava Mohsin asteikkoa. Se on esimerkki järjestysasteikosta, joka ei ole välimatka-asteikko. Tämä käy ilmi seuraavasta lainauksesta:

> "Mineraalit on jaettu kymmeneen kovuusluokkaan ns. Mohsin kovuusasteikon mukaan. Asteikossa ylemmän luokan mineraalilla kyetään naarmuttamaan alemman luokan mineraalia. [...] Asteikko ei ole läheskään tasavälinen, minkä paljastaa mineraalien todellisia kovuuksia kuvaava ns. Rosiwallin asteikko."
*Kalle Taipale: Kivet ja mineraalit Suomen luonnossa, Otava, 2010, s. 78.*

{% include box.html  
header="Lisätieto: Suhdeasteikko" 
content="
Havaintoarvot noudattavat *suhdeasteikkoa*, jos arvojen erotus on mielekkäästi tulkittavissa ja muuttujan arvoilla on jokin absoluuttinen nollakohta. Suhdeasteikko on aina välimatka-asteikko. Esimerkiksi pituus ja rahan määrä ovat suhdeasteikkoja. 			
" %}

Välimatka-asteikolla voi laskea moodin ja mediaanin lisäksi keskiarvon. 

{% include box.html  
type="definition"
header="Keskiarvo" 
content="
(Aritmeettinen) *keskiarvo* on havaintoarvojen summa jaettuna havaintoyksiköiden lukumäärällä.
" %}	

{% include box.html  
header="Lisätieto: Keskiarvoista" 
content="
Edellä määritelty keskiarvo on \"aritmeettinen keskiarvo\", mutta sana \"aritmeettinen\" jätetään pois, koska tässä moduulissa ei käsitellä muita keskiarvoja. Muita yleisesti käytettyjä keskiarvoja ovat \"geometrinen keskiarvo\" ja \"harmoninen keskiarvo\".						
" %}

Tutkitaan lapsiperhe-esimerkin lasten lukumäärän (aritmeettista) keskiarvoa. Lasketaan lasten lukumäärä kertomalla ensin lasten lukumäärät niiden frekvensseillä ja laskemalla sitten saadut luvut yhteen: 
$$
\begin{split}
	&241\,709 \cdot 1 + 220\,116 \cdot 2 + 75\,326 \cdot 3 + 18\,409 \cdot 4 + 5\,493 \cdot 5 + 2\,289 \cdot 6
	+  1\,235 \cdot 7 + 752 \cdot 8\\
	&\quad + 476 \cdot 9
	+ 262 \cdot 10 + 117 \cdot 11 + 41 \cdot 12 + 12 \cdot 13 + 3 \cdot 14 +0 \cdot 15 + 3 \cdot 16
	=1\,046\,336
\end{split}
$$
ja jaetaan se perheiden lukumäärällä
$$
\frac{1\,046\,336}{566\,242}\approx 1{,}85.
$$
Näin ollen lapsiperheiden lasten lukumäärän keskiarvo on noin 1,85. 

{% include box.html  
type="exercise"
header="Teknisen apuvälineen käyttö tunnuslukujen selvittämisessä" 
content="
Syötä aiemman lapsiperheiden kokoa kuvaavan taulukon luvut tietokoneohjelmaan, ja laske ohjelman avulla moodi, keskiarvo ja mediaani. Tarkista, että saat samat vastaukset kuin tässä materiaalissa.				
"  %}

Huomaa, että lapsiperhe-esimerkissä moodi, keskiarvo ja mediaani ovat kaikki eri lukuja. Ne voivat olla kaikki samoja, kaksi on samoja ja yksi on eri tai kaikki eri lukuja.
				
{% include box.html  
type="exercise"
header="Moodi, mediaani ja keskiarvo" 
content="
Anna esimerkki kokonaislukujen 4, ..., 10 havaintoarvoista, jossa
1. moodi, mediaani ja keskiarvo ovat samoja
1. moodi ja mediaani ovat samoja mutta keskiarvo eroaa näistä,
1. moodi, mediaani ja keskiarvo ovat kaikki eri suuria.
" %}	

{% include box.html  
type="exercise"
header="Moodi, mediaani ja keskiarvo" 
content="
Ovatko seuraavat väitteet totta?
1. Mediaani on aina suurempi kuin moodi.
1. Moodi on aina pienempi kuin keskiarvo.
1. Keskiarvo ja mediaani eivät voi olla yhtä suuria.
" %}

Huomaa, että järjestysasteikossa havaintoarvot voidaan samaistaa mihin tahansa kasvavaan kokoelmaan lukuja. Samaistuksen jälkeen keskiarvon tekninen laskeminen on mahdollista, mutta saatu tulos ei välttämättä kerro mitään alkuperäisestä tilanteesta, kuten seuraavassa esimerkissä. 
				
Olisiko seuraavat tehtävät TSII? 

{% include box.html  
type="exercise"
header="Asteikot" 
content="
Aleksanteri on lähdössä Kemijärveltä maastopyörävaellukselle. Hän luokittelee kiinnostavat kohteet kolmeen luokkaan: luokassa 1 etäisyys Kemijärveltä on alle 50 km, luokassa 2 etäisyys Kemijärveltä on  50-150 km, luokassa 3 etäisyys Kemijärveltä on  yli 150 km. 
				
Nyt havintoyksikköinä ovat paikat ja havaintoarvoina numerot 1, 2 ja 3. Havaintoarvot muodostavat järjestysasteikon, mutta eivät välimatka-asteikkoa. Miksi?
" 
dropdown="
Esimerkiksi Savukosken kuntakeskus kuuluu luokkaan 2 ja Kemihaara luokkaan 3. Nyt Kemihaaran ja Savukosken kuntakeskuksen luokkien erotuksella  $3-2 =1$ ei ole järkevää tulkintaa.  Siitä ei esimerkiksi voi päätellä mitään Kemihaaran ja Savukosken kuntakeskuksen välisestä etäisyydestä. Myöskään luokkien keskiarvolla $\frac{2+3}{2}= \frac52$ ei ole järkevää tulkintaa. 							
" %}		

{% include box.html  
type="exercise"
header="Moodi, mediaani ja keskiarvo" 
content="
Lomakkeissa kysytään usein koulutusta. Mitkä keskiluvut voidaan määrittää, jos vastausvaihtoehdot ovat 
1. peruskoulu, ammattikoulu, lukio, alempi korkeakoulututkinto, ylempi korkeakoulututkinto, jatkotutkinto,
1. peruskoulu, 2. asteen koulutus,  korkeakoulututkinto, jatkotutkinto?
" %}		

{% include box.html  
type="exercise"
header="Luokitteluasteikot" 
content="
Keksi esimerkkejä havaintoarvioista, joille voit soveltaa  
1. moodia, mutta et mediaania,
1. moodia ja mediaania, mutta et keskiarvoa,
1. moodia, mediaania ja keskiarvoa?
" %}

## Keskihajonta

Eri havaintoarvojen joukoilla voi olla sama keskiarvo, esimerkiksi silloin, kun joukot ovat 5, 7, 9 ja 7, 7, 7. Keskiarvo ei siis kerro, miten  havaintoarvot ovat jakautuneet. Tutustumme tässä luvussa *keskihajontaan*., joka  kuvaa havaintoarvojen jakautumista keskiarvon ympärille. Tässä luvussa ajattelemme, että meillä on käytössä välimatka-asteikko, jolloin voimme laskea havaintoarvojen erotuksia.

{% include box.html  
type="definition"
header="Vaihteluväli" 
content="
Pienin ja suurin havaintoarvo määräävät *vaihteluvälin*. Vaihteluvälin pituus on suurimman ja pienimmän havaintoarvon erotus.                  
" %}

Alla olevassa taulukossa on Tuulian ja Lukan koearvosanoja. Molemmilla on sama keskiarvo 8, sama vaihteluväli  $[6, 10]$ ja sama vaihteluvälin pituus $10-6=4$, mutta siitä huolimatta näyttää siltä, että Tuulian arvosanoissa on enemmän vaihtelua. 


| **Arvosana**		| 4	| 5 | 6 | 7 | 8	| 9	| 10	|
| **Tuulia (lkm %)**| 0 | 0 | 3	| 0	| 1	| 0 | 3		|
| **Luka (lkm %)**	| 0	| 0	| 1	| 1	| 3	| 1	| 1		|

{% include box.html  
type="definition"
header="Keskihajonta" 
content="
*Keskihajonta* on
$$
\sqrt{\frac1n \sum_{j=1}^n (x_i - \bar x)^2} ~,
$$
missä $x_1, \ldots, x_n$ ovat havaintoarvot ja $\bar x$ on niiden keskiarvo. Keskihajontaa merkitään usein kirjaimella $\sigma$.              
" %}	

Jatketaan Tuulian ja Lukan koearvosanojoen analysointia ja lasketaan Tuulian ja Lukan koearvosanojen keskihajonta, yllä olevan taulukon tiedoilla. Molempien koearvosanojen keskiarvo on 8.  Tuulian koearvosanojen keskihajonta on
		
$$
\begin{split}
	&\sqrt{\frac{1}{7}\left( (6-8)^2+ (6-8)^2 +(6-8)^2 + (8-8)^2 + (10-8)^2+ (10-8)^2+ (10-8)^2\right)}\\
	&= \sqrt{\frac{1}{7}\left(4+4+4+0+4+4+4\right)} \approx 1{,}9
\end{split}
$$
ja Lukan koearvosanojen keskihajonta on
$$
\begin{split}
	&\sqrt{\frac{1}{7}\left((6-8)^2+ (7-8)^2 +(8-8)^2 + (8-8)^2 + (8-8)^2+ (9-8)^2+ (10-8)^2\right)}\\
	&= \sqrt{\frac{1}{7}\left(4+1+0+0+0+1+4\right)} \approx 1{,}2. 
\end{split}
$$
Kuten aiemmin jo huomattiin, Tuulian koearvosanoissa on enemmän vaihtelua kuin Lukan.  
					
{% include box.html  
type="exercise"
header="Tunnusluvut teknisen apuvälineen avulla" 
content="
Tilastokeskuksen sivuilta osoitteesta [http://www.tilastokeskus.fi/til/lop/index.html] löyttyy taulukko lukion opiskelijamääristä maakunnittain. Lataa aineisto ja laske siitä tietokoneohjelmalla moodi, mediaani, keskiarvo ja keskihajonta.
" %}

{% include box.html  
type="exercise"
header="Keskihajonta" 
content="
Jos kahden joukon havaintoarvoilla on sama keskiarvo ja sama keskihajonta, niin ovatko joukot välttämättä samoja? 
" %}

## Diagrammit

Diagrammeilla voidaan havainnollistaa ja konkretisoida havaintoaineistoa. Pylväsdiagrammi sopii esimerkiksi absoluuttisten määrien esittämiseen, kun taas ympyrädiagrammi havainnollistaa hyvin suhteita. Diagrammin tyyppiä valitessa tulee kiinnittää erityistä huomiota siihen, että diagrammi havainnollistaa haluttua asiaa.

Alla olevissa diagrammeissa on esitetty lapsiperheiden kokonaismäärä ja suhteellinen osuus:

![Pylväsdiagrammi](/images/pylvasdiagrammi-lapsiperheet.png "Pylväsdiagrammi")
![Ympyrädiagrammi](/images/ympyradiagrammi-lapsiperheet.png "Ympyrädiagrammi")    

Ajatellaan että havaintoarvot noudattavat järjestysasteikkoa, ja järjestetään havointoarvot nousevaan järjestykseen. Tällöin voimme laske summafrekvenssin ja suhteellisen summafrekvenssin.

{% include box.html  
type="definition"
header="Summafrekvenssi ja suhteellinen summafrekvenssi" 
content="
Olkoot $x_1, \ldots, x_k$ havaintoarvot, jotka ovat suuruusjärjestyksessä. Olkoon $f_i$ havaintoarvoa $x_i$ vastaava frekvenssi, sekä $f_i\%$ havaintoarvoa $x_i$ vastaava suhteellinen frekvenssi. Tällöin  *summafrekvenssi* on funktio

$$
S_j =\sum_{i=1}^j f_i
$$ 
ja *suhteellinen summafrekvenssi* on funktio
$$
\Sa_j=\sum_{i=1}^j f_i\%.
$$
Molemmissa funktioissa $j \in \{1, 2, 3, \ldots, k\}$.
" %}

Huomaa, että $S_k$ antaa havaintojen kokonaismäärän ja $\Sa_k=1$. Funktio $S$ on kasvava ja se saa korkeintaan $k$ eri arvoa. Huomaa, että summafrekvenssi voidaan määritäää myös rekurssivisesti
$$
S_{j+1} = \sum_{i=1}^{j+1} f_i = \sum_{i=1}^{j} f_i + f_{j+1} = S_j + f_{j+1}. 
$$

Vastaavasti suhteellinen summafrekvenssi on 
kasvava funktio, joka saa korkeintaan $k$ eri arvoa. Myös suhteellisen summafrekvenssin voi  samalla tavalla esittää rekursiivisesti.  

Määritellään summafrekvenssi ja suhteellinen summafrekvenssi  lapsiperhe esimerkissä. Lasketaan ensin summafrekvenssin ja suhteellisen summafrekvenssin arvot eri pisteissä. Huomaa, että suhteellinen summafrekvenssi pyöristyy kahden desimaalin tarkkuudella arvoon $100{,}00\%$ alkaen muuttujan arvosta 10. Piirretään tämän jälkeen niiden kuvaajat.
 
| $x_j$	|	$S_j$ 			| $Sa_j$ 			| 
| ---	| ---				| ---				|
| 1		| $S_1 =  241,709$ 	| $Sa_1 = 42{,}7 %$	|
| 2		| $S_2 = S_1 +   220,116 = 461,825$	| $Sa_2 = Sa_1 + 38{,}9=81,6  %$ |
| 3		| $S_3 = S_2 +   75,326 = 537, 151$	| $Sa_3 = Sa_2 + 13{,}3= 94,9  %$ |
| 4		| $S_4 = S_3 + 18,409 = 555,560$	| $Sa_4 = Sa_3 + 3{,}3= 98,2 %$ |
| 5	| $S_5=  551,053$	| $Sa_5 = 99,2 %$ |
| 6	| $S_6 =    563,342$	| $Sa_6=99{,}6 %$ |
| 7	| $S_7=  564,577$	| $Sa_7=99{,}8 %$ |
| 8	| $S_8=  565,328$	| $Sa_8=99{,}9 %$ |
| 9	| $S_9=  565,804$	| $Sa_9=99{,}98 %$ |
| 10	| $S_{10}=  566,066$	| $Sa_{10} = 100,00 %$ |
| 11	| $S_{11}=   566,183$	| $Sa_{11}=100,00 %$ |
| 12	| $S_{12}=   566,224$	| $Sa_{12}=100,00 %$ |
| 13	| $S_{13}=   566,236$	| $Sa_{13}=100,00 %$ |
| 14	| $S_{14}=   566,239$	|  $Sa_{14}=100,00 %$ |
| 15	| $S_{15}=   566,239$	| $Sa_{15}=100,00 %$ |
| 16	| $S_{16}=   566,242$	|$Sa_{16}=100,00 %$ |

**Taulukko: apsiperheiden lukumäärä alle 18-vuotiaiden lasten määrän mukaan: summafrekvenssi ja suhteellinen summafrekvenssi.**

![Summafrekvenssin kuvaaja](/images/summaf.png "Summafrekvenssin kuvaaja")
![Suhteellisen summafrekvenssin kuvaaja](/images/suht-summaf.png "Suhteellisen summafrekvenssin kuvaaja")    

Suhteellisen summafrekvenssin kuvaajasta voidaan graafisesti määrittää mediaani. Esimerkkikuvaajassa mediaani on 2, sillä kuvaaja saavuttaa 50\% arvon kohdassa 2. Samanlainen päättely voidaan tehdä myös muille prosenttiosuuksille.  Esimerkiksi  arvo 25\% saavuteen muuttujan arvolla 1 ja 95\% muuttujan arvolla 4. Prosenttiosuuksista saamme vastauksen kysymykseen millä havaintoarvolla ja sitä pienemmillä havaintoarvoilla on annettu prosenttiosuus havaintoyksiköistä.     

{% include box.html  
type="exercise"
header="Diagrammit" 
content="
Tutustu ohjelmistosi eri diagrammeihin. Analysoi eri diagrammityyppien hyviä ja huonoja puolia.
1. Mitkä niistä sopivat aiemman Esimerkin 1 pihalinnuista havainnollistamiseen?
1. Mitkä niistä sopivat lapsiperheiden frekvenssien ja suhteellisten frekvenssien havainnollistamiseen?
" %}    

{% include box.html  
type="exercise"
header="Luokittelu ja suhteellinen frekvenssi" 
content='
Suomessa on yhteensä 311 kuntaa. Asukasluvultaan suurin on Helsinki \(635181 asukasta\). Manner-Suomen pienin kunta on Luhanka \(756 asukasta\) ja Ahvenanmaan pienin kunta on Sottunga \(96 asukasta\). Melkein kaikissa kunnissa on eri määrä asukkaita, joten havaintoarvot täytyy luokitella ennen frekvenssien laskemista.

[Kuntaliiton verkkosivujen](https://www.kuntaliitto.fi/vaestotietoja-kunnittain) \(luettu 21.10.2020\) kuvassa kunnat, eli havaintoyksiköt, on luokiteltu asukasmäärän, eli havaintoarvon, mukaan viiteen eri luokkaan.

![Kuntaliiton verkkosivujen kuva Suomen kunnista](images/kunta.png "Suomen kunnat")

1. Miten asukasmäärät on luokiteltu?
1. Mitä tarkoittavat kuvan luvut 21, 34, 43, 80 ja 133?
1. Laske luokkien suhteelliset frekvenssit.
' 
extra="
1. alle 5000 asukasta, 5000–10000 asukasta, 10001–20000 asukasta, 20001–50000 asukasta ja yli 50000 asukasta.
1. Luokkien frekvenssit.	
" %}

## Tehtäväsarja 2

{% include box.html  
type="exercise"
header="Frekvenssi" 
content="
Mikä seuraavissa tapauksissa on havaintoyksikkö ja mikä on havaintoarvo? Huomaa, että kysymykseen ei ole olemassa vain yhtä oikeata vastausta.
1. Puolueiden kannatusmittaus.
1. Kuukausittainen kuluttajahintaindeksi.
1. Viime vuonna tapahtuneet liikenneonnettomuudet.
1. Suomen kuntien väkiluku. 
" 
dropdown="
1. Havaintoyksikkö: kyselyyn osallistuja henkilö. Havaintoarvo: puolue.
1.  Havaintoyksikkö: kuukausi (ja vuosi). Havaintoarvo: indeksin arvo.
1.   Havaintoyksikkö: yksittäinen onnettomuus. Havaintoarvo: loukkaantuneiden lukumäärä.
1.  Havaintoyksikkö: kunta. Havaintoarvo: väkiluku.
" %}

{% include box.html  
type="exercise"
header="Frekvenssi" 
content="
Tilastokeskuksen [Paavo-tietokannasta](https://www.stat.fi/tup/paavo/index.html) löytyy tietoa postinumeroittain. Tutkitaan 18 vuotta täyttäneiden koulutusastetta. Etsi kahden [postinumeroalueen koulutusastetiedot](http://pxnet2.stat.fi/PXWeb/pxweb/fi/Postinumeroalueittainen\_avoin\_tieto/Postinumeroalueittainen\_avoin\_tieto\_\_2020/paavo\_pxt\_12ez.px/) (perusaste, ylioppilastutkinto, ammatillinen tutkinto, alempi korkeakoulututkinto, ylempi korkeakoulututkinto) kaikilta 18 vuotta täyttäneiltä ja laske suhteelliset frekvenssit.
" 
dropdown="" %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Tutki [THL:n ekaluokkalaisen vanhemmille tarkoitettua esitietolomaketta](https://www.thl.fi/attachments/kasvunkumppanit/kouluterveydenhuolto/THL\_1lk\_vanhemmille\_FI\_lomake.pdf). Tehtävässä voidaan ajatella että jokainen ekaluokkalainen on havaintoyksikkö ja mikä tahansa kysymyksen vastaus voidaan valita havaintoarvoksi. Etsi kysymys, jonka vastaukset
1. noudattavat luokitteluasteikkoa mutta eivät järjestysasteikkoa,
1. noudattavat järjestysasteikkoa mutta eivät välimatka-asteikkoa,
1. noudattavat välimatka-asteikkoa
" 
dropdown='
1. Esimerkiksi "Lapsi asuu", \[molempien vanhempien kanssa/äidin kanssa/isän kanssa/muu järjestely\]
1. Esimerkiksi "Millaiseksi arvioitte lapsenne nykyisen terveydentilan?", \[hyvä/keskinkertainen/huono\]
1. Esimerkiksi "Lapsemme nukkuu arkisin ____ tuntia."						
' %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Mitkä seuraavista noudattavat järjestysasteikkoa, välimatka-asteikkoa tai ei kumpaakaan?
1. Vuorokauden keskilämpötila.
1. Koiran sukupuoli.
1. Judossa saavutetun vyön väri (valkoinen, keltainen, vihreä, sininen, ruskea ja musta).
1. Sävelasteikko.
1. Käytetyn auton odometri (kuljettu kokonaismatka).
" %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Oheisessa taulukossa on kevään 2020 pitkän matematiikan arvosanojen lukumäärät. (Lähde: YTL)
| L 	| E 	| M 	| C 	| B 	| A 	| I 	|
| --- 	| ---	| ---	| ---	| ---	| --- 	| ---	|
|852  	| 2397	| 3144	| 3331	| 2245	| 983	| 335	|

1. Mitkä keskiluvut (moodi, mediaani, keskiarvo) aineistosta voi määrittä?
1. Määritä a-kohdan keskiluvut.
" %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Taulukosta puuttuu yksi kokonaisluku.
|$x$	| 0	| 1	| 2	| 3	| 4	| 5	|
|$f$	| 9	| 3	| 4	| 	| 6 | 8	| 

Mitä pystyt päättelemään puuttuvasta luvusta, jos tiedot että  muuttujan $x$

1. moodi on $3$?
1. mediaani on $2$?
1. keskiarvo on $\frac83$?
" 
dropdown='
1. Luku on aidosti suurempi kuin $9$.
1. Lukua on $0$ tai $1$.
1. Merkitään puuttuvaa lukua muuttujalla $z$. Yhtälö
$$
\frac{9\cdot 0 + 3 \cdot 1 + 4 \cdot 2 +  z \cdot 3 + 6 \cdot 4 + 8 \cdot 5}{7+3+4+z+6+8}=\frac83,
$$ 
josta $z=5$.				
' %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Tarkastellaan seuraava taulukkoja, jossa $z$ on positiivinen kokonaisluku, 
|$x$	| a	| b	| c	| d	| e	| f	|
|$f$	| 7	| z	| 4	| z	| 6 | 8	| 

Millä luvun $z$ arvoilla muuttujan $x$

1. moodi on $f$?
1. mediaani on $d$?
" 
dropdown='
1. $z<8$
1. Havaintoarvoja on yhteensä $7+z+4+z+6+8= 25+2z$ kappaletta. Huomataan että alkioita on pariton määrä, siis on olemassa keskimmäinen alkio, ja tämän tulee olla muuttujan $x$ arvon $d$ kohdalla. Keskimmäinen alkio on  $\frac{25+2z-1}{2}+1=13+z$ alkio vasemmalta tai oikealta laskien. Havaintoarvo $f$ on $8$ kappaletta ja havaintoarvoa $e$ $6$ kappaletta. Täytyy siis olla että $13+z > 8+6$, eli $z \ge 2$. Toisaalta tulee olla $13+z >7+z+4$ mutta tämä on aina totta. Siis kaikki lukua $2$ suuremmat kokonaisluvut kelpaavat.
' %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Perheessä on kaksi tyttöä ja kaksospojat. Isä laski, että perheen lasten ikien keskiarvo on 12 vuotta. Perheen tytöt ovat 7- ja 15-vuotiaita. Kuinka vanhoja ovat perheen pojat?
" %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Eräänä vuonna jokaisen kuukauden 15. päivän lämpötilat eräässä Suomen kaupungissa klo 12.00 on lueteltu seuraavassa taulukossa. Laske lämpötilojen keskiarvo ja mediaani. Pohdi, kuvaako laskemasi keskilämpötila hyvin kaupungin keskilämpötilaa kyseisenä vuonna.

| Kuukausi	| Lämpötila $^\circ$C	|
| --- 		| ---					|
| Tammikuu	| $-2{,}8$				|
| Helmikuu	| $-10{,}1$				|
| Maaliskuu	| $-0{,}3$				|
| Huhtikuu	| $+2{,}2$				|
| Toukokuu	| $+5{,}9$				|
| Kesäkuu	| $+9{,}7$				|
| Heinäkuu	| $+21{,}4$				|
| Elokuu	| $+18{,}8$				|
| Syyskuu	| $+5{,}8$				|
| Lokakuu	| $+0{,}6$				|
| Marraskuu	| $-1{,}5$				|
| Joulukuu	| $+2{,}0$				|
" %}

{% include box.html  
type="exercise"
header="Keskiluvut" 
content="
Tarkastellaan lukuja 7, 9, 7, 8, 10 ja 8. Mitkä 4 näistä on valittu, kun niiden mediaani on 7,5, moodi 8.
" 
dropdown='
Koska moodi on 8, niin valituista luvuista 2 on 8. Koska mediaani on 7,5, niin yhden luvun tulee olla pienempi kuin 8 eli 7. Valittuja lukuja voivat siten olla joko 7, 8, 8, ja 9 tai 7, 8, 8 ja 10.
' %}

{% include box.html  
type="exercise"
header="Keskihajonta" 
content="
Lataa [Tilastokeskuksen sivulta taulukko](https://www.stat.fi/tup/alue/kuntienavainluvut.html), jossa on kaikkien Suomen kuntien asukasluku. Laske aineistosta moodi, mediaani ja keskiarvo, sekä keskihajonta.
" %}

{% include box.html  
type="exercise"
header="Keskihajonta" 
content="
1. Määritä joukon $\{\-1, 1\}$ keskihajonta.
1. Onko olemassa toista kaksialkioista joukkoa jolla on sama keskihajonta kuin a-kohdan joukolla? 
1. Onko olemassa toista kaksialkioista joukkoa, jolla on sama keskiarvo ja keskihajonta kuin a-kohdan joukolla.
" 
dropdown='
1. Keskihajonta on 1.
1. Mikä tahansa muotoa $\{a-1, a+1\}$ oleva joukko, missä $a \in \R$, täyttää ko ehdot.
1. Jotta keskiarvo olisi nolla, täytyy joukon olla muotoa $\{-x, x\}$, $x>0$. Tälläisen joukon keskiahjonta
$\sqrt{\frac12(|x|^2+|x|^2)}=|x|$, vain kun $x=1$. Joten toista tälläistä joukkoa ei ole.  
' %}

{% include box.html  
type="exercise"
header="Keskihajonta" 
content="
Onko olemassa sellaista kolmialkioista joukkoa $\{a, b, c\}$ reaalilukuja, jonka keskiarvo on $0$ ja keskihajonta on $\sqrt{2}$? 
" 
dropdown='
Valitaan joukko $\{-x, 0, x\}$, missä $x>0$. Nyt keskiarvo on nolla, ja keskihajonta on $\sqrt{\frac13\cdot 2|x|^2}$. Ratkaisemalla yhtälö $\sqrt{\frac13\cdot 2|x|^2}=\sqrt{2}$ löydetään sopiva $x$.
' %}
             
{% include box.html  
type="exercise"
header="Diagrammit" 
content="
[Tilastokeskuksen sivulta](https://www.stat.fi/tup/alue/kuntienavainluvut.html) löytyy maakuntien asukasluvut. (Avainluvut pylväskuvioina maakunnittain.) Luokittele maakunnat asukasluvun mukaan luokkiin  $[0, 50 000)$, $[50000, 100000)$, $[100000, 150000)$, $[150000, 200000)$, $[200000, 400000)$ ja yli 4000000 asukasta. 
1. Laske luokkien suhteelliset frekvenssit.
1. Esitä frekvenssit kahdella eri diagrammilla.
1. Mieti miten hyvin valitsemasi diagrammit sopivat tilanteeseen? Listaa näiden kahden diagrammien hyvät ja huonot puolet (tässä tilanteessa).
" %}    

{% include box.html  
type="exercise"
header="Diagrammit" 
content="
Sivulta [https://asuntojen.hintatiedot.fi] löytyy tietoa toteutuneista asuntokaupoista. Hae tieto Helsingin Kalliossa (kaupunki: Helsinki, kaupunginosa: Kallio) myydyistä yksiöistä. Tutkitaan neliöhintoja. Luokittele neliöhinnat 500 euron pituisiin luokkiin. Laske luokille suhteelliset frekvenssin ja piirrä summafrekvenssin kuvaaja. Päättele summafrekvenssin kuvaajasta seuraavat asiat:
1. 90\% yksiöistä on tätä neliöhintaa edullisempia.
1. 60\% yksiöitä on tätä neliöhintaa kalliimpia.  
" %} 

{% include box.html  
type="exercise"
header="Diagrammit" 
content='
[Tilastokeskuksen sivua](http://www.tilastokeskus.fi/til/ksyyt/2018/ksyyt$\_$2018$\_$2019-12-16$\_$kat$\_$001$\_$fi.html) on esitetty suomalaisten kuolemansyiden rakenne. 

![Kuolinsyyt](/images/pylvasdiagrammi-lapsiperheet.png "Kuolinsyyt")

Arvioi diagrammin perusteella minkäikäisten ihmisten todennäköisin kuolinsyy on
1. tapaturmat.
1. verenkiertoelinten sairaudet.
1. kasvaimet.
1. alkoholiperäiset syyt.
' %}      
				
## Tehtäväsarja 3

{% include box.html  
type="exercise"
header="Tehtävä" 
content='
Sisältö
1. Alatehtävä.
1. Alatehtävä.
dropdown='
Vastauksen sisältö.
' %}

##Itsearviointitehtävä
Varmista, että olet oppinut tämän luvun keskeiset asiat tekemällä itsearviointitesti [opetus.tv:n polku-palvelussa](https://polku.opetus.tv/). Samalla harjoittelet omien ratkaisujesi pisteyttämistä pisteytysohjeiden avulla.