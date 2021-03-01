---
layout: post
title: Tilastolliset tunnusluvut
date: 2019-01-01 00:00:00 +0800
category: tutorial
thumbnail: /style/image/thumbnail.png
icon: book
---

* content
{:toc}

<input type="hidden" id="chapterNumber" name="theoremStart" value="1"/>
<input type="hidden" id="theoremStart" value="1"/>

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

Tässä luvussa tutkitaan Suomessa asuvia lapsiperheitä, joissa on alle 18-vuotiaita lapsia. Lapsiperheitä koskevat tiedot on poimittu <a href="https://www.stat.fi/">Tilastokeskuksen sivulta</a>. Tämä lähestyminen seuraa <a href="http://yle.fi/plus/abitreenit/2020/kevat/2020-03-18_N_fi/index.html#6">kevään 2020 lyhyen matematiikan ylioppilaskokeen tehtävää 6</a>.

Tutkimista varten määritellään muutamia tilastotieteen keskeisiä käsitteitä.
### MÄÄRITELMÄ: HAVAINTOYKSIKKÖ JA HAVAINTOARVO
Tutkittavan joukon alkioita kutsutaan <em>havaintoyksiköiksi</em>. Havaintoyksikköön liittyvää arvoa tai suuretta kutsutaan <em>havaintoarvoksi</em>					
Tässä tutkittava joukko on Suomessa asuvat lapsiperheet, joissa on alle 18-vuotiaita lapsia. Jokainen perhe on havaintoyksikkö ja perheen alle 18-vuotiaiden lasten lukumäärä on havaintoarvo. 

### Havaintoyksikkö ja havaintoarvo: kotipihan linnut
Aleksanteri tutkii kotipihallaan pesivien lintujen linnunpönttöjen asukkaat. Niissä pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen.
* Mikä Aleksanterin tutkimuksessa on havaintoyksikkö?
* Mikä Aleksanterin tutkimuksessa on havaintoarvo?

#### VASTAUS
* Linnunpöntöt ovat havaintoyksiköitä, niitä on kuusi kappaletta.
* Jokaiseen havaintoyksikköön liittyy suure, joka on linnun laji. Linnun laji on siis havaintoarvo.

### Lisätieto: Tilastollinen muuttuja
<em>Tilastolliseksi muuttujaksi</em> kutsutaan funktiota, joka kuvaa jokaisen havaintoyksikön sitä vastaavalle havaintoarvolle. Kommentti: nyt tämä on irrallinen; joko lisää tietoa tai pois.

Tässä moduulissa tutustutaan vain tilanteisiin, joissa havaintoarvoja on äärellinen määrä tai joissa havaintoarvot voidaan numeroida luonnollisilla luvuilla. Tällaisia tilanteita kutsutaan <em>diskreeteiksi</em>. Jos tutkittava ominaisuus voi saada mitä tahansa reaalilukuarvoja jollakin välillä, kuten koulun oppilaiden pituudet, ei kyse ole diskreetistä tilanteesta. Näitä tilanteita tutkitaan moduulissa MAA12.

Jos joukossa on vähän havaintoyksiköitä, niin havaintoarvot voi esittää luettelemalle ne peräkkäin. Jos havaintoyksiköitä on paljon, niin havaintoarvojen luetteleminen on epäkäytännöllistä ja epähavainnollista. Tällöin havaintoyksiköt pitää <em>luokitella</em>. Luokittelussa lasketaan, kuinka moni havaintoyksikkö vastaa kutakin havaintoarvoa. Jos havaintoarvoja on hyvin paljon, täytyy ne ensin luokitella sopiviin luokkiin ennen havaintoyksikköjen laskemista.

