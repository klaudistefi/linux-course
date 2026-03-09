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

