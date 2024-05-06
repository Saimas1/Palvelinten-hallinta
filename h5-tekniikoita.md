## Tehtävä h5 Tekniikoita

# Tehtävä x)

"Hello Windows Salt"
  
  Salt-tilan, joka luo tiedoston "suolaikkuna.txt" kirjoittaminen
  - Ensin luodaan init.sls tiedosto Salt-projektikansioon nimeltä hello-windows
  - Tiedoston luominen Notepadissa
 - Salt-tilan suorittaminen salt-call, --file, --root-lipulla
  - Salt tilan suorittaminen onnistuneesti sekä tiedoston luominen varmistettiin

# Lähteet
- [Hello Windows Salt, Tuomas Valkamo, 2022](https://tuomasvalkamo.com/CMS-course/week-5/)

# Tehtävä a)

-Saltin asennuksen testaus Windowsilla. Testasin asennuksen onnistumisen komennolla:
```
salt-call --local test.ping
```
![h5_a1](https://github.com/Saimas1/Palvelinten-hallinta/assets/165194309/22def108-af19-40f4-bc46-f4f963ea90a4)

# Tehtävä b)

- Keräsin tietoa Windows-koneestani komennolla:
  ```
  salt-call --local grains.items
  ```
 - biosstring:
   Se kertoo BIOS-version ja valmistajan, joka oli HPQOEM-0
- cpu_model:
  Kertoo koneen prosessorin mallin, joka on Intel(R) Core(TM) i7-7600U CPU @ 2.80GHz.
  -cwd:
  Kertoo käynnissä olevan prosessorin nykyisen tyäskentelykansion, joka on C:\WINDOWS\system32.
- mem_total:
  Kertoo kokonaismuistin määrän megatavuina, joka on 16259 MB
- num_cpus
  Kertoo prosessorien määrän joka on koneessani 4
- osversion:
  Kertoo käyttöjärjestelmän tarkan version, joka on 10.0.19045.

# Tehtävä c)
