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