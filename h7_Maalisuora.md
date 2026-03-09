Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 03.-09.2.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

# h7 Maalisuora

Koko tehtävän olen suorittanut pikku hiljaa joka päivä, oli välillä tosi haastava, mutta samalla mielenkiintoista.

Erittäin vaikeaa oli osa 3 “Ratkaise vanha arvioitava laboratorioharjoitus soveltuvin osin”. Jouduin käyttämään siihen paljon aikaa, miten ongelmat pitäisi ratkaista. Tutustuin myös vähän PHPn, se oli minulle uusi asia. 

Mutta törmäsin kuitenkin yhteen ongelmaan, johon en löytänyt ratkaisua. Yritin etsiä tietoa ja testata eri tapoja, mutta en onnistunut ratkaisemaan sitä. Muut tehtävän osat kuitenkin onnistuivat.

Kohdat “Kirjoita ja aja Hei maailma kolmella kielellä” ja “Linuxiin uusi, itse tekemäsi komento niin, että kaikki käyttäjät voivat ajaa sitä” olivat helpompia suorittaa. 


## 1) Kirjoita ja aja "Hei maailma" kolmella kielellä

Käytiin  kolmea ohjelmointikieltä Bash, Python ja C. Jokaisella kielellä kirjoitin, jonka muotoinen ”Hello World” teksti ja ajoin sen.

### Python kieli

Loin uuden Python tiedoston snake.py komennolla ``` micro snake.py ```. Tämä komento avaa Micro editorin, sitten kirjoitin sinne ```#!/usr/bin/python3 print (”Hello World”)```.

Selitys: # alussa kertoo käyttöjärjestelmälle, että tiedosto suoritetaan Pythonilla.

Komento print("Hello World") tulostaa tekstin. Tallensin tiedoston ```Ctrl + S``` ja poistuin ```Ctrl + Q```.

Komennolla ```chmod ugo+x snake.py ``` annoin tiedostolle suoritusoikeudet.

Ajoin ohjelma komennolla ```./nake.py ```. Se tulosti tekstin “Hello World”.

Komennot:<br>
```$micro snake.py```<br>
```$chmod ugo+x snake.py```<br>
```$./nake.py```<br>

<img width="639" height="217" alt="image" src="https://github.com/user-attachments/assets/305b10fd-c795-462a-8645-b982ce6fabfb" />

<img width="726" height="150" alt="image" src="https://github.com/user-attachments/assets/4886d4ab-a942-4643-82c4-bda74a62de2a" />
<img width="726" height="72" alt="image" src="https://github.com/user-attachments/assets/6769bc9f-dd7c-4dc8-b4c4-01f0ce72ec08" />

### C kieli

Loin uuden kansion clang komennolla ```mkdir clang```. Sitten siirryin kansioon komennolla ```cd clang/```. Loin uuden C tiedoston komennolla ```micro helpc.c```. Kirjoitiin Micro tekstieditorin ```#include ¬<stdio.h> int main () { printf (”Hello Klaudis\n”); return 0; }```. Tallensin tiedoston ja poistuin terminaalille.

Selitys: ”printf("Hello Klaudis\n");” tulostaa tekstin. \n tekee rivinvaihdon. return 0; kohta kertoo, että ohjelma päättyi ilman virheitä.

Komento ```sudo apt install gcc``` asentaa GCC kääntäjän. Komento ``` gcc helpc.c ``` muuttaa koodin semmoiseksi, että sitä voi suorittaa. ”Kääntämisen” jälkeen ajoin ohjelman komennolla  ```./a.out```. Se tulosti tekstin “Hello Klaudis”.


Komennot:<br>
```$mkdir clang```<br>
```$cd clang/```<br>
```$sudo apt install gcc```<br>
```$micro helpc.c```<br>
```$gcc helpc.c```<br>
```$ls -l```<br>
```$./a.out```<br>

<img width="940" height="149" alt="image" src="https://github.com/user-attachments/assets/762da4a9-1c53-42b3-8343-ab20f55c76ee" />
<img width="814" height="288" alt="image" src="https://github.com/user-attachments/assets/8215219b-5cd7-4a4d-bf78-e05839ae4456" />
<img width="940" height="264" alt="image" src="https://github.com/user-attachments/assets/91d5e6cc-4edd-44b6-af2d-33e150f03942" />

###  Bash kieli

Tein bash skriptin komennolla ```nano helloworld.sh```. Se loi uuden tiedoston ja kirjoitin sinne ```echo ”Hello World Klaudis”```. Tallensin tiedoston ja poistuin terminaalille.

Bash skriptit toimivat Linuxissa valmiiksi. Ajoin  ```bash hellowordls.sh``` ja se tulosti tekstin “Hello World Klaudis”.


Komennot:<br>
```$nano hellowordls.sh```<br>
```$bash hellowordls.sh```<br>

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/b58b1e18-e42c-4123-8d69-e80bcd494f66" />

<img width="940" height="73" alt="image" src="https://github.com/user-attachments/assets/f4888ca5-1202-4e19-861e-080f4a4a8494" />

<img width="900" height="134" alt="image" src="https://github.com/user-attachments/assets/01521b45-70b9-4964-a9ca-be93df5a1074" />


## 2) Linuxiin uusi, itse tekemäsi komento niin, että kaikki käyttäjät voivat ajaa sitä

Aloitin luomalla uuden kansion komennolla ```mkdir bin```, sitten siirryin kansioon ja loin uuden skriptin komennolla ```micro newkomment.sh``` ja teksti ```#!/bin/bash echo “Now is the worlds moment $(date)” ```.

Selitys: #!/bin/bash kommunikoi järjestelmälle, että skripti suoritetaan Bashlla. $(date) hakee järjestelmästä nykyisen päivämäärän ja kellonajan.

Testasin skriptiä komennolla ```bash newkomment.sh```. Komennoilla ```$chmod ugo+x /home/klaudija/bin/newkomment.sh``` annoin tiedostolle suoritusoikeudet, jotta kaikki käyttäjät voivat suorittaa sitä. 

Komennoilla ```sudo cp newkomment.sh /user/local/bin``` kopioin skriptin kansioon /usr/local/bin, jota kaikki käyttäjät voivat käyttää sitä. 

Tarkistin että se toimi mistä vaan kansiosta.

Komennot:<br>
```$mkdir bin```<br>
```$cd bin/```<br>
```$micro newkomment.sh```<br>
```$bash newkomment.sh```<br>
```$ls -l ```<br>
```$chmod ugo+x /home/klaudija/bin/newkomment.sh```<br>
```$ls -l```<br>
```$sudo cp newkomment.sh /user/local/bin```<br>
```$ newkomment.sh```<br>


<img width="910" height="134" alt="image" src="https://github.com/user-attachments/assets/0b7ba0a8-ec1c-415d-99e1-4fbc27b14e60" />
<img width="910" height="127" alt="image" src="https://github.com/user-attachments/assets/dab76647-d67c-4196-80d9-6ca8e57c8dd3" />
<img width="775" height="68" alt="image" src="https://github.com/user-attachments/assets/76efac18-f3df-4581-9855-73ca81dc29e5" />
<img width="940" height="87" alt="image" src="https://github.com/user-attachments/assets/da5caed5-5012-4d50-a3e4-1b90719dff00" />
<img width="885" height="319" alt="image" src="https://github.com/user-attachments/assets/b962488f-f3e4-4af6-ba9f-3b96f282aafc" />

## 3) Ratkaise vanha arvioitava laboratorioharjoitus soveltuvin osin

Arvioitava tehtävä, jonka päätin tehdä, on Arvioitava laboratorioharjoitus – Linux palvelimet ict4tn021-2 (uusi OPS) alkukeväällä 2017 p1.(linkki alhaalla)

Miksi tämä tehtävä? Koska ajattelin että se oli ”helpoin” ymmärtää, mutta myös vähän haastava. Sekä se olisi testannut minun osaamisia. Seurasin tarkkaa järjestystä, jotta en sekoittanut enkä rikkonut mitään.


### Tässä tehtävässä piti tehdä

