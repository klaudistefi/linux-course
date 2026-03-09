Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 03.-09.2.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>
# h7 Maalisuora
Koko tehtävän olen suorittanut pikku hiljaa joka päivä, oli välillä tosi haastava, mutta samalla mielenkiintoinen.
Eritäin vaikea oli osa 3 “Ratkaise vanha arvioitava laboratorioharjoitus soveltuvin osin”. Jouduin käyttämään siihen paljon aikaa, miten ongelmat pitäisi ratkaista. Tutustuin myös vähän PHPn, se oli minulle uusi asia. 
Mutta törmäsin kuitenkin yhteen ongelmaan, johon en löytänyt ratkaisua. Yritin etsiä tietoa ja testata eri tapoja, mutta en onnistunut ratkaisemaan sitä. Muut tehtävän osat kuitenkin onnistuivat.
Kohdat “Kirjoita ja aja Hei maailma kolmella kielellä” ja “Linuxiin uusi, itse tekemäsi komento niin, että kaikki käyttäjät voivat ajaa sitä” olivat helpompia suorittaa. 

## 1) Kirjoita ja aja "Hei maailma" kolmella kielellä
Käytiin  kolmea ohjelmointikieltä Bash, Python ja C. Jokaisella kielellä kirjoitin, jonka muotoinen ”Hello World” teksti ja ajoin sen.
### Python kieli
Loin uuden Python tiedoston snake.py komennolla ``` micro snake.py ```. Tämä komento avaa Micro editorin, sitten kirjoitin sinne ```#!/usr/bin/python3 
print (”Hello World”)```.
Selitys: # alussa kertoo käyttöjärjestelmälle, että tiedosto suoritetaan Pythonilla.
Komento print("Hello World") tulostaa tekstin. Tallensin tiedoston ```Ctrl + S``` ja poistuin ```Ctrl + Q```.
Komennolla ```chmod ugo+x snake.py ``` annoin tiedostolle suoritusoikeudet.
Ajoin ohjelma komennolla ```./nake.py ```. Se tulosti tekstin “Hello World”.

Komennot:
```$micro snake.py```
```$chmod ugo+x snake.py```
```$./nake.py```

<img width="639" height="217" alt="image" src="https://github.com/user-attachments/assets/305b10fd-c795-462a-8645-b982ce6fabfb" />

<img width="726" height="150" alt="image" src="https://github.com/user-attachments/assets/4886d4ab-a942-4643-82c4-bda74a62de2a" />
<img width="726" height="72" alt="image" src="https://github.com/user-attachments/assets/6769bc9f-dd7c-4dc8-b4c4-01f0ce72ec08" />

### C kieli
Loin uuden kansion clang komennolla ```mkdir clang```. Sitten siirryin kansioon komennolla ```cd clang/```. Loin uuden C tiedoston komennolla ```micro helpc.c```. Kirjoitiin Micro tekstieditorin ```#include ¬<stdio.h> int main () { printf (”Hello Klaudis\n”); return 0; }```. Tallensin tiedoston ja poistuin terminaalille.
Selitys: ”printf("Hello Klaudis\n");” tulostaa tekstin. \n tekee rivinvaihdon. return 0; kohta kertoo, että ohjelma päättyi ilman virheitä.
Komento ```sudo apt install gcc``` asentaa GCC kääntäjän. Komento ``` gcc helpc.c ``` muuttaa koodin semmoiseksi, että sitä voi suorita. ”Kääntämisen” jälkeen ajonut ohjelma komennolla  ```./a.out```. Se tulosti tekstin “Hello Klaudis”.
Komennot:
```$mkdir clang```
```$cd clang/```
```$sudo apt install gcc```
```$micro helpc.c```
```$gcc helpc.c```
```$ls -l```
```$./a.out```

<img width="940" height="149" alt="image" src="https://github.com/user-attachments/assets/762da4a9-1c53-42b3-8343-ab20f55c76ee" />
<img width="814" height="288" alt="image" src="https://github.com/user-attachments/assets/8215219b-5cd7-4a4d-bf78-e05839ae4456" />
<img width="940" height="264" alt="image" src="https://github.com/user-attachments/assets/91d5e6cc-4edd-44b6-af2d-33e150f03942" />

###  Bash kieli
Tein bash skriptin komennolla ```nano helloworld.sh```. Se loi uuden tiedoston ja kirjoitin sinne ```echo ”Hello World Klaudis”```. Tallensin tiedoston ja poistuin terminaalille.
Bash skriptit toimivat Linuxissa valmiiksi. Ajoin  ```bash hellowordls.sh``` ja se tulosti tekstin “Hello World Klaudis”.

Komennot:
```$nano hellowordls.sh```
```$bash hellowordls.sh```

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/b58b1e18-e42c-4123-8d69-e80bcd494f66" />

