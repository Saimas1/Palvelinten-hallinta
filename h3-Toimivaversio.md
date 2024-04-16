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
  

   
  
