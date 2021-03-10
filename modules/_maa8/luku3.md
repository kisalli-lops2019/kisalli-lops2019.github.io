---
layout: module-page
title: Todennäköisyysjakauma ja odotusarvo
chapter: 3
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

## Diskreetti todennäköisyysjakauma
Määritellään ensin käsite satunnaismuuttuja. Satunnaismuuttuja liittää tapahtumiin reaalilukuarvon.
             				
{% include box.html  
type="definition"
header="Satunnaismuuttuja" 
content="
*Satunnaismuuttuja* on funktio, joka kuvaa jokaisen alkeistapauksen reaaliluvulle tai jokaisen havaintoyksikön sitä vastaavaksi havaintoarvoksi.
" %}

Satunnaismuuttuja voi esimerkiksi kuvata nopan jokaiseen silmäluvun sitä vastaavalle reaalilukuarvolle
![Noppia](/images/noppia.png "Noppia")

tai se voi kuvata jokaisen lapsiperheen kyseessä olevan perheen lasten lukumääräksi.

Huomaa, että satunnaismuuttuja voi ilmetä teoreettisessa tarkastelussa tai tilastossa. Jälkimmäisessä tapauksessa oletamme, että havaintoarvoilla on välimatka-asteikko. Jos tilastossa on mukana mahdollisia havaintoarvoja, jotka eivät ole havaintoarvoja, niin niihin ei kuvaudu mikään havaintoyksikkö. Satunnaismuuttuja on  siinä mielessä harhaanjohtava termi, että satunnaismuuttujassa ei ole mitään satunnaista. Koska satunnaismuuttuja on funktio, niin sen arvo on yksikäsitteisesti määrätty jokaisessa määrittelyjoukon pisteessä. Satunnaismuuttujan avulla saamme todennäköisyysjakauman. Se kuvaa, kuinka yleisiä satunnaismuuttujan eri arvot ovat.
                
{% include box.html  
type="definition"
header="Todennäköisyysjakauma" 
content="
*Todennäköisyysjakauma* on funktio, joka yhdistää satunnaismuuttujan arvot niitä vastaaviin todennäköisyyksiin.
" %}

Todennäköisyydet saadaan joko teoreettisesta tarkastelusta tai vaihtoehtoisesti ne ovat  havaintoarvojen suhteelliset frekvenssit. Tarvittaessa todennäköisyysjakaumaa voi täydentää arvoilla, joita vastaavat todennäköisyydet ovat nollia. Näin saamme mahdolliset havaintoarvot mukaan todennäköisyysjakaumaan. Jos todennäköisyysjakauma tulee tilastosta, niin se on sama asia kuin  Luvussa [frekvenssi](/maa8/luku1) määritelty jakauma. 
					
Huomaa, että todennäköisyyksien summa on 1 eli $100 \%$. 

{% include box.html  
type="definition"
header="Lisätieto" 
content="
Jos halutaan korostaa, että kyseessä on diskreetin todennäköisyysjakauman yhden tapahtuman todennäköisyys, niin voidaan käyttää termiä *pistetodennäköisyys*.
" %}
	
Yksinkertaisin jakauma on tasainen jakauma, jossa jokaisen arvon suhteellinen frekvenssi on sama. Esimerkiksi kuusisivuisen nopan jokaisen silmäluvun todennäköisyys on $1/6 \approx 16{,}7 \%$.

![Nopanheiton todennäköisyysjakauma](/images/nopan_jakauma.png "Nopanheiton todennäköisyysjakauma")
					
Usein jakauma ei kuitenkaan ole tasainen. Tarkastellaan lapsiperheiden lukumäärää, joka on esitetty alla olevassa kuvassa:

![Lapsiperheiden lasten lukumäärän todennäköisyysjakauma](/images/lapsiperheet_jakauma.png "Lapsiperheiden lasten lukumäärän todennäköisyysjakauma")
					
Todennäköisyysjakaumia kuvataan usein niiden ulkomuodon perusteella. Esimerkiksi yllä olevan kuvan jakaumaa voisi luonnehtia vasemmalle vinoksi. Muita tyypillisiä kuvauksia ovat huippujen lukumäärä, symmetrisyys ja häntien paksuus, kuten alla.

![Vasemmalla kaksihuippunen todennäköisyysjakauma ja oikealla todennäköisyysjakauma, joka muistuttaa normaalijakaumaa](/images/kaksihuippuinen_jakauma.png "Vasemmalla kaksihuippunen todennäköisyysjakauma ja oikealla todennäköisyysjakauma, joka muistuttaa normaalijakaumaa")

Todennäköisyysjakaumasta voidaan määritellä yksittäisten todennäköisyyksien lisäksi todennäköisyyksia, jotka koostuvat eri havaintoarvoista. Esimerkiksi lapsiperheiden tapauksessa voitaisiin kysyä, millä todennäköisyydellä satunnaisesti valitulla lapsiperheellä on enintään 3 lasta? Tai 3-5 lasta?
       
{% include box.html  
type="exercise"
header="Lapsiperheet" 
content='
Alla olevassa taulukossa on esitetty lapsiperheiden lasten lukumäärän jakauma.

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

1. Millä todennäköisyydellä lapsiperheessä on enintään kolme lasta?
1. Millä todennäköisyydellä lapsiperheessä on 3--5 lasta?
1. Millä todennäköisyydellä satunnaisesti valitussa lapsiperheessä on vähintään 3 lasta?
'
dropdown='
1. Lapsiperheissä enintään 3 lasta tarkoittaa, että lapsia on 1, 2 tai 3. Kuvaajassa tämä tarkoittaa kolmea vasemmanpuoleista pylvästä. Todennäköisyys saadaan laskemalla yhteen
$$
42{,}7\ \% + 38{,}9\ \% + 13{,}3 \% \approx 94{,}9\ \%.
$$
1. 3-5 lasta tarkoittaa 3, 4 tai 5 lasta ja sen todennäköisyys on
$$
13{,}3\ \% + 3{,}3\ \% + 1{,}0\ \% \approx 18\ \%.
$$ 
1. Nyt olemme kiinnostuneita perheistä, joiden lasten lukumäärä on 3, 4, 5,... , 15, 16. Tämä voidaan siis laskea vastaavien suhteellisten frekvessien $f \%$ avulla
$$
  13{,}3\ \% + 3{,}3\ \% + \cdots + 0{,}0005\ \%\approx 18{,}4\ \%.
$$
Toisaalta voimme hyödyntää tietoa, että kaikkien tapahtumien todennäköisyyksien summa on 100 %. Nyt laskemme ensin todennäköisyyden, että lapsia on 1 tai 2
$$
  42{,}7\ \% + 38{,}9\ \% \approx 81{,}6\ \%.
$$
Tämän avulla saamme laskettua todennäköisyyden vähintään kolmelle lapselle vähentämällä tämän 100 prosentista eli
$$
  100\ \%-81{,}6\ \% = 100\ \% - 81{,}6\ \% = 18{,}4\ \%.
$$
' %}		

## Binomijakauma
Toistokoe on tilanne, jossa sama koe suoritetaan useampaan kertaan ja tapahtumat ovat toisistaan riippumattomia. Lisäksi toistokokeessa on vain kaksi tulosvaihtoehtoa: onnistuminen ja epäonnistuminen. Toistokokeeseen liittyvää todennäköisyyttä kutsutaan *binomitodennäköisyydeksi*.	

Tarkastellaan tilannetta, jossa kokeen onnistumisen todennäköisyys $p$ on $0{,}3$. Jos sama koe toistetaan 5 kertaa, niin mahdollisia kokeiden tuloksien vaihtoehtoja on $2^5=32$.  Erilaisia toistokokeen lopputuloksia on kuusi: 0 onnistumista, 1 onnistuminen,... , 5 onnistumista. Katso alla oleva taulukko:
![Toistokeen kaikki mahdolliset lopputulokset. Numero 1 tarkoittaa kokeen onnistumista ja numero 0 epäonnistumista.](/images/noppa_toistokoe.png "Toistokeen kaikki mahdolliset lopputulokset. Numero 1 tarkoittaa kokeen onnistumista ja numero 0 epäonnistumista.")

Huomataan aluksi, että jokaisessa lopputuloksessa olevien sarakkeiden lukumäärä taulukossa saadaan binomikertoimella. Merkitään, että numero 1 tarkoittaa kokeen onnistumista ja numero 0 epäonnistumista. Olkoon $A=\{1, 2, \ldots, 5\}$. Valitaan joukosta $A$ $k$ kappaletta alkioita, $k\in[0,5]$. Ajatellaan, että valitut $k$ alkiota kertovat, mihin jonon paikkoihin luku $1$ asetetaan. Loppuihin $5-k$ paikkaan asetetaan luku 0. Tällöin jokainen joukon $A$ $k$-alkioinen osajoukko vastaa yhtä jonoa, jossa on täsmälleen $k$ kappaletta lukuja $1$, ja toisinpäin. Näin ollen jonoja on yhtä paljon kuin $k$-alkioisia osajoukkoja eli $\displaystyle \binom{5}{k}$.
						
					
## Tehtäväsarja 2

{% include box.html  
type="exercise"
header="Tehtävä" 
content='
Sisältö
1. Alatehtävä.
1. Alatehtävä.
'
dropdown='
Vastauksen sisältö.
' %}

## Tehtäväsarja 3

{% include box.html  
type="exercise"
header="Tehtävä" 
content='
Sisältö
1. Alatehtävä.
1. Alatehtävä.
'
dropdown='
Vastauksen sisältö.
' %}

##Itsearviointitehtävä
Varmista, että olet oppinut tämän luvun keskeiset asiat tekemällä itsearviointitesti [opetus.tv:n polku-palvelussa](https://polku.opetus.tv/). Samalla harjoittelet omien ratkaisujesi pisteyttämistä pisteytysohjeiden avulla.