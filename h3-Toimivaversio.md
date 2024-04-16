## Tiivistä

# X) 

# " Getting Started - What is Git? "

-  Git on versionhallintajärjestelmä, joka ajattelee tietoja kuvina tiedostojärjestelmästä, ei muutoksina tiedostoihin
- Gitin toiminta on pääasiassa paikallista. Suurin osa toiminnoista vaatii pelkästään paikallisia tiedostoja sekä resursseja
- Gitissä tiedostot voivat olla kolmessa tilassa : muutettu, valmisteltu ja sitoutettu
- Tiedostojen muutokset tallennetaan paikallisesti ennen kuin ne sitoutetaan Git-tietokantaan


 # Gitin käyttö

1. ```
   git add
   ```
   

   - Tämä komento lisää kaikki uudet tai muokatut tiedostot "staging area"-alueelle
   - "Staging area" on väliaikainen alue missä määritellään se, mitkä tiedostot sisällytetään seuraavaan committiin


2. ```
   git commit
   ```

   

 - Tämä komento tallentaa "staging area"-alueen muutokset Git-tietokantaan uutena committina



3. ```
   git pull
   ```
- Tämä komento hakee uusimmat muutokset etäisestä Git-respositoriosta ja yhdistää ne paikalliseen koodiin.

4. ```
   git push
   ```
   - Tämä komento lähettää paikalliset commitit etäiseen Git-respostorioon
  

     # Lähteet :
    - [Git Documentation push](https://git-scm.com/docs/git-push)
     
    - [Git Documentation pull](https://git-scm.com/docs/git-pull)
     
    - [Git Documentation commit](https://git-scm.com/docs/git-commit)
     
   -  [Git Documentation add](https://git-scm.com/docs/git-add)
  
# Tehtävä b)

- Tein uuden varaston Githubiin nimeltä summer2024
-  Tämän jälkeen kloonasin varaston komennolla
  ```
git clone (varaston url)
```

-Siirryin kloonatuun varastoon komennolla:"
```
cd summer2024
```

-Tämän jälkeen muokkasin README.md tiedostoa lisäämällä tekstiä

-Lisäsin muutokset stagetus-alueelle komennolla:

```
git add README.md
```

-Tallensin muutokset ja puskin ne Githubiin komennoilla

```
git commit -m "Teksti"
git push origin main
```

-Siirryin Githubiin tarkistamaan tiedoston ja sinne oli siirtynyt teksti:

![git_muutokset3](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/13302658-3bd5-424b-a117-d007087f0f45)

# Tehtävä c)

- Lisäsin README.md tiedostoon tyhjän rivin komennolla:
  ```
  echo "Tyhjä rivi" >> README.md
  ```

- Jonka jälkeen tarkistin odottavat muutokset komennolla git status. Se näytti tehdyt muutokset, joita ei ollut vielä commitoitu:

![git_tehtäväc](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/8eb130ef-cb02-4dea-adbf-33a55c3b04fc)

- Tämän jälkeen poistin kaikki muutokset ja palautin viimeisimmän commitin tilan komennolla:
  ```
  git reset --hard
  
  ```
  # Tehtävä d)

- Sähköpostin ja nimen asettaminen komennoilla:
  ```
  git congif --global user.name "Nimi"
  git config --global user.email "Sähköposti"
  ```

-  Varaston lokia voidaan tarkastella komennolla:
```
git log
```

- "commit hash": kertoo tunnisteen commitille
- "Author": Kertoo nimen ja sähköpostiosoitteen siitä, joka teki commitin
- "Date": Kertoo milloin kommit tehtiin
- "Commit message": Kertoo viestin, joka kertoo mitä muutoksia commit sisältää

  
