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

| Onnistumisia kpl	| Sarakkeiden lukumäärä	|
| --- 				| ---					|
| 0					| $\displaystyle \binom{5}{0}=1$	|
| 1					| $\displaystyle \binom{5}{1}=5$	|
| 2					| $\displaystyle \binom{5}{2}=10$	|
| 3					| $\displaystyle \binom{5}{3}=10$	|
| 4					| $\displaystyle\binom{5}{4}=5$		|
| 5					| $\displaystyle\binom{5}{5}=1$		|

Seuraavaksi huomataan, että jos yhden kokeen onnistumisen todennäköisyys on $0{,}3$, niin epäonnistumisen todennäköisyys on $1-0{,}3 = 0{,}7$.

Seuraavaksi selvitämme kunkin mahdollisen lopputuloksen todennäköisyydet. Aloitetaan lopputuloksesta, jossa kaikki kokeet epäonnistuivat. Tämä saadaan ainoastaan, kun jokainen koe epäonnistuu eli todennäköisyys on siis
$$
0{,}7 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 =  0{,}7^5 = 0{,}16807 \approx 16{,}8\ \% .
$$
Tarkastellaan seuraavaksi lopputulosta, jossa 1 koe onnistuu ja 4 epäonnistuu. Nyt onnistunut koe voi olla mikä tahansa 5 kokeesta, joten lopputulos voidaan saada 5 eri tavalla. Jos ensimmäinen koe onnistuu ja muut 4 eivät, niin todennäköisyys on
$$
   0.3 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 = 0{,}07203 \approx 7{,}2\ \% .
$$
Jos toinen koe onnistuu, niin
$$
   0.7 \cdot 0{,}3 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 = 0{,}07203 \approx 7{,}2\ \% .
$$
Vastaavasti 3, 4 ja 5 kokeen onnistumisille saadaan todennäköisyys $0{,}07203 \approx 7{,}2 \%$. Koska kaikkien viiden tapahtuman todennäköisyys on sama, niin lopputuloksen todennäköisyydeksi saadaan
$$
   5 \cdot 0{,}3 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 = 5 \cdot 0{,}3 \cdot 0{,}7^4  =0{,}36015 \approx 36{,}0\ \% .
$$
Kolmantena lopputuloksena on 2 onnistunutta koetta ja 3 epäonnistunutta. Erilaisten kombinaatioiden lukumäärä saadaan binomikertoimen avulla $\displaystyle\binom{5}{2} = \frac{5!}{2! 3!} = 10$, joten erilaisia vaihtoehtoja on 10 kappaletta. Jokaisen näiden todennäköisyys on
$$
   0{,}3 \cdot 0{,}3 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 = 0{,}3^2 \cdot 0{,}7^3=0{,}03087 \approx 3{,}1\ \% .
$$
Lopputulukosen todennäköisyys on
$$
   10 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}7 \cdot 0{,}7 \cdot 0{,}7 = 10 \cdot 0{,}3^2 \cdot 0{,}7^3 = 0{,}3087 \approx 30{,}9\ \% .
$$
Seuraava lopputulos on 3 onnistunutta koetta ja 2 epäonnistunutta. Binomikertoimen avulla saamme, että eri kombinaatioita on $\displaystyle\binom{5}{3} = 10$. Jokaisen näiden todennäköisyys on
$$
   0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}7 \cdot 0{,}7 = 0{,}3^3 \cdot 0{,}7^2= 0{,}01323 \approx 1{,}3\ \% 
$$
joten lopputuloksen todennäköisyys on
$$
   10 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}7 \cdot 0{,}7 = 10 \cdot 0{,}3^3 \cdot 0{,}7^2 =0{,}1323 \approx 13{,}2\ \% .
$$
Lopputuloksen 4 onnistunutta ja 1 epäonnistunut erilaisia vaihtoehtoja on 5, joista jokaisen todennäköisyys on
$$
   0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}7 = 0{,}3^4 \cdot 0{,}7=0{,}00567 \approx 0{,}6\ \% .
$$
Lopputuloksen todennäköisyys on
$$
   5 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}7 = 5 \cdot 0{,}3^4 \cdot 0{,}7=0{,}02835 \approx 2{,}8\ \% .
$$
Lopputulos 5 onnistunutta voidaan saada vain yhdellä tavalla ja sen todennäköisyys on
$$
   0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}3 \cdot 0{,}3 =0{,}3^5 \approx 0{,}00243\ \% .
$$
Voimme seuraavaksi muotoilla yleisen lausekkeen toistokokeen onnistumistodennäköisyydelle.

{% include box.html  
type="theorem"
header="" 
content="
Jos toistokokeen yhden kokeen onnistumistodennäköisyys on $p \in [0,1]$ ja toistokoe suoritetaan $n \ge 1$ kertaa, niin todennäköisyys, että koe onnistuu $k \in \{ 0,1,\dots, n \}$ kertaa, on
$$
\displaystyle\binom{n}{k}\, p^k (1-p)^{n-k}.
$$
" %}

Varmista ennen kuin käytät yllä olevaa teoreemaa, että toistettavat kokeet ovat riippumattomia ja selvitä muuttujien $n$ (toistojen lukumäärä), $k$ (onnistumisten lukumäärä) ja $p$ (yhden kokeen onnistumistodennäköisyys) arvot.		

{% include box.html  
type="exercise"
header="Toistokoe nopalla" 
content='
Tavallista noppaa heitetään 7 kertaa. Millä todennäköisyydellä saadaan täsmälleen kaksi kertaa silmäluku 5 tai 6?
'
dropdown='
Kyseessä on toistokoe, sillä aikaisempi nopan heitto ei vaikuta seuraavan tulokseen. Toistojen lukumäärä $n$ on 7 ja haluamme selvittää, milloin näistä $k=2$ onnistuu. 
							
Aiemman tehtävän xxxx perusteella onnistumistodennäköisyys $p$ on $\frac13$. Teoreeman 5 avulla saamme
$$
\displaystyle\binom{7}{2} \left( \frac13 \right)^2 \left( 1-\frac13 \right)^{7-2} = 21 \cdot \left( \frac13 \right)^2 \cdot \left( \frac23 \right)^5 \approx 24{,}0\ \%.
$$
' %}	

{% include box.html  
type="exercise"
header="Toistokoe nopalla" 
content='
Tavallista noppa heitetään seitsemän kertaa. Laske, millä todennäköisyydellä saadaan 0, 1, 3, 4, 5, 6 ja 7 kertaa silmäluku 5 tai 6. Muodosta tuloksista yhdessä aiemman tehtävän avulla todennäköisyysjakauma.
'
dropdown='
' %}		
	
Yleisin toistokokeen todennäköisyyksiin liittyvä laskuvirhe on binomikertoimen unohtaminen.

## Odotusarvo
	
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

## Itsearviointitehtävä
Varmista, että olet oppinut tämän luvun keskeiset asiat tekemällä itsearviointitesti [opetus.tv:n polku-palvelussa](https://polku.opetus.tv/). Samalla harjoittelet omien ratkaisujesi pisteyttämistä pisteytysohjeiden avulla.