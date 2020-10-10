# Web-ohjelmointi

## 5.9.2020

Hajosin täysin HackMD-sivuston toimintaperiaatteisiin ja kyynistyn entisestään tätä alustaa kohtaan. Sain sentään liitettyä sen githubiin, jotta tässä olisi edes jotain koodaamisen makua. Mielummin olisin käyttänyt Github Pages...

++Demo 1 tehtävä 3++

Tehtävässä ei ollut itselle mitään uutta. Tehtävä vaati lähinnä kirjoittajan sormia, että jaksoi kaikki getterit ja setterit asettaa. Sijoitin tehtävän githubiin.

## 20.9.2020

Tein demot 2, jossa luotiin Node.js, Express, MySQL pohjainen API, jossa on GET, POST, PUT ja DELETE komennot tietokannalle *puhelinluettelo*, taulukolle *henkilot*.

Proseduurit toteutettiin suoraan tietokannan luovaan koodiin, jolloin niitä ei tarvinnut enää kirjoittaa javascript-tiedostoon (index.js), vaan niiden kutsuminen riitti. Proseduureja testattiin *root*-käyttäjällä.

Ymmärrykseni RESTistä, Expressistä ja Node.js'stä kasvoi ja opein jotenkuten myös käyttämään PostMania. Mielestäni **kirjallista** ohjeistusta näistä olisi voinut olla enemmän ja selkeämmin kirjoitettuna.

Mikäli tulevaisuudessa tulen työskentelemään APIen kanssa (epätodennäköistä), suunnittelisin ja toteuttaisin ne varmaan hieman eri tavalla, koska tämä tapa tuntui kömpelöhköltä.

## 26.9.2020

Tein frontendin puhelinluettelolle. JSON-osuus ja tietokannasta hakeminen oli uutta, kuten myös toiminnallinen CSS. Jälkimmäisestä olen ollut tietoinen, mutten ikinä kokeillut.

## 5.10.2020

Rakensin tietokannan ja osittain REST-backendin ohjelmalle. Hankaluuksia tuotti POST-metodin aikaisempi väärin ymmärrys. Jokaisen selaimen FETCH API:lla tämäkin selvisi. Yritin aluksi siis luoda POST-metodia siten, että URL koostuu tarvittavista tiedoista, jolloin tietenkin urheilijan kuvan www-osoite aiheutti ongelmia. Nyt POST toteutus tapahtuu HTML `<forms>` + FETCH + JSON.

Seuraavaksi jatkan backendin loppuun (päivitys ja poisto), jonka jälkeen luodaan vastaavat FETCH API -toteutukset niille.

Tämän jälkeen suoritan sivuston varsinaisen rakenteen suunnittelun ja Bootstrapin soveltamisen.

## 6. - 11.10.2020

Backendin kanssa oli muutamia ongelmia, koska en ajattellut muuttujien nimien olevan niin tarkkoja, joten käytin muotoa \_muuttujannimi, joka johti siihen, että oikeat arvot eivät tallentuneet oikeisiin paikkoihin.

Seuraavia ongelmia tuotti muutamat kirjoitusvirheet, joista nettikielet eivät varoita, joka on uskomattoman raivostuttavaa. Tämänkin ajan olisin saanut käytettyä paremmin, jos virheilmoituksissa olisi kerrottu minulla lukevan "componen" eikä "component". Edes punaista alleviivausta en saanut...

Sitten ongelmia aiheutti tiedon vieminen tietokantaan. Jostain syysta MariaDB kanssa lukutiedon vieminen suoraan tietokantaan on vähintäänkin haastavaa, joten päädyin tietojen säilömiseen VARCHAReina.

Kun kaikki oli saatu toimimaan, oli aika säätää bootstrapin ja tavallisen CSS'n kanssa. Tein svg-logon sivulle ja yritin laittaa sitä ::before-pseudoelementtinä, josta React ei ilmeisesti pitänyt. Jotta sain logon sivulle suunnilleen niin kuin alunperin suunnittelin, oli minun luotava sille oma komponentti koodiin. Tämä on yksi syy sille, miksi en tule jatkossa käyttämään minkäänlaisia frameworkeja; ne eivät vain ole toimiva ratkaisu ihmiselle, joka haluaa muokata kaikkea mielensä mukaan ja juuri sieltä mistä haluaa.

Bootstrapin CSS on myös paikoitellen ärsyttävää käyttää, kun jokaiseen elementtiin pitää laittaa sama class, sen sijaan että tekisi oman CSS-tiedoston, jossa voisi tarkemmin sorvia tyylit kohdileen. Toistaiseksi ainoa positiivinen kokemus Bootstrapin CSS'sta ja jQuerysta on drop-down menun tekeminen, joka tosin olisi sekin onnistunut helpommin tavallisella CSS'lla ja jQuerylla.

Kaiken kaikkiaan opein, että frameworkit ovat turhan rajoittavia omalta osaltani, mutta onneksi en niiden kanssa tule olemaan tekemisissä tämän kurssin ulkopuolella. Tälle kurssille vaadittavan ePortfolion tulen tekemään staattisena HTML-sivustona, jossa kuitenkin käytetään vaadittua Bootstrapia.