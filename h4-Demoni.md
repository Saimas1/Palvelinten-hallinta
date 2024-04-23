## Tehtävä 4 Demoni

# Tehtävä x) Lue ja tiivistä

# "Salt Vagrant - automatically provision one master and two slaves"

- Salt Vagrant luo automaattisesti yhden herran ja kaksi orjaa
- Satoja tietokoneita voidaan hallita konfiguraatiohallinnan avulla
- Komentoja voi ajaa orjilla herran kautta
- Tavoitteena on idempotenttien käyttö, jossa muutoksia tehdään vain tarvittaessa
-  "Hello"- tila luo esimerkkitiedoston
-  "top.sls" määrittelee sen, mitä tiloja suoritetaan millekkin orjalle

  # "Salt contributors: Salt overview"

YAML:n säännöt:
- YAML on merkintäkieli, jota käytetään Saltissa. Sen rakenne koostuu avain-arvo pareista, kartoista ja lohkorakenteista. Se vaatii välilyöntejä sarkainetn perään sekä on kirjainkoosta riippuvainen

- YAML:n yksinkertainen rakenne:
-  YAML koostuu listoista, sanakirjoista ja skaalareista. Skaalarit ovat avain-arvo karttoja. Ne sisältävät arvoja erillisillä riveillä,jotka on edeltävinä välilyönteinä ja väliviivoina
 - Listat ja sanakirjat- YAML-lohkorakenteet:
   - YAML on järjestetty lohkorakenteisiin
    - Sarkaimilla asetetaan konteksti. Ominaisuudet ja lista täytyy sisentää yhdellä tai useammalla välilyönnillä, mutta kaksi on standardi
    - Kokoelma, mikä on lista tai sanakirjablokin sekvenssi, ilmaistaan väliviivalla ja välilyönnillä

 # " Pkg-File-Service – Control Daemons with Salt – Change SSH Server Port"

-Salt- tilan (sshd.sls) avulla asennetaan "openssh-server", sekä hallitaan "/etc/ssh/sshd_config"-tiedostoa. Lisäksi varmistetaan, että SSH-palvelu on käynnissä. Konfiguraatiotiedostossa (sshd_config) porttinumero on muutettu ja kommentit poistettu
-Lopuksi tila (sshd) levitetään orjille komennolla:
```
sudo salt '*' state.apply sshd
```
-Jonka jälkeen portin toimivuus testataan orjalla

# Lähteet

- Karvinen 2023, [Salt Vagrant - automatically provision one master and two slaves](https://terokarvinen.com/2023/salt-vagrant/#infra-as-code---your-wishes-as-a-text-file)
- Salt contributors, [Salt overview](https://docs.saltproject.io/salt/user-guide/en/latest/topics/overview.html#rules-of-yaml)
- Karvinen 2018, [Pkg-File-Service – Control Daemons with Salt – Change SSH Server Port](https://terokarvinen.com/2018/04/03/pkg-file-service-control-daemons-with-salt-change-ssh-server-port/?fromSearch=karvinen%20salt%20ssh)


# Tehtävä a)

- Aloitin tehtävän luomalla "hello"-nimisen kansion C:\salt\hello-hakemistoon
- Sen jälkeen avasin ja muokkasin notepadilla tiedostoa
- Kun lähdin suorittamaan tilaa komennolla:
  ```
  salt-call --local state.apply C:\salt\hello\init.sls
  ```
  -Komento ei onnistunut vaan sain jatkuvasti ilmoituksen: " Data failed to compile:" "No matching sls  found.."
-En tiedä miksi komento ei toiminut, joten en saanut tehtävää tehtyä.

# Tehtävä b)
- Tässä tehtävässä kävi sama kuin ylemmässä, sain saman ilmoituksen taas enkä onnistunut tätä tehtävää tekemäään

  # Tehtävä c)

  - Sain apachen asennettua ja toimimaan:
  ![demoni_b1](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/43190bc0-2b6e-4242-8580-e3dd687aec33)

- Loin tarvittavat tiedostot "top.sls" , "hello.sls" ja "apache.sls"
- Kun yritin ajaa tilat virtuaalikoneessa sain kyseisen ilmoituksen:
 ![demoni_eitoimi2](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/36cc178e-13a4-4948-8749-01066bafc412)

 # Tehtävä d) 

 - Aloitin tarkistamalla "sshd_config"-tiedoston määritellyt portit komennolla:
   ```
   cat /etc/ssh/sshd_config | grep Port
   ```
- Sen jälkeen lisäsin uuden portin asetustiedostoon komennolla:
  ```
  echo "Port 2222" | sudo tee -a /etc/sshd_config
  ```

- Tämän jälkeen käynnistin ssh-palvelun uudelleen, jotta muutokset tulevat voimaan
![demoni_c1](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/96bbc42a-d742-4651-94c3-ecca6f863fd8)

 - Näiden vaiheiden jälkeen lisäsin asetustiedostoon service-watchin
 - Tämän jälkeen yritin suorittaa Salt-tilan komennoilla:
   ```
sudo cp sshd_port.sls /srv/salt/
sudo salt-call --local state.apply sshd_port
```
-Sain kuitenkin ilmoituksen, että jokin oli mennyt pieleen. Ehkä syötin tiedostoon on virheelliset komennot.. selvitän asiaa vielä lisää, jotta se toimisi
  
