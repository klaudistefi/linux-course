Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 24.1 - 25.1.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

## x) Tiivistelmät

Tässä tehtävässä perehdyin Linuxin komentorivin peruskäyttöön. Komentorivin käyttö tuntui aluksi haastavalta ja myös lopussa se oli vielä haastavaa, mutta ymmärrys parani vähän harjoittelun aikana.

Käytetty Linux Debian 64 bit.

## a) Micro. Asenna micro-editori.

Käytetty komento: _sudo apt install micro_

Käytetty komento: _micro test.txt_

Selitys: Asennin Micro-editori. Tämän jälkeen micro käynnistettiin komentoriviltä ja tiedosto test.txt avattiin muokattavaksi. Micro on kevyt tekstieditori, jota käytetään suoraan terminaalissa.

<img width="405" height="317" alt="image" src="https://github.com/user-attachments/assets/80f695b1-12ab-4988-9436-59350237dd5b" />
<img width="380" height="383" alt="image" src="https://github.com/user-attachments/assets/dab01838-b953-4281-a5ed-da7afd8f577b" />

## b) Asenna kolme itsellesi uutta komentoriviohjelmaa.

Ensin asensin kolme uutta komentoriviohjelmaa komennolla: _sudo apt-get install s-tui git tree_

**- s-tui - Se on suorittimen (CPU) valvontaohjelma.**

Selitys: Käynnistin ohjelman terminaalista, ja se näytti reaaliaikaisesti suorittimen käytön, taajuuden ja lämpötilan.

<img width="643" height="368" alt="image" src="https://github.com/user-attachments/assets/7dcbe8c1-fc7b-4aa6-a7b1-5f7fc31329df" /> <br> <br>

**- Git - Versiohallintajärjestelmä.**

Selitys: Käytetään tiedostomuutosten seuraamiseen sekä projektien ja koodin hallintaan. 

Käytetty komento: _git init_

<img width="394" height="151" alt="image" src="https://github.com/user-attachments/assets/7ea05cd4-c822-4c8a-842a-0274dba06d11" />

Käytetty komento: _git status_

<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/0dc26e8e-0713-4eb9-ac35-085b659aaa48" /> <br> <br>

-**Tree - näyttää hakemistorakenteen "puunäkymässä".**

Käytetty komento: _tree_

Selitys: Käytin sitä  ja tarkislenin kotihakemiston kansiorakennetta. Komento auttoi hahmottamaan kansioiden rakenteen selkeämmin.

<img width="168" height="250" alt="image" src="https://github.com/user-attachments/assets/cf955f90-101f-46ea-8d40-271fa1fd283e" />

## c) FHS

-**/ - Linux juurihakemisto**

Käytetty komento: _ls /_

Selitys: Juurihakemisto on Linux-järjestelmän ylin taso, ja kaikki muut hakemistot sijaitsevat sen alla.

Luettelo kansioista: 

<img width="460" height="47" alt="image" src="https://github.com/user-attachments/assets/b1c81f44-ec77-4604-a2dd-986cd0a5963e" /> <br>

- **/home/ - sisältää kaikkien käyttäjien kotihakemistot**

Käytetty komento: _ls /home_

Selitys: Näen käyttäjätunnuksesi.

<img width="181" height="38" alt="image" src="https://github.com/user-attachments/assets/59fa29e8-4133-492b-b2ae-1b15c0165d99" /> <br>

- **/home/klaudija/ - henkilökohtainen kansio**

Käytetty komento: _ls /home/klaudija_

Selitys: henkilökohtainen kansio omille tiedostoille.

<img width="564" height="41" alt="image" src="https://github.com/user-attachments/assets/1a4b6774-67ea-4be6-93f4-c6c831dc85df" /> <br>

**- /etc/ -	sisältää järjestelmän asetustiedostot**

Käytetty komento: _ls /etc_

Selitys: simerkiksi tiedosto passwd sisältää käyttäjätietoja.

<img width="630" height="305" alt="image" src="https://github.com/user-attachments/assets/24e4dc4f-8ab1-4686-9963-0b17dcdb1267" /> <br>

**/media/ - käytetään irrotettavien laitteiden**

Käytetty komento: _ls /media_

Selitys: käytetään irrotettavien laitteiden, kuten USB-muistien.

<img width="197" height="34" alt="image" src="https://github.com/user-attachments/assets/a93d6c2b-3816-4e19-b0d8-b5208308ce88" /> <br>

**/var/log/ - sisältää järjestelmän log tiedostot**

Käytetty komento: _ls /var/log/_

Selitys: sisältää järjestelmän log tiedostot.

<img width="533" height="44" alt="image" src="https://github.com/user-attachments/assets/26fa9c2d-0bb6-4205-8886-c5a1129da8c4" /> <br>

## d) The Friendly M

Mitä on grep? grep on komentorivityökalu, jolla etsitään tekstiä tiedostoista tai komentojen tulosteista.

**1. ls /etc | grep net**<br>
Käytetty komento: _ls /etc | grep net_  <br>
Selitys: Tämä komento näyttää vain ne /etc-hakemiston tiedostot, joissa on sana net.

<img width="196" height="59" alt="image" src="https://github.com/user-attachments/assets/5af8a78e-fdff-4d3a-9a51-9bb92af271a4" /> <br>

**3. grep -F**<br>
Käytetty komento: _grep -F_ <br>
Selitys: 

<img width="203" height="29" alt="image" src="https://github.com/user-attachments/assets/c8159280-9c44-4313-95b3-53ac74c230ec" /> <br>

**3. grep --help**<br>
Käytetty komento: _grep --help_ <br>
Selitys: Tällä komennolla sain lisätietoa grep-komennon käytöstä.

<img width="392" height="332" alt="image" src="https://github.com/user-attachments/assets/9450b466-66a0-4ad9-b36a-f4c693d5ecd1" />

## e) Pipe
Esimerkki putkista (pipes, "|").

Käytetty komento: _journalctl | grep error_ <br>
Selitys: Tässä komennossa järjestelmän lokit ohjataan grep ille, joka etsii virheilmoituksia.

<img width="631" height="341" alt="image" src="https://github.com/user-attachments/assets/f9ccb6b4-0ee5-476c-9376-89d6bf871810" />

## f) Rauta
Asensin **lshw** komennolla _sudo apt install lshw_.
Sen jälkeen suoritin: _run a sudo lshw -short -sanitize_

Selitys: Tämä komento näyttää koneen tärkeimmät laitteet selkeässä taulukkomuodossa.

Tässä on lista mitä tuli esille.

<img width="459" height="284" alt="image" src="https://github.com/user-attachments/assets/b9a3e020-79ce-447c-bf4d-c4b91fcd1d1a" />

## Lähteet: 
Tero Karvinen – Linux-palvelimet: https://terokarvinen.com/linux-palvelimet/