<img width="940" height="73" alt="image" src="https://github.com/user-attachments/assets/f4888ca5-1202-4e19-861e-080f4a4a8494" />

<img width="900" height="134" alt="image" src="https://github.com/user-attachments/assets/01521b45-70b9-4964-a9ca-be93df5a1074" />


## 2) Linuxiin uusi, itse tekemäsi komento niin, että kaikki käyttäjät voivat ajaa sitä

Aloitin luomalla uuden kansion komennolla ```mkdir bin```, sitten siirryin kansioon ja loin uuden skriptin komennolla ```micro newkomment.sh``` ja teksti ```#!/bin/bash
echo “Now is the worlds moment $(date)” ```.
Selitys: #!/bin/bash kommunikoi jestelmälle, että skripti suoritetaan Bashlla. $(date) hakee järjestelmästä nykyisen päivämäärän ja kellonajan.
Testasin skriptiä komennolla ```bash newkomment.sh```. Komennoilla ```$chmod ugo+x /home/klaudija/bin/newkomment.sh``` annoin tiedostolle suoritusoikeudet, jotta kaiki käyttäjiät voivat suorittaa sitä. 
Komennoilla ```sudo cp newkomment.sh /user/local/bin``` kopioin skriptin kansioon /usr/local/bin, jota kaikki käyttäjät voivat käyttää sitä. 
Tarkistin että se toimi mistä vaan kansiosta.

Komennot:
```$mkdir bin```
```$cd bin/```
```$micro newkomment.sh```
```$bash newkomment.sh```
```$ls -l ```
```$chmod ugo+x /home/klaudija/bin/newkomment.sh```
```$ls -l```
```$sudo cp newkomment.sh /user/local/bin```
```$ newkomment.sh```


<img width="910" height="134" alt="image" src="https://github.com/user-attachments/assets/0b7ba0a8-ec1c-415d-99e1-4fbc27b14e60" />
<img width="910" height="127" alt="image" src="https://github.com/user-attachments/assets/dab76647-d67c-4196-80d9-6ca8e57c8dd3" />
<img width="775" height="68" alt="image" src="https://github.com/user-attachments/assets/76efac18-f3df-4581-9855-73ca81dc29e5" />
<img width="940" height="87" alt="image" src="https://github.com/user-attachments/assets/da5caed5-5012-4d50-a3e4-1b90719dff00" />
<img width="885" height="319" alt="image" src="https://github.com/user-attachments/assets/b962488f-f3e4-4af6-ba9f-3b96f282aafc" />

## 3) Ratkaise vanha arvioitava laboratorioharjoitus soveltuvin osin

Arvioitava tehtävä, jonka päätin tehdä, on Arvioitava laboratorioharjoitus – Linux palvelimet ict4tn021-2 (uusi OPS) alkukeväällä 2017 p1.
Miksi tämä tehtävä? Koska ajattelin että se oli ”helpoin” ymmärtää, mutta myös vähän haastava. Sekä se olisi testannut minun osaamisia. Seurasin tarkkaa järjestystä, jotta en sekoittanut eikä rikkonut mitään.

### Tässä tehtävässä piti tehdä

Asentaa Apache, PHP ja MariaDB
Luoda kaikki käyttäjät
Tehdä HTML sivut
Luoda sudo käyttäjä Maija
Tehdä tietokanta Pekalle
Konfiguroida sleep.example.com
Asettaa palomuuri
Luoda komento kaikille – wowstats


### Asenna Apache, PHP ja MariaDB 
Ensin päivitin järjestelmän komennolla ```sudo apt update```. Apache oli jo asennettu. Tarkistin kuitenkin komennolla ```systemctl status apache2``` (Mutta jos Apache olisi pitänyt asentaa käytäisi komento ```sudo apt-get install apache2```).
Asensin PHPn komennolla ```sudo apt-get install php libapache2-mod-php```  ja tarkistin asennus komennolla ```php -v```.

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/31e83caa-d942-4850-ae58-58dc4a32c92e" />
<img width="940" height="151" alt="image" src="https://github.com/user-attachments/assets/ff347e1d-66ea-49a2-aa13-6f05d19dc96c" />

Nyt pitäisi asentaa tietokannan. Asensin MariaDB tietokannan komennolla ```sudo apt-get install mariadb-server```. Tarkistin, että se toimi komennolla ```sudo systemctl status mariadb```. Loin kansion ```mkdir labra```.

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/2cb0edfc-9f5c-4613-8d1f-d377885ca300" />
<img width="637" height="149" alt="image" src="https://github.com/user-attachments/assets/f74ed7fe-2bb8-4d0e-9b81-3a0f265ad7bc" />