- Asentaa Apache, PHP ja MariaDB
- Luoda kaikki käyttäjät
- Tehdä HTML sivut
- Luoda sudo käyttäjä Maija
- Tehdä tietokanta Pekalle
- Konfiguroida sleep.example.com
- Asettaa palomuuri
- Luoda komento kaikille – wowstats


### Asenna Apache, PHP ja MariaDB 

Ensin päivitin järjestelmän komennolla ```sudo apt update```. Apache oli jo asennettu. Tarkistin kuitenkin komennolla ```systemctl status apache2``` (Mutta jos Apache olisi pitänyt asentaa käytäisi komento ```sudo apt-get install apache2```).

Asensin PHPn komennolla ```sudo apt-get install php libapache2-mod-php```  ja tarkistin asennus komennolla ```php -v```.

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/31e83caa-d942-4850-ae58-58dc4a32c92e" />
<img width="940" height="151" alt="image" src="https://github.com/user-attachments/assets/ff347e1d-66ea-49a2-aa13-6f05d19dc96c" />

Nyt pitäisi asentaa tietokannan. Asensin MariaDB tietokannan komennolla ```sudo apt-get install mariadb-server```. Tarkistin, että se toimi komennolla ```sudo systemctl status mariadb```. Loin kansion ```mkdir labra```.

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/2cb0edfc-9f5c-4613-8d1f-d377885ca300" />
<img width="637" height="149" alt="image" src="https://github.com/user-attachments/assets/f74ed7fe-2bb8-4d0e-9b81-3a0f265ad7bc" />

### Luo käyttäjät

Loin työntekijöiden käyttäjät komennolla ```adduser jorma```, ``` adduser pekka```, ``` adduser ronaldo```, ``` adduser hakan```, ``` adduser einar```, ``` adduser einari``` ja ``` adduser eija```. Koko nimet ovat Jorma Mähkylä, Pekka Hurme, Ronaldo Smith, Håkan Petersson, Einari Mikkonen, Einari Vähäkäähkä, Eija Vähäkäähkä. Tarkistin kotihakemistot komennolla ```ls /home```. Käyttäjät  löytyvät.

<img width="940" height="285" alt="image" src="https://github.com/user-attachments/assets/e44c2722-a82a-426a-8a7d-fe87caa088a6" />
<img width="940" height="259" alt="image" src="https://github.com/user-attachments/assets/2eadc838-f2e7-48e3-9a10-5876838f899e" />
<img width="441" height="194" alt="image" src="https://github.com/user-attachments/assets/d7699f17-d263-4c26-bd32-13952b91a75c" />

<img width="940" height="57" alt="image" src="https://github.com/user-attachments/assets/b390d786-6af9-462f-b1c4-3a30a00b6f26" />


### Tee HTML sivut

Siirryin kansioon komennoilla ```cd /var/www/html```. Loin jokaiselle käyttäjälle oman sivun komennolla ```sudo nano jorma.html```.

<!DOCTYPE html>
<html lang=”fi”>
<head>
<meta charset=”UTF-8”>
<title>Jorma</title>
</head>
<body>
<h1>Jorma Mähkylä testisivu</h1>
</body>
</html>


Testasin selaimessa, mutta sivu ei toiminut. Alkoi prosessi selvitä mitä ei ole oikean. Komennolla ```sudo systemctl retart apache2``` restarttasin Apachen. Ei auttanut.  Tarkistin ```ls```  komennolla, että sivu on oikeassa kansiossa, se oli. 

<img width="940" height="421" alt="image" src="https://github.com/user-attachments/assets/e27d3525-8156-4548-af75-baa11088d926" />
<img width="940" height="179" alt="image" src="https://github.com/user-attachments/assets/dc8aab10-0154-40d5-8c74-7caeb27c9cfd" />

Selvitin oikean kansion komennolla ```sudo grep -R DocumentRoot /etc/apache2```. Oikea kansio löytyi polulla ```/etc/apache2/sites-enabled/hattu.example.com.conf``` ja DocumentRoot on ```/home/klaudija/hattu.example.com/```. Se on jäänyt näin toisesta tehtävästä ja ajattelin jatka vain siellä.