Lapsiperheiden luokittelussa lasketaan, kuinka monessa perheessä, eli havaintoyksikössä, on yksi lapsi (havaintoarvo 1), kuinka monessa on kaksi lasta (havaintoarvo 2), jne. Tiedot on koottu alla olevaan taulukoon:
				<table style="margin-left: auto; margin-right: auto;">
											
						<tr>
							<th>Lasten lkm</th>
							<th>$f$</th>
							</tr>
						<tr>
							<td>1</td>
							<td>241709</td>
						</tr>
						<tr>
							<td>2</td>
							<td>220116</td>
						</tr>
						<tr>
							<td>3</td>
							<td>75326</td>
						</tr>
						<tr>
							<td>4</td>
							<td>18409</td>
						</tr>
						<tr>
							<td>5</td>
							<td>5493</td>
						</tr>
						<tr>
							<td>6</td>
							<td>2289</td>
						</tr>
						<tr>
							<td>7</td>
							<td>1235</td>
						</tr>
						<tr>
							<td>8</td>
							<td>751</td>
						</tr>
						<tr>
							<td>9</td>
							<td>476</td>
						</tr>
						<tr>
							<td>10</td>
							<td>262</td>
						</tr>
						<tr>
							<td>11</td>
							<td>117</td>
						</tr>
						<tr>
							<td>12</td>
							<td>41</td>
						</tr>
						<tr>
							<td>13</td>
							<td>12</td>
						</tr>
						<tr>
							<td>14</td>
							<td>3</td>
						</tr>
						<tr>
							<td>15</td>
							<td>0</td>
						</tr>
						<tr>
							<td>16</td>
							<td>3</td>
						</tr>
						<tr>
							<th>Yhteensä</th>
							<th>566242</th>
						</tr>
				</table>
				<p>
					Yllä olevassa taulukossa ensimmäinen sarake "Lasten lkm" vastaa aineiston eri havaintoarvoja. Toinen sarake $f$ taas kertoo perheiden lukumäärän.
					Luku 15 ei ole havaintoarvo, koska missään perheessä ei ole 15 lasta. Se vaikuttaa mahdolliselta havainnolta, koska suurempiakin perheitä on olemassa. Sanotaan, että luku 15 on <em>mahdollinen havaintoarvo</em>, ja se otetaan tämän takia mukaan.
				</p>
				<p>
					Lasten lukumääränä  17 myös on mahdollinen havaintoarvo; huomaa, että nolla ei ole mahdollinen havaintoarvo, koska tutkitaan perheitä,
					joissa on lapsia. Luokittelussa lapsiperheisiin liittyvät mahdolliset havaintoarvot rajataan ottamalla mukaan vain kaikki mahdollisuudet pienimmän havaintoarvon ja suurimman havaintoarvon väliltä.
				</p>
			</div>
			<div class="definition">
                    <h3>MÄÄRITELMÄ: MAHDOLLINEN HAVAINTOARVO</h3>
                    <p>
                       <em>Mahdollinen havaintoarvo</em> on arvo tai suure, johon jokin havaintoyksikkö voisi liittyä.
                    </p>
			</div>
			
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t100ab">
                                Mahdollinen havaintoarvo: kotipihan linnut (jatkoa)
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t100ab" class="collapse">
                        <p>
                            Aleksanteri jatkaa linnunpönttöjen tutkimista tutkimalla myös naapurien linnunpöntöt.
						</p>
						<ol class="a">
                            <li>Anna esimerkki lintulajista, joka on mielekäs mahdollinen havaintoarvo</li>
                            <li>Anna esimerkki lintulajista, joka ei ole mielekäs mahdollinen havaintoarvo.</li>
                        </ol>
                        <h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t100ab_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t100ab_v" class="collapse">
                           <ol class="a">
                                <li>Kaikki havaintoarvot ovat mahdollisia havaintoarvoja, joten Aleksanterin pihan lintulajit (havaintoarvot) kelpaavat vastaukseksi. Myös esimerkiksi talitiainen on mielekäs mahdollinen havaintoarvo.</li>
                                <li>Strutsi, koska se ei pesi pöntössä.</li>
                            </ol>
                        </div>
					</div>	
				</div>
			</div>
			<div class="teoria">			
					<p>
						Luku, joka kertoo, kuinka moni havaintoyksikkö liittyy havaintoarvoon, on <em>frekvenssi</em>. 
					</p>
					<p>
						Yllä olevasta taulukosta nähdään esimerkiksi, että havaintoarvon 10 frekvenssi on 262, eli kymmenlapsisia perheitä on Suomessa 262 kappaletta. Jos mahdollinen havaintoarvo ei ole havaintoarvo, niin siihen ei liity yhtään havaintoyksikköä, joten sen frekvenssi on nolla.
					</p>
            </div>			
				
			<div class="definition">
                    <h3>MÄÄRITELMÄ: FREKVENSSI JA SUHTEELLINEN FREKVENSSI</h3>
                    <p>
						Mahdollisen havaintoarvon <em>frekvenssi</em> on  sitä vastaavien havaintoyksiköiden lukumäärä.	
			    Frekvenssiä merkitään yleensä kirjaimella $f$. 
					</p>
					
                    <p>
						Mahdollisen havaintoarvon <em>suhteellinen frekvenssi</em> on sen havaintoyksiköiden osuus kaikista 
			    havaintoyksiköistä.	Suhteellista frekvenssiä merkitään yleensä symbolilla $f$ %.
					</p>
			</div>
		<div class="teoria">				
					<p>
						Esimerkiksi voidaan laskea, että kolmilapsisia perheitä on Suomessa $\frac{75326}{566242}=0{,}1330\ldots\approx 13{,}3$ %, joten havaintoarvon 3 suhteellinen frekvenssi on $13{,}3$ %.
					</p>
					
            </div>	
		
		<div class="tehtavat">
			<div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t9921">
                                Suhteellinen frekvenssi ja teknisen apuvälineen käyttö: Suomen lapsiperheet
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t9921" class="collapse">
					<p>
					Tehtävänä on täydentää taulukkoon suhteelliset frekvenssit. 
					</p>
			    <table style="margin-left: auto; margin-right: auto;">
											
						<tr>
							<th>Lasten lkm</th>
							<th>$f$</th>
							</tr>
						<tr>
							<td>1</td>
							<td>241709</td>
						</tr>
						<tr>
							<td>2</td>
							<td>220116</td>
						</tr>
						<tr>
							<td>3</td>
							<td>75326</td>
						</tr>
						<tr>
							<td>4</td>
							<td>18409</td>
						</tr>
						<tr>
							<td>5</td>
							<td>5493</td>
						</tr>
						<tr>
							<td>6</td>
							<td>2289</td>
						</tr>
						<tr>
							<td>7</td>
							<td>1235</td>
						</tr>
						<tr>
							<td>8</td>
							<td>751</td>
						</tr>
						<tr>
							<td>9</td>
							<td>476</td>
						</tr>
						<tr>
							<td>10</td>
							<td>262</td>
						</tr>
						<tr>
							<td>11</td>
							<td>117</td>
						</tr>
						<tr>
							<td>12</td>
							<td>41</td>
						</tr>
						<tr>
							<td>13</td>
							<td>12</td>
						</tr>
						<tr>
							<td>14</td>
							<td>3</td>
						</tr>
						<tr>
							<td>15</td>
							<td>0</td>
						</tr>
						<tr>
							<td>16</td>
							<td>3</td>
						</tr>
						<tr>
							<th>Yhteensä</th>
							<th>566242</th>
						</tr>
				</table>
					<ol class="a">
					<li>Laske yksilapsisten perheiden osuus kaikista perheistä, eli havaintoarvon 1 suhteellinen frekvenssi.
					</li>
					<li>Kopioi taulukko  maalaamalla solut ja liitä tiedot taulukkolaskentaohjelmaan, esimerkiksi LibreOffice Calc- ohjelmaan. 
					</li>
					<li>
					Syötä suhteellisen frekvenssin sarakkeeseen havaintoarvoa 1 vastaavalle riville a-kohdan lausekkeesi kaavana. Jos luku 241709 on solussa B1, niin kirjoita viereiseen soluun =B1/566242*100 ja paina enter. 		
					</li>
					<li>
					Kopioi kaava jokaiseen havaintoarvoon tarttumalla edellisen kohdan solun oikeasta alakulmasta kiinni ja maalaamalla sarake Yhteensä-riville asti. 	
					</li>	
					<li>
					Tarkista vastauksesta, saitko tehtyä samanlaisen taulukon.
					</li>
					</ol>
					
						<h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t9921_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t9921_v" class="collapse">

						<ol class="a">
					<li>Koska tilastossa on lapsiperheitä yhteensä 566242 kappaletta, niin yksilapsisten perheiden osuus kaikista aineiston perheistä on 
					$$\frac{241709}{566242}\approx 42,7\ \%.$$
					</li>
					<li>Taulukkolaskentaohjelman avulla saadaan seuraava taulukko:
					<table style="margin-left: auto; margin-right: auto;">
											
						<tr>
							<th>Lasten lkm</th>
							<th>$f$</th>
							<th>$f$ %</th>
						</tr>
						<tr>
							<td>1</td>
							<td>241709</td>
							<td>42,7 %</td>
						</tr>
						<tr>
							<td>2</td>
							<td>220116</td>
							<td>38,9 %</td>
						</tr>
						<tr>
							<td>3</td>
							<td>75326</td>
							<td>13,3 %</td>
						</tr>
						<tr>
							<td>4</td>
							<td>18409</td>
							<td>3,3 %</td>
						</tr>
						<tr>
							<td>5</td>
							<td>5493</td>
							<td>1,0 %</td>
						</tr>
						<tr>
							<td>6</td>
							<td>2289</td>
							<td>0,4 %</td>
						</tr>
						<tr>
							<td>7</td>
							<td>1235</td>
							<td>0,2 %</td>
						</tr>
						<tr>
							<td>8</td>
							<td>751</td>
							<td>0,1 %</td>
						</tr>
						<tr>
							<td>9</td>
							<td>476</td>
							<td>0,08 %</td>
						</tr>
						<tr>
							<td>10</td>
							<td>262</td>
							<td>0,05 %</td>
						</tr>
						<tr>
							<td>11</td>
							<td>117</td>
							<td>0,03 %</td>
						</tr>
						<tr>
							<td>12</td>
							<td>41</td>
							<td>0,007 %</td>
						</tr>
						<tr>
							<td>13</td>
							<td>12</td>
							<td>0,002 %</td>
						</tr>
						<tr>
							<td>14</td>
							<td>3</td>
							<td>0,0005 %</td>
						</tr>
						<tr>
							<td>15</td>
							<td>0</td>
							<td>0 %</td>
						</tr>
						<tr>
							<td>16</td>
							<td>3</td>
							<td>0,0005 %</td>
						</tr>
						<tr>
							<th>Yhteensä</th>
							<th>566242</th>
							<th>100 %</th>
						</tr>
				</table>
					</li>
					</ol>
					</div>
					</div>	
				</div>
			<div class="teoria">				
					<p>
						Mahdollisten havaintoarvojen ja suhteellisten frekvenssien muodostamaa kokonaisuutta kutsutaan <em>jakaumaksi</em>. Jakaumiin tutustutaan tarkemmin luvussa <a>jakaumat</a>. 
					</p>
					
            </div>	
	
				
				
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t99">
                                Frekvenssi ja suhteellinen frekvenssi: kotipihan linnut (jatkoa)
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t99" class="collapse">
                        <p>
                     Aleksin kotipihalla pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen. Kerää lintulajien frekvenssit ja suhteelliset frekvenssit taulukkoon.
						</p>
						<h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t99_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t99_v" class="collapse">

						<table style="margin-left: auto; margin-right: auto;">
						
						<tr>
							<th>Havaintoarvo</th>
							<th>$f$</th>
							<th>$f$ %</th>
						</tr>
						<tr>
							<td>punarinta</td>
							<td>1</td>
							<td>$\frac{1}{6}\approx 16,7\ \%$</td>
						</tr>
						<tr>
							<td>kirjosieppo</td>
							<td>2</td>
							<td>$\frac{2}{6}\approx 33,3\ \%$</td>
						</tr>
						<tr>
							<td>sinitiainen</td>
							<td>3</td>
							<td>$\frac{3}{6}=50\ \%$</td>
						</tr>
						<tr>
							<th>Yhteensä</th>
							<th>6</th>
							<th>100 %</th>
						</tr>
						</table>
						</div>
					</div>	
			</div>	
			<div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t98">
                                Luokittelu ja suhteellinen frekvenssi
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t98" class="collapse">
					<p>
                        Suomessa on yhteensä 311 kuntaa. Asukasluvultaan suurin on Helsinki (635181 asukasta). Manner-Suomen pienin kunta on Luhanka (756 asukasta) ja Ahvenanmaan pienin kunta on Sottunga (96 asukasta). Melkein kaikissa kunnissa on eri määrä asukkaita, joten havaintoarvot täytyy luokitella ennen frekvenssien laskemista.
					</p>
					
						<a href="https://www.kuntaliitto.fi/vaestotietoja-kunnittain">Kuntaliiton verkkosivujen</a> (luettu 21.10.2020) kuvassa kunnat, eli havaintoyksiköt, on luokiteltu asukasmäärän, eli havaintoarvon, mukaan viiteen eri luokkaan.
					</p>	
					<img src="../kuvat/kunta.png" style="max-width: 100%; width: auto; height: auto;"/>
					<ol class="a">
				
                            <li>Miten asukasmäärät on luokiteltu?</li>
                            <li>Mitä tarkoittavat kuvan luvut 21, 34, 43, 80 ja 133?</li>
						<li> Laske luokkien suhteelliset frekvenssit.</li>
                        </ol>
                        <h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t98_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t98_v" class="collapse">
                           <ol class="a">
				 
                                <li>alle 5000 asukasta, 5000–10000 asukasta, 10001–20000 asukasta, 20001–50000 asukasta ja yli 50000 asukasta.</li>
                                <li>Luokkien frekvenssit.</li>
                            </ol>
                        </div>
					</div>	
						
				</div>
			</div>	

			<div class="teoria">			
					<p>
						Summafrekvenssi ja suhteellinen summafrekvenssi???
					</p>
            </div>
			
	
	<section class="panel">
        <header class="otsikko">
            <h1>      
                <a data-toggle="collapse" class="collapsed" data-target="#keskiluvut">
                    Keskiluvut
                </a>
            </h1>
        </header>
        <div id="keskiluvut" class="collapse">
            
            <div class="teoria">
				<p>
					Aineistoja tutkittaessa mielenkiinnon kohteena on usein löytää aineiston "tyypillisin" tai "keskimmäisin" tapaus. Tätä kuvaamaan käytetään erilaisia keskilukuja. Niiden määrittämisen mielekkyys riippuu havaintoarvojen luonteesta, eli siitä mitä on mielekästä kutsua "tyypilliseksi" kyseisessä aineistossa.
				</p>
					Yksi keskiluku on aineiston yleisin havaintoarvo. Lapsiperheitä tutkiessa huomattiin, että  yksilapsisia perheitä on havaintoyksiköistä kaikkein eniten. Tilastotieteessä yleisintä havaintoarvoa kutsutaan <em>moodiksi</em>.
				</p>
			</div>

			<div class="definition">
                    <h3>MÄÄRITELMÄ: MOODI</h3>
                    <p>
                       <em>Moodi</em> on havaintoarvo, jolla on suurin frekvenssi. Jos useammalla havaintoarvolla on suurin frekvenssi, niin ne kaikki ovat moodeja.
					</p>
            </div>	
			<div>
				<p>
					Havaintoarvot noudattavat <em>luokitteluasteikkoa</em>, jos  arvot voidaan ainoastaan luokitella, mutta niitä ei voi asettaa suuruusjärjestykseen. Tällaisia  ovat esimerkiksi silmien väri, sukupuoli, asuinkunta jne.
				</p>
			</div>
			
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t01">
                                Luokitteluasteikko ja moodi: kotipihan linnut (jatkoa)
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t01" class="collapse">
                        <p>
                        Aleksanterin kotipihalla pesii sinitiainen, kirjosieppo, sinitiainen, kirjosieppo, punarinta ja sinitiainen.
						</p>
						<ol class="a">
							<li>Noudattavatko arvot luokitteluasteikkoa?</li>
							<li>Mikä on niiden moodi?</li>
						</ol>
						<h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t01_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t01_v" class="collapse">
						<ol class="a">
							<li>Lintulajeija ei voi laittaa suuruusjärjestykseen, mutta ne voidaan luokitella. Eli kyseessä on luokitteluasteikko.</li>
							<li>Moodi on "sinitiainen".</li>
						</ol>
						</div>
					</div>	
				</div>	
            </div>				
			
			<div class="teoria">
				<p>
					Havaintoarvot noudattavat <em>järjestysasteikkoa</em>, jos  arvot voidaan asettaa suuruusjärjestykseen. Tälläisiä ovat esimerkiksi sotilasarvo tai ylioppilastutkinnon arvosanat (I, A, ..., E, L). Peruslaskutoimitukset eivät ole sallittuja (numeerisella) järjestysasteikolla, koska luokkien väliset etäisyydet voivat olla erisuuria.
				</p>
            </div>	
			
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t02">
                                Järjestysasteikko
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t02" class="collapse">
                        <p>
                       Ylioppilastutkinnossa arvosanat rinnastetaan lukuihin seuraavasti: I vastaa lukua 0, A vastaa lukua 2, B vastaa lukua 3, ...,  E vastaa lukua 6 ja L vastaa lukua 7.  Ajatellaan seuraavaa tilannetta:
					</p>
					<p>
						"Maija ja Matti kävivät uusimassa matematiikan ylioppilaskokeen. Maija sai korotettua arvosanasta I arvosanaan B ja Matti arvosanasta M arvosanaan L."
					</p>
					<p>
						Voidaanko tästä päätellä, että Maijan parannus on suurempi kuin Matin? Perustele.
					</p>	
						<h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t02_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t02_v" class="collapse">
							<p>
								Ei voida, koska emme tunne eri havaintoarvojen välisiä etäisyyksiä. Maijan arvosanan parannus 3 ei kuvaa arvosanojen I ja B välistä etäisyyttää, kuten ei myöskään Matin arvosanan parannus 2 arvosanojen M ja L välistä etäisyyttä. Koska luvut eivät kuvaa etäisyyksiä, niin niitä ei voi verrata. 
							</p>
						</div>
					</div>	
				</div>	
            </div>				
						
			<div class="teoria">
				<p>
					Järjestysasteikolla havaintoarvoille voidaan määrittää moodin lisäksi mediaani.
				</p>
            </div>	
			
			<div class="definition">
                    <h3>MÄÄRITELMÄ: MEDIAANI</h3>
                    <p>
						<em>Mediaani</em> on suuruusjärjestykseen järjestettyjen havaintoarvojen keskimmäinen havaintoarvo, jos havaintoarvoja on pariton määrä tai jos parillisessa tapauksessa kaksi keskimmäistä arvoa ovat samat. Jos parillisessa tapauksessa kaksi keskimmäistä havaintoarvoa ovat erisuuret, niin silloin mediaan on nämä molemmat arvot.
					</p>
			</div>
			<div class="definition">
                    <h3>LISÄTIETO:</h3>
					<p>
						Välimatka-asteikolla parillisessa tapauksessa  mediaani voi  vaihtoehtoisesti olla keskimmäisten lukujen keskiarvon.
					</p>
            </div>
			
			<div class="teoria">
                    <p>
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
                    </p>
					<p>
						Tässä on yhteensä 566242 lukua, joka on parillinen määrä. Näin ollen keskimmäistä lukua ei ole. Ensimmäisen puolikkaan viimeinen luku on 2, kuten myös toisen puolikkaan ensimmäinen luku. Mediaani on siis 2.
					</p>
			</div>
			
            <div class="tehtavat">
                <div class="tehtava first-exercise" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t101">
                                Suhteellinen frekvenssi ja mediaani
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t101" class="collapse">
                        <p>
                            Laske alla olevaan taulukkoon suhteelliset frekvenssit. Pystyykö pelkistä suhteellisista frekvensseistä määrittämään mediaanin?
						</p>
						<table style="margin-left: auto; margin-right: auto;">
						
						<tr>
							<th>Arvosana</th>
							<td>4</td>
							<td>5</td>
							<td>6</td>
							<td>7</td>
							<td>8</td>
							<td>9</td>
							<td>10</td>						
						</tr>
						<tr>
							<th>Lkm</th>
							<td>1</td>
							<td>0</td>
							<td>3</td>
							<td>1</td>
							<td>2</td>
							<td>1</td>
							<td>2</td>						
						</tr>
						<tr>
							<th>$f$ %</th>
							<td> </td>
							<td> </td>
							<td> </td>
							<td> </td>
							<td> </td>
							<td> </td>
							<td> </td>	
						</tr>
					</table>
				</div>
			</div>
			
			<div class="teoria">
				<p>
					Havaintoarvot noudattavat <em>välimatka-asteikkoa</em>, jos arvojen erotus on mielekkäästi tulkittavissa. Tällaisia  ovat esimerkiksi kouluarvosana, vuosiluku, jne. 
				</p>
				<p>
					Esimerkiksi mineraalien luokittelussa ja tunnistamisessa käytetään kovuutta kuvaava Mohsin asteikkoa. Se on esimerkki järjestysasteikosta, joka ei ole välimatka-asteikko. Tämä käy ilmi seuraavasta lainauksesta: <br />
					"Mineraalit on jaettu kymmeneen kovuusluokkaan ns. Mohsin kovuusasteikon mukaan. Asteikossa ylemmän luokan mineraalilla kyetään naarmuttamaan alemman luokan mineraalia. [...] Asteikko ei ole läheskään tasavälinen, minkä paljastaa mineraalien todellisia kovuuksia kuvaava ns. Rosiwallin asteikko."<br />
					<em>Kalle Taipale: Kivet ja mineraalit Suomen luonnossa, Otava, 2010, s. 78.</em>
					</p>
            </div>	
			
			<div class="definition">
                    <h3>LISÄTIETO: SUHDEASTEIKKO</h3>
					<p>
						Havaintoarvot noudattavat <em>suhdeasteikkoa</em>, jos arvojen erotus on mielekkäästi tulkittavissa ja muuttujan arvoilla on jokin absoluuttinen nollakohta. Suhdeasteikko on aina välimatka-asteikko. Esimerkiksi pituus ja rahan määrä ovat suhdeasteikkoja. 
					</p>
					
            </div>
			
			<div class="teoria">
				<p>
					Välimatka-asteikolla voi laskea moodin ja mediaanin lisäksi keskiarvon. 
				</p>
            </div>
			
			<div class="definition">
                    <h3>MÄÄRITELMÄ: KESKIARVO</h3>
					<p>
						(Aritmeettinen) <em>keskiarvo</em> on havaintoarvojen summa jaettuna havaintoyksiköiden lukumäärällä.
					</p>
            </div>
		    <div class="teoria">
		<h3><a data-toggle="collapse" class="collapsed" data-target="#lisa_2">Lisätieto: Keskiarvoista</a></h3>	
		    <div id="lisa_2" class="collapse">
                  
					<p>
						Edellä määritelty keskiarvo on "aritmeettinen keskiarvo", mutta sana "aritmeettinen" jätetään pois, koska tässä moduulissa ei käsitellä muita keskiarvoja. Muita yleisesti käytettyjä keskiarvoja ovat "geometrinen keskiarvo" ja "harmoninen keskiarvo".
					</p>
            </div>
			
			<div class="teoria">
				<p>
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
				</p>
            </div>
			
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t102">
                                Teknisen apuvälineen käyttö tunnuslukujen selvittämisessä
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t102" class="collapse">
                        <p>
                            Syötä aiemman lapsiperheiden kokoa kuvaavan taulukon luvut tietokoneohjelmaan, ja laske ohjelman avulla moodi, keskiarvo ja mediaani. Tarkista, että saat samat vastaukset kuin tässä materiaalissa.
						</p>
						
				</div>
			</div>
			<div class="teoria">
				<p>
					Huomaa, että lapsiperhe-esimerkissä moodi, keskiarvo ja mediaani ovat kaikki eri lukuja. Ne voivat olla kaikki samoja, kaksi on samoja ja yksi on eri tai kaikki eri lukuja.
				</p>
            </div>
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t103">
                                Moodi, mediaani ja keskiarvo
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t103" class="collapse">
                        <p>
                            Anna esimerkki kokonaislukujen 4, ..., 10 havaintoarvoista, jossa
						</p>
						<ol class="a">
							<li>moodi, mediaani ja keskiarvo ovat samoja</li>
							<li>moodi ja mediaani ovat samoja mutta keskiarvo eroaa näistä,</li>
							<li>moodi, mediaani ja keskiarvo ovat kaikki eri suuria.</li>
						</ol>	
					</div>		
				</div>
				<div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t104">
                                Moodi, mediaani ja keskiarvo
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t104" class="collapse">
                        <p>
                            Ovatko seuraavat väitteet totta?
						</p>
						<ol class="a">
							<li>Mediaani on aina suurempi kuin moodi.</li>
							<li>Moodi on aina pienempi kuin keskiarvo.</li>
							<li>Keskiarvo ja mediaani eivät voi olla yhtä suuria.</li>
						</ol>
					</div>	
				</div>
			</div>
			
			<div class="teoria">
				<p>
					Huomaa, että järjestysasteikossa havaintoarvot voidaan samaistaa mihin tahansa kasvavaan kokoelmaan lukuja. Samaistuksen jälkeen keskiarvon tekninen laskeminen on mahdollista, mutta saatu tulos ei välttämättä kerro mitään alkuperäisestä tilanteesta, kuten seuraavassa esimerkissä. 
				</p>
				
				<p>
					Olisiko seuraavat tehtävät TSII? 
				</p>
            </div>
			
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t1052">
                                Asteikot
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t1052" class="collapse">
                        <p>
                            Aleksanteri on lähdössä Kemijärveltä maastopyörävaellukselle. Hän luokittelee kiinnostavat kohteet kolmeen luokkaan: luokassa 1 etäisyys Kemijärveltä on alle 50 km, luokassa 2 etäisyys Kemijärveltä on  50--150 km, luokassa 3 etäisyys Kemijärveltä on  yli 150 km. 
						</p>
						<p>
							Nyt havintoyksikköinä ovat paikat ja havaintoarvoina numerot 1, 2 ja 3. 
							Havaintoarvot muodostavat järjestysasteikon, mutta eivät välimatka-asteikkoa. Miksi?
						</p>	
						<h2>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t022_v">
                                VASTAUS
                            </a>
                        </h2>
                        <div id="MAA8t022_v" class="collapse">
							<p>	
								Esimerkiksi Savukosken kuntakeskus kuuluu luokkaan 2 ja Kemihaara luokkaan 3. Nyt Kemihaaran ja Savukosken kuntakeskuksen luokkien erotuksella  $3-2 =1$ ei ole järkevää tulkintaa.  Siitä ei esimerkiksi voi päätellä mitään Kemihaaran ja Savukosken kuntakeskuksen välisestä etäisyydestä. Myöskään luokkien keskiarvolla $\frac{2+3}{2}= \frac52$ ei ole järkevää tulkintaa. 
							</p>
						</div>
					</div>		
				</div>
				
				<div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t105">
                                Moodi, mediaani ja keskiarvo
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t105" class="collapse">
                        <p>
                            Lomakkeissa kysytään usein koulutusta. Mitkä keskiluvut voidaan määrittää, jos vastausvaihtoehdot ovat 
						</p>
						<ol class="a">
							<li>peruskoulu, ammattikoulu, lukio, alempi korkeakoulututkinto, ylempi korkeakoulututkinto, jatkotutkinto,</li>
							<li>peruskoulu, 2. asteen koulutus,  korkeakoulututkinto, jatkotutkinto?</li>
						</ol>	
					</div>		
				</div>
				<div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t106">
                                Moodi, mediaani ja keskiarvo
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t106" class="collapse">
                        <p>
                            Keksi esimerkkejä havaintoarvioista, joille voit soveltaa 
						</p>
						<ol class="a">
							<li>moodia, mutta et mediaania,</li>
							<li>moodia ja mediaania, mutta et keskiarvoa,</li>
							<li>moodia, mediaania ja keskiarvoa?</li>
						</ol>
					</div>	
				</div>
			</div>
			
		</div>
        <div class="close-section">
                <a data-toggle="collapse" class="collapsed" data-target="#keskiluvut">
                    Sulje kappale
                </a>
            </div>
        </div>
    </section>
	
	<section class="panel">
        <header class="otsikko">
            <h1>      
                <a data-toggle="collapse" class="collapsed" data-target="#keskihajonta">
                    Keskihajonta
                </a>
            </h1>
        </header>
        <div id="keskihajonta" class="collapse">
            
            <div class="teoria">
                <p>
                    Eri havaintoarvojen joukoilla voi olla sama keskiarvo, esimerkiksi silloin, kun joukot ovat 5, 7, 9 ja 7, 7, 7. Keskiarvo ei siis kerro, miten  havaintoarvot ovat jakautuneet. Tutustumme tässä luvussa <em>keskihajontaan</em>., joka  kuvaa havaintoarvojen jakautumista keskiarvon ympärille. Tässä luvussa ajattelemme, että meillä on käytössä välimatka-asteikko, jolloin voimme laskea havaintoarvojen erotuksia.
                </p>
            </div>
			
			<div class="definition">
                    <h3>MÄÄRITELMÄ: VAIHTELUVÄLI</h3>
                    <p>
                        Pienin ja suurin havaintoarvo määräävät <em>vaihteluvälin</em>. Vaihteluvälin pituus on suurimman ja pienimmän havaintoarvon erotus.  
                    </p>
            </div>
			
			<div class="teoria">
                <p>
                    Alla olevassa taulukossa on Tuulian ja Lukan koearvosanoja. Molemmilla on sama keskiarvo 8, sama vaihteluväli  $[6, 10]$ ja sama vaihteluvälin pituus $10-6=4$, mutta siitä huolimatta näyttää siltä, että Tuulian arvosanoissa on enemmän vaihtelua. 
                </p>
				<table style="margin-left: auto; margin-right: auto;">
						
						<tr>
							<th>Arvosana</th>
							<td>4</td>
							<td>5</td>
							<td>6</td>
							<td>7</td>
							<td>8</td>
							<td>9</td>
							<td>10</td>						
						</tr>
						<tr>
							<th>Tuulia (lkm %)</th>
							<td>0</td>
							<td>0</td>
							<td>3</td>
							<td>0</td>
							<td>1</td>
							<td>0</td>
							<td>3</td>						
						</tr>
						<tr>
							<th>Luka (lkm %)</th>
							<td>0</td>
							<td>0</td>
							<td>1</td>
							<td>1</td>
							<td>3</td>
							<td>1</td>
							<td>1</td>	
						</tr>
					</table>
            </div>
			
			<div class="definition">
                    <h3>MÄÄRITELMÄ: KESKIHAJONTA</h3>
                    <p>
						<em>Keskihajonta</em> on
						$$
						\sqrt{\frac1n \sum_{j=1}^n (x_i - \bar x)^2} ~,
						$$
						missä $x_1, \ldots, x_n$ ovat havaintoarvot ja $\bar x$ on niiden keskiarvo. Keskihajontaa merkitään usein kirjaimella $\sigma$. 
                    </p>
            </div>
			
			<div class="teoria">
                <p>
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
                    </p>
            </div>
			
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t107">
                                Tunnusluvut teknisen apuvälineen avulla
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t107" class="collapse">
                        <p>
                            Tilastokeskuksen sivuilta osoitteesta 
				<a href="http://www.tilastokeskus.fi/til/lop/index.html">http://www.tilastokeskus.fi/til/lop/index.html</a>
				löyttyy taulukko lukion opiskelijamääristä maakunnittain. 
				Lataa aineisto ja laske siitä tietokoneohjelmalla moodi, mediaani, keskiarvo ja keskihajonta.
						</p>
					</div>		
				</div>
				<div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t108">
                                Keskihajonta
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t108" class="collapse">
                        <p>
                            Jos kahden joukon havaintoarvoilla on sama keskiarvo ja sama keskihajonta, niin ovatko joukot välttämättä samoja? 
						</p>
					</div>	
				</div>
			</div>

            <div class="close-section">
                <a data-toggle="collapse" class="collapsed" data-target="#keskihajonta">
                    Sulje kappale
                </a>
            </div>
        </div>
    </section>
	
		<section class="panel">
        <header class="otsikko">
            <h1>      
                <a data-toggle="collapse" class="collapsed" data-target="#diagrammit">
                    Diagrammit
                </a>
            </h1>
        </header>
        <div id="diagrammit" class="collapse">
            
            <div class="teoria">
                <p>
                    Diagrammeilla voidaan havainnollistaa ja konkretisoida havaintoaineistoja.
					Pylväsdiagrammi sopii esimerkiksi absoluuttisten määrien esittämiseen, kun taas ympyrädiagrammi havainnollistaa hyvin suhteita. Diagrammin tyyppiä valitessa tulee kiinnittää erityistä huomiota siihen, että diagrammi havainnollistaa haluttua asiaa. 
                </p>
				<p>
					Alla olevissa diagrammeissa on esitetty lapsiperheiden kokonaismäärä ja suhteellinen osuus:
				</p>
				<img src="../kuvat/pylvasdiagrammi-lapsiperheet.png" style="max-width: 100%; width: auto; height: auto;"/>
				<img src="../kuvat/ympyradiagrammi-lapsiperheet.png" style="max-width: 100%; width: auto; height: auto;"/>
            </div>
						
			<div class="tehtavat">
                <div class="tehtava" id="38c3acd0-d55e-4923-bab0-2360a70eab5c">
                    <header>
                        <h1>                            <div class="checkbox-group"></div>
                            <a data-toggle="collapse" class="collapsed" data-target="#MAA8t109">
                                Diagrammit
                            </a>
                        </h1>
                    </header>
                    <div id="MAA8t109" class="collapse">
                        <p>
                            Tutustu ohjelmistosi eri diagrammeihin. Analysoi eri diagrammityyppien hyviä ja huonoja puolia.
						</p>
							<ol class="a">
								<li>Mitkä niistä sopivat aiemman Esimerkin 1 pihalinnuista havainnollistamiseen?</li>
								<li>Mitkä niistä sopivat lapsiperheiden frekvenssien ja suhteellisten frekvenssien havainnollistamiseen?</li>
							</ol>
					</div>		
				</div>
			</div>

            <div class="close-section">
                <a data-toggle="collapse" class="collapsed" data-target="#diagrammit">
                    Sulje kappale
                </a>
            </div>
        </div>
    </section>
	
	<section class="panel">
        <header class="otsikko">
            <h1>                        
                <a data-toggle="collapse" class="collapsed" data-target="#MAA8luku1-tehtavasarja2">
                    TEHTÄVÄSARJA II
                </a>
            </h1>
        </header>

        <div id="MAA8luku1-tehtavasarja2" class="collapse">
            <!-- Tästä alkaa piilotus -->

            <div class="tehtava" id="a7066042-d4b8-4eca-847b-a65650ec2b25">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t111">
                           Havaintoyksikkö ja -arvo
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t111">
                    <p>
                           <ol class="a">
                            <li>  
                                Anna esimerkki tilanteesta, jossa jokainen ryhmän oppilas on havaintoyksikkö.
                            </li>
                            <li>
				    Anna esimerkki tilanteesta, jossa havaintoarvoja ovat luonnolliset luvut välillä $10--60$.  
                            </li>
                        </ol>
                    </p>
                    
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t111_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t111_v" class="collapse">
                        <ol class="a">
                            <li>  
                              Jokaisen ryhmän jäseneen liittyvä havaintoarvo voi olla vaikka silmien väri, syntymäkuukausi, tai vaikka korvien lukumäärä.
                            </li>
                            <li> 
                                Havaintoyksiköitä voisivat olla ryhmän oppilaat ja havaintoarvoja kengän numero.
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="6e5f9461-2964-4a3d-b0f0-00c7e7ab32d2">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t112">
                            Juurifunktiot ja -yhtälöt
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t112">
                    <p>
                        Selvitä funktion $g$ määrittelyjoukko ja nollakohdat, jos  
                    </p>
                    <ol class="a">
                        <li> $g(x) = \sqrt{4x+5} - x$ </li>
                        <li> $g(x) = 2x - 1 + \sqrt{x^2 + 8}$ </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t112_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t112_v" class="collapse">
                        <ol class="a">
                            <li>  
                                Funktio on määritelty, jos ja vain jos $x \geq -\frac{5}{4}$. 
                                <br>
                                Funktiolla on nollakohta $x = 5$.
                            </li>
                            <li> 
                                Funktio on määritelty kaikilla muuttujan arvoilla.
                                <br>
                                Funktiolla on nollakohta $x = -1$.
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="14af0384-bc1a-438e-8692-c633cd54db46">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t120">
                            Juuriyhtälöt
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t120">
                    <p>
                        Eräs opiskelija sai tehtäväksi ratkaista yhtälön
                        $$
                        2x + \sqrt{5-x} = 0.
                        $$
                        Hän muisti, että neliöjuuresta pääsee eroon toiseen potenssiin korottamalla ja kirjoitti seuraavan ratkaisun:
                        \begin{align*}
                        2x + \sqrt{5-x} &= 0 \\
                        (2x)^2 + 5-x &= 0 \\
                        4x^2 + 5 - x &= 0 
                        \end{align*}
                        Koska diskriminantti 
                        $$D = (-1)^2-4\cdot 4 \cdot 5 = -79$$ 
                        on negatiivinen, yhtälöllä ei ole ratkaisuja.
                    </p>
                    <ol class="a">
                        <li> Miten opiskelija voisi tarkistaa, onko hän päätynyt oikeaan johtopäätökseen? </li>
                        <li> Onko opiskelijan ratkaisu oikein? Tarvittaessa korjaa ratkaisu oikeaksi. </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t120_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t120_v" class="collapse">
                        <ol class="a">
                            <li>  
                                Johtopäätöksen voi varmistaa esimerkiksi piirtämällä funktion 
                                $$
                                f(x) = 2x + \sqrt{5-x}
                                $$
                                kuvaajan ja katsomalla, leikkaako se $x$-akselin. Mahdolliset leikkauskohdat ovat yhtälön $f(x) = 0$ ratkaisuja. 
                            </li>
                            <li> 
                                Ratkaisu ei ole oikein. Ennen toiseen potenssiin korotusta yhtälöä kannattaa muokata niin, että neliöjuurilauseke on yksinään yhtälön toisella puolella:
                                \begin{align*}
                                2x + \sqrt{5-x} &= 0 \\
                                2x  &= -\sqrt{5-x}\\
                                (2x)^2 &= (-\sqrt{5-x})^2 \\
                                4x^2 &= 5 - x \\
                                4x^2 + x - 5 &=0 \\[2mm]
                                x &= \frac{-1\pm \sqrt{81}}{8} 
                                \end{align*}
                                Ratkaisuehdokkaiksi saadaan $x_1 = 1$ ja $x_2 = -1{,}25$. Sijoittamalla huomataan, että yhtälöllä on tasan yksi ratkaisu $x = -1{,}25$.
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="45caed56-70dd-4d42-910d-40480ea74ff1">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t113">
                            Juurifunktion derivaatta
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t113">
                    <p>
                        Osoita, että käyrät $y = x^2$ ja 
                        $$
                        y = \frac{1}{\sqrt{x}}
                        $$
                        leikkaavat toisensa kohtisuorasti.
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t113_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t113_v" class="collapse">
                        <p>
                            Käyrillä on yksi leikkauspiste $(1,1)$, joka löydetään ratkaisemalla yhtälö
                            $$
                            x^2 = \frac{1}{\sqrt{x}}.
                            $$
                            Funktion $f(x) = x^2$ kuvaajan pisteeseen $(1,1)$ asetetun tangentin kulmakerroin on 
                            $$
                            f'(1) = 2\cdot 1 = 2.
                            $$
                            Funktion 
                            $$
                            g(x) = \frac{1}{\sqrt{x}}
                            $$
                            kuvaajan pisteeseen $(1,1)$ asetetun tangentin kulmakerroin on 
                            $$
                            g'(1) = -\frac{1}{2 \cdot 1 \cdot \sqrt{1}} = -\frac{1}{2}.
                            $$
                            Kulmakertoimien tulo on $-1$, joten pisteeseen $(1,1)$ asetetut tangentit ovat kohtisuorassa toisiaan vastaan. 
                        </p> 
                    </div>
                </div>
            </div>

            <div class="tehtava" id="6c212b1c-45f3-4535-b782-921114e7eea8">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t114">
                            Juurifunktion derivaatta
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t114">
                    <p>
                        Neliön pinta-ala on alussa nolla ja kasvaa sen jälkeen tasaisella nopeudella $3 \text{ cm}^2$ sekunnissa. 
                    </p>
                    <ol class="a">
                        <li> 
                            Mikä on neliön pinta-ala 
                            <ul>
                                <li> 1 sekunnin kuluttua </li>
                                <li> 2 sekunnin kuluttua </li>
                                <li> 3 sekunnin kuluttua </li>
                                <li> 4 sekunnin kuluttua? </li>
                            </ul>
                        </li>
                        <li>
                            Muodosta funktio $A(t)$, joka ilmaisee neliön pinta-alan $t$ sekunnin kuluttua.
                        </li>
                        <li>
                            Jos tunnet neliön pinta-alan, miten saat selville neliön sivun pituuden? Muodosta funktio $s(t)$, joka ilmaisee neliön sivun pituuden $t$ sekunnin kuluttua.
                        </li>
                        <li>
                            Millä nopeudella neliön sivun pituus kasvaa 0,5 sekunnin kuluttua? Entä 3 sekunnin kuluttua? Anna vastaukset millimetrin tarkkuudella.
                        </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t114_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t114_v" class="collapse">
                        <ol class="a">
                            <li>  Neliön pinta-ala on 
                                <ul>
                                    <li> $3 \text{ cm}^2$ </li>
                                    <li> $6 \text{ cm}^2$ </li>
                                    <li> $9 \text{ cm}^2$ </li>
                                    <li> $12 \text{ cm}^2$. </li>
                                </ul>
                            </li>
                            <li>
                                $A(t) = 3t$.
                            </li>
                            <li>
                                Koska neliön pinta-ala on sivun pituuden toinen potenssi ($A = s^2$), saadaan sivun pituus selville ottamalla pinta-alasta neliöjuuri. Siten $s(t) = \sqrt{3t}$.
                            </li>
                            <li>
                                Derivaattafunktio on 
                                $$
                                s'(t) = \frac{3}{2\sqrt{3t}}.
                                $$
                                Siten 
                                \begin{align*}
                                s'(0{,}5) &= \sqrt{\frac{3}{2}} \approx 1{,}2 \text{ cm/s} \\[2mm]
                                s'(3) &= 0{,}5 \text{ cm/s.}
                                \end{align*}
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="43329bed-40c8-45a3-b322-54a30f724987">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t115">
                            Juurifunktion derivaatta
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t115">
                    <p>
                        Missä pisteessä funktion 
                        $$f(x) = 6\sqrt{x} - x$$
                        kuvaajalle muuttujan arvon 16 kohdalle piirretty normaali leikkaa
                    </p>
                    <ol class="a">
                        <li>
                            $x$-akselin
                        </li>
                        <li>
                            $y$-akselin?
                        </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t115_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t115_v" class="collapse">
                        <p>
                            Normaalin yhtälö on $y = 4x - 56$.
                        </p>
                        <ol class="a">
                            <li>
                                Pisteessä $(14,0)$.
                            </li>
                            <li>
                                Pisteessä $(0,-56)$.
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="22b25da7-4f0b-4ba7-bd27-38a1d8685ff9">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t119">
                            Juurifunktion derivaatta
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t119">
                    <p>
                        Kuumailmapallo kohoaa suoraan ylöspäin tasaisella nopeudella 0,75 m/s. Riina ja Valtteri seuraavat pallon nousua 50 metrin päässä pallo lähtöpaikasta. Tehtävänä on selvittää, millä nopeudella pallo etääntyy heistä, kun maasta irtautumisesta on kulunut yksi minuutti.
                    </p>
                    <ol class="a">
                        <li>
                            Piirrä tilanteesta mallikuva.
                        </li>
                        <li> 
                            Muodosta funktio $h(t)$, joka ilmaisee pallon sijaintikorkeuden $t$ sekunnin kuluttua maasta irtautumisesta. 
                        </li>
                        <li> 
                            Muodosta funktio $f(t)$, joka ilmaisee pallon etäisyyden Riinasta ja Valtterista $t$ sekunnin kuluttua maasta irtautumisesta. 
                        </li>
                        <li>
                            Millä nopeudella pallo etääntyy Riinasta ja Valtterista, kun maasta irtautumisesta on kulunut yksi minuutti? 
                        </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t119_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t119_v" class="collapse">
                        <ol class="a">
                            <li>
                                Mallikuva:
                                <br>
                                <img src="/kurssit/maa8/kuvat/MAA8kuva044.png" style="max-width: 100%; width: auto; height: auto;"/>
                            </li>
                            <li> 
                                $h(t) = 0{,}75t$ 
                            </li>
                            <li> 
                                $f(t) = \sqrt{2500 + 0{,}5625t^2}$ 
                            </li>
                            <li>
                                Etääntymisnopeuden ilmaisee derivaatta
                                $$
                                f'(t) = \frac{1{,}125t}{2\sqrt{2500 + 0{,}5625t^2}}.
                                $$
                                Minuutin kuluttua etääntymisnopeus on
                                $$
                                f'(60) \approx 0{,}50 \text{ m/s.}
                                $$
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="13791fc4-f6f8-4e1d-a899-9a85425116b0">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t118">
                            Juurifunktion derivaatta
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t118">
                    <p>
                        Tutki, sivuaako suora 
                        $$
                        y = \frac{x}{10} + \frac{5}{2}
                        $$
                        käyrää 
                        $$
                        y = \sqrt{x}.
                        $$
                        Perustele vastauksesi huolellisesti.
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t118_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t118_v" class="collapse">
                        <p>
                            Suoralla ja käyrällä on yhteinen piste $(25,5)$. Funktion $f(x) = \sqrt{x}\,$ kuvaajalle asetetun tangentin kulmakerroin on
                            $$
                            f'(25) = \frac{1}{2\sqrt{25}} = \frac{1}{10}
                            $$
                            eli sama kuin suoran kulmakerroin. Suora ja käyrä siis sivuavat toisiaan.
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="61793728-2845-494d-8bef-ae01a107fe70">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t101">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t101">
                    <p>
                        Tutki, onko funktiolla
                        $$
                        f(x) = \sqrt{2x} + \sqrt{3-x}
                        $$
                        suurinta tai pienintä arvoa. Jos jompi kumpi tai molemmat ovat olemassa, määritä ne.
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t101_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t101_v" class="collapse">
                        <p>
                            Suurin arvo on $f(2) = 3$ ja pienin arvo on $f(0) = \sqrt{3}$.
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="4abd984c-347f-4b3f-b6f5-e59f66b0cfbb">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t102">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t102">
                    <p>
                        Suunnistaja on maastossa 800 metrin etäisyydellä suorasta rastille johtavasta polusta. Jos hän suunnistaisi kohtisuoraan polulle, hän joutuisi kulkemaan polkua pitkin 1500 metriä päästäkseen rastille. Kuinka suunnistajan kannattaa valita reittinsä, kun hänen keskinopeutensa on maastossa 6 km/h ja polulla 10 km/h?
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t102_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t102_v" class="collapse">
                        <p>
                            Suunnistajan kannattaa tulla polulle kohdassa, josta on rastille matkaa 900 m.
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="1ca1d37e-6e4d-4177-ac1e-2b0137073017">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t103">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t103">
                    <p>
                        Millä muuttujan $x$ arvoilla funktio
                        $$
                        g(x) = \sqrt{2x - \sqrt{x}}
                        $$
                        on 
                    </p>
                    <ol class="a">
                        <li> määritelty </li>
                        <li> kasvava </li>
                        <li> vähenevä? </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t103_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t103_v" class="collapse">
                        <ol class="a">
                            <li> $x = 0$ tai $x \geq \frac{1}{4}$ </li>
                            <li> 
                                $x \geq \frac{1}{4}$ 
                                <br>
                                Huom. Derivaattafunktion nollakohtia tutkiessa pitää olla tarkkana määrittelyjoukon kanssa. Muuten saattaa löytää "nollakohdan", joka on funktion määrittelyjoukon ulkopuolellla ja siten myös derivaattafunktion määrittelyjoukon ulkopuolella.
                            </li>
                            <li> Ei millään. </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="4ede8dfd-ca98-416f-9000-96105ef46636">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t104">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t104">
                    <p>
                        Mikä luku on eniten neliöjuurtaan pienempi?
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t104_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t104_v" class="collapse">
                        <p>
                            $\dfrac{1}{4}$
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="db2f85df-ace9-40cc-8833-3a6be491ee2b">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t105">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t105">
                    <p>
                        Kaksi suoraa metsäpolkua risteää kohtisuorasti. Polkujen risteystä lähestyvät toista polkua kulkeva lenkkeilijä, jonka nopeus on 8 km/h, ja toista polkua jolkotteleva susi, jonka nopeus on 6 km/h. Molemmat ovat yhden kilometrin päässä polkujen risteyksestä. Kuinka pitkän ajan kuluttua lenkkeilijän ja suden etäisyys on pienimmillään? Mikä on tämä pienin etäisyys? Missä lenkkeilijä ja susi tällöin ovat?
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t105_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t105_v" class="collapse">
                        <p>
                            Etäisyys on pienimmillään 200 metriä, kun aikaa on kulunut 8,4 minuuttia eli 8 min 24 s. Lenkkeilijä on tällöin kulkenut risteyksen jälkeen 120 m polkua pitkin ja susi on vielä lähestymässä risteystä 160 metrin päässä. 
                        </p>
                        <p>
                            Vinkki: Oletetaan, että lenkkeilijä on alkutilanteessa pisteessä $(1,0)$ ja susi pisteessä $(0,1)$, ja polkujen risteys on origossa. Etäisyyttä ajan funktiona voi kuvata esimerkiksi funktiolla
                            $$
                            f(t) = \sqrt{(1-8t)^2 + (1-6t)^2},
                            $$
                            missä $t$ on aika tunteina. 
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="ba645743-ba6b-4d6f-9cb0-e18c03e476e6">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t117">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t117">
                    <p>
                        Osoita, että yhtälöllä
                        $$
                        x\sqrt{x} = 4x - 10
                        $$
                        ei ole ratkaisuja.
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t117_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t117_v" class="collapse">
                        <p>
                            Funktion 
                            $$
                            f(x) = x\sqrt{x} - 4x + 10
                            $$
                            derivaattafunktio
                            $$
                            f'(x) = \frac{3}{2}\sqrt{x} - 4.
                            $$
                            Funktio $f$ saa derivaattafunktion nollakohdassa pienimmän arvonsa
                            $$
                            f\left(\frac{64}{9}\right) = \frac{14}{27} > 0.
                            $$
                            Funktion arvot ovat siis aina positiivisia, joten tarkastelullla yhtälöllä ei ole ratkaisuja.
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="ca046b10-bf69-4ef2-93a8-e1c45ec7649c">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t106">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t106">
                    <p>
                        Vierekkäisille neliön muotoisille tonteille rakennetaan alakoulu ja päiväkoti. Tonttien yhteenlaskettu pinta-ala on $9\,000 \text{ m}^2$. Tonttien ympärille ja väliin pystytetään aita. Aitaurakoitsija haluaa maksimoida oman etunsa ja toivoo, että aidan kokonaispituudesta tulisi mahdollisimman suuri. Miten tonttien pinta-alat pitäisi valita, jotta aitaurakoitsijan toive toteutuisi?
                        <br>
                        <img src="/kurssit/maa8/kuvat/MAA8kuva036.png" style="max-width: 100%; width: auto; height: auto;"/>
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t106_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t106_v" class="collapse">
                        <p>
                            Isomman tontin pinta-alaksi pitäisi valita $5\,760 \text{ m}^2$ ja pienemmän tontin pinta-alaksi $3\,240 \text{ m}^2$.
                        </p>
                        <p>
                            Vinkki: Aidan pituutta voidaan kuvata funktiolla
                            $$
                            f(x) = 4x + 3\sqrt{9000 - x^2},
                            $$
                            missä $x$ on isomman tontin sivun pituus.
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="74d57bae-486a-4ca5-b656-f6431adf8fc9">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t107">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t107">
                    <p>
                        Kangas on muodoltaan neliö, jonka sivujen pituudet ovat 8,0 metriä. Neliön nurkista leikataan pois samanlaiset keskipisteeseen ulottuvat palat. Jäljelle jäävä kangas ommellaan säännöllisen nelisivuisen pyramidin muotoisen teltan katoksi.
                    </p>
                        <ol class="a">
                            <li> Määritä leikkauskohtien etäisyys nurkista niin, että teltan tilavuus on mahdollisimman suuri. Anna vastauksen tarkka arvo sekä likiarvon kolmen merkitsevän numeron tarkkuudella. </li>
                            <li> Kuinka suuri on tällaisessa teltassa se lattiapinta-ala, jossa 180 cm pitkä henkilö mahtuu seisomaan suorana? Anna vastaus kahden merkitsevän numeron tarkkuudella. </li>
                        </ol>
                        <img src="/kurssit/maa8/kuvat/MAA8kuva037.png" style="max-width: 100%; width: auto; height: auto;"/>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t107_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t107_v" class="collapse">
                        <ol class="a">
                            <li> 
                                Leikkauskohdan etäisyys nurkasta on 
                                $$
                                \left(4 - \frac{4}{3}\sqrt{6}\right) \text{ m} \approx 0{,}734 \text{ m.}
                                $$
                                Vinkki: Teltan tilavuutta voi kuvata esimerkiksi funktiolla
                                $$
                                f(x) = \frac{1}{3}(8-2x)^2\sqrt{8x-x^2},
                                $$
                                missä $x$ on kysytty leikkauskohdan etäisyys kankaan nurkasta. Tässä pohjan ala on $(8-2x)^2$ ja korkeus saadaan yhtälöstä $$
                                h^2 = 4^2 - (4-x)^2.
                                $$
                                Tämä yhtälö saadaan muodostettua tarkastelemalla valmiin teltan poikkileikkauksen puolikasta, jota seuraavat kuvat havainnollistavat:
                                <br>
                                <img src="/kurssit/maa8/kuvat/MAA8kuva037b.png" style="max-width: 100%; width: auto; height: auto;"/>
                                <br>
                                <img src="/kurssit/maa8/kuvat/MAA8kuva037c.png" style="max-width: 100%; width: auto; height: auto;"/>
                            </li>
                            <li>  
                                Kysytty lattiapinta-ala on noin $2{,}1 \text{ m}^2$. 
                                <br>
                                Vinkki: teltan poikkileikkauksen yhdenmuotoiset kolmiot:
                                <br>
                                <img src="/kurssit/maa8/kuvat/MAA8kuva038.png" style="max-width: 100%; width: auto; height: auto;"/>
                                <br>
                                Tästä saadaan 
                                $$
                                x = \sqrt{2}\left(\frac{4}{\sqrt{3}} - \frac{9}{5}\right) \approx 0{,}7204
                                $$
                                ja pinta-ala 
                                $$
                                (2x)^2 = 4x^2 \approx 2{,}1.
                                $$
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="66aa3016-cab6-46bd-855d-d9b48a9c35c6">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t108">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t108">
                    <p>
                        Teräsputkesta, jonka pituus on 5,00 metriä, taivutetaan Z-kirjaimen muotoinen kehikko. Kuinka pitkiin osiin putki tulee taivuttaa, jotta kehikon rajaaman suorakulmion pinta-ala on mahdollisimman suuri? Anna vastaukset senttimetrin tarkkuudella.
                    </p>
                    <img src="/kurssit/maa8/kuvat/MAA8kuva039.png" style="max-width: 100%; width: auto; height: auto;"/>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t108_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t108_v" class="collapse">
                        <p>
                            Vaakasuorien osien pituus noin 1,05 metriä ja keskimmäisen osan pituus noin 2,90 metriä. 
                        </p>
                        <p>
                            Vinkki: Osien pituudet toteuttavat yhtälön 
                            $$
                            2x + y = 5.
                            $$
                            Suorakulmion korkeus saadaan yhtälöstä
                            $$
                            h^2 = y^2 - x^2
                            $$
                            eli yhtälöstä
                            $$
                            h = \sqrt{(5-2x)^2 - x^2}.
                            $$
                            Suorakulmion pinta-alan ilmaisee siis funktio
                            $$
                            f(x) = x\sqrt{25-20x + 3x^2},
                            $$
                            missä $0 \leq x \leq 2{,}5 \text{ m.}$
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="509400e5-b9e1-417f-a30d-faacc88f5791">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t109">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t109">
                    <p>
                        Sähköjohdon vetäminen metsään maksaa kilometriä kohti kolme kertaa niin paljon kuin johdon vetäminen pitkin tienvartta. Suunnittele sähköjohdon edullisin reitti tukiasemalta $A$ muuntajalle $B$. 
                    </p>
                    <img src="/kurssit/maa8/kuvat/MAA8kuva040.png" style="max-width: 100%; width: auto; height: auto;"/>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t109_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t109_v" class="collapse">
                        <p>
                            Johto vedetään suoraan tielle kohtaan, josta on muuntajalle matkaa vielä 7,6 km. 
                        </p>
                        <p>
                            Vinkki: Kustannusta voidaan kuvata esimerkiksi funktiolla
                            $$
                            f(x) = 9-x + 3\sqrt{16 + x^2},
                            $$
                            missä $x$ on kuten alla olevassa kuvassa:
                            <br>
                            <img src="/kurssit/maa8/kuvat/MAA8kuva041.png" style="max-width: 100%; width: auto; height: auto;"/>
                        </p>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="e550a20e-e2b0-49b9-9d0f-3ab31ed79fa4">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t110">
                            Juurifunktion kulku
                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t110">
                    <p>
                        Ohut ja pitkä metalliputki pitäisi kuljettaa käytävän mutkan läpi. Alla käytävät näkyvät ylhäältä katsottuna. 
                    </p>
                    <ol class="a">
                        <li> Kuinka pitkä putki mahtuu mutkan läpi vaakasuorassa asennossa? </li>
                        <li> Kuinka pitkä putki mahtuu mutkan läpi, jos sitä voidaan kuljetuksen aikana kallistaa? Käytävän korkeus on 2,5 metriä.</li>
                    </ol>
                    <img src="/kurssit/maa8/kuvat/MAA8kuva042.png" style="max-width: 100%; width: auto; height: auto;"/>
                    <p>
                        Ohje: Aloita piirtämällä a-kohdan tilanteesta mallikuva. Merkitse kapean käytävän puolella olevan putken osan pituutta kirjaimella $x$.
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t110_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t110_v" class="collapse">
                        <ol class="a">
                            <li> 
                                Enintään 7,0 metriä pitkä putki. 
                                <br>
                                <img src="/kurssit/maa8/kuvat/MAA8kuva043.png" style="max-width: 100%; width: auto; height: auto;"/>
                                <br>
                                Mutkaan mahtuvan putken pituutta eri asennoissa voidaan kuvata funktiolla
                                $$
                                f(x) = x + \frac{3x}{\sqrt{x^2 - 4}}.
                                $$  
                                Sen derivaatalla on yksi nollakohta:
                                $$
                                x = \sqrt{4 + 2\sqrt[3]{18}}.
                                $$
                                Kulkukaaviosta nähdään, että tämä on putken pituuden minimikohta, eli hankalimmassa kohdassa putken pituus saa olla enintään
                                $$
                                f\left(\sqrt{4 + 2\sqrt[3]{18}}\right) \approx 7{,}0.
                                $$
                            </li>
                            <li> Enintään 7,4 metriä pitkä putki. </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="close-section">
                <a data-toggle="collapse" class="collapsed" data-target="#MAA8luku1-tehtavasarja2">
                    Sulje kappale
                </a>
            </div>
        </div>
    </section>


    <section class="panel">
        <header class="otsikko">
            <h1>                    
                <a data-toggle="collapse" class="collapsed" data-target="#MAA8luku1-tehtavasarja3">
                    TEHTÄVÄSARJA III
                </a>
            </h1>
        </header>

        <div id="MAA8luku1-tehtavasarja3" class="collapse">
            <!-- Tästä alkaa piilotus -->

            <div class="tehtava" id="348b27a9-6b6f-4c79-b46f-10ae4162fe6c">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t101">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t101">
                    <ol class="a">
                        <li> 
                            Sievennä lauseke 
                            $$\sqrt{a\sqrt{a\sqrt{a^2}}},$$ 
                            kun $a \geq 0$. 
                        </li>
                        <li>
                            Luku on yhtä suuri kuin puolet sen neliöjuuresta. Määritä kaikki tällaiset luvut.
                        </li>
                    </ol>
                    <p>
                        [Pitkä S2016/2a &amp; S2014/2b]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t101_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t101_v" class="collapse">
                        <ol class="a">
                        <li> 
                            \begin{align*}
                            \sqrt{a\sqrt{a\sqrt{a^2}}} &= \sqrt{a\sqrt{a^2}} \\
                            &= \sqrt{a^2} \\
                            &= a
                            \end{align*}
                        </li>
                        <li>
                            Kysytyt luvut ovat $0$ ja $\dfrac{1}{4}$.
                        </li>
                    </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="2f7256af-74e3-400c-b924-a9d9d3669ade">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t102">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t102">
                    <ol class="a">
                        <li> 
                            Piirrä kuva epäyhtälöiden 
                            $$0 \leq y \leq \sqrt{\left| x \right|}$$ 
                            määräämästä tasoalueesta, kun $-1 \leq x \leq 1$. 
                        </li>
                        <li> 
                            Ratkaise yhtälö 
                            $$x\sqrt{1+x} = \sqrt{2x}.$$
                            [Pitkä K2015/2]
                        </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t102_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t102_v" class="collapse">
                        <ol class="a">
                            <li> 
                                Kuva tasoalueesta: 
                                <br>
                                <img src="/kurssit/maa8/kuvat/MAA8kuva019.png" max-width: 100%; width: auto; height: auto;/>
                            </li>
                            <li> Yhtälö toteutuu, jos ja vain jos $x = 0$ tai $x = 1$. </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="tehtava" id="d6f92758-f374-484f-bc77-607b005b3b29">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t103">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t103">
                    <p>
                        Ympyräsektorin säde on 3 ja keskuskulman suurus on $\alpha$. Sektori taivutetaan ympyräpohjaisen kartion vaipaksi. Mikä on kulman $\alpha$ tarkka arvo silloin, kun kartion tilavuus on mahdollisimman suuri?
                        <br>
                        <img src="/kurssit/maa8/kuvat/MAA8kuva033.png" max-width: 100%; width: auto; height: auto;/>
                        <br>
                        [Pitkä S2017/6]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t103_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t103_v" class="collapse">
                        <p>
                            Kulma $\alpha = 2\pi\sqrt{\dfrac{2}{3}}$.
                        </p>
                        <p>
                            Kartion pohjaympyrän kehän pituus on $3\alpha$ ja säde
                            $$
                            r = \frac{3\alpha}{2\pi}.
                            $$
                            Kartion sivujanan pituus on $3$, joten kartion korkeudeksi saadaan Pythagoraan lauseen avulla välivaiheiden jälkeen
                            $$
                            h = \frac{3}{2\pi}\sqrt{4\pi^2 - \alpha^2}.
                            $$
                            Kartion tilavuus on
                            $$
                            V = \frac{\pi}{3}r^2h = \frac{9}{8\pi^2}\alpha^2\sqrt{4\pi^2 - \alpha^2},
                            $$
                            missä $0 \leq \alpha \leq 2\pi$. Suurin arvo löytyy derivaatan nollakohdasta tai välin päätepisteistä. Derivointia voi helpottaa teoreeman 5 avulla.
                        </p>    
                    </div>
                </div>
            </div>

            <div class="tehtava" id="3ae60645-0b63-4d91-add3-7ad9e9837453">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t104">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t104">
                    <p>
                        Suoran ympyräkartion muotoista telttaa varten on varattu 16 neliömetriä kangasta. Kangasta ei käytetä teltan pohjaan. Määritä pohjaympyrän halkaisija silloin, kun teltan tilavuus on suurin mahdollinen.
                    </p>
                    <figure>
                        <img src="/kurssit/maa8/kuvat/MAA8yo02.jpg" max-width: 100%; width: auto; height: auto;/>
                        <figcaption>
                            Kuva: <a href="http://www.indios.cz/cs/rytirske-a-stredoveke-stany/merlin/">indios.cz</a>
                        </figcaption>
                    </figure>
                    <p>
                        [Pitkä K2015/9]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t104_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t104_v" class="collapse">
                        <p>
                            Kysytty lattian halkaisija on 
                            $$2r = \dfrac{8}{\sqrt[4]{3\pi^2}}.$$
                        </p>
                        <p>
                            Teltan vaipan ala $A = \pi rs = 16$, joten sivujana on 
                            $$
                            s = \frac{16}{\pi r}.
                            $$
                            Teltan korkeus on
                            $$
                            h = \sqrt{s^2 - r^2}.
                            $$
                            Kartion tilavuus on
                            \begin{align*}
                            V &= \frac{\pi}{3}r^2h \\[2mm]
                            &= \frac{1}{3}\pi r^2\sqrt{\frac{256}{\pi^2r^2} - r^2} \\[2mm]
                            &= \frac{1}{3}\sqrt{256r^2 - \pi^2r^6}.
                            \end{align*}
                            Tutkitaan, missä juurrettava 
                            $$f(r) = 256r^2 - \pi^2r^6$$ 
                            saa suurimman arvonsa, sillä tällöin myös tilavuusfunktio $V(r)$ saa suurimman arvonsa. Derivaattafunktiolla on kolme nollakohtaa, mutta positiivisia niistä on vain yksi: 
                            $$
                            r = \frac{4}{\sqrt[4]{3\pi^2}}
                            $$  
                            Esimerkiksi kulkukaavion avulla havaitaan, että funktio $f$ saa tässä kohdassa suurimman arvonsa.
                        </p>    
                    </div>
                </div>
            </div>
           
            <div class="tehtava" id="2f17193b-c4e9-48ce-ac0e-caf104f07a77">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t105">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t105">
                    <p>
                        Mikä paraabelin $y = 5-x^2$ piste on lähinnä origoa? Piirrä kuvio.
                        <br>
                        [Pitkä K2009/9]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t105_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t105_v" class="collapse">
                        <p>
                            Lähinnä origoa ovat paraabelin pisteet $\left(\frac{3}{\sqrt{2}}, \frac{1}{2}\right)$ ja $\left(-\frac{3}{\sqrt{2}}, \frac{1}{2}\right)$.
                            <br>
                            <img src="/kurssit/maa8/kuvat/MAA8kuva034.png" max-width: 100%; width: auto; height: auto;/>
                        </p>   
                    </div>
                </div>
            </div>

            <div class="tehtava" id="abbac79c-2b8e-47eb-86f6-9e490f6df919">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t106">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t106">
                    <p>
                        Ratkaise yhtälön 
                        $$
                        \sqrt{2-x} = x + 2
                        $$
                        reaalijuuret.
                        <br>
                        [Pitkä S2008/7]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t106_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t106_v" class="collapse">
                        <p>
                            Yhtälöllä on täsmälleen yksi ratkaisu:
                            $$
                            x = \frac{-5 + \sqrt{17}}{2}
                            $$  
                        </p>     
                    </div>
                </div>
            </div>

            <div class="tehtava" id="cefd5f74-790a-4488-9662-15289f8d5428">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t108">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t108">
                    <p>
                        Määritä funktion 
                        $$
                        f(x) = x + \sqrt{9-x^2},
                        $$
                        missä $-3 \leq x \leq 3$ suurin ja pienin arvo. Piirrä funktion kuvaaja.
                        <br>
                        [Pitkä K2008/9]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t108_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t108_v" class="collapse">
                        <p>
                            Pienin arvo on $f(-3) = -3$ ja suurin arvo on 
                            $$
                            f\left(\frac{3}{\sqrt{2}}\right) = 3\sqrt{2}.
                            $$
                            <img src="/kurssit/maa8/kuvat/MAA8kuva035.png" max-width: 100%; width: auto; height: auto;/>
                        </p>     
                    </div>
                </div>
            </div>

            <div class="tehtava" id="d969750b-e00c-49a8-b35a-14243b3984cd">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t109">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t109">
                    <p>
                        Suoran kolmisivuisen pyramidin pohja on tasasivuinen kolmio. Pyramidin sivusärmän pituus on 60 cm. Miten on pohjasärmän pituus valittava, jotta pyramidin tilavuus olisi mahdollisimman suuri?
                        <br>
                        [Pitkä S2007/7]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t109_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t109_v" class="collapse">
                        <p>
                            Sivusärmän pituudeksi on valittava $60\sqrt{2} \text{ cm } \approx 84{,}9 \text{ cm.}$
                        </p>     
                    </div>
                </div>
            </div>

            <div class="tehtava" id="b827bf48-b8c4-423a-8b5e-1760a3bcdf5c">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t110">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t110">
                    <p>
                        Ratkaise yhtälö
                        $$
                        \sqrt{x-2} = 1 + \frac{2}{\sqrt{x-2}}
                        $$
                        <br>
                        [Pitkä S2000/2]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t110_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t110_v" class="collapse">
                        <p>
                            $x = 6$
                        </p>     
                    </div>
                </div>
            </div>

            <div class="tehtava" id="bf626302-fb9d-4532-b1a2-56db7032f379">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s3t107">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s3t107">
                    <p>
                        Ympyrälevystä, jonka säde on $r$, leikataan pois sektori, ja jäljelle jäänyt osa taivutetaan suoran ympyräkartion vaipaksi. Määritä pois leikatun sektorin keskuskulma asteen tarkkuudella, kun kartion tilavuus on mahdollisimman suuri.
                        <br>
                        [Pitkä S2008/9]
                    </p>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s3t107_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s3t107_v" class="collapse">
                        <p>
                            Poisleikatun sektorin keskuskulma on noin $66^\circ$.
                        </p>     
                    </div>
                </div>
            </div>

            <div class="tehtava" id="927257fc-a6e3-4489-8868-f02ff78f786f">
                <header>
                    <h1>                            <div class="checkbox-group"></div>
                        <a data-target="#MAA8s2t116">

                        </a>
                    </h1>
                </header>
                <div id="MAA8s2t116">
                    <p>
                        Pallon tilavuus on alussa nolla ja kasvaa sen jälkeen tasaisella nopeudella $120 \text{ cm}^3$ sekunnissa. 
                    </p>
                    <ol class="a">
                        <li>
                            Muodosta funktio $V(t)$, joka ilmaisee pallon tilavuuden $t$ sekunnin kuluttua.
                        </li>
                        <li>
                            Jos tunnet pallon tilavuuden, miten saat selville pallon säteen? Muodosta funktio $r(t)$, joka ilmaisee pallon säteen $t$ sekunnin kuluttua.
                            <br>
                            Vinkki: kertaa tarvittaessa <a href="http://kisallioppiminen.fi/kurssit/maa3/luku3/">MAA3-kurssin</a> teoreema 21.
                        </li>
                        <li>
                            Millä nopeudella pallon säde kasvaa 2 sekunnin kuluttua? Entä 4 sekunnin kuluttua? Anna vastaukset millimetrin tarkkuudella.
                        </li>
                        <li>
                            Millä nopeudella pallon pinta-ala kasvaa 0,5 sekunnin kuluttua? Entä 3 sekunnin kuluttua? Anna vastaukset neliömillimetrin tarkkuudella. 
                            <br>
                            Vinkki: <a href="http://kisallioppiminen.fi/kurssit/maa3/luku3/">MAA3-kurssin</a> teoreema 21 ja <a href="http://kisallioppiminen.fi/kurssit/maa7/luku3/">MAA7-kurssin</a> teoreema 23.
                        </li>
                    </ol>
                    <h2>
                        <a data-toggle="collapse" class="collapsed" data-target="#MAA8s2t116_v">
                            Vastaus
                        </a>
                    </h2>
                    <div id="MAA8s2t116_v" class="collapse">
                        <ol class="a">
                            <li>
                                $V(t) = 120t$.
                            </li>
                            <li>
                                Yhtälöstä
                                $$V = \frac{4\pi r^3}{3}$$ saadaan ratkaistua
                                $$
                                r = \sqrt[3]{\frac{3V}{4\pi}}.
                                $$
                                Siten 
                                $$
                                r(t) = \sqrt[3]{\frac{90t}{\pi}}.
                                $$
                            </li>
                            <li>
                                Derivaattafunktio on 
                                $$
                                r'(t) = \frac{30}{\pi}\sqrt[3]{\frac{\pi^2}{8100t^2}}.
                                $$
                                Siten 
                                \begin{align*}
                                r'(2) &\approx 0{,}6 \text{ cm/s} \\
                                r'(4) &\approx 0{,}4 \text{ cm/s.}
                                \end{align*}
                            </li>
                            <li>
                                Pinta-alan ilmaisee funktio
                                $$
                                A(t) = 4\pi (r(t))^2.
                                $$
                                Sen derivaattafunktio on 
                                \begin{align*}
                                A'(t) &= 4\pi\cdot 2r(t) \cdot r'(t) \\[2mm]
                                &=8\pi \sqrt[3]{\frac{90t}{\pi}} \frac{30}{\pi}\sqrt[3]{\frac{\pi^2}{8100t^2}} \\[2mm]
                                &= 240 \sqrt[3]{\frac{\pi}{90t}}.
                                \end{align*}
                                Siten 
                                \begin{align*}
                                A'(2) &\approx 62{,}25 \text{ cm}^2/\text{s} \\
                                A'(4) &\approx 49{,}41 \text{ cm}^2/\text{s.}
                                \end{align*}
                            </li>
                        </ol>
                    </div>
                </div>
            </div>

            <div class="close-section">
                <a data-toggle="collapse" class="collapsed" data-target="#MAA8luku1-tehtavasarja3">
                    Sulje kappale
                </a>
            </div>
        </div>
    </section>

    <section class="panel">
        <header>
            <h1>                        
                <a data-toggle="collapse" class="collapsed" data-target="#MAA8L1itsearviointi">
                    Itsearviointitehtävät
                </a>
            </h1>
        </header>
        <div id="MAA8L1itsearviointi" class="collapse">
            <p>
                Varmista, että olet oppinut tämän luvun keskeiset asiat tekemällä <a href="">itsearviointitesti</a> opetus.tv:n polku-palvelussa. Samalla harjoittelet omien ratkaisujesi pisteyttämistä pisteytysohjeiden avulla. 
            </p>
            <div class="close-section">
                <a data-toggle="collapse" class="collapsed" data-target="#MAA8L1itsearviointi">
                    Sulje kappale
                </a>
            </div>
        </div>
    </section>
