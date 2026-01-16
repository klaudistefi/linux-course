Kurssi: Linux palvelimet ICI003AS2A-3016 

Tehtävänannot: https://terokarvinen.com/linux-palvelimet/

# Oma Linux -raportti

**Asensin onnistuneesti Linux Debian -käyttöjärjestelmän Virtualboxiin. Kuvaillen koko prosessi + Bonus lopussa.**

Tein harjoituksen perjantaina 16.1.2026. Käytin omaa tietokonetta asennuksia varten. Käyttöjärjestelmäni on Windows 11 Home, 64-bittinen, pöytätietokone.

Asensin Linux Debian -käyttöjärjestelmän VirtualBoxiin.

## 1. Virtualboxin asentaminen

Klo 15:45 avasin Johanna Heinosen ohjeet ja aloitin niiden seuraamisen. Asensin VirtualBoxin tietokoneeseen. Perusasennus sujui hyvin ja meni onnistuneesti läpi.

Latasin VirtualBoxin tästä: https://www.virtualbox.org/wiki/Downloads

## 2. Linux Debian lataaminen

Klo 13:00 seurasin Johanna Heinosen Linux Debianin lataus ja asennusohjeita. Kaikki meni hyvin. Painoin latauspainiketta, ja tiedosto tallentui minun tietokoneen kansiooni.

Latasin Linux Debian tästä: https://www.debian.org/download

## 3. Uuden VirtualBox-virtuaalikoneen luominen

<img width="421" height="205" alt="image" src="https://github.com/user-attachments/assets/33030827-d280-40ea-a94d-0e59347e3d96" />

Klo 13.20 avasin VirtualBoxin ja painoin “Create a new virtual machine (VM)”. Avautui ikkuna, jossa annoin virtuaalikoneelle nimen. ISO Image kohtaan valitsin omasta tietokone kansiostani ladatun Linux Debian ISO tiedoston. Poistin valinnan kohdasta “Proceed without Unattended Installation”.

Painoin Next.

Seuraavaksi siirryin kohtaan, jossa määritettiin RAM-muisti ja prosessorit:

- Base Memory 4096 MB
- Number of CPUs 2
- Disk Size 40,00 GB

Tämän jälkeen tämä osa oli valmis.

## 4. Linux Debianin asentaminen VirtualBoxiin

Klo 13.30 seurasin ohjeita ja aloitin Linux Debianin asentamisen virtuaalikoneeseen.

Painoin hiiren oikealla painikkeella juuri luodun virtuaalikoneen päällä ja valitsin Start → Start with GUI. Minulla oli hieman eri näkymä kuin ohjeessa, joten valitsin Graphical Install.

<img width="435" height="277" alt="image" src="https://github.com/user-attachments/assets/f0142f60-a1a9-4d18-93b6-0c7493832ed5" />

Tämän jälkeen valinnat olivat samanlaiset kuin ohjeessa, kielen valitsimisessa ja sijannista.

- Kieli - English
- Sijanti - other → Europe → Finland
- Näppäimisto - Finnish

Seuraavaksi tein verkon määritys. Hostname kenttään kirjoitin "linux-test" ja domain-nimeksi "klaudilinux.com". En ollut täysin varma, mitä tähän piti laittaa, mutta valitsin tämä.

Seuraavaksi VM pyysi root salasanaa. Jätin sen tyhjäksi. Tämän jälkeen VM pyysi käyttäjän koko nimi "Full name of the user", johon kirjoitin oman etu ja sukunimeni. "User name for the account" kohtaan kirjoitin oman etunimeni. Sen jälkeen oli aika kekisa salasanan ja jatkoin eteenpäin (muistaakseni opetaja mainittiin, että salasanaa ei ole pakko asettaa, päätin asettaa sen varmuuden vuoksi).

Seuraavaksi siirryttiin partition disks osion. Tässä noudatin ohjetta ihan step-by-step:

- Guided – use entire disk
- Select disk to partition - virtuaalikoneen levy
- All files in one partition (recommended for new users)
- Finish partitioning and write changes to disk
- Write changes to the disk - YES.

Tämän jälkeen asennuksessa tuli vielä muutamia lisäkysymyksiä, jotka erosivat hieman ohjeesta. Alla on 2 esimerkkejä minkälaisia lisää kysymyskija sain.

<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/5dfc7edd-5a4e-461c-9919-68c2bc790660" >
<img width="434" height="272" alt="Näyttökuva 2026-01-16 140053" src="https://github.com/user-attachments/assets/4a4e285d-3067-4383-a68d-8a6b00691b86" />


Vastasin niihin oman harkinnan mukaan ja jatkoin eteenpäin. Asennus kysyi vielä uudelleen kielivalintaa ja joitakin muita asetuksia. Näistä en valitettavasti ottanut kuvakaappauksia.


<img width="434" height="272" alt="Näyttökuva 2026-01-16 141439" src="https://github.com/user-attachments/assets/983abb43-8233-4c85-8515-e9eea68087c4" />

Kaiken kaikkiaan Debianin asennus valmistui ja pääsin kirjautumaan järjestelmään. 

<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/9c9dd2be-8884-47f1-8e13-c883bf440720" />


**Valmis.**

**Bonus**

Klo 14.30 päätin kokeilla asentaa "Krita" ohjelman Linuxille.
Krita on avoimen lähdekoodin maalausohjelma.

Avasin Software-kaupan ja painoin Install. Asennus kesti muutaman minuutin, ohjelma avautui ja pääsin käyttämään sitä ja piirtämään.

<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/ec3bf9ef-be6c-472e-a58c-e8799a52031e" />
<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/bb1f2cad-b6cd-46e3-9589-34fa6fd4a6e2" />
<img width="434" height="272" alt="image" src="https://github.com/user-attachments/assets/b74991a6-3974-4687-8499-bd67c60e0e46" />


## Yhteenveto

Kokonaisuudessa koko prosessi oli suoraviivainen ja helppo. Asennus meni pääosin ohjeiden mukaan, eikä suuria ongelmia tuullut vastaan. 

Raporttin kirjoittaessa yritin ottaa riitävästi kuvakaappauksia eri vaiheista, mutta jälkikäteen ymmärsin, että välivaiheista olisi hyvä ottaa enemmän kuvakaappauksia. Opetus seuraavalle kerralle.

Uutta tietoa itselleni, jos haluan nuolin tekstissä, esimerkiksi ↑↓→←, nuolet saa Alt + 24, Alt + 25, Alt + 26 ja Alt + 27. 


## Lähteet: 
Heinonen, Johanna 2025. How to Install Linux to Virtualbox? Luettavissa: https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-20082025.md#1-virtualbox-installation
