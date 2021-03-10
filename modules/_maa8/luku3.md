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
Sisältö
1. Alatehtävä.
1. Alatehtävä.
dropdown='
Vastauksen sisältö.
' %}					
					
## Tehtäväsarja 2

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