# Tehtävä h2 - Soitto kotiin

## Tiivistäminen x)

## "Two Machine Virtual Network With Debian 11 Bullseye and Vagrant"

- VirtualBoxin ja Vagrantin asentaminen on helppoa Ubuntulla ja Debianilla komennoilla:
  
  ```
  sudo apt-get update
  sudo apt-get install vagrant virtualbox   

- Komentojen avulla luodaan kaksi isäntää yksityisverkossa
- "Ping"-komennolla voi tarkistaa ovatko isännät yhteydessä toisiinsa sekä Internettiin

## "Salt Quickstart – Salt Stack Master and Slave on Ubuntu Linux"

- Saltissa pääpalvelimen tulee olla julkisella palvelimella, mutta orjat voivat olla missä tahansa
- Pääpalvelin ja orjat yhdistetään asentamalla salt-master ja salt-minion
- Salt mahdollistaa tuhansien koneiden hallinnan

## "Hello Salt Infra-as-Code"

- Sltin asennus komennolla:
  
  ```
  sudo apt-get -y install salt minion
  ```
- Salt-minionin asennuksen jälkeen luodaan "hello"-moduulikansio
- Moduulikansiossa määritellään idempotentti Salt-koodi
- Idempotentti takaa sen, ettei järjestelmään tehdä tarpeettomia muutoksia
  

## Omat havainnot

- Vagrant on erittäin hyvä työkalu testausta ja kehitystä varten. Sen avulla voidaan tehokkaasti hallita virtuaalikoneita eri käyttöjärjestelmissä
- Saltin asentaminen ja käyttöönotto oli suhteellisen helppoa, mikä tekee siitä hyvän vaihtoehdon laajamittaiseen tietokoneiden hallintaan
- Saltin idempotenttisuus on hyvin tärkeä piirre. Sen avulla varmistetaan että järjestelmän tila pysyy oikeana

## Tehtävä a)

-Virtuaalikoneet samassa verkossa ja voivat pingata toisiaan:

![virtuaalikone1_snip](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/eda371bc-e5e8-4c48-acac-d652bb31123e)
![virtuaalikone2_snip](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/7db88f32-dc7d-4f2b-a51c-c5ef996a3fdd)
![t001_ping](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/ef4ea5a3-8f6c-45e9-8afd-5d61c56598ec)
![t002_ping](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/30e12686-d181-4b1f-93c3-9acd60da4b65)


## Tehtävä b)

-Salt herra-orja asennus ja toimivuus
![herra_ping](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/713e2293-f061-4a33-992e-08991f8a1a2d)
![vagrant_herra_avain](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/d9415c22-3d3c-453b-b98e-c196cab89bbd)
![herra_orja](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/1919142c-11aa-4529-86fc-185c09a45158)

## Tehtävä c)

-Shell-komento orjalla
![herra_cmd](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/6742a59c-46a6-4fb0-9c62-66e2c89264f2)

## Tehtävä d)

![teht_1_c](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/8d557ec1-cb5f-4c14-a906-d16875510ee3)
![c_1](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/5030f856-e9ef-43d4-b90f-fa9a4888f34e)

## Tehtävä e)

![grains_snip](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/e6b277bc-5b51-44c1-ba23-765c29378c13)



  
