Kurssi: Linux palvelimet ICI003AS2A-3016 

Tehtävänannot: https://terokarvinen.com/linux-palvelimet/

# H1 - Oma Linux -raportti

**Asensin onnistuneesti Linux Debian -käyttöjärjestelmän Virtualboxiin. Kuvaillen koko prosessi + Bonus lopussa.**

Tein harjoituksen perjantaina 16.1.2026. Käytään oma tietokonetta asennuksien varten. Minun kätäkäyttöjärjestelmä on Windows 11 Home, 64 -bittinen, pöytätiertokone.

Asennan Linux Debian -käyttöjärjestelmän Virtualboxiin.

## 1. Virtualboxin asentaminen

klo. 15:45 avasin Johanna Heinosen ohjeitä ja alkonut seurata niitä. Asensin VirtualBoxin tietokoneeseen. Perus asennus, meni hienosti läpi.

Latasin VirtualBoxin tästä: https://www.virtualbox.org/wiki/Downloads

## 2. Linux Debian lataaminen

klo. 13:00 seuran Johanna Heinosen ohjeitä Linux Debian latamisen ja asentamisen varteen. Kaikki meni hyvin. Painosin lataus nappi ja tiedosto tallentui minun kansioni.

Latasin Linux Debian tästä: (https://www.debian.org/download)

## 3. Uuden virtuali koneen VirtualBoxin luominen

<img width="421" height="205" alt="image" src="https://github.com/user-attachments/assets/33030827-d280-40ea-a94d-0e59347e3d96" />

Klo. 13:20 avasin VirtualBoxin ja painasin Create a new virtual machine (VM). Avautui ikkuna  mihin olen laitaannut VM nimi ja ISO Image kohteesen olen löytänyt omasta kansiosta asken laadattu Linux Debian ISO tiedosto. Ja olen ottanut pois ruksi Proceed without Unattended Installation.

Painasin Next. 

Pääsin kohteseen missä pitäis määrritä RAM Memory and CPUs.

- Määrritiin Base Merory 4096 MB
- Number of CPUs 2
- Disk Size 40,00 GB

Valmis.

## 4. Linux Debian asentaminen VirtualBoxin

Klo. 13:30 Seuran ohjeita. Asenin seuravaksi tämä virtuali koneseen Linux Debian.

Painan oikealla hiiri näosauksella juuri asenettu virtuali koneen pääle ja painan Start - Start with GUI. Minulla oli vähän erilainen vaihtoehto kuin ohjedessa. Painasin Graphical Install. 

<img width="435" height="277" alt="image" src="https://github.com/user-attachments/assets/f0142f60-a1a9-4d18-93b6-0c7493832ed5" />

Sen jälkeen oli samalisija vaihtoehtoja kuin ohjessa kielen valitsimisessa ja sijannista.

- Kieli - English
- Sijanti - other - Europe - Finland
- Näppäimisto - Finnish

Seuravaksi oli verkon konfigurointi. Hostname kirjoitiin - linux-test ja Domain on klaudilinux.com. En ollut varma mikä pitöäisi laitta, mutta päätyin tämmöseen. 
Sen jälkeen oli Kysytty keksija root salsana, jäätin sen tyhjäkisi. Sitten oli kysytty set up Full name of the user. Antoi oma nimi ja sukunimi. Sitten oli pyydetty kekisa User name for the account olen laittanut oma etunimi. Sen jälkeen oli aika kekisa salasana. Laitasin salasana ja menin etenpäin. (muistakseni opetaja sanoi, että ei tarvitse laita, muttao len joka tapauksessa laitanut koska ohjessa luki että kanatta). 

Nyt siiryyn partition disks osion. Tässä seurasin ohjeet ihan step-by-step. Guided - use entire dick - select disk to partition: oma niminen Virtual machine - All files in one partition (recommended for new users) - finish partitioning and write changes to disk - Write changes to the disk valitsin YES.

Täsät ettänpäin minun oma asennus ja ohjeiden mainnittu määrä mitä Virtuali kone ole pyytänyt eroa. Alla on muuttama esimerkkija mistä lisää kysymyskija olen saanut. 

<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/5dfc7edd-5a4e-461c-9919-68c2bc790660" >
<img width="434" height="272" alt="Näyttökuva 2026-01-16 140053" src="https://github.com/user-attachments/assets/4a4e285d-3067-4383-a68d-8a6b00691b86" />


Painasin intuition mukkan ja meni lääpi. Se myös kysyi uudeleen kielen vallinan.


<img width="434" height="272" alt="Näyttökuva 2026-01-16 141439" src="https://github.com/user-attachments/assets/983abb43-8233-4c85-8515-e9eea68087c4" />

Kaikken kaikken jälkeen olen pääsyt asentamaan Linux Debian ja pääsin sisään. 

<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/9c9dd2be-8884-47f1-8e13-c883bf440720" />


**Valmis.**

**Bonus**

Klo. 14:30 ajatelin kokeilla ja asenta Krita ohjelma Linuxlille. Krita on avoimen lähdekoodin maalausohjelma. menin Software "kauppaan" ja painasin Install oikealle ohjelmille. Asennus kesti muutamma minuttia ja pääsin siisän piirtämän. 

<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/ec3bf9ef-be6c-472e-a58c-e8799a52031e" />
<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/bb1f2cad-b6cd-46e3-9589-34fa6fd4a6e2" />
<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/b74991a6-3974-4687-8499-bd67c60e0e46" />



## Yhteenveto


Raporttin kirjoitamisen aikana yritin otta kuvia, mutta jäki kääten nyt ymmärän että olisi hyvä enemäk väliproseisesta kuvia. Opetus seuravalle kerralle. 


## Lähteet: 
Heinonen, Johanna 2025. How to Install Linux to Virtualbox? Luettavissa: https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-20082025.md#1-virtualbox-installation