Siirsin tiedoston komennolla ```cd /home/klaudija/hattu.example.com``` sinne ja loin uuden jorma.html sivun. Alkoi toimimaan ja jatkanut luoman seuraavat sivut. 


Testasin sivut selaimessa http://localhost/jorma.html, http://localhost/pekka.html, http://localhost/ronaldo.html, http://localhost/hakan.html, http://localhost/einar.html, http://localhost/einari.html ja http://localhost/eija.html. Sivut toimivat oikein. Jokaisella sivulla on otsikossa oma nimi.

<img width="940" height="92" alt="image" src="https://github.com/user-attachments/assets/dfe11b9a-5200-4d5e-af07-b839f964a2bd" />
<img width="940" height="218" alt="image" src="https://github.com/user-attachments/assets/f7933b0e-94b7-4dfc-9a22-40232959682b" />
<img width="940" height="242" alt="image" src="https://github.com/user-attachments/assets/303d132d-dcfa-4c38-806a-5d5cf9639a0b" />
<img width="940" height="260" alt="image" src="https://github.com/user-attachments/assets/d76691ab-c167-4646-a47f-07f129f76a2c" />
<img width="940" height="274" alt="image" src="https://github.com/user-attachments/assets/82eb2044-e944-4ac5-80a7-f813688486b4" />
<img width="940" height="259" alt="image" src="https://github.com/user-attachments/assets/5231ee0c-253d-4821-8a5c-8ba044661aeb" />
<img width="940" height="243" alt="image" src="https://github.com/user-attachments/assets/8a4de7ad-311f-4e74-9916-98c6f05bc05b" />
<img width="940" height="256" alt="image" src="https://github.com/user-attachments/assets/1070174e-cc1d-413f-8612-5e42e87d5a42" />
<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/7daf686b-2b53-4c0e-be5a-18d52273d80c" />
<img width="940" height="130" alt="image" src="https://github.com/user-attachments/assets/e7ca9440-5dee-4dc2-a2da-ace3da803cab" />
<img width="940" height="37" alt="image" src="https://github.com/user-attachments/assets/bdbb4b60-bc5b-467a-b38d-8b4d60692820" />

### Luo sudo käyttäjä Maija

Seuraava vaihe on luoda käyttäjän Maija. Tein sitä komennolla sudo adduser maija. Sitten pitänyt antaa hänelle sudo ryhmään komennolla sudo usermod -a -G sudo maija. Tarkistin ryhmät komennolla groups maija. Maija voi nyt käyttää sudo komentoja.



<img width="940" height="363" alt="image" src="https://github.com/user-attachments/assets/a7c9139a-f521-4ce4-8a0d-008a0f81ee29" />

### Tee tietokanta Pekalle

Siirryin MariaDB tietokanan sisälle komennolla sudo mysql. Loin Pekalle oman tietokannan nimeltä pekka_db komennolla CREATE DATABASE pekka_db;
Komennolla USE pekka_db; loin taulukko:
CREATE TABLE pekkatest (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(50)
);
Lisäsin yhden rivin INSERT INTO pekkatest (name) VALUES ('Hei, Pekka sano Hei tietokannalle');. Sitten testasin, että se meni okien komennolla SELECT * FROM pekkatest;. Sitten exit;. Toimi oikein. 

<img width="940" height="229" alt="image" src="https://github.com/user-attachments/assets/ef0f2688-ff73-4878-88bd-09da0bca6a1a" />
<img width="940" height="176" alt="image" src="https://github.com/user-attachments/assets/375fe7cd-a3d8-4433-830d-8d4f61775d8e" />



Seuraava vaihe on luoda PHP Pekka sivu. Komennolla nano pekka.php.

<img width="940" height="38" alt="image" src="https://github.com/user-attachments/assets/0fd5592e-b0e2-45f6-a04e-4273b6d44bf5" />

<?php
$db = mysqli_connect("localhost", "root", "", "pekka_db");
$result = mysqli_query($db, "SELECT name FROM pekkatest");
$row = mysqli_fetch_assoc($result);
echo $row['name'];
?> 

