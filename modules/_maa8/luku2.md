---
layout: module-page
title: Todennäköisyys
chapter: 2
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

## Joukko-opin merkintöjä
 Määrittelemme käsitteet joukko ja jono sekä tutustumme niihin liittyviin merkintöihin. 
 * *Joukko* tarkoittaa kokoelmaa *alkioita*. Lisäksi oletamme, että jokaisen alkion osalta on yksikäsitteisesti pääteltävissä, kuuluuko se joukkoon vai ei. Joukkoja merkitään yleensä isoilla kirjaimilla. Jos joukko $A$ sisältää täsmälleen alkiot $1$, $2$ ja $3$, niin kirjoitamme $A=\{1, 2, 3\}$. Joukon merkinnässä alkiot voivat olla missä järjestyksessä tahansa. Merkitsemme sumboolilla $\in$ että alkio kuuluu joukkoon, esim.\ $2 \in A$. Joukot ovat samoja, jos niissä on samat alkiot, merkitsemme tämän yhtäsuuruudella. Joukon merkinnässä sama alkio voi esiintyä useamman kerran, näin esimerkiksi $\{1, 2, 3\}= \{1, 3, 2, 3, 1\}$. Jos joukon määrittelee jokin ehto $P$, niin joukko voidaan kirjoittaa  muodossa $\{x \colon x \text{ toteutaa ehdon } P\}$. Esimerkiksi parilliset luonnolliset luvut voidaan kirjoittaa muodossa $\{ n \in \mathbb{N} \colon \frac{n}2 \in \mathbb{N}\}$, eli otamme joukkoon kaikki ne luonnolliset luvut, joilla on se ominaisuus, että luku jaettuna kahdella on luonnollinen luku. Jos joukon alkiot määrää jokin lauseke, niin joukko voidaan ilmoittaa tämän lausekkeen avulla, esimerkiksi $\{2n\colon n=1, 2, 3\} =\{2, 4, 6\}$. 
 * Sanomme, että joukko $A$ on joukon $B$ *osajoukko*, jos jokainen joukon $A$ alkio kuuluu joukkoon $B$. Merkitsemme tällöin $A \subset B$. Esimerkiksi $\{2, 4\} \subset \{ n \in \mathbb{N} \colon \frac{n}2 \in \mathbb{N}\}$. Huomaa, että jokainen joukko on itsensä osajoukko. 
 * *Tyhjää joukkoa*, jossa ei ole lainkaan alkioita, merkitään $\emptyset$.
* *Jonolla* tarkoitetaan äärellistä tai ääretöntä määrää alkioita, joille on annettu järjestys. Jonossa sama alkio voi esiintyä useamman kerran eri paikassa. Jonoa merkitään kaarisuluilla, jonka sisään alkiot merkitään järjestyksessä, esim. $(1, 3, 2, 1)$ on 4-alkioinen jono. Joukko ja jono ovat eri käsitteitä. Ajatellaan lukuja 1, 2 ja 3. Niistä voidaan kaikki luvut mukaan ottamalla muodostaa vain yksi joukko $\{1, 2, 3\}$, mutta kuusi erilaista kolmen mittaista jonoa: $(1, 2, 3)$, $(1, 3, 2))$, $(3, 1, 2)$, $(3, 2, 1)$,  $(2, 1, 3)$ ja $(2, 3, 1)$. Jonossa jokaisella alkiolla on paikka toisin kuin joukossa. 
             				
