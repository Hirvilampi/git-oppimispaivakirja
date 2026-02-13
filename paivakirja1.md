# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

add, commit on helppoja, koska niitä on tullut paljon tehtyä

Sen sijaan revert, restore, jopa log uusi . Sekä rm mv gitin kanssa käytettynä.
revert ja restore on kyllä sellaisia, joita saa alkaa harjoittelemaan.
Eikä noita opi kuin harjoittelemalla ja oikeilla tiedostoilla. 
Myös restore ja restore --staged eron ymmärtäminen on tärkeä tieto

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git init | luotiin kansiosta git projekti
| git add . | lisää kaikki untracked filet ja kansiot tracked:ksi |
| git commit -m "viesti" | lisää filet gittiin ja luo login, jossa näkyy kyseinen viesti |
| git mv hello.html index.html | muuttaa tiedoston nimen toiseksi |
| git status | antaa stauksen missä branchissä ollaan sekä näyttää untracked files, sekä tracked files |
| git log | näyttää git:n login, eli commitin hash tiedon, authorin, aijan sekä commit viesti |
| git log --stat | git log tietojen lisäksi näyttää mitä tiedostoja on muutettu, lisätty tai poistettu |
| git rm text.txt | poistaa untrackatyn text.txt tiedoston kokonaan |
| git checkout b035df7d5 | siirtyy hash mainittuun committiin |
| git tag harjoitus2 | lisää viimeisimpään talletukseen tunnisteen harjoitus2 | 
| git log --tags | näyttää tallenukset missä tag, mutta minulla kyllä kaikki muutkin, git log --tags --oneline toimi paremmin"
| git checkout main | paluu main talletukseen |
| git switch - | palaa edelliseen paikkaan mistä siirryttiin |
| git restore noob.txt | palauttaa tiedoston viimeisimpään committiin ja hylkää muutokset |
| git restore --staged noob.txt | poistaa tiedoston staging alueelta, mutta ei itse tiedostoa, tämä siis peruu add:äyksen |
| git revert lehma.txt | revert ei toimi yksittäisiin tiedostoihin vain committeihin |
| git revert 86e7f5b9ab8bcf | poistaa tämän commitin kokonaisuudessaan |
| git tag harjoitus3 | lisätään tagi viimeisen commitin tunnisteeseen |
| code hello.html | avaa hello.html koodieditorissa, jos sellainen on määritelty - mulla visual studio code |
| git switch -c tyylit | luodaan uusi haara tyylit |
| git merge tyylit --no-ff | yhdistää tyylit haaran nykyiseen haaraana käyttämättä fast forwardia |
| git tag harjoitus 4 | lisätään tagi viimeisen commitin loppuun | 