<img width="940" height="283" alt="image" src="https://github.com/user-attachments/assets/045daeb5-85c8-4468-9dc3-351b28eb1dab" />


Loin PHP sivun, joka hakee tiedot tietokannasta. Testasin sivun selaimessa osoitteessa http://localhost/pekka.php. Mutta sivu ei toimi, ajanut komento sudo apt-get install php-mysql. Ei aitonut.  Ajanut komento sudo tail /var/log/apache2/error.log. Virhe on line 6. Korjasin php teksti. Ei aitonut.  Ajanut taas sudo tail /var/log/apache2/error.log. Virhe oli line 8. Korjasin php teksti. Ei aitonut. 

<img width="940" height="512" alt="image" src="https://github.com/user-attachments/assets/7203144f-7e3a-44be-8e9d-e2ebe3ab022c" />

<img width="856" height="18" alt="image" src="https://github.com/user-attachments/assets/c4e876d5-2a7a-4420-9429-46b074a1b426" />

Ajanut taas sudo tail /var/log/apache2/error.log. Nyt virhe on seuraava kuvassa:
<img width="940" height="46" alt="image" src="https://github.com/user-attachments/assets/40d7337f-f5a7-4683-9de9-a71f6658d267" />


Tämän jälkeen olen ajanut erilaisia komento kombinaatioita kuten sudo systemctl restart apache2, sudo apt install php-mysql jne.
Yrittänyt muuttua pekka.php teksti monta kerta, mutta silti ei mennyt läpi. Silti se ei ilmestynyt selaimessa. Päätin jätä tämän välin, kun itse ei ole niin teetollinen PHPsta ja miten se toimi. 

<img width="940" height="389" alt="image" src="https://github.com/user-attachments/assets/40ea6bd2-54e2-4e40-978f-5a9825354181" />


### Konfiguroi sleep.example.com 

Avasin host tiedosto sudo nano /etc/hosts ja lisäsin hosts sinne 127.0.0.1 sleep.example.com. 



<img width="940" height="53" alt="image" src="https://github.com/user-attachments/assets/49e68c7e-c59e-47e4-9515-fc42eaab5d03" />
<img width="940" height="242" alt="image" src="https://github.com/user-attachments/assets/6b9e78cd-e8fb-46ab-a314-fa03d0414981" />


Loin kansion ja index.html mkdir /home/klaudija/sleep.example.com.
Loin sivu komennolla nano /home/klaudija/sleep.example.com/index.html. 



<img width="940" height="466" alt="image" src="https://github.com/user-attachments/assets/a15af57a-a69f-48ad-a610-ab595163f159" />


Loin Apache konfiguraation komennolla sudo nano /etc/apache2/sites-available/sleep.example.com.conf.


<img width="940" height="298" alt="image" src="https://github.com/user-attachments/assets/a4bc6a86-0fdb-417d-93f2-5290b5621017" />


Otin sivun käyttöön sudo a2ensite sleep.example.com.conf ja sudo systemctl restart apache2. 
"<VirtualHost *:80>
ServerName sleep.example.com
DocumentRoot /home/klaudija/hattu.example.com/
<Directory  /home/klaudija/hattu.example.com/>
Require all granted
</Directory>
</VirtualHost>"

<img width="940" height="318" alt="image" src="https://github.com/user-attachments/assets/afb6f7de-6328-4872-ba7f-a1f85aafbe0e" />

<img width="940" height="288" alt="image" src="https://github.com/user-attachments/assets/249f282e-57a7-4edc-bae9-da84809d1b53" />

Korjasin hosts-tiedostosta kirjoitusvirheen, mikä oli tiedostossa /etc/hosts. Ajoin sudo systemctl restart apache2.  Sivusto alkoi toimia.


<img width="940" height="216" alt="image" src="https://github.com/user-attachments/assets/f2ecfc9e-831a-47d6-afea-747edc6fa170" />


<img width="940" height="392" alt="image" src="https://github.com/user-attachments/assets/4ddbd51a-db38-40d6-b2be-d3720ccab956" />


### Aseta palomuuri

