Kurssi: Linux palvelimet ICI003AS2A-3016 

Tehtävänannot: https://terokarvinen.com/linux-palvelimet/

# H1 - Oma Linux -raportti

**Asensin onnistuneesti Linux Debian -käyttöjärjestelmän Virtualboxiin. Kuvailen koko prosessi.**

Tein harjoituksen perjantaina 16.1.2026. Käytään oma tietokonetta asennuksien varten. Minun kätäkäyttöjärjestelmä on Windows 11 Home, 64 -bittinen, pöytätiertokone.

Asennan Linux Debian -käyttöjärjestelmän Virtualboxiin.

## 1. Virtualboxin asentaminen

klo. 15:45 avasin Johanna Heinosen ohjeitä ja alkonut seurata niitä. Asensin VirtualBoxin tietokoneeseen. Perus asennus, meni hienosti läpi.

Latasin VirtualBoxin tästä: https://www.virtualbox.org/wiki/Downloads

## 2. Linux Debian lataaminen

klo. 13:00 seuran Johanna Heinosen ohjeitä Linux Debian latamisen ja asentamisen varteen. Kaikki meni hyvin. Painosin lataus nappi ja tiedosto tallentui minun kansioni.

Latasin Linux Debian tästä: (https://www.debian.org/download)

## 3. Uuden virtuali koneen VirtualBoxin luominen

<img width="421" height="198" alt="image" src="https://github.com/user-attachments/assets/33030827-d280-40ea-a94d-0e59347e3d96" />

Klo. 13:20 avasin VirtualBoxin ja painasin Create a new virtual machine (VM). Avautui ikkuna  mihin olen laitaannut VM nimi ja ISO Image kohteesen olen löytänyt omasta kansiosta asken laadattu Linux Debian ISO tiedosto. Ja olen ottanut pois ruksi Proceed without Unattended Installation.

Painasin Next. 

Pääsin kohteseen missä pitäis määrritä RAM Memory and CPUs.

- Määrritiin Base Merory 4096 MB
- Number of CPUs 2
- Disk Size 40,00 GB

Valmis.

## 4. Linux Debian asentaminen VirtualBoxin

Seuran ohjeita. Asenin seuravaksi tämä virtuali koneseen Linux Debian.

Painan oikealla hiiri näosauksella juuri asenettu virtuali koneen pääle ja painan Start - Start with GUI.

<img width="870" height="572" alt="image" src="https://github.com/user-attachments/assets/f0147e80-b151-4b59-b521-1d3e8be7eda4" />

Minulla oli vähän erilainen vaihtoehto hjeden kanssa. painasin Graphical Install


<img width="803" height="600" alt="image" src="https://github.com/user-attachments/assets/b741a05e-4ae9-49b5-a9ce-008af5726aea" />
Tätä ei ollut ohjeissa. Pianasin 
Se myös kysyi pari kysymystä mitä ei ollut ohjeissa, Valitse maa uudeleen. 

<img width="804" height="602" alt="image" src="https://github.com/user-attachments/assets/5dfc7edd-5a4e-461c-9919-68c2bc790660" />


## Lähteet: 
Heinonen, Johanna 2025. How to Install Linux to Virtualbox? Luettavissa: https://github.com/johannaheinonen/johanna-test-repo/blob/main/linux-20082025.md#1-virtualbox-installation
