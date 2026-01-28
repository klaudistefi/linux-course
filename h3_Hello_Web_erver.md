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

 ## c) Etusivu uusiksi. Uusi name based virtual host. 

Luon kansion ja uuden html tiedoston:

**Käytetty komento:**

1. mkdir ~/hattu.example.com <br>
2. nano ~/hattu.example.com/index.html <br>
3. sudo nano /etc/apache2/sites-available/hattu.example.com.conf <br>
  

**Vanhan sivuston poisto ja uuden käyttöönotto:**

**Käytetty komento:**

1. sudo a2dissite klaudija.conf <br>
2. sudo a2ensite hattu.example.com.conf <br>
3. sudo systemctl reload apache2 <br>
 
Ilmoitetaan järjestelmälle, että hattu.example.com on uusi localhost:

Se ei mennyt ihan helposti, pitänyt säätää vähän sen jälkeen ennen kuin tajusin, että ongelma oli hattu.example.com config. Kun korjasin sen localhost muuttui. 
 
**Selitys:** Loin uusi name based virtual host nimellä hattu.example.com. Vanhan ”oletussivusto” poistin käytöstä ja otin uuden sivuston käyttöön. Aluksi sivu ei toiminut, koska virtual host asetuksissa oli virhe. Kun asetukset korjattiin ja localhost määritettiin oikein, sivu alkoi toimia.

## e) Tee validi HTML5 sivu.
**Selitys:** Tein etusivu HTML5 standardin mukaisesti. Sivulla on otsikko, teksti ja oikea HTML rakenne. Sivun koodin validoin HTML validaattorilla. Validaattori ehdotti lang attribuutin lisäämistä HTML tagiin kielen määrittämiseksi.
 
 
## f) Anna esimerkit 'curl -I' ja 'curl' -komennoista. Selitä 'curl -I' muutamasta näyttämästä otsakkeesta (response header), mitä ne tarkoittavat.
Käytetty komento:
1. sudo apt update
2. sudo apt install curl
3. curl http://localhost
4. curl -I http://localhost
Selitys: Ensin asensin curl. Sitten  - Curl komento hakee sivun sisällön ja näyttää HTML koodin terminaalissa. curl -I näyttää vain http vastausotsakkeet. 
 
 
 
m) Vapaaehtoinen: Hanki GitHub Education -paketti.
Minulla on jo GitHub-tunnus. Lisäsin Haaga-Helian sähköpostiosoitteen GitHubiin ja täytin GitHub Education hakemuksen. Hakemus on hyväksytty.
 
 
 
Lähteet:
Tero Karvinen – Linux-palvelimet: https://terokarvinen.com/linux-palvelimet/
The Apache Software Foundation 2023: Apache HTTP Server Version 2.4 Documentation: Name-based Virtual Host Support: https://httpd.apache.org/docs/2.4/vhosts/name-based.html 
Karvinen 2018: Name Based Virtual Hosts on Apache – Multiple Websites to Single IP Address: https://terokarvinen.com/2018/04/10/name-based-virtual-hosts-on-apache-multiple-websites-to-single-ip-address/ 
Karvinen 2012: https://terokarvinen.com/2012/short-html5-page/ 
Onko weppisivu validi https://validator.w3.org
Github Education: https://github.com/education 