Tarkistin tilan komennolla sudo ufw status. Päällä. Jos ei ole päällä komennto sudo ufw allow 'Apache' ja sudo ufw enable auttaa. 



<img width="940" height="64" alt="image" src="https://github.com/user-attachments/assets/4808c6a8-7e22-4ee9-8175-d63b69ce7cd5" />



### Luo komento wowstats

Loin tiedoston komennolla sudo nano /usr/local/bin/wowstats. Lisäsin komennot.


<img width="940" height="56" alt="image" src="https://github.com/user-attachments/assets/1bbfd3db-0875-4dc9-be93-db3e56e0ff06" />

<img width="823" height="519" alt="image" src="https://github.com/user-attachments/assets/127a9736-9488-4855-be2d-8be04586317e" />

Tarkoitus:
df - näyttää levytilan
free - näyttää muistin
date - näyttää päivämäärän
ls - listaa tiedostot
echo "" - tulostaa tekstiä
Tein tiedoston suoritettavaksi komennolla  ```$ sudo chmod ugo+x /usr/local/bin/wowstats ```. 

<img width="940" height="29" alt="image" src="https://github.com/user-attachments/assets/7cd68894-93c1-4647-ae23-675aa0fed333" />


Testasin komennolla wowstats. Se toimi.


<img width="940" height="286" alt="image" src="https://github.com/user-attachments/assets/93098539-8d47-4a62-8bbe-796db21ef86a" />





## LÄHTEET:

Tero Karvinen – Linux-palvelimet. Luettavissa: https://terokarvinen.com/linux-palvelimet/

Karvinen 2018: Hello World Python3, Bash, C, C++, Go, Lua, Ruby, Java – Programming Languages on Ubuntu 18.04. Luettavissa: https://terokarvinen.com/2018/hello-python3-bash-c-c-go-lua-ruby-java-programming-languages-on-ubuntu-18-04/   

Command Line Basics Revisited. Luettavissa: https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited 

Shell Scripting. Luettavissa: https://terokarvinen.com/2007/12/04/shell-scripting-4/ 

How to create custom commands in Unix/Linux? [closed] Luettavissa: https://unix.stackexchange.com/questions/84686/how-to-create-custom-commands-in-unix-linux 

Arvioitava laboratorioharjoitus – Linux palvelimet ict4tn021-2 (uusi OPS) alkukeväällä 2017 p1. Luettavissa: https://terokarvinen.com/2017/03/14/arvioitava-laboratorioharjoitus-linux-palvelimet-ict4tn021-2-uusi-ops-alkukevaalla-2017-p1/?fromSearch=arvioitava 

Installing from packages on Debian GNU/Linux and related distributions.  Luettavissa: https://www.php.net/manual/en/install.unix.debian.php 

Install MariaDB. Luettavissa: https://mariadb.com/get-started-with-mariadb/ 

Basics Guide MariaDB. Luettavissa: https://mariadb.com/docs/server/mariadb-quickstart-guides/basics-guide 

Is using "sudo mysql" to use database and learn, OK? Is is normal thing to do in Linux environment? Luettavissa: https://www.reddit.com/r/linux4noobs/comments/ggzj63/is_using_sudo_mysql_to_use_database_and_learn_ok/ 

Install apache2 php module. Luettavissa: https://askubuntu.com/questions/1388251/install-apache2-php-module 

Installing MariaDB Server Guide. Luettavissa: https://mariadb.com/docs/server/mariadb-quickstart-guides/installing-mariadb-server-guide 

Grep command in Unix/Linux. Luettavissa: https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux/ 

Allow user to use sudo command has multiple ways, which one is better? Luettavissa: https://superuser.com/questions/618473/allow-user-to-use-sudo-command-has-multiple-ways-which-one-is-better 

Stored Procedures. Luettavissa:  https://www.php.net/manual/en/mysqli.quickstart.stored-procedures.php 

How to provide a link from a resultset variable? Luettavissa: https://community.adobe.com/questions-621/how-to-provide-a-link-from-a-resultset-variable-636258?lang=fi 

h3 Hello Web Server. Luettavissa: https://github.com/klaudistefi/linux-course/blob/main/h3_hello_web_server.md 































