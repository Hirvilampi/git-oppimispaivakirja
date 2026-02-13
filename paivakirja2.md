# Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Kirjoita tähän vastauksesi

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| repositorion luonti githubiin | git on tyhjä |
| git remote add origin htts://github.com/hirvilampi/githarjoitus5.git | luo uuden etärepositorion, mikä on paikallisesti origin, mutta huomasin, että tässä on väärä alku htts  |
| git remote set-url origin https://github.com/hirvilampi/git-harjoitus5.git | korjasin remote url osoitteen |
| git remote -v | näyttää origin ja annetun url:n. Nyt on oikein |
| git branch -m main master | muutin main branchin nimen masteriksi (varmaan mainin puskeminen olisi riittänyt, mutta kokeillaan tätäkin) |
| git push -u origin master | pushataan master etärepositorioon. -u laittaa upstream kohteeksi, mikä tässä ei olisi ollut tarpeen. Githubin repositorio sivulla näkyy nyt master branchin tiedostot, ei kuitenkaan toista haaraa tyylit  |
| git fetch | hain etärepositoriosta muuttuneet tiedot. Tässä tapauksessa siellä tehdyn readme.md tiedoston |
| git checkout origin/master | tämä aiheutta sen, että HEAD ei ole enää kiinni master haarassa, vaan on detached at origin/master |
| git switch - | ilmoittaa, mikä oli HEAD position ja, että ollaan kommittin jäljessä | 
| git status | sanoo, että olen yhden kommitin origin/masteria jäljessä, joten kannattaa tehdä git pull. Samalla se myös ilmoittaa, että fast-forward on mahdollinen. Virheitä ei siis pitäisi tulla ja myös tämän vuoksi suosittelee suoraan git pull komentoa |
| git pull | haki README.MD tiedoston master haaraan |
| git branch | näkyy vain master ja tyylit. Head detached poistui samalla |
| git commit -m "saatiin loppuun" | kommitoidaan muutokset |
| git tag harjoitus5 | lisää viimeisimpään committiin tag:n harjoitus5 |






