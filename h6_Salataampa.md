Kurssi: Linux palvelimet ICI003AS2A-3016 <br>
Tekijä: Klaudija Majamäki <br>
Päivämäärä: 24.-25.2.2026 <br>
Paikka: Pöytätietokone, Windows 11 -kone <br>

# h6 Salataampa


## x) Tiivistelmät


**Let's Encrypt 2024**<br>
- Let’s Encrypt antaa sertifikaatin
- Sertifikaatit pitäisi päivitä 
- Certbot ohjelma hoitaa yhteyden Let’s Encrypt palveluun

**The Apache Software Foundation 2025**<br>
- Apacheen täytyy ottaa käyttöön SSL laajennus
- ServerName kertoo Apachelle, mille domainille asetukset kuuluvat


## a) Hanki ja asenna palvelimellesi ilmainen TLS-sertifikaatti Let's Encryptilta. Osoita, että se toimii.


Asensin sertifikaatin 24.2.2026.


Kirjauduin ensin palvelimelle ja suoritin seuraavat komennot VirtualBoxin terminaalissa: 


_$ sudo apt update<br>
$ sudo apt install python3-certbot-apache<br>
$ sudo certbot<br>
$ curl majamakik.site<br>
$ curl https://majmakik.site<br>_


Asennus onnistui. Näin seuraavan viestin “Congratulations! You have successfully enabled HTTPS on https://majamakik.site”

<img width="844" height="248" alt="image" src="https://github.com/user-attachments/assets/cf206b03-ed14-4d6b-84c8-10459be32ae8" />
<img width="815" height="75" alt="image" src="https://github.com/user-attachments/assets/543533f8-6b27-4ec3-b665-fbe267cce172" />
<img width="868" height="257" alt="image" src="https://github.com/user-attachments/assets/63de71b6-1935-44e1-8e9a-7e752076074b" />
<img width="988" height="95" alt="image" src="https://github.com/user-attachments/assets/159a48d2-3411-40b4-a68c-6164cb099c37" />

## b) Testaa oma sivusi TLS 
Aloitin testauksen 24.2.2026.


Kun asennus onnistui ja näin seuraavan viestin “Congratulations! You have successfully enabled HTTPS on https://majamakik.site”. Kuitenkin kun avasin sivun selaimessa HTTPS-yhteydellä, sain virheen “This site can’t be reached”. Testasin sivua myös SSL Labs testillä, mutta se näytti vain virheilmoituksen. 
Yritin asentaa sertifikaatin uudelleen, mutta tulos oli sama. Koska kello oli jo paljon, päätin jatkaa seuraavana päivänä.


Jatkoin 25.2.2026.


Kävin kaikki uudelleen läpi ja lueskelin vinkit erilaisessa foorumeista. Kokeilin avata portin 443 palomuurissa. Koska ilman tätä porttia ulkopuolinen liikenne ei pääse palvelimelle.


$ curl majamakik.site 443 komennolla testasin, vastaako palvelin portissa 443. sudo ufw reload komennolla latasin palomuurin asetukset uudelleen.
sudo systemctl restart apache2 komennolla käynnistin apache verkkopalvelimen uudelleen. Se varmista, että uudet asetukset ja sertifikaatit toimivat.
sudo ufw allow ’apache Full’, pitäisi avata portit 80 ja 443, jotta verkkosivu toimii selaimessa.

Komennot:<br>
_$ curl majamakik.site 443<br>
$ sudo ufw reload<br>
$ sudo systemctl restart apache2<br>
$ sudo ufw allow ’apache Full’<br>_

<img width="806" height="472" alt="image" src="https://github.com/user-attachments/assets/9ef0affb-cf72-41e8-b1da-a63f4a09652c" />
<img width="816" height="525" alt="image" src="https://github.com/user-attachments/assets/f4996655-72b7-4b05-9258-75f9ed839535" />
<img width="825" height="180" alt="image" src="https://github.com/user-attachments/assets/964c28bc-7105-445a-8742-3981684da4a8" />
<img width="825" height="57" alt="image" src="https://github.com/user-attachments/assets/9893858e-51e5-4708-a47b-424e3c035879" />
<img width="825" height="73" alt="image" src="https://github.com/user-attachments/assets/656fdaf8-40e4-4330-8cce-48d0a3d3e5e1" />
<img width="940" height="543" alt="image" src="https://github.com/user-attachments/assets/388cd03c-cc5a-4137-937f-2e991ec7ccfe" />
<img width="619" height="248" alt="image" src="https://github.com/user-attachments/assets/c039722f-b663-4ea8-ab3b-cbdcb2624361" />

## LÄHTEET:

Tero Karvinen – Linux-palvelimet. Luettavissa: https://terokarvinen.com/linux-palvelimet/


Let's Encrypt 2024: How It Works Luettavissa: https://letsencrypt.org/how-it-works/ 


The Apache Software Foundation 2025: Apache HTTP Server Version 2.4 [Official] Documentation: SSL/TLS Strong Encryption: How-To: Basic Configuration Example Luettavissa: https://httpd.apache.org/docs/2.4/ssl/ssl_howto.html#configexample 


SSLLabs Luettavissa: https://www.ssllabs.com/ssltest/ 


Allow access to Apache on both port 80 and 443 in Ubuntu 16.04 Luettavissa: https://unix.stackexchange.com/questions/460480/allow-access-to-apache-on-both-port-80-and-443-in-ubuntu-16-04 
