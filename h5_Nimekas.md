Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 18.-19.2.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

# h5 Nimekäs

## a) Nimi

Rekisteröidyin palveluun https://www.namecheap.com/ ja hankin domainin **majamakik.site** sieltä.


Namecheapin hallintapaneelissa lisäsin A-tietueen, joka osoittaa UpCloud-palvelimeni julkiseen IP-osoitteeseen, domainille tuleva liikenne ohjautuu oikealle palvelimelle.


Host-kenttä kertoo, mihin osaan domainia tietue liittyy. Käytin Host-kentässä merkkiä @, koska se tarkoittaa päädomainia ilman etuliitteitä. Tämän ansiosta osoite **majamakik.site** ohjautuu suoraan määrittämälleni palvelimelle.


P.S. Yritin saada domainin ilmaiseksi GitHub Education paketin avulla, mutta se ei onnistunut. Ongelma saattoi johtua siitä, että Haaga-Helia ei ole heidän oppilaitoslistallaan, tai en onnistunut yhdistämään opiskelijatiliä oikein. Otin yhteyttä Namecheapin tukeen, mutta en ole vielä saanut vastausta.

<img width="940" height="106" alt="image" src="https://github.com/user-attachments/assets/156c57e8-93e2-442b-b442-38ba0fb95c5e" />
<img width="887" height="555" alt="image" src="https://github.com/user-attachments/assets/c0d632ba-ca9b-4d4a-b5a7-2d6b0ebad8fc" />
<img width="940" height="434" alt="image" src="https://github.com/user-attachments/assets/93b38993-5be3-4172-b286-2b79a68d92ce" />
<img width="940" height="292" alt="image" src="https://github.com/user-attachments/assets/a8178083-924e-40e6-9ea3-168709de4ad1" />


## b) Alidomain

Yritin luoda kaksi alidomainia päädomainin alle. Tarkoituksena oli testata kahta eri tapaa ohjata alidomainit samalle palvelimelle. Aluksi sain virheilmoituksen, että sivustoa ei voi saavuttaa. Käynnistin VirtualBoxin ja kirjauduin palvelimelle, mikä onnistui, mutta sivu ei silti "auennut".


Jonkin ajan kuluttua ja useiden yritysten jälkeen osoite **majamakik.site** alkoi toimia . En ole täysin varma, mikä korjasi ongelman, ehkä  DNS muutosten päivittyminen vei aikaa (kesti yli tunti).


Lisäsin uuden A-tietueen. Host-kenttään kirjoitin **linukstesti** ja toiseen **www**. Näin syntyi osoite **http://linukstesti.majamakik.site/**, joka ohjautuu suoraan määritettyyn IP-osoitteeseen.


Bonus. Muutin sivun sisältöä päivittämällä palvelimen **index.html** tiedoston VirtualBoxin terminaalissa. 


<img width="698" height="414" alt="image" src="https://github.com/user-attachments/assets/bb3232f1-2ffc-4b39-a864-f19b333d3192" />
<img width="940" height="338" alt="image" src="https://github.com/user-attachments/assets/10de4653-536c-401d-a2b9-63c24308122d" />
<img width="940" height="140" alt="image" src="https://github.com/user-attachments/assets/7b24a83a-88a1-4942-9e2b-fccc7b34b762" />
<img width="764" height="91" alt="image" src="https://github.com/user-attachments/assets/09260608-0324-4974-ad22-50a00866762a" />
<img width="910" height="149" alt="image" src="https://github.com/user-attachments/assets/065c8b6a-081a-4bf6-b51c-2d1043da9e10" />

## c) Tutki jonkin nimen DNS-tietoja 'host' ja 'dig' -komennoilla

Tutkin kolmen verkkosivun tietoja komennoilla host ja dig. Tarkoitus oli nähdä, mitä tietoja nimipalvelin palauttaa ja miten eroavat toisistaan.


Komentoa host, sain nopeasti perustiedot domainista. Komento palautti IP osoitteen A-tietueen ja se kertoo, mihin palvelimeen verkkosivu osoittaa.  Komento dig antoi paljon tarkempaa tietoa. 


Alla selitän tarkemmin yksityis tulokset namechep.com esimerkistä. 


**majamakik.site tuloksia**

<img width="678" height="173" alt="image" src="https://github.com/user-attachments/assets/d70cc9bb-d4dd-46ab-aa6c-16e49985f119" />
<img width="670" height="391" alt="image" src="https://github.com/user-attachments/assets/4a05a946-82c6-4637-9355-df4be147a923" />

**namecheap.com tuloksia**

<img width="613" height="123" alt="image" src="https://github.com/user-attachments/assets/5ee85f5c-592f-4365-a2d8-4244dd64269d" />
<img width="650" height="389" alt="image" src="https://github.com/user-attachments/assets/0e82302f-c2d0-49fc-adfb-35c0ead3395c" />

Komennon _dig namecheap.com_, sain yksityiskohtaista tietoa. Kohdassa HEADER kerrotaan kyselyn tila. Status NOERROR tarkoittaa, että kysely onnistui ja domain löytyi. Rivillä näkyvät myös liput siis flags, että vastaus saatiin nimipalvelimelta.


QUESTION SECTION, mitä tietoa kysyttiin. ANSWER SECTION. Siinä näkyy varsinainen vastaus nimipalvelimelta namecheap.com IN A 198.54.117.250. Se tarkoittaa, että domain namecheap.com osoittaa IP osoitteeseen. Numero 60 on TTL-arvo sekunteina. Tieto säilyy välimuistissa 60 sekuntia ennen uutta hakua.


Query time, kertoo kuinka kauan kysely kesti, siis 51 millisekuntia. SERVER näyttää, mikä DNS-palvelin vastasi kyselyyn. 

**microsoft.com tuloksia**

<img width="773" height="525" alt="image" src="https://github.com/user-attachments/assets/49c5443f-6244-4e18-be56-f155708f9151" />

**Tuloksien erot**

Vertailun perusteella host on hyvä työkalu nopeaan tarkistukseen, kun taas dig sopii tarkempaan analyysiin. 


Kun vertasin _dig namecheap.com_ ja _dig microsoft.com_ komentojen tuloksia, huomasin useita eroja. 


Ero näkyy ANSWER SECTION. Namecheapin tuloksessa oli vain yksi A-tietue, se osoitti yhteen IP osoitteeseen. Domain ohjaa yhteen pääpalvelimeen. Microsoftin tuloksessa oli kaksi A-tietuetta, eli kaksi eri IP osoitetta. Tämä tarkoitta kuormanjakoon eli load balancing, jossa liikenne jaetaan useille palvelimille paremman suorituskyvyn. 


Toinen ero on TTL arvoissa. Namecheapin TTL oli 60 sekuntia, se tarkoittaa, että DNS tieto päivittyy usein. Lyhyt TTL helpottaa muutosten tekemistä nopeasti. Microsoftin TTL oli 2858 sekuntia, tieto säilyy välimuistissa pidempään. Suuremmat palvelut käyttävät usein pidempää TTL arvoa parantaakseen suorituskykyä.


Query time oli myös erilainen. Namecheapin kysely kesti 51 millisekuntia, kun taas Microsoftin vain 3 millisekuntia. Tämä voi tarkoitta välimuistista tai siitä, että Microsoftin DNS tiedot olivat jo tallennettuina paikalliselle palvelimelle.



# LÄHTEET:

Tero Karvinen – Linux-palvelimet: https://terokarvinen.com/linux-palvelimet/ 


www.microsoft.com 


www.namecheap.com 


https://www.linux.fi/wiki/Dig 


https://www.linux.fi/wiki/Host 
