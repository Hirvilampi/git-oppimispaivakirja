# Kurssi: Git-versionhallinta - SOF013AS2A-3002

Tekijä: Timo Lampinen

## Sisältö
Tässä repositoriossa on oppimispäiväkirjatehtävät 1–3.

Repositorion päiväkirjat on toteutettu jokainen omana markdown tiedostonaan.  Suorat linkit tässä:  
  
[Päiväkirja 1](paivakirja1.md)  
[Päiväkirja 2](paivakirja2.md)  
[Päiväkirja 3](paivakirja3.md)    

Ne on myös yhdistetty tähän tiedostoon alapuolelle kohtaan Oppimispäiväkirjat.   

## Oppimispäiväkirjat 

Kaikki oppimispäiväkirjat.  

# Päiväkirja 1
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

# Päiväkirja 2
# Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__  

Kaikki oli hyvin tuttua. itselleni selkästi helpointa on päästää irti.. eli tuhota yhdistettyjä haaroja. Ei siis vaikeaa komentojen kannalta vaan, jotenkin sellainen jatkuva luottamuksen puute siiten, että muutokset ovat tallessa.

Tämä git remote set-url origin ... oli hyvä tieto, kun silloin tällöin tulee kirjoitettua väärin. Sormet toimivat nopeammin kuin ajatus.

git remote -v on myös uusi ja hyvä tieto.  


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


# Päiväkirja 3
# Oppimispäiväkirja: Git projektissa

__Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?__

Omasta kokemuksesta voi sanoa, että versionhallinta on elintärkeä myös yksin kehittäessä. 
Ensinnäkin se mahdollistaa ikäänkuin pelin tallentamisen eri tilanteissa ja jos uusi kehityksessä otettu suunta ei toimi, voidaan palata kohtaan ennen tuota. 

Se myös mahdollistaa asioiden kokeilemisen. Voit tehdä haaran, missä alat kokeilemaan uutta ominaisuutta. Voit myös todeta, että tätä ei ole järkevä totteuttaa näin, joten haaraan ei tarvitse yhdistää alkuperäiseen pisteeseen.

Harjoittelussa käytettiin tekoäly-kehitystä ja siinä se vasta tärkeää olikin, kun tekoälyn tekemät muutokset olivat mitä sattuu.

Aktiivisen sovelluksen/sivun kehittämisessä haarat mahdollistavat testaamisen, kehittämisen yms siten, ettei kaikki menen "suoraan tuotantoon" ja käyttäjien kiroiltaviksi. 

__Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?__

Lähdetään samasta tilanteesta kuin yksin kehittäessä, mutta tässä tilanteessa se on tärkeintä. Jokainen kehittää aina oman uuden haaransa (issuen) tehtävää. Kun tehtävä on saatu valmiiksi, on tärkeää, että projektia hallinnoi joku, joka arvioi sopiiko muutokset kokonaisuuteen vai meneekö jokin toiminto mahdollisesti rikki. Joskus voi myös käydä, että välissä on tapahtunut useampi merge jo välissä ja haaran koodi vaatii lisämuokkausta toimiakseen yhdessä.

Näissä tapauksissa huolehditaan yleensä myös koodin yhdenmukaisuudesta. On tärkeää, että kaikki kirjoittavat saman projektin koodin lähes samalla tavalla. Tällöin kokonaisuus on muille helpompaa luettavaa.

__Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.__

Yleiset säännöt ja ohjeet versionhallintaan (git):
- Projektissamme on main haara ja sen alla develop haara 
- Tehdään tehtävää koskeva oma haara aina developin alle ja pushataan valmis developiin. 
- Jokainen käy itse läpi mergen konfliktit, jos niitä on. Jos kohtaat ongelmia, mistä et ole varma. Keskeytä ja kysy projektin viestikanavalla asiasta. Voimme yhdessä tuumailla mitä tehdään. Jos joku tietää suoraan mitä pitää tehdä, hän saa antaa ohjeen eteenpäin ja sitä voi noudattaa. Työelämässä mergen varmaan aina hyväksyy joku muu, mutta tällä kurssilla tehdään oppimisen vuoksi näin. 
- Jokainen lukee viestikanvan viestit. Näin saadaan kaikki myös mahdollisimman paljon oppia tästä projektista. 
- Jokaisella sprintillä Scrum Master hoitaa developin yhdistämisen mainiin ja näihin liittyvät konfliktit. Scrum Master saa myös kysyä apua. 
- Sprintin lopuksi main haaran sisältö esitellään muille

__Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?__

Hyvähän tämä oli. Toisaalta on "paljon" kokemusta gitistä. Vuosi koulua ei vielä ole kovin paljoa, mutta paljon tässä on tullut asioita toistettua ja myös uusia asioita opittua. Toki näin pienellä toistolla ne eivät jää mieleen, jos niitä ei jatkuvasti tee uudestaan.

Rebase olisi voinut olla lisänä. Siihen en koulussa ole törmännyt vielä millään kursilla oikein kunnolla, mutta harjoittelussa sitä käytettiin tosi paljon - melkein aina. Varsinkin, kun harjoittelussa koodattiin tekoälyn avulla, niin materiaalia tuli nopeasti ja paljon. Rebase oli käytännössä jokaisessa mergessä käytössä.

Jossain tehtävissä jäin miettimään, mitä piti tehdä missäkin järjestyksessä. Usein se vastaus kyllä löytyi sieltä, mutta välillä piti tarkastaa tekoälyn avulla, että tarkoitetaanko tällä juuri tätä. Enemmän näissä taisi olla kyse siitä, että on jo jonkinlainen ajatus syntynyt siitä, missä järjestyksessä asiat toimii ja automaationa toteuttaa tiettyjä vaiheita, vaikka niitä ei tehtävässä pyydetä. Hyvää tietysti on, että näissä joutuu myös miettimään. Minulla esimerkiksi ei ollut yhdistetty styles.css index.html:n.. se oli yhdistetty johonkin toiseen .html tiedostoon jonka poistin. Vasta tuossa toiseksi viimeissä tehtävässä aloin ihmettelemään, kun oli kuva sivusta ja mietin, että eihän tämä nyt näin voi olla.  
 
 

