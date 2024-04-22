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
  -Komento ei onnistunut vaan sain jatkuvasti ilmoituksen:
![demoni_a](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/4bcc09c1-3286-4fa8-9f0b-594403504eb1)

-En tiedä miksi komento ei toiminut, joten en saanut tehtävää tehtyä.

