# Tehtävä h1-Viisikko

## x) - Salt: Salt komennot toimivat Linuxissa ja Windowsissa. Keskeisiä toimintoja ovat: pkg, file,service,user sekä cmd. Salttia käyteään yleensä hallitsemaan useita tietokoneita verkossa.
- Github: Sen avulla voidaan julkaista nettisivu nopeasti vain muutamalla klikkauksella. Tiivistettynä: rekisteröidy, luo uusi repositorio, lisää .md-tiedosto, kirjoita teksti ja paina commit ja sivusi on julkaistu.
  -Raportin kirjoittaminen: Raportin tulee olla tarkka ja toistettava, siinä kuvaillaan tehtävät, tulokset ja ympäristö. Tulee käyttää imperfektiä ja tarkkaa kieltä sekä viitata mahdollisiin lähteisiin. Raportin tulee olla helppolukuinen väliotsikoita käyttäen. Tulee välttää plagiointia.


 - a) Saltin testaus Windowsilla. Testasin Saltin toimivuuden komennolla: "salt-minion --version". Vastaukseksi sain: "salt-minion 3007.0 (Chlorine)" Eli versionnumeron siitä Saltista mikä minulla on asennettuna. 
 - b) Vagrantin testaus. Suoritin testauksen komennolla "vagrant --version". Vastaukseksi sain "Vagrant 2.4.1" eli versionumeron vagrantista.
 - c) Seuraavaksi oli vuorossa uuden virtuaalikoneen luominen Vagrantilla. Käytin tässä apunani Vagrantin sivuilta löytyviä ohjeita asennukseen, Install Vagrant [Google](https://developer.hashicorp.com/vagrant/tutorials/getting-started/getting-started-install) 
 -d) Asensin virtuaalikoneelle Saltin komennoilla: sudo apt update, sudo apt install salt-minion. 
  -e) Viisi tärkeintä tilafunktiota: 
pkg
Komennolla " sudo salt-call --local -l info state.single pkg.installed tree" asennetaan tree paketti. sivun loppuun tulee myös yhteenveto tuloksista, joissa kerrotaan mm että yksi tila onnistui (Succeeded:1), yksi asetus on muutettu (changed=1), yhtään tilaa ei epäonnistunut (failed=0) sekä kokonaisuus ajan tilan suorittamiselle.

File managed

Komennolla:     "sudo salt-call --local -l info state.single file.managed /tmp/helloworld" luodaan uusi tiedosto nimeltä /tmp/helloworld. Tulokset kertovat että tiedosto on tyhjä sekä samat kuin edellisessä eli tilan onnistumiset, asetuksen muutoksen sekä mahdolliset epäonnistumiset.

Service

Komennolla: " sudo salt-call --local -l info state.single service.running apache2 enable=True" varmistaa onko "apache2"-palvelu käynnissä ja asetettu käynnistymään automaattisesti järjestelmän käynnistyessä.

User

Komennolla: "sudo salt-call --local -l info state.single user.present saimas01" Voidaan varmistaa onko tietty käyttäjä olemassa ja tarvittaessa luo sen. user.present tarkistaa onko käyttäjä olemassa järestelmässä, jos on komento ei tee mtään,mutta jos käyttäjäää ei ole olemassa se luo sen järjstelemään

Cmd

Komennolla: " sudo salt-call --local -l info state.single cmd.run 'touch /tmp/foo' creates="/tmp/foo" luodaan tyhjä tiedosto nimeltä "foo" hakemistoon "/tmp".  sekä samalla tarkistaa onko kyseistä tiedostoa jo olemassa.  Komento on hyödyllinen erityisesti kun halutaan varmistaa tiettyjen tiedostojen tai hekmistojen olemassaolo.

f) Idempotenssi on toiminto, jota ajetaan useita kertoja peräkkäin mutta lopputulos pysyy siitä huolimatta samana.Esimerkki idempotenssista "sudo salt-call --local state.single file.directory /tmp/my_directory". 
Komento "salt-call --local grains.items" kertoo minionin yleisiä tietoja kuten käyttöjärjestelmän.
Komento "salt-call --version" kertoo Saltin versionumeron mikä on käytössä

g) Kolme kiinnostavaa kohtaa: Osfinger Ubuntu 20.04: Kertoo minionin käyttöjärjestelmän sekä sen version. Virtual: "virtualbox" kertoo että kyseessä on virtuaalikone joka toimii VirtualBox-alustalla.

#Näyttökaappaukset komennoista ja tuloksista

![salt pkg](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/8729eee2-5252-4c86-b031-f9728bc8513c)
![salt_file_managed](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/e20095e6-09c3-42a2-8759-0fce282b697b)
![salt_service](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/c0698c9d-9193-4c44-8e2f-b18282d549f7)
![salt_user](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/a2a5b6ae-8f36-40f1-bc2f-22cce7d8753d)
![salt_osfinger](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/b174710b-6467-4006-b2e3-38d842705595)
![saltsnip](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/7421876d-20e7-4559-9e51-b0fcb685a4f6)
![vagrant_kirjauduttu](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/924db0c3-5de1-4d53-be6c-77fded4e7058)


# Lähdeviitteet

Install Vagrant:[Install Vagrant](https://developer.hashicorp.com/vagrant/tutorials/getting-started/getting-started-install)
Tero Karvinen, 2023 [Run Salt](https://terokarvinen.com/2021/salt-run-command-locally/) 


