Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 27.1 - 28.1.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

## h3 Hello Web Server

## x) Tiivistelmä

- Tässä tehtävässä opettelin Apache-webpalvelimen perustoimintaa ja name based virtual hostin käyttöä. <br>
- Testasin, että palvelin vastaa localhost-osoitteesta ja tutkin Apache-lokitiedostoja. <br>
- Loin uuden virtual hostin ja tein sille oman HTML5-etusivun. <br>
- Opin myös käyttämään curl-komentoa. <br>

## a) Testaa. Weppipalvelimeni vastaa localhost-osoitteesta. Asenna Apache-weppipalvelin.

Apache-webpalvelin oli jo asennettu luennon aikana. Palvelimen toiminta testattiin avaamalla osoite http://localhost selaimessa. Oletussivu latautui onnistuneesti.

## b) Etsi lokista rivit, jotka syntyvät, kun lataat sivun. 

**Käytetty komento:** _sudo tail -f /var/log/apache2/access.log_

**Selitys:** Lokirivi näyttää HTTP tiedot, kun sivu avattiin selaimessa. Rivillä näkyy IP-osoite, päivämäärä ja kellonaika sekä käytetty http metodi. Lisäksi lokissa näkyy käytetty selain, käyttöjärjestelmä, http versio, tilakoodi ja vastauksen koko tavuina. 

<img width="940" height="124" alt="image" src="https://github.com/user-attachments/assets/7076388d-a81c-43a6-9fe4-3103250af6c8" /> <br>


 ## c) Etusivu uusiksi. Uusi name based virtual host. 

Luon kansion ja uuden html tiedoston:

**Käytetty komento:**

_1. mkdir ~/hattu.example.com <br>
2. nano ~/hattu.example.com/index.html <br>
3. sudo nano /etc/apache2/sites-available/hattu.example.com.conf <br>_
  
<img width="387" height="344" alt="image" src="https://github.com/user-attachments/assets/6609213c-e9f5-465c-95fa-f3b0d52480f1" />
<img width="548" height="192" alt="image" src="https://github.com/user-attachments/assets/d4a06d81-a186-4299-9f6a-fa94989a5c53" /> <br>

**Vanhan sivuston poisto ja uuden käyttöönotto:**

**Käytetty komento:**

_1. sudo a2dissite klaudija.conf <br>
2. sudo a2ensite hattu.example.com.conf <br>
3. sudo systemctl reload apache2 <br>_

<img width="940" height="372" alt="image" src="https://github.com/user-attachments/assets/fd071ae9-32ef-40f4-af24-46d1eca5ee49" /> <br>

 
**Ilmoitetaan järjestelmälle, että hattu.example.com on uusi localhost:**

Se ei mennyt ihan helposti, pitänyt säätää vähän sen jälkeen ennen kuin tajusin, että ongelma oli hattu.example.com config. Kun korjasin sen localhost muuttui. 

<img width="940" height="577" alt="image" src="https://github.com/user-attachments/assets/64876ff4-64fe-422a-a2b4-537635fefb1a" />
<img width="940" height="235" alt="image" src="https://github.com/user-attachments/assets/3d57ce33-f332-4019-954d-98993705d7c1" />
<img width="940" height="283" alt="image" src="https://github.com/user-attachments/assets/8e60b8f2-7037-4d98-9e1f-57238af9bdcf" /> <br>
 
**Selitys:** Loin uusi name based virtual host nimellä hattu.example.com. Vanhan ”oletussivusto” poistin käytöstä ja otin uuden sivuston käyttöön. Aluksi sivu ei toiminut, koska virtual host asetuksissa oli virhe. Kun asetukset korjattiin ja localhost määritettiin oikein, sivu alkoi toimia.

## e) Tee validi HTML5 sivu.
**Selitys:** Tein etusivu HTML5 standardin mukaisesti. Sivulla on otsikko, teksti ja oikea HTML rakenne. Sivun koodin validoin HTML validaattorilla. Validaattori ehdotti lang attribuutin lisäämistä HTML tagiin kielen määrittämiseksi.

 <img width="806" height="64" alt="image" src="https://github.com/user-attachments/assets/65dd3174-f003-4bde-8d9b-7d0f2b81fc3e" />
 <img width="819" height="417" alt="image" src="https://github.com/user-attachments/assets/ef42877b-7ee5-444d-b061-d079582a822c" /> <br>

 
## f) Anna esimerkit 'curl -I' ja 'curl' -komennoista. Selitä 'curl -I' muutamasta näyttämästä otsakkeesta (response header), mitä ne tarkoittavat.

**Käytetty komento:**

_1. sudo apt update <br>
2. sudo apt install curl <br>
3. curl http://localhost <br>
4. curl -I http://localhost <br>_

**Selitys:** Ensin asensin curl. Sitten  - Curl komento hakee sivun sisällön ja näyttää HTML koodin terminaalissa. curl -I näyttää vain http vastausotsakkeet.  

 <img width="940" height="424" alt="image" src="https://github.com/user-attachments/assets/21651c0d-4481-487d-8fb6-5b680d9aa0a2" />
<img width="617" height="316" alt="image" src="https://github.com/user-attachments/assets/808297c7-47d6-478b-ba13-2dfff56c2392" />
<img width="856" height="264" alt="image" src="https://github.com/user-attachments/assets/c9a80727-477c-4e87-b325-19395337f997" /> <br>
 
## m) Vapaaehtoinen: Hanki GitHub Education -paketti.

Minulla on jo GitHub-tunnus. Lisäsin Haaga-Helian sähköpostiosoitteen GitHubiin ja täytin GitHub Education hakemuksen. Hakemus on hyväksytty. 

 <img width="532" height="120" alt="image" src="https://github.com/user-attachments/assets/0d50772d-d106-4475-864b-37dec691001a" />
<img width="739" height="238" alt="image" src="https://github.com/user-attachments/assets/3692893d-cc6b-4e0b-a581-8d5b458a3bdb" /> <br

 
## Lähteet:
Tero Karvinen – Linux-palvelimet: https://terokarvinen.com/linux-palvelimet/ <br>

The Apache Software Foundation 2023: Apache HTTP Server Version 2.4 Documentation: Name-based Virtual Host Support: https://httpd.apache.org/docs/2.4/vhosts/name-based.html <br>

Karvinen 2018: Name Based Virtual Hosts on Apache – Multiple Websites to Single IP Address: https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/  <br>

Karvinen 2012: https://terokarvinen.com/2012/short-html5-page/ <br>

Onko weppisivu validi https://validator.w3.org <br>

Github Education: https://github.com/education 
