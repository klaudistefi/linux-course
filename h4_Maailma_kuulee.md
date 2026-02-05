Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 5.2.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

# h4 Maailma kuulee

# x) Tiivistelmät

## Susanna Lehto 2022: Teoriasta käytäntöön pilvipalvelimen avulla

- Pilvipalvelimen vuokraus ja asennus - Tekstissä kuvataan realistiset ohjeet siitä miten pilvipalvelimen voi vuokrata ja asentaa, missä kohdissa pitää tehdä omaa harkintaa kuten datakeskuksen valinta sijainnin mukaan.<br>
- Palvelin suojaan palomuurilla - Tekstissä näkyy, lyhyt ja ytimekäs kuvaus siitä miten palomuuri asennetaan, miten siihen tehdään reikä porttia varten sekä miten se laitetaan päälle.<br>
- Kotisivut palvelimelle – miten luodaan virtuaalipalvelimeen käyttäjä, Apachen testisivu ja miten avataan julkinen kotisivu. <br>
- Palvelimen ohjelmien päivitys – tämäkin oli lyhyt ja selkeä, millä komennoilla voi asentaa päivitykset sekä tietoturvapäivityksen palvelimelle. <br>

## Karvinen 2017: First Steps on a New Virtual Private Server
- Hyvä vinkki miten voisi hakea pilvipalvelin ja siihen liittyviä ohjeita esim miten voi avata palomuurin. <br>
- Tärkeä muistaa että aina pitää tehdä reikä palomuuriin.<br>

# a) Vuokraa oma virtuaalipalvelin haluamaltasi palveluntarjoajalta

_$ ssh -keygen <br>
$ cd .ssh <br>
$ cat it_ed25519.pub <br>
$ ssh root@185.20.136.42_ <br>

Selitys: Tässä tehtävässä vuokrasin oman virtuaalipalvelimen pilvipalveluntarjoajalta. Upcloud.com. Käyttöjärjestelmäksi Ubuntu. Yhdistin palvelimeen SSH-yhteydellä omalta tietokoneelta käyttäen palvelimen IP-osoitetta.<br>
Polku Upcloud.com ssa - FI HEL1 – CPU 1 core – Memory 1 GB – Storage 10 GB – Debian Linux – SSH key – klaudi2

<img width="940" height="206" alt="image" src="https://github.com/user-attachments/assets/095e2465-6e44-4393-bc4c-76df605c8be4" />
<img width="685" height="438" alt="image" src="https://github.com/user-attachments/assets/08e72904-65bc-441e-9635-14fcfbcc62b5" />
<img width="676" height="63" alt="image" src="https://github.com/user-attachments/assets/fa78b05c-2386-4fcc-8233-a71aec27a091" />
<img width="611" height="253" alt="image" src="https://github.com/user-attachments/assets/6732b8d6-fc4a-417d-a71b-bd9bfc7b0521" />

# b) Tee alkutoimet omalla virtuaalipalvelimellasi: tulimuuri päälle, root-tunnus kiinni, ohjelmien päivitys

_$ ssh root@185.20.136.42_

## Tulimuuri <br>
_#sudo apt install ufw <br>
#sudo ufw allow 22/tcp <br>
#sudo ufw allow 80/tcp <br>
#sudo ufw enable <br>
#sudo ufw status <br>_

<img width="423" height="66" alt="image" src="https://github.com/user-attachments/assets/52360c62-4920-4b3d-82b6-9c54b605790f" />
<img width="419" height="57" alt="image" src="https://github.com/user-attachments/assets/b18d5f2d-81b5-46e6-b343-8e00adb625d9" />
<img width="748" height="102" alt="image" src="https://github.com/user-attachments/assets/4f96c59e-01f9-4490-b5f6-9db4a31df1d2" />
<img width="501" height="135" alt="image" src="https://github.com/user-attachments/assets/51442f51-cf33-4743-9589-10b85e765461" />

## Ohjelmien päivitys

_#sudo apt-get update <br>
#sudo apt-get dist-upgrade <br>
#sudo systemctl reboot_ <br>

<img width="429" height="64" alt="image" src="https://github.com/user-attachments/assets/b6addec4-3e91-4310-8ffa-89abb6051204" />
<img width="469" height="51" alt="image" src="https://github.com/user-attachments/assets/50972b87-d84a-4f74-a390-007b3879c77a" />
<img width="769" height="60" alt="image" src="https://github.com/user-attachments/assets/60d671fc-d6bd-4d7a-b201-cde47c0e7008" /><br>


Selitys: Pääsin UpCloud palvelimelle ssh root@ komennolla. Sitten tein palvelimelle alkutoimet. Otin palomuurin käyttöön. Päivitin myös järjestelmän onnistuneesti. Tarkistin lopuksi, että kaikki palvelut olivat oikeassa tilassa status komennolla.<br>

Root tunnuksen vaihe ei kuitenkaan onnistunut. Ajoin ohjeiden mukaiset komennot, mutta niiden jälkeen koko palvelin jäi jumiin eikä vastannut enää. Tämän vuoksi jouduin luomaan kokonaan uuden palvelimen. Sen jälkeen tein kaikki vaiheet uudelleen alusta asti.

# c) Asenna weppipalvelin omalle virtuaalipalvelimellesi. Korvaa testisivu. Kokeile, että se näkyy julkisesti

_$ssh root@185.20.136.42 <br>
#sudo apt-get install apache2 <br>
#echo “Klaudi weppi on nyt…tässä?” | sudo tee /var/www/html/index.html_ <br>

<img width="617" height="76" alt="image" src="https://github.com/user-attachments/assets/9cf018ca-a298-48c0-9cc8-ba91c8878dc1" />
<img width="744" height="379" alt="image" src="https://github.com/user-attachments/assets/299cbb99-3fd3-42bf-b98b-3aa1ec87672f" />
<img width="853" height="54" alt="image" src="https://github.com/user-attachments/assets/dcdf526e-1b6f-46c8-b0a3-af0b86b80452" />
<img width="701" height="81" alt="image" src="https://github.com/user-attachments/assets/fc62604e-9c40-4588-b822-724893e4f4b6" />

Selitys: Asensin palvelimelle Apache verkkopalvelimen, jotta voin julkaista verkkosivu. Sitten muokkasin Apachen oletussivua ja korvasin sen omalla tekstila komennolla echo “Klaudi weppi on nyt… tässä?” | sudo tee /var/www/html/index.html.
Testasin, että sivusto toimii oikein. Kirjoitin palvelimen IP osoitteen 185.20.136.42 selaimeen. Sivu avautui ja toimi.


# LÄHTEET:

- Karvinen 2012: First Steps on a New Virtual Private Server – an Example on DigitalOcean and Ubuntu 16.04 LTS https://terokarvinen.com/2017/first-steps-on-a-new-virtual-private-server-an-example-on-digitalocean/ <br>
- Susanna Lehto 2022: Teoriasta käytäntöön pilvipalvelimen avulla (h4) (opiskelijan esimerkkiraportti), kohdat https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/ <br>
- Tero Karvinen – Linux-palvelimet: https://terokarvinen.com/linux-palvelimet/ <br>



