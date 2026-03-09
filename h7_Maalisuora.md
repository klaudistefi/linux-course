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

