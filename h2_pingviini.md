Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 24.1.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

## x) Tiivistelmät
Tässä tehtävässä ...
Lisää jokin oma kysymys, idea tai huomio)

## a) Micro. Asenna micro-editori.
<img width="405" height="317" alt="image" src="https://github.com/user-attachments/assets/80f695b1-12ab-4988-9436-59350237dd5b" />
<img width="380" height="383" alt="image" src="https://github.com/user-attachments/assets/dab01838-b953-4281-a5ed-da7afd8f577b" />

Komentorivin: _sudo apt install micro_

Komentorivin: _micro test.txt_

## b) Asenna kolme itsellesi uutta komentoriviohjelmaa.
Asensin kolme uutta komentoriviohjelmaa. Apt-get komeno milla saa kolme ohjelmaa kerralla: _sudo apt-get install s-tui git tree_

**s-tui** - Se on suorittimen (CPU) valvontaohjelma. Tässä mitä se näyttää:

<img width="643" height="368" alt="image" src="https://github.com/user-attachments/assets/7dcbe8c1-fc7b-4aa6-a7b1-5f7fc31329df" />

Sen tarkoittus on s-tui is a terminal-based user interface tool for monitoring CPU performance. I launched s-tui from the terminal, and it displayed CPU usage, frequency, and temperature in real time.

**Git** - Versiohallintajärjestelmä
Käytetään: Tiedostomuutosten seurantaan ja projektien ja koodin kanssa työskentelyynse 

_git init_

<img width="394" height="151" alt="image" src="https://github.com/user-attachments/assets/7ea05cd4-c822-4c8a-842a-0274dba06d11" />

_git status_

<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/0dc26e8e-0713-4eb9-ac35-085b659aaa48" />

Tässä miten se toimi...Git is a version control system used to track changes in files.
I checked its status using the command line.

**Tree** - näyttää hakemistorakenteen "puunäkymässä".

Tässä miten se toimi...Tree is a command-line tool that displays directory structures in a tree format. I used tree to view the folder structure of my home directory.

<img width="168" height="250" alt="image" src="https://github.com/user-attachments/assets/cf955f90-101f-46ea-8d40-271fa1fd283e" />


## c) FHS

**/** - Root directory. 

Käytetty komento: _ls /_

Root directory of the Linux filesystem. All other directories are located under it.
Luettelo kansioista: 

<img width="460" height="47" alt="image" src="https://github.com/user-attachments/assets/b1c81f44-ec77-4604-a2dd-986cd0a5963e" />

Selitys: 

**/home/** - Contains home directories for all users.

Käytetty komento: _ls /home_

<img width="181" height="38" alt="image" src="https://github.com/user-attachments/assets/59fa29e8-4133-492b-b2ae-1b15c0165d99" />

Selitys: Näen käyttäjätunnuksesi.

**/home/klaudija/** - my personal "home" directory

Käytetty komento: _ls /home/klaudija_

is the personal home directory of the user. It is the main place for storing user files.

<img width="564" height="41" alt="image" src="https://github.com/user-attachments/assets/1a4b6774-67ea-4be6-93f4-c6c831dc85df" />

Selitys:

**/etc/** - 	All system wide settings. 

Käytetty komento: 

<img width="630" height="305" alt="image" src="https://github.com/user-attachments/assets/24e4dc4f-8ab1-4686-9963-0b17dcdb1267" />


Selitys: Valitse yksi tiedosto, esimerkiksi passwd. /etc contains system-wide configuration files stored as plain text.


**/media/** - Removable media

/media is used for mounting removable media such as USB drives.

Käytetty komento: 

<img width="197" height="34" alt="image" src="https://github.com/user-attachments/assets/a93d6c2b-3816-4e19-b0d8-b5208308ce88" />

Selitys:

**/var/log/** - System wide logs

/var/log contains system log files.

Käytetty komento: 

<img width="533" height="44" alt="image" src="https://github.com/user-attachments/assets/26fa9c2d-0bb6-4205-8886-c5a1129da8c4" />

Selitys: 


## d) The Friendly M

Mitä on grep - a command-line tool used to search for text patterns inside files.

1.
Käytetty komento: _ls /etc | grep net_
Selitys: This command filters directory contents and shows only entries that contain the word "net".
<img width="196" height="59" alt="image" src="https://github.com/user-attachments/assets/5af8a78e-fdff-4d3a-9a51-9bb92af271a4" />


2.
Käytetty komento: _grep -F_
Selitys: 

<img width="203" height="29" alt="image" src="https://github.com/user-attachments/assets/c8159280-9c44-4313-95b3-53ac74c230ec" />

3.
Käytetty komento: _grep --help_
Selitys: 

<img width="392" height="332" alt="image" src="https://github.com/user-attachments/assets/9450b466-66a0-4ad9-b36a-f4c693d5ecd1" />


## e) Pipe
Esimerkki putkista (pipes, "|").

Käytetty komento: _journalctl | grep error_
Selitys: This command pipes system log output to grep to search for error messages.

<img width="631" height="341" alt="image" src="https://github.com/user-attachments/assets/f9ccb6b4-0ee5-476c-9376-89d6bf871810" />


## f) Rauta
Asensin lshw by giving a command _sudo apt install lshw_ ja sen jälkeen I _run a sudo lshw -short -sanitize_

<img width="459" height="284" alt="image" src="https://github.com/user-attachments/assets/b9a3e020-79ce-447c-bf4d-c4b91fcd1d1a" />

Yllä on listta mitä tuli esille. 

Analyysi: 

## Lähteet: 
Tero Karvinen – Linux-palvelimet: https://terokarvinen.com/linux-palvelimet/