{% include box.html  
type="exercise"
header="Joukko-opin merkintöjä" 
content="
1. Ovatko joukot $\{\frac{2n}{n^2}: n= 1, \ldots, 4\}$ ja $\{\frac2{n-5}: n= 6, \ldots, 9\}$ samoja?
1. Kuinka monta kaksialkioista jonoa voidaan joukon $\{a, b, c\}$ alkioista muodostaa?
" %}

{% include box.html  
type="exercise"
header="Joukko-oppi" 
content="
Tarkastellaan joukkoja $A=\{0,1,2,3,4\}$, $B=\{3,4,5\}$ ja
$C=\{2,3\}$.
1. Mitä ovat joukot $A\cup B$, $B\cap C$, $(A\cup B)\cap C$ ja $A\setminus C$?
1. Onko totta, että $B\subset C$?  Ehtä $C\subset A$?
1. Keksi jokin sellainen joukkojen $A$, $B$ ja $C$ välinen joukko-operaatio, että saat tuloksena joukon $\{0,1\}$.
" %}

{% include box.html  
type="exercise"
header="Joukko-oppi" 
content="
Tarkastellaan jonoa $(\lfloor\ln(n)\rfloor\colon n=1,\ldots,9)$, missä merkintä $\lfloor x\rfloor$ tarkoittaa luvun $x$ kokonaisosaa. Esimerkiksi $\lfloor 1\rfloor=1$ ja $\lfloor 2{,}3\rfloor=2$. Määritä jonon ensimmäinen, viides ja viimeinen jäsen. Miksi ei ole mielekästä kysyä, että määritä  joukon $\{\lfloor\ln(n)\rfloor\colon n=0,1,\ldots,9\}$ ensimmäinen, viides ja viimeinen jäsen? Kuinka monta alkiota joukossa $\{\lfloor\ln(n)\rfloor\colon n=0,1,\ldots,9\}$ on?
" %}

{% include box.html  
type="exercise"
header="Joukko-oppi" 
content="
1. Selitä omin sanoin mitä eroa on joukon alkiolla ja osajoukolla.
1. Selitä omin sanoin mitä eroa on joukolla ja jonolla.
" %}

## Klassinen todennäköisyys

Klassinen todennäköisyys perustuu *symmetrisiin alkeistapauksiin*.	Tarkoitamme tällä, että lähtötilanteesta voi sattuman takia päätyä useampaan tulokseen, joista mihin tahansa päätyminen on yhtä todennäköistä. Kaikkien mahdollisten tulosten joukkoa kutsutaan *perusjoukoksi*. Heitetään noppaa yhden kerran. Ennen heittoa emme tiedä nopanheiton tulosta. Tiedämme kuitenkin, että tuloksena on jokin luku perusjoukosta $\{1, 2, 3, 4, 5, 6\}$. Tässä jokainen silmäluku on alkeistapaus ja ne ovat yhtä todennäköisiä. 

*Tapahtumat* ovat perusjoukon osajoukkoja. Seuraavassa tehtävässä on nopanheiton perusjoukko $\{ 1, 2, 3, 4, 5, 6\}$ ja sen osajoukko $\{5, 6\}$, joka vastaa tapahtumaa "tuloksena on viisi tai kuusi".

{% include box.html  
type="definition"
header="Klassinen todennäköisyys" 
content="
Tapahtuman $A$ *klassinen todennäköisyys* on
$$
P(A)=\frac{n(A)}{n(E)},
$$
missä $n(A)$ on tapahtuman $A$ alkioiden eli \"suotuisten alkeistapausten\" lukumäärä ja $n(E)$ on perusjoukon $E$ alkioiden eli kaikkien alkeistapausten lukumäärä.
" %}

{% include box.html  
type="exercise"
header="Yhden nopan heitto" 
content="
Tarkastellaan yhden nopan heittoa, jolloin perusjoukkona on nopanheiton mahdolliset tulokset $E=\{1,2,3,4,5,6\}$. Laske todennäköisyys sille, että tuloksena on viitonen tai kuutonen.
" 
dropdown="
Lasketaan todennäköisyys sille, että tuloksena on viitonen tai kuutonen. Tätä varten merkitään $A=\{5,6\}$, jonka todennäköisyys on
$$
P(A)=\frac{n(A)}{n(E)}=\frac{2}{6}=\frac{1}{3}.
$$
" %}

Tapahtumien todennäköisyydet on tapana ilmoittaa murtolukuina (tarkkoina arvoina), desimaalilukuina esim. kahden merkitsevän numeron tarkkuudella tai prosentteina. Edellisen esimerkin vastauksen voi siis esittää $\frac{1}{3}$, $0{,}33$ tai $33\ \%$.
					
{% include box.html  
type="exercise"
header="Kahden nopan heitto" 
content="
Heitetään kahta noppaa ja tutkitaan noppien silmälukujen summaa.
1. Määritä perusjoukko.
1. Laske todennäköisyys tapahtumalle \"silmälukujen summa on vähintään 10\".
" %}					

Tulkitsemme nyt joukko-opin merkintöjä todennäköisyyden kannalta. Tapahtuma $A = \emptyset$ (tyhjä joukko), jos tapahtuma $A$ on mahdoton eli se ei sisällä alkioita.

Tapahtumien $A$ ja $B$ *yhdiste* on 
$$
A \cup B = \{ A\text{ tapahtuu tai } B \text{ tapahtuu}\}.
$$
Tässä "tai" sisältää mahdollisuuden, että molemmat  $A$ ja $B$ tapahtuvat. Tapahtumien $A$ ja $B$ *leikkaus* on 
$$
A \cap B = \{ A\text{ tapahtuu ja } B \text{ tapahtuu}\},
$$
joka tarkoittaa, että molemmat tapahtumat $A$ ja $B$ tapahtuvat. Tapahtumien $A$ ja $B$ *erotus* on 
$$
A \setminus B = \{ A\text{ tapahtuu ja } B \text{ ei tapahdu}\}.
$$
Joukon $A$ *komplementtia* perusjoukon $E$ suhteen merkitään $\overline{A}=E\setminus A$. Tällöin $P(\overline{A})$ merkitsee todennäköisyyttä, että "$A$ ei tapahdu".

{% include box.html  
type="definition"
header="Erilliset tapahtumat" 
content="
Tapahtumat $A$ ja $B$ ovat *erilliset*, jos $A\cap B=\emptyset$
" %}

Huomaa, että erillisyys riippuu vain joukoista $A$ ja $B$, ei lainkaan niiden todennäköisyyksistä. 

Seuraavat klassisen todennäköisyyden *laskusäännöt* ja muut *perusominaisuudet* voidaan johtaa määritelmän perusteella tarkastelemalla joukkojen alkioiden lukumäärien osamääriä.

{% include box.html  
type="theorem"
header="" 
content="
Olkoot $A$ ja $B$ tapahtumia.
1. Jos $A$ ja $B$ ovat erilliset, niin $P(A\cup B)=P(A)+P(B)$.
1. $P(\overline{A})=1-P(A)$.
1. $0\leqslant P(A)\leqslant 1$.
1. Jos $A\subset B$, niin $P(A)\leqslant P(B)$.
1. $P(A\setminus B)=P(A)-P(A\cap B)$.
1. $P(A\cup B)=P(A)+P(B)-P(A\cap B)$ (\"yhteenlaskukaava\").
" 
dropdown="
Todistamme tässä malliksi kohdat (a) ja (c).
1. Olkoot $A$ ja $B$ erillisiä, eli $A \cap B = \emptyset$. Tällöin joukon $A \cup B$ alkioiden lukumäärä  $n(A\cup B)$ on $n(A) + n(B)$. Saamme
									$$
									P(A \cup B) = \frac{n(A\cup B)}{n(E)} = \frac{n(A) + n(B)}{n(E)} = \frac{n(A) }{n(E)} + \frac{n(B)}{n(E)}= P(A) + P(B). 
									$$
1. -
1. Koska joukon $A$ alkioiden lukumäärä on ei-negatiivinen luku eli $n(A)\ge 0$, ja perusjoukon $E$ alkioiden lukumäärä on positiivinen, eli $n(A)>0$, niin $P(A) = \frac{n(A)}{n(E)} \ge 0$. Toisaalta koska perusjoukon $E$ osajoukkoa $A$ sisältää korkeintaan yhtä monta alkiota kuin perusjoukko itse, eli $n(A) \le n(E)$, niin saamme $P(A) = \frac{n(A)}{n(E)} \le \frac{n(E)}{n(E)} =1$.
1. -
1. -
1. -
" %}

{% include box.html  
type="exercise"
header="Todista laskusäännöt" 
content="
Todista edellisen teoreeman kohdat (b) ja (d)-(e).
" %}
     
{% include box.html  
type="exercise"
header="Yhden nopan heitto" 
content="
Heitetään noppaa. Merkitään $A =\{5, 6\}$ ja $B=\{2,4,6\}$ eli $B$ vastaa tapahtumaa \"tulos on parillinen\". Laske 
1. $P(B)$
1. $P(A\cap B)$
1. $P(A\cup B)$
" 
dropdown="
1. $P(B)=\frac{n(B)}{n(E)}=\frac{3}{6}=\frac{1}{2}$.                                
1. $A\cap B=\{6\}$ ja näin ollen $P(A\cap B)=\frac{n(A\cap B)}{n(E)}=\frac{1}{6}$.
1. Yhteenlaskukaavan (e) perusteella
$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)=\frac{1}{3}+\frac{1}{2}-\frac{1}{6}=\frac{4}{6}.
$$
Tämä on helppo laskea suoraan määritelmästäkin, kun huomaa, että $A\cup B=\{2,4,5,6\}$
" %}	

Nostetaan korttipakasta kaksi korttia peräjälkeen ilman takaisinpanoa. Huomaamme että jälkimmäisellä kerralla pakassa on vain 51 korttia, joten  ensin nostettu kortti vaikuttaa tilanteeseen. 

{% include box.html  
type="definition"
header="Todennäköisyys ehdolla" 
content="
Olkoon $B$ tapahtuma, jolle $P(B)>0$. Tapahtuman $A$ *todennäköisyys ehdolla* $B$ on
						$$
						P(A\mid B)=\frac{P(A\cap B)}{P(B)}.
						$$
" %}

Tapahtuman $A$ todennäköisyys ehdolla $B$ merkitsee sitä, että ehdosta $B$ tehdään satunnaiskokeen uusi perusjoukko ja lasketaan tapahtuman $A$ todennäköisyys tällöin. Ehdollisen todennäköisyyden idea on kuvailla tapahtuman $A$ sattumista olettaen, että tiedämme ehdon $B$ tapahtuneen. 

{% include box.html  
type="exercise"
header="Korttien nosto ilman takaisinpanoa" 
content="
Nostetaan korttipakasta kaksi korttia peräjälkeen ilman takaisinpanoa. Millä todennäköisyydellä jälkimmäinen on kuningas kun tiedämme ensimmäisen olleen kuningas?
" 
dropdown="
Perusjoukko koostuu järjestetyista pareista, joista ensimmäinen jäsen  vastaa ensimmäistä nostoa ja toinen jäsen toista nostoa. Pareja on  $52 \cdot 51 = 2652$ kappaletta. Merkitään että $A$  on niiden parien joukko, joissa ensimmäinen jäsen on \"kuningas\" ja $B$ on niiden parien joukko, joissa toinen jäsen on \"kuningas\".  Näin ollen $A$ vastaa tapahtumaa \"ensimmäinen kortti on kuningas\" ja $B$ vastaa tapahtumaa \"toinen kortti on kuningas\". Saamme
$$
P(A) = \frac{4 \cdot 51}{52 \cdot 51} =\frac1{13} \quad\text{ja} \quad  P(A \cap B) = \frac{4 \cdot 3}{52 \cdot 51}= \frac{1}{13 \cdot 17},
$$
ja näiden avulla
$$
P(B\mid A) = \frac{P(A \cap B)}{P(A)}= \frac{\frac{1}{13 \cdot 17}}{\frac1{13}}=\frac1{17}.
$$
Samaan tulokseen olisimme päässeet myös seuraavalla päättelyllä: Koska ensimmäinen nostettu kortti oli kuningas, niin pakkaan jää 51 korttia, joista 3 on kuninkaita. Todennäköisyys on siis
$$
P(B\mid A)= \frac{3}{51}= \frac1{17}.
$$ 
" %}

Ehdollisen todennäköisyyden määritelmästä seuraa suoraan *kertolaskukaava*:    

{% include box.html  
type="theorem"
header="Mahdollinen havaintoarvo" 
content="
Kun $A$ ja $B$ ovat tapahtumia ja $P(B)>0$, niin $P(A\cap B)=P(B)P(A\mid B)$.
" %}   

{% include box.html  
type="exercise"
header="Pallojen nosto ilman takaisinpanoa" 
content="
Pussissa on 40 palloa, jotka on numeroitu $1, \ldots, 40$. Nostetaan pussista kaksi palloa niin, että ensin nostettua palloa ei palautetta takaisin pussiin.  Mikä on tapahtuman \"tuloksena on 13 ja 40\" todennäköisyys?
" 
dropdown="
Ei ole väliä missä järjestyksessä pallot nostetaan. Tutkitaan ensin tapausta, jossa pallo 13 nousee ensin. Perusjoukko koostuu $40\cdot39=1560$ järjestetystä parista, joista ensimmäinen vastaa ensimmäistä nostoa ja toinen vastaa toista nostoa.

Olkoot $A$ niiden paria joukko joiden ensimmäinen jäsen on  13 ja  $B$ niiden parien joukko joiden toinen jäsen on  40.  Saamme
$$
P(A \cap B) = P(A) P(B\mid A) = \frac{1\cdot 39}{40 \cdot 39} \cdot \frac1{39} = \frac1{1560}.
$$
Tähän samaan tulokseen olisimme päätyneet huomaamalla että tapahtumaa $A\cap B$ on joukko jossa on yksi alkio $(13, 40)$, ja tällöin todennäköisyys on yksi jaettuna perusjoukon alkioiden lukumäärällä.   

Lopputuloksen kannalta ei  ole merkitystä, kumpi luvuista saadaan ensin, joten huomioidaan molemmat mahdollisuudet \"13 ja 40\" sekä \"40 ja 13\". Jälkimmäinen tapaus on samanlainen ensin mainitun kanssa. Saamme kysytyksi todennäköisyydeksi $\frac1{1560} + \frac1{1560} = \frac1{780}$.																					 
" %}

Tutkitaan seuraavaksi tapahtumia, jotka eivät vaikuta toisiinsa.  

{% include box.html  
type="definition"
header="Riippumattomuus" 
content="
Tapahtumat $A$ ja $B$ ovat riippumattomat, jos $P(A\cap B)=P(A)P(B)$.
" %}	

{% include box.html  
type="exercise"
header="Nopan heitto kaksi kertaa" 
content="
Heitetään noppaa kaksi kertaa. Olkoon $A$ tapahtuma \"saadaan ensimmäisellä heitolla 6\" ja $B$ tapahtuma \"saadaan toisella heitolla 6\". Ovatko tapahtumat riippumattomia?
" 
dropdown="
Nyt $A$ on sellaisten järjestettyjen parien joukko, joissa ensimmäinen alkio on 6. Näitä on $1 \cdot 6 =6$ kappaletta. Joukko $B$ on sellaisten järjestettyjen parien joukko, joissa toinen alkio on 6. Näitä on $6 \cdot 1 =6$ kappaletta. Joukko $A\cap B$ koostuu yhdestä alkiosta $(6, 6)$. Perusjoukossa on $6 \cdot 6= 36$ alkiota. Tällöin
$$
P(A)P(B) = \frac{6}{36} \cdot \frac{6}{36} = \frac1{36} \quad\text{ja}\quad P(A\cap B) = \frac1{36}. 
$$ 
Tästä saamme että tapahtumat $A$ ja $B$ ovat riippumattomia.
" %} 

{% include box.html  
type="exercise"
header="Korttipakasta nosto" 
content="
Nostetaan korttipakasta kortteja. Olkoot $A$ tapahtuma \"ensimmäinen kortti on ässä\" ja $B$ tapahtuma \"toinen kortti on kuningatar\". Vaikuttaako tapahtumien $A$ ja $B$ riippumattomuuteen se, että palautetaanko nostettu kortti pakkaan vai ei?
" 
dropdown="
xxx
" %}

{% include box.html  
type="exercise"
header="Nopan heitto viisi kertaa" 
content="
Heitetään noppaa viisi kertaa peräkkäin. Kumpi tuloksista $1, 1, 1, 1, 1$ vai $4, 3, 1, 5, 1$ on todennäköisempi?
" 
dropdown="
xxx
" %}

Ehdollinen todennäköisyys ja tapahtumien riippumattomuus liittyvät toisiinsa läheisesti. Jos tapahtumat $A$ ja $B$ ovat riippumattomia, niin tapahtuman $A$ ehdollistaminen tapahtumalla $B$ ei vaikuta $A$:n todennäköisyyteen. 

{% include box.html  
type="theorem"
header="Mahdollinen havaintoarvo" 
content="
Olkoot $A$ ja $B$ tapahtumia ja $P(B)>0$. Tällöin $A$ ja $B$ ovat riippumattomia täsmälleen silloin, kun $P(A\mid B)=P(A)$.
" 

dropdown="
Jos oletetaan, että $A$ ja $B$ ovat riippumattomia, niin
$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}=\frac{P(A)P(B)}{P(A)}=P(A).
$$
Jos oletetaan, että $P(A\mid B)=P(A)$, niin ehdollisen todennäköisyyden määritelmän perusteella
$$
P(A\cap B)=P(B)P(A\mid B)=P(A)P(B)
$$ 
ja näin ollen $A$ ja $B$ ovat riippumattomia.
" %}       

Tapahtumien $A$ ja $B$ riippumattomuus merkitsee sitä, että tapahtuma $A$ ei vaikuta tapahtuman $B$ todennäköisyyteen ja tapahtuma $B$ ei vaikuta tapahtuman $A$ todennäköisyyteen. Tapahtumien $A$ ja $B$ riippumattomuuudelle on olennaista niiden todennäköisyydet, sen sijaan tapahtumien erillisyys riippuu vain joukoista $A$ ja $B$, ei lainkaan niiden todennäköisyyksistä. Jos tapahtumat $A$ ja $B$ ovat erilliset, niin $P(A\cap B)=P(\emptyset)=0$, jos taas tapahtumat $A$ ja $B$ ovat riippumattomat, niin $P(A\cap B)=P(A)P(B)$.  Näin ollen tapahtumien $A$ ja $B$ erillisyys ja riippumattomuus voivat toteutua yhtä aikaa vain, jos $P(A)=0$ tai $P(B)=0$. Erityisen tarkka on oltava kaavojen $P(A\cup B)=P(A)+P(B)$ ja $P(A\cap B)=P(A)P(B)$ käytössä. Ensimmäinen on voimassa, kun $A$ ja $B$ ovat erilliset, ja jälkimmäinen on voimassa, kun $A$ ja $B$ ovat riippumattomat.
              
{% include box.html  
type="exercise"
header="Riippumattomuus" 
content="
Pussissa on 40 palloa, jotka on numeroitu $1, \ldots, 40$. Nostetaan pussista kaksi palloa niin, että ensin nostettu pallo palautetaan takaisin pussiin ja vasta sitten nostetaan toinen pallo.  Mikä on tapahtuman \"tuloksena on 13 ja 40\" todennäköisyys?				
" 
dropdown="
Ei ole väliä missä järjestyksessä pallot nostetaan. Tutkitaan ensin tapausta, jossa pallo 13 nousee ensin. Koska nostettu pallo palautetaan pussiin, niin tapahtumat $A=$ \"ensimmäisen noston tulos on 13\" ja  $B=$ \"toisen noston tulos on 40\" ovat riippumattomia.  Saamme
$$
P(A \cap B) = P(A) P(B) = \frac1{40} \cdot \frac1{40} = \frac1{1600}.
$$
Lopputuloksen kannalta ei  ole merkitystä, kumpi luvuista saadaan ensin, joten huomioidaan molemmat mahdollisuudet \"13 ja 40\" sekä \"40 ja 13\". Jälkimmäinen tapaus on samanlainen ensin mainitun kanssa. Saamme kysytyksi todennäköisyydeksi $\frac1{1600} + \frac1{1600} = \frac1{800}$.
" %}

{% include box.html  
type="exercise"
header="Yhden nopan heitto" 
content="
Heitetään noppaa kerran. Merkitään $A =\{5, 6\}$ ja $B=\{2,4,6\}$. Ovatko tapahtumat erillisiä tai riippumattomia?
" 
dropdown="
Koska $A\cap B=\{6\}\neq\emptyset$, niin tapahtumat $A$ ja $B$ eivät ole erillisiä. Sen sijaan ne ovat riippumattomat, sillä
$$
P(A\cap B)=\frac{1}{6}=\frac{1}{3}\cdot\frac{1}{2}=P(A)P(B).
$$
" %}

{% include box.html  
header="Lisätietoa" 
content="
Jos tapahtumat $A$ ja $B$ eivät ole riippumattomia, niin niillä on jotakin *stokastista* vuorovaikutusta  toisiinsa. On kuitenkin varottava vetämästä liian suuria johtopäätöksiä tästä vuorovaikutuksesta, jolla ei yleensä ole *kausaalista* luonnetta (syy-seuraussuhdetta).             
" %}

{% include box.html  
type="exercise"
header="Klassinen todennäköisyys" 
content="
Korttipakasta nostetaan kolme korttia. Mikä on todennäköisyys, että
kaikki ovat eri maata?
" %}

{% include box.html  
type="exercise"
header="Klassinen todennäköisyys" 
content="
Heitetään kolikkoa viisi kertaa peräkkäin. Mikä on todennäköisyys, että saadaan
1. kolme kruunaa ja kaksi klaavaa,
1. ensin kolme kruunaa ja sitten kaksi klaavaa?
" %}

{% include box.html  
type="exercise"
header="Klassinen todennäköisyys" 
content="
Heitetään noppaa 10 kertaa peräkkäin. Mikä on todennäköisyys, että ei saada silmälukuja 3 ja 4 lainkaan?
" %}

{% include box.html  
type="exercise"
header="Toistokoe" 
content="
Pussissa on kolme punaista ja viisi mustaa palloa. Matti nostaa pussista yhden pallon kerrallaan ja sen värin kirjattuaan palauttaa pallon pussiin. Mikä on todennäköisyys, että kahdeksassa nostossa tulee kolme punaista ja viisi mustaa palloa? 
" %}

{% include box.html  
type="exercise"
header="Klassinen todennäköisyys" 
content="
Anna nopanheiton avulla esimerkki tapahtumista $A$ ja $B$, jotka toteuttavan Lauseen 2.1 (TN laskusääntöjä ja perusominaisuuksia) kohdat. Anna jokaiselle kohdalle oma esimerkki.
" %}

{% include box.html  
type="exercise"
header="Klassinen todennäköisyys" 
content="
Olkoon $A$, $B$ ja $C$ tapahtumia, joille $P(A)+P(B)+P(C)=1$. Lisäksi $P(A)=P(B \cap C)$, $P(A)=P(B)$ ja $P(C)=2 P(B)$.
1. Kuinka paljon on $P(A)$?
1. Ovatko $B$ ja $C$ erillisiä?
" %}

## Kombinatoriikka

Erilaiset tavat tehdä valintoja joukkojen alkioista liittyvät keskeisesti todennäköisyyslaskennan klassiseen malliin.  *Kombinatoriikka* on matematiikan osa-alue, joka tutkii eri vaihtoehtojen määrittämistä. Aloitetaan yksinkertaisella esimerkillä. 

Nukella on  kaksi hattua, kolme paitaa, yhdet housut ja kahdet kengät. Kuinka monella eri tavalla nuken voi pukea? Havaitaan ensin että että hatun valitseminen ei vaikuta paidan valitsemiseen, tai yleisemmin eri vaatekappaleiden valinnat ovat toisistaan riippumattomia. Lisäksi jokaisen vaatekappaleen kohdalla sen voi jättää pukematta. Näin ollen eri vaihtoehtoja on 
$(2+1)\cdot (3+1)\cdot (1+1) \cdot (2+1) = 72$. Tämä luku sisältää myös vaihtoehdon että nukelle ei pueta mitään päälle.	

Voimme yleisesti soveltaa yllä olevaa ajatusta seuraavasti. Ajatellaan että meillä on tilanne jossa suoritetaan valinta $k$:ssa eri askeleessa. Oletetaan että eri askeleiden valinnat ovat toisistaan riippumattomia. Merkitään että askeleessa $i$ meillä on mahdollista tehdä valinta $n_i$ eri vaihtoehdosta. Tällöin vaihtoehtoja on yhteensä
		$$
		n_1 \cdot n_2 \cdot \ldots \cdot n_{k-1} \cdot n_k
		$$ 
kappaletta. Tätä päättelyä kutsutaan *tuloperiaateeksi*.

Määritellään seuraavaksi kombinatoriikan peruskäsitteet.

{% include box.html  
type="definition"
header="Permutaatio" 
content="
Äärellisen joukon *permutaatio* on jono, jossa joukon jokainen alkio esiintyy täsmälleen kerran.
" %}

Huomaa, että jonossa alkioilla on järjestys, mutta joukossa alkioilla ei ole järjestystä.

{% include box.html  
type="exercise"
header="Permutaatiot" 
content="
Kuinka monta permutaatiota on joukolla $A=\{a, b, c\}$?
" 
dropdown="
Joukon $A=\{a, b, c\}$ permutaatioita ovat jonot $(a, b, c)$, $(a, c, b)$, $(b, a, c)$, $(b, c, a)$, $(c, a, b)$ ja $(c, b, a)$. Havaitaan, että kolmialkioisella joukolla $A$ on 6 erilaista permutaatiota.
" %}

{% include box.html  
type="exercise"
header="Permutaatiot" 
content="
Edellisessä tehtävässä havaittiin, että kolmialkioisella joukolla on 6 erilaista permutaatiota. Jos joukossa on $n$ alkiota, niin kuinka monta erilaista permutaatiota sillä on? Voit ensin tarkastella esimerkiksi nelialkioisen joukon permutaatioita ja yrittää keksiä yleisen säännön, jolla permutaatioiden lukumäärän voi laskea.
" 
dropdown="
xxxxx
" %}

{% include box.html  
type="definition"
header="$k$-kombinaatio" 
content="
Olkoon $A$ joukko, jossa on $n$ alkiota ja $1\leqslant k\leqslant n$. Joukon $A$ $k$*-kombinaatio* on joukon $A$ osajoukko, joka muodostuu joukon $A$ $k$:sta alkiosta.              
" %}

Esimerkiksi joukon $A=\{a, b, c\}$ 2-kombinaatiot ovat joukot $\{a, b\}$, $\{a, c\}$ ja $\{b, c\}$. Havaitaan, että kolmialkioisella joukolla on 3 erilaista 2-kombinaatiota.
               
Huomaa, että permutaatiot ovat jonoja ja kombinaatiot ovat joukkoja.

{% include box.html  
type="theorem"
content="
Olkoon $A$ joukko, jossa on $n$ alkiota.
1. Joukon $A$ permutaatioiden lukumäärä on $n!=1\cdot 2\cdot 3\cdots n$.
1. Joukon $A$ $k$-kombinaatioiden lukumäärä on $\displaystyle\binom{n}{k}=\frac{n!}{k!(n-k)!}$.
" 
dropdown="
1. Aloitetaan $n$ alkion asettaminen jonoon, johon ensimmäiseksi jäseneksi on $n$ vaihtoehtoa. Tämän jälkeen toiseksi jäseneksi jonossa on $n-1$ vaihtoehtoa, ja näin jatkamalla seuraavaksi jonon jäseneksi on aina yksi vaihtoehto vähemmän kuin edelliseksi jäseneksi oli. Jonon viimeiseksi jäseneksi on jäljellä enää yksi vaihtoehto. Näin ollen kertomalla vaihtoehtojen lukumäärät keskenään nähdään, että $n$-alkioisella joukolla on $n\cdot(n-1)\cdots 1=n!$ permutaatiota.                            
1. Vastaavasti kuin permutaatioiden lukumäärä voidaan päätellä, että $n$ alkiosta voidaan valita $k$ alkiota jonoon $n\cdot(n-1)\cdots(n-k+1)$ tavalla. Tässä samojen alkioiden eri järjestykset ovat eri jonoja, joten $k$-kombinaatioiden lukumäärä saadaan tästä jakamalla luvulla $k!$, joka on eri tapojen lukumäärä järjestää $k$ alkiota jonoon. Saadaan siis, että $n$-alkioisen joukon $k$-kombinaatioiden lukumäärä on
$$
\frac{n\cdot(n-1)\cdots(n-k+1)}{k!}=\frac{n\cdot(n-1)\cdots(n-k+1)\cdot(n-k)!}{k!(n-k)!}=\frac{n!}{k!(n-k)!}
=\binom{n}{k}.
$$
" %}

Lukua $n!$ kutsutaan luvun $n$ kertomaksi ja se luetaan "$n$:n kertoma". Lukua $\displaystyle\binom{n}{k}$ kutsutaan *binomikertoimeksi* ja se luetaan "$n$ yli $k$" tai "$n$ alle $k$".  Binomikerrointa voidaan myös merkitä $\text{nCr}(n, k)$. Useimmat laskimet ja laskinohjelmistot käyttävät tällaista merkintää. Esimerkiksi 
$$
\binom{9}{4}=\text{nCr}(9, 4) =126.
$$

{% include box.html  
type="exercise"
header="Lotto" 
content="
Lotossa on 40 numeroa, joista arvotaan 7 numeroa. Monta erillaista lottoriviä on olemassa?
" 
dropdown="
Erilaisia 7 numeron lottorivejä on
$$
\binom{40}{7}=\frac{40!}{7!33!}=\frac{93\,963\,542\,400}{5\,040}=18\,643\,560.
$$
" %}

{% include box.html  
type="exercise"
header="Lotto" 
content="
Raili miettii lottoriviään seuraavaan arvontaan. Kuudessa edellisessä arvonnassa lottorivissä on ollut luku 9. Kannattaako Railin valita luku 9 omaan riviinsä? 
" 
dropdown="
xxxxxx
" %}

{% include box.html  
type="exercise"
header="Yhdistys" 
content="
Yhdistyksen kokouksessa on 60 osallistujaa. Kuinka monella tavalla heistä voidaan valita puheenjohtaja, varapuheenjohtaja ja sihteeri? Kuinka monella tavalla valitsematta jääneistä voidaan valita 2 toiminnantarkastajaa?  
" 
dropdown="
xxxxx
" %}

Joukon, jossa on $n$ alkiota, $k$-permutaatioiden lukumäärää voidaan merkitä $\text{nPr}(n, k)$. Useimmat laskimet ja laskinohjelmistot käyttävät tällaista merkintää, esimerkiksi 
$$
\text{nPr}(9, 4) =  9\cdot 8 \cdot 7 \cdot 6=3024.
$$

{% include box.html  
type="exercise"
header="Kombinaatiot" 
content="
Korttipakassa on 10 korttia, jotka ovat joko punaisia tai mustia. Kun pakasta nostetaan 3 korttia, niin todennäköisyys että kaikki ovat punaisia on X(annetaan tähän sopivaluku). Kuinka monta punaista oli alunperin pakassa? 
" %}

{% include box.html  
type="exercise"
header="Kombinatoriikka" 
content="
Luettele kaikki 4-alkioiset
1. jonot,
1. joukot
jotka voit muodostaa joukon $\{1,2,3,4,5\}$ alkioista. 
" %}

{% include box.html  
type="exercise"
header="Kombinatoriikka" 
content="
Pohjoismaiden pääministerit asettuvat istumaan pyöreän pöydän ääreen. Kuinka monessa eri järjestyksessä he voivat istua? Järjestys on sama, jos se saadaan pöytää kiertämällä. Kuinka monessa istumajärjestyksessä Suomen pääministeri voi istua Ruotsin ja Norjan pääministerien vieressä?
" %}

{% include box.html  
type="exercise"
header="Kombinatoriikka" 
content="
Vartion retkellä on mukana 6 jäsentä. Kuinka monella tavalla voidaan valita yksi saunan lämmittäjä ja kaksi veden kantajaa?  
" %}

## Klassisen todennäköisyyden laajennus 

Klassisessa todennäköisyydessä kaikki alkeistapahtumat ovat yhtä todennäköisiä. Tutustumme esimerkkitehtävin tapahtumiin, joissa alkeistatapahtumien todennäköisyydet ovat eri suuria, mutta tilanteiden analysoinnissa voi silti käyttää klassisesta todennäköisyydestä tuttuja menetelmiä.
               
{% include box.html  
type="exercise"
header="Erikoinen noppa" 
content='
Jussilla on noppa, jonka silmäluvut ovat 1, 1, 1, 2, 3, 4. Jussi heittää noppaa kaksi kertaa. Millä todennäköisyydellä tuloksena on luvut 1 ja 2?
' 
dropdown='
Lasketaan ensin todennäköisyys tapahtumalle "ensimmäisen heiton tulos on 1 ja toisen tulos on 2": 
								$$\frac36 \cdot \frac16 = \frac3{36}$$
Vastaavasti tapahtuman "ensimmäisen heiton tulos on 2 ja toisen tulos on 1" todennäköisyys on 
								$$\frac16 \cdot \frac36 = \frac3{36}$$.
Kysytty todennäköisyys on täten $\frac3{36} + \frac3{36} = \frac16$.
' %}

{% include box.html  
type="exercise"
header="Erikoinen noppa" 
content='
Kuusisivuisen nopan kunkin sivun silmäluvuksi voidaan valita mikä tahansa luvuista $1,\ldots,6$. Miten silmäluvut pitää valita, jotta kahdella heitolla tapahtuman "tuloksena ovat 1 ja 2" todennäköisyys on $\frac49$?
' 
dropdown='
1, 1, 1, 1, 2, 2 tai toisin päin.
' %}

Joissain tilanteissa tapausten todennäköisyydet saadaan pinta-aloista. Tarkastellaan tavallista tikkataulua ja tilannetta, jossa tikka osuus satunnaisesti tauluun.  Tällöin kunkin numeron todennäköisyys on sitä vastaava pinta-ala jaettuna koko tikkataulun pinta-alalla.

{% include box.html  
type="exercise"
header="Tikkataulu" 
content='
Kuvassa on tavallinen tikkataulu, jonka halkaisija on 30 cm. Millä todennäköisyydellä 3 tikalla saadaan kaksi ykköstä ja yksi kahdeksikko?
![Tikkataulu, jonka halkaisija on 30 cm](/images/tikkataulu.png "Tikkataulu, jonka halkaisija on 30 cm.")
' 
dropdown="
zzzzz
" %}

{% include box.html  
type="exercise"
header="Onnenpyörä" 
content='
Nikolai ostaa onnenpyöräpelin, jossa kaikki sektorit ovat yhtä suuria, kuten alla olevassa kuvassa. Pyöräytettäessä onnenpyörä pysähtyy satunnaiseen kohtaan. Millä todennäköisyydellä onnenpyörä pysähtyy mustaan tai valkoiseen sektoriin?
						
![Ikean onnenpyöräpeli](/images/tikkataulu.png "Ikean onnenpyöräpeli")
_Ikean [onnenpyöräpeli](https://www.ikea.com/fi/fi/p/lustigt-onnenpyoeraepeli-30387038/)_ (luettu 23.10.2020).
' 
dropdown="
zzzzz
" %}

{% include box.html  
type="exercise"
header="Geometrinen todennäköisyys" 
content='
Lentokoneesta pudotetaan paketti, joka putoaa ympyrän sisälle (otetaan Google Mapsista ilmakuva, johon piirretään ympyrä). Jokainen ympyrän kohta on yhtä todennäköinen putoamiskohta. Millä todennäköisyydellä paketti putoaa vesistöön?
' %}

{% include box.html  
type="exercise"
header="Modifioitu noppa" 
content='
Tutkitaan 6-sivuista noppaa. Neljällä sivulla on kullakin yksi väri: punainen, sininen, keltainen ja vihreä.
Yhdellä sivulla nopan heittäjä saa valita punaisen ja sinisen välillä, ja yhdellä sivulla nopan heittäjä saa valita kaikista väreistä.
1. (a) Nopan heittäjä tarvitsee sinisen tai vihreän voittaakseen pelin. Laske todennäköisyys tapahtumalle sininen tai vihreä.
1. Laske kunkin värin todennäköisyys. Summaa todennäköisyydet yhteen. Mitä havaitset? Mistä tämä johtuu?
' 
dropdown='
Värit eivät ole alkeistapauksia, joten niiden summa ei ole $1$.
' %}

{% include box.html  
type="exercise"
header="Geometrinen todennäköisyys" 
content='
Janalle, jonka pituus on $1$, sijoitetaan umpimähkään ja toisistaan riippumatta kaksi pistettä. Laske todennäköisyys,  että pisteiden etäisyys on suurempi kuin $\frac{1}{2}$.
'
dropdown='
Vihje: Perusjoukko on neliö, jonka sivun pituus on 1. Tulkitse pisteiden sijoittaminen neliössä niin, että ensimmäinen piste sijoitetaan neliön alemmalle vaakasivulle ja toinen piste vasemmalle pystysivulle.
' %}

{% include box.html  
type="exercise"
header="Geometrinen todennäköisyys" 
content='
Keksi tikkataulusta tehtävä jonka jonka vastauksena on todennäköisyys $0{,}2$.
'
dropdown='
Esimerkiksi saadaan 10 tai 1.
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