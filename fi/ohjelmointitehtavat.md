# Ohjelmointitehtävät

Voit käyttää samaa repositoriota (_repository_), jota käytit edellisen kurssin Python-tehtävissä.

Luo kansio jokaiselle moduulille ja jokaisen moduulin sisälle oma kansio jokaiselle tehtävälle. Tee jokaista tehtävää varten yksi HTML-tiedosto ja yksi JavaScript-tiedosto. Tiedostojen nimissä on oltava tehtävän numero. Kaiken HTML-koodin on oltava validia eli HTML-standardin mukaista.

Lisää JavaScript-tehtäviesi GitHub-repositorion `README.md`-tiedostoon linkit moduulikansioihisi users.metropolia.fi-palvelussa. Linkitä kansioihin, älä yksittäisiin tiedostoihin.

- [Verkkosivuston julkaisu Metropolian opiskelijoiden kotisivupalvelussa](https://metropolia-sw.github.io/webdev/04-website-deployment.html)
- [YouTube-ohjeet tiedostojen siirtämiseen palvelimelle](https://www.youtube.com/watch?v=CDXEu4piXRA&list=PLKenVLUxjmH-y89AiiI2xcXDy5QG83D4K&index=8)

## Esimerkkipalautus

Lisää `README.md`-tiedostoosi vastaava sisältö jokaisesta tehtävämoduulista:

```markdown
---

## Ohjelmisto 2 -ohjelmointitehtävät

### JS-moduulit 1 ja 2

[Linkki JS-moduulin 1 kansiooni users.metropolia.fi-palvelussa](https://users.metropolia.fi/~username/js1-folder)

Tehdyt tehtävät:

- Tehtävä 1: 2 p
- Tehtävä 4: 3 p
- Tehtävä 5: 6 p

**Yhteensä 11 p**

Kirjoita tähän huomiot mahdollisista ongelmista tai lisäominaisuuksista.

---

### JS-moduuli 3

[Linkki JS-moduulin 3 kansiooni users.metropolia.fi-palvelussa](https://users.metropolia.fi/~username/js2-folder)

Tehdyt tehtävät:

... ja niin edelleen ...
```

Palauta linkki OMA-palautustehtävään ohjeiden mukaisesti.

---

## Lue tämä ennen kuin jatkat

Voit valita tehtävät oman osaamistasosi mukaan. Huolehdi vain siitä, että teet riittävästi tehtäviä, jotta vaatimukset täyttyvät (vähintään 10 pistettä moduulia kohden). Mitä enemmän tehtävästä saa pisteitä, sitä haastavampi se on.

---

## JS-moduulit 1 ja 2: Vuorovaikutteiset ohjelmat ja ohjausrakenteet

1. Kirjoita ohjelma, joka [tulostaa konsoliin](05-js1-vuorovaikutteiset-ohjelmat.md#konsoli) tekstin `I'm printing to console!` (**1 p**)
2. Kirjoita ohjelma, joka [kysyy](05-js1-vuorovaikutteiset-ohjelmat.md#syötteen-lukeminen) käyttäjän nimeä ja tervehtii sitten käyttäjää. Tulosta tervehdys [HTML-dokumenttiin](05-js1-vuorovaikutteiset-ohjelmat.md#tulostus-verkkosivulle): `Hei, Nimi!` (**2 p**)
3. Kirjoita ohjelma, joka kysyy kolme kokonaislukua. Ohjelma tulostaa lukujen summan, tulon ja keskiarvon [HTML-dokumenttiin](05-js1-vuorovaikutteiset-ohjelmat.md#tulostus-verkkosivulle). (**3 p**)
   - Muista [muuntaa merkkijonot luvuiksi](05-js1-vuorovaikutteiset-ohjelmat.md#tyypin-muuttaminen) ennen kuin lasket ne yhteen.
4. Harry Potter -lastenkirjoissa lajitteluhattu sijoittaa Tylypahkan noitien ja velhojen koulun uuden oppilaan yhteen neljästä tuvasta, jotka ovat Rohkelikko, Luihuinen, Puuskupuh ja Korpinkynsi. Kirjoita sähköinen lajitteluhattu, joka kysyy oppilaan nimeä ja arpoo oppilaalle tuvan. Jos annat nimeksi esimerkiksi Anna, ohjelma tulostaa HTML-dokumenttiin ”Anna, sinä olet Korpinkynsi.” (**3 p**)
   - Käytä metodia [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) arvon (1, 2, 3 tai 4) arpomiseen.
   - Kun luku on arvottu, tarvitset valintarakenteen, jossa on useita vaihtoehtoja ([if, else if, ..., else tai switch](06-js2-ohjausrakenteet.md#valintarakenteet)).
5. Kirjoita ohjelma, joka pyytää käyttäjää syöttämään vuosiluvun ja ilmoittaa, onko vuosi karkausvuosi. Vuosi on karkausvuosi, jos se on jaollinen neljällä. Sadalla jaolliset vuodet ovat kuitenkin karkausvuosia vain, jos ne ovat jaollisia myös neljälläsadalla. Tulosta tulos HTML-dokumenttiin. (**3 p**)
6. Kirjoita ohjelma, joka näyttää vahvistusikkunassa tekstin ”Lasketaanko neliöjuuri?”. Jos käyttäjä valitsee OK, ohjelma kysyy luvun, laskee sen neliöjuuren ja tulostaa neliöjuuren HTML-dokumenttiin. Jos käyttäjä valitsee Cancel, ohjelma tulostaa HTML-dokumenttiin tekstin ”Neliöjuurta ei lasketa.” (**3 p**)
   - Vahvistusikkunan saat näkyviin funktiolla [confirm()](08-js4-dom-ja-tapahtumat.md#confirm). Funktio palauttaa arvon `true`, jos käyttäjä valitsee OK, ja arvon `false`, jos käyttäjä valitsee Cancel.
   - Negatiivisen luvun neliöjuurta ei voi laskea. Jos käyttäjän syöttämä luku on negatiivinen, ohjelma tulostaa HTML-dokumenttiin ”Negatiivisen luvun neliöjuurta ei ole määritelty.”
7. Kirjoita ohjelma, joka heittää noppaa käyttäjän antaman määrän kertoja ja näyttää heittojen silmälukujen summan. (**2 p**)
   - Ensin ohjelma kysyy käyttäjältä, montako kertaa noppaa heitetään.
   - Sitten ohjelma heittää noppaa niin monta kertaa kuin käyttäjä antoi.
   - Tulosta silmälukujen summa konsoliin tai HTML-dokumenttiin.
8. Kirjoita ohjelma, joka kysyy käyttäjältä alku- ja loppuvuoden. Ohjelma tulostaa kaikki karkausvuodet käyttäjän antamalta väliltä. Tulosta vuodet HTML-dokumenttiin järjestämättömänä luettelona (`<ul>`). (**3 p**)
   - Esimerkki tulosteen HTML-koodista:
   ```html
   <ul>
     <li>1992</li>
     <li>1996</li>
     <li>2000</li>
     <li>2004</li>
     <li>2008</li>
   </ul>
   ```
9. Kirjoita ohjelma, joka kysyy käyttäjältä kokonaisluvun ja kertoo, onko luku alkuluku. (**2 p**)
   - Alkuluku on ykköstä suurempi kokonaisluku, joka on jaollinen vain luvulla 1 ja itsellään.
   - Esimerkiksi 13 on alkuluku, koska sen voi jakaa vain luvuilla 1 ja 13 niin, että tulos on kokonaisluku.
   - Sen sijaan esimerkiksi 21 ei ole alkuluku, koska sen voi jakaa myös luvuilla 3 ja 7.
   - Tulosta tulos HTML-dokumenttiin.
10. Kirjoita ohjelma, joka kysyy käyttäjältä noppien lukumäärän ja silmälukujen summan, josta käyttäjä on kiinnostunut. Ohjelma selvittää, millä todennäköisyydellä annettu määrä noppia tuottaa annetun silmälukujen summan. Jos käyttäjä esimerkiksi syöttää noppien lukumääräksi 3 ja silmälukujen summaksi 17, ohjelma laskee todennäköisyyden sille, että kolmen nopan silmälukujen summa on 17. (**5 p**)
    - Ratkaise ongelma simuloimalla: heitä annettua määrää noppia for-silmukassa monta kertaa (esim. 10 000 kertaa) ja laske, kuinka suuressa osassa heittokerroista silmälukujen summa oli käyttäjän antama summa.
    - Tulosta tulos HTML-dokumenttiin:
    ```text
    Todennäköisyys saada summa 7 kahdella nopalla on 15.64%
    ```

    - Voit rajoittaa desimaalien määrää metodilla [toFixed()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed).
    - Testiarvoja:
      - 2 noppaa, summa 7: todennäköisyys on noin 15–17 %
      - 3 noppaa, summa 15: todennäköisyys on noin 5 %

---

## JS-moduuli 3: Taulukot ja funktiot

1. Kirjoita ohjelma, joka kysyy käyttäjältä viisi lukua ja tulostaa ne päinvastaisessa järjestyksessä kuin käyttäjä ne syötti (ei siis suuruusjärjestyksessä). Tulosta tulos konsoliin. (**2 p**)
   - Tallenna luvut taulukkoon ja käy taulukko sitten for-silmukalla läpi lopusta alkuun.
   - Älä käytä metodia `array.reverse()`.
2. Kirjoita ohjelma, joka kysyy käyttäjältä osallistujien lukumäärän. Tämän jälkeen ohjelma kysyy kaikkien osallistujien nimet. Lopuksi ohjelma tulostaa osallistujien nimet verkkosivulle numeroituna luettelona (`<ol>`) aakkosjärjestyksessä. (**2 p**)
3. Kirjoita ohjelma, joka kysyy kuuden koiran nimet. Ohjelma tulostaa koirien nimet järjestämättömään luetteloon (`<ul>`) käänteisessä aakkosjärjestyksessä. (**2 p**)
4. Kirjoita ohjelma, joka kysyy käyttäjältä lukuja, kunnes käyttäjä syöttää nollan. Ohjelma tulostaa annetut luvut konsoliin suurimmasta pienimpään. (**2 p**)
5. Kirjoita ohjelma, joka kysyy käyttäjältä lukuja. Kun käyttäjä syöttää luvun, jonka hän on jo aiemmin syöttänyt, ohjelma ilmoittaa, että luku on jo annettu, lopettaa toimintansa ja tulostaa kaikki annetut luvut konsoliin nousevassa järjestyksessä. (**2 p**)
6. Kirjoita funktio, joka palauttaa satunnaisen nopanheiton tuloksen väliltä 1–6. Funktiolla ei saa olla parametreja. Kirjoita pääohjelma, joka heittää noppaa, kunnes tulos on 6. Pääohjelman on tulostettava jokaisen heiton tulos järjestämättömään luetteloon (`<ul>`). (**2 p**)
7. Muokkaa edellistä funktiota niin, että sillä on parametri, joka kertoo nopan tahkojen lukumäärän. Muokatulla funktiolla voit heittää esimerkiksi 21-tahkoista roolipelinoppaa. Toisin kuin edellisessä tehtävässä, pääohjelma heittää noppaa, kunnes tulos on nopan suurin silmäluku. Pääohjelma kysyy tahkojen lukumäärän käyttäjältä ohjelman alussa. (**2 p**)
8. Kirjoita funktio nimeltä `concat()`, jonka parametri on merkkijonoja sisältävä taulukko. Funktio palauttaa merkkijonon, joka muodostetaan yhdistämällä taulukon alkiot toisiinsa. (**2 p**)
   - Esimerkki: Nelialkioisessa taulukossa ovat alkiot Johnny, DeeDee, Joey ja Marky. Funktio palauttaa merkkijonon JohnnyDeeDeeJoeyMarky.
   - Älä käytä metodia `array.join()`.
   - Voit kirjoittaa taulukon suoraan koodiin. `prompt()`-funktiota ei tarvita.
   - Tulosta tulos HTML-dokumenttiin.
9. Kirjoita funktio nimeltä `even()`, jonka parametri on lukuja sisältävä taulukko. Funktio palauttaa uuden (yleensä lyhyemmän) taulukon, jossa ovat alkuperäisen taulukon parilliset luvut. Funktio ei saa muuttaa alkuperäistä taulukkoa. (**3 p**)
   - Esimerkki: Kolmialkioisessa taulukossa ovat alkiot 2, 7 ja 4. Funktio palauttaa kaksialkioisen taulukon, jossa ovat alkiot 2 ja 4.
   - Tulosta pääohjelmassa funktiokutsun jälkeen sekä alkuperäinen että uusi taulukko konsoliin.
   - Voit kirjoittaa taulukon suoraan koodiin. `prompt()`-funktiota ei tarvita.
10. Kirjoita alla kuvattu äänestysohjelma pienimuotoiseen kokouskäyttöön. (**8 p**)
    - Ohjelma kysyy ehdokkaiden lukumäärän.
    - Sitten ohjelma kysyy ehdokkaiden nimet: `Ehdokkaan 1 nimi`
    - Tallenna jokaisen ehdokkaan nimi ja äänimäärän alkuarvo omaan olioonsa ja oliot taulukkoon näin:

      ```javascript
      [
        {
          name: "ellie",
          votes: 0,
        },
        {
          name: "frank",
          votes: 0,
        },
        {
          name: "pamela",
          votes: 0,
        },
      ];
      ```

    - Ohjelma kysyy äänestäjien lukumäärän.
    - Ohjelma kysyy vuorotellen jokaiselta äänestäjältä, ketä hän äänestää. Äänestäjä syöttää ehdokkaan nimen. Jos äänestäjä jättää nimen syöttämättä, ääni tulkitaan tyhjäksi.
    - Ohjelma tulostaa konsoliin voittajan nimen ja tulokset:

      ```text
      Voittaja on pamela 3 äänellä.
      tulokset:
      pamela: 3 ääntä
      frank: 1 ääntä
      ellie: 1 ääntä
      ```

    - Vähän apua:

    ```javascript
    // Vertaile äänimääriä. Tulosta a ja b konsoliin, niin näet, miten pääset käsiksi oikeaan ominaisuuteen.
    someArray.sort((a, b) => {
      console.log(a, b);
      return b - a;
    });
    ```

---

## JS-moduuli 4: DOM ja tapahtumat

[Lataa tämä ZIP-tiedosto](../assets/dom-starters.zip), pura se ja siirrä sisältö kansioon, jossa ovat muut tämän kurssin tiedostosi.

1. Avaa kansio `t1` kehitysympäristössäsi tai editorissasi. Lisää HTML-koodia `innerHTML`-ominaisuuden (_property_) avulla. (**2 p**)
   - Lisää seuraava HTML-koodi elementtiin, jolla on `id="target"`:
   ```html
   <li>First item</li>
   <li>Second item</li>
   <li>Third item</li>
   ```

   - Lisää samalle elementille luokka `my-list`.
2. Avaa kansio `t2` kehitysympäristössäsi tai editorissasi. Lisää HTML-koodia metodien `createElement()` ja `appendChild()` avulla. (**2 p**)
   - Lisää seuraava HTML-koodi elementtiin, jolla on `id="target"`:
   ```html
   <li>First item</li>
   <li>Second item</li>
   <li>Third item</li>
   ```

   - Lisää luettelon toiselle `<li>`-elementille luokka `my-item`.
3. Avaa kansio `t3` kehitysympäristössäsi tai editorissasi. Lisää HTML-koodia `innerHTML`-ominaisuuden avulla. (**2 p**)
   - Lisää seuraava HTML-koodi elementtiin, jolla on `id="target"`. Lisää `names`-taulukon arvot `<li>`-elementteihin for-silmukassa.
   ```html
   <li>John</li>
   <li>Paul</li>
   <li>Jones</li>
   ```
4. Avaa kansio `t4` kehitysympäristössäsi tai editorissasi. Lisää HTML-koodia metodien `createElement()` ja `appendChild()` avulla. (**2 p**)
   - Lisää seuraava HTML-koodi elementtiin, jolla on `id="target"`. Lisää `students`-taulukon arvot `<option>`-elementteihin for-silmukassa.
   ```html
   <option value="2345768">John</option>
   <option value="2134657">Paul</option>
   <option value="5423679">Jones</option>
   ```

   - Näet koko lopputuloksen selaimen kehittäjätyökalujen (_developer tools_) elementtitarkastimesta: napsauta sivua hiiren oikealla painikkeella ja valitse Tarkista (_Inspect_).
5. Avaa kansio `t5` kehitysympäristössäsi tai editorissasi. Luo useita `<article>`-elementtejä, joissa on otsikko, kuva, kuvateksti ja kuvaus. Täytä ne `picArray`-taulukon tiedoilla. Lisää `<article>`-elementit `<section>`-elementtiin. (**5 p**)
   - Jokaisen `<article>`-elementin rakenteen on oltava tällainen:
   ```html
   <article class="card">
     <h2>title_from_picArray</h2>
     <figure>
       <img src="medium_image_from_picArray" alt="title_from_picArray" />
       <figcaption>caption_from_picArray</figcaption>
     </figure>
     <p>description_from_picArray</p>
   </article>
   ```
6. Avaa kansio `t6` kehitysympäristössäsi tai editorissasi. Tee skripti, joka avaa ilmoitusikkunan tekstillä ”Button Clicked”, kun `<button>`-elementtiä napsautetaan. (**1 p**)
7. Avaa kansio `t7` kehitysympäristössäsi tai editorissasi. Tee JavaScriptillä hover-efekti eli muutos, joka tapahtuu, kun hiiri viedään elementin päälle. (**2 p**)
   - Kun käyttäjä vie hiiren `<p id="trigger">`-elementin päälle, vaihda `<img id="target">`-elementin kuva `picA.jpg`:stä `picB.jpg`:hen.
   - Kun käyttäjä vie hiiren pois elementin päältä, vaihda kuva takaisin alkuperäiseksi.
8. Avaa kansio `t8` kehitysympäristössäsi tai editorissasi. Tee yksinkertainen laskin. (**4 p**)
   - Sivulla on kaksi syötekenttää, joihin käyttäjä syöttää luvut. Pudotusvalikon valinnan perusteella laskin laskee näiden kahden luvun summan, erotuksen, tulon tai osamäärän.
   - Päättele valitun `<option>`-elementin `value`-attribuutin perusteella, mikä laskutoimitus laskimen pitää tehdä. [Esimerkki.](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_select_value2)
   - Näytä tulos `<p id="result">`-elementissä, kun painiketta napsautetaan.
9. Avaa kansio `t9` kehitysympäristössäsi tai editorissasi. Tämä on jatkoa edelliselle tehtävälle. Nyt sivulla on vain yksi syötekenttä, johon käyttäjä kirjoittaa koko laskutoimituksen (yhteen-, vähennys-, kerto- tai jakolasku). (**4 p**)
   - Voit käyttää metodeja [includes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes) ja [split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split).
   - Älä käytä `eval()`-funktiota.
   - Desimaalilukuja ei tarvitse tukea. Riittää, että laskin toimii kokonaisluvuilla.
   - Esimerkkisyötteitä: `3+5`, `2-78`, `3/6` jne.
10. Avaa kansio `t10` kehitysympäristössäsi tai editorissasi. Lue etu- ja sukunimi lomakkeelta ja tulosta ne `<p id="target">`-elementtiin. (**2 p**)
    - Muista estää lomakkeen oletustoiminto eli lomakkeen lähettäminen, joka lataa sivun uudelleen.
    - Voit valita `<input>`-elementit `querySelector()`-metodilla käyttämällä [attribuuttivalitsimia](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) (_attribute selector_).
    - Esimerkkituloste: `Nimesi on Luke Skywalker`
11. Jatka tehtävää 5. Kansio `t11` on jo olemassa. Noudata tiedoston `t11.txt` ohjeita. Muokkaa ohjelmaa niin, että suuri kuva avautuu [modaali-ikkunaan](#modal), kun `<article>`-elementtiä napsautetaan. (**6 p**) - Jos loit `<article>`-elementin sisältöineen `innerHTML`-ominaisuudella, saatat tässä kohtaa katua sitä. - Lisää seuraava HTML-koodi käsin HTML-dokumenttiin tagien `</div>` ja `</body>` väliin (ei JavaScriptillä):
`html
    <dialog>
       <span>&#x2715;</span>
       <img>
    </dialog>
    ` - `picArray`-taulukon jokaisella kohteella on kaksi kuvaa: medium ja large. Medium-kuvaa käytetään `<article>`-elementin sisällä olevassa `<img>`-elementissä ja large-kuvaa `<dialog>`-elementin sisällä olevassa `<img>`-elementissä. - Käytä metodeja [showModal() ja close()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement#instance_methods) `<dialog>`-elementin näyttämiseen ja piilottamiseen. - Kun avaat modaali-ikkunan, aseta suuri kuva modaali-ikkunan `<img>`-elementtiin. - Muista lisätä `alt`-attribuutti. - Käytä `<dialog>`-elementin sisällä olevaa `<span>`-elementtiä modaali-ikkunan sulkemiseen.
<hr>
<sub id="modal"><sup>- Modaali-ikkuna (<i>modal</i>) on dialogi- tai ponnahdusikkuna, joka näytetään sivun päällä. Sivun muuta sisältöä ei voi käyttää, ennen kuin ikkuna suljetaan.</sup></sub>

---

## Python Flask -palvelin

1. Toteuta Flask-taustapalvelu (_backend_), joka kertoo, onko URL-osoitteessa annettu luku alkuluku vai ei. Käytä pohjana aiempaa alkulukutehtävää. Esimerkiksi luvun 31 GET-pyyntö (_request_) lähetetään osoitteeseen `http://127.0.0.1:3000/prime_number/31`. Vastauksen (_response_) on oltava muotoa `{"Number": 31, "isPrime": true}`. (**4 p**)

2. Toteuta Flask-taustapalvelu, joka saa URL-osoitteessa englanninkielisen sanan ja palauttaa sen suomenkielisen käännöksen JSON-muodossa. Tallenna englanti–suomi-sanakirja levylle erilliseen JSON-tiedostoon. (**10 p**)
   - Esimerkiksi sanan ”hello” GET-pyynnön `http://127.0.0.1:3000/translate/hello` on palautettava:

   ```json
   {
     "English": "hello",
     "Finnish": "hei"
   }
   ```

   - Tallenna sanakirja erilliseen `dictionary.json`-tiedostoon näin (lisää sanoja):

   ```json
   {
      "hello": "hei",
      "computer": "tietokone",
      "school": "koulu",
      ... lisää sisältöä tähän ...
   }
   ```

   - Haku ei saa erotella isoja ja pieniä kirjaimia.
   - Jos sanaa ei löydy, palauta JSON-muotoinen virheilmoitus HTTP-tilakoodilla 404, esimerkiksi:

   ```json
   {
     "error": "Word not found"
   }
   ```

   - Vapaaehtoinen: Toteuta päätepiste (_endpoint_) `/words`, joka palauttaa kaikki saatavilla olevat _englanninkieliset_ sanat JSON-taulukkona.

3. Toteuta Flask-taustapalvelu, joka lisää sanakirjaan uusia sanoja. (**6 p**)
   - Englanninkielinen sana ja sen suomennos lähetetään palvelimelle samassa HTTP-pyynnössä. Oikea metodi tähän olisi POST, mutta tässä tehtävässä saat käyttää GET-metodia. Esimerkki: `GET http://127.0.0.1:3000/add?en=book&fi=kirja`
   - Palvelin tallentaa uudet sanat levylle lisäämällä ne `dictionary.json`-tiedostoon.

---

## JS-moduuli 5: AJAX

1. Tee sovellus, joka hakee tietoja syöttämästäsi TV-sarjasta ja tulostaa ne konsoliin. (**2 p**)
   - Käytettävä rajapinta (_API_): [TVMaze API](http://www.tvmaze.com/api#show-search)
   - Tee ensin validi HTML-sivu, jolla on hakulomake. Esimerkkilomake:
   ```html
   <form action="https://api.tvmaze.com/search/shows">
     <input id="query" name="q" type="text" />
     <input type="submit" value="Search" />
   </form>
   ```

   - Testaa lomaketta. Selaimen pitäisi näyttää sivu, joka on täynnä JSON-muotoista dataa.
2. Kehitä sovellusta eteenpäin.
   - Lisää JavaScript-koodi, joka lukee lomakkeeseen syötetyn arvon ja lähettää [fetch-funktiolla](10-js5-ajax-ja-rajapinnat.md#tässä-sama-esimerkki-mutta-nyt-lentokentän-koodi-syötetään-lomakkeella) pyynnön osoitteeseen `https://api.tvmaze.com/search/shows?q=${value_from_input}`. Tulosta hakutulos konsoliin. (**3 p**)
3. Kehitä sovellusta vielä pidemmälle. Tulosta verkkosivulle seuraavat tiedot kaikista hakutuloksen sarjoista. (**7 p**)
   - Vaaditut tiedot: nimi, linkki lisätietoihin (url), keskikokoinen kuva (medium) ja tiivistelmä (summary).
   - Näytä nimi `<h2>`-elementissä.
   - Näytä linkki `<a>`-elementissä. Lisää linkkiin myös attribuutti `target="_blank"`, jotta linkki avautuu uuteen välilehteen.
   - Näytä keskikokoinen kuva elementillä `<img src="" alt="">`. Aseta keskikokoisen kuvan osoite `src`-attribuuttiin ja `name`-ominaisuuden arvo `alt`-attribuuttiin.
   - Joillakin TV-sarjoilla ei ole kuvaa. Silloin `image`-ominaisuuden arvo on `null`, ja `medium`-ominaisuuden lukeminen aiheuttaa virheen. Voit korjata virheen käyttämällä `image`-ominaisuuden perässä `?.`-operaattoria. Esimerkki: `tvShow.show.image?.medium;`. Tätä kutsutaan nimellä [valinnainen ketjutus](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining) (_optional chaining_).
   - Näytä tiivistelmä `<div>`-elementissä (ei `<p>`-elementissä). Tiivistelmä on nimittäin jo valmiiksi `<p>`-elementin sisällä, eikä HTML-koodi ole validia, jos `<p>`-elementti on toisen `<p>`-elementin sisällä.
   - Kokoa kunkin sarjan elementit omaan `<article>`-elementtiinsä ja lisää `<article>`-elementit HTML-dokumenttiin.
     - Lisää HTML-dokumenttiin `<div id="results">`-elementti, johon lisäät `<article>`-elementit.
   - Tyhjennä vanhat tulokset komennolla `innerHTML = ''` ennen kuin lisäät uudet tulokset.
4. Kehitä sovellusta vielä pidemmälle. Valinnainen ketjutus ei ole paras tapa käsitellä puuttuvaa kuvaa. Käytä [ehdollista operaattoria](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) (_ternary operator_) tai if/else-rakennetta ja näytä oletuskuva, jos TV-sarjalta puuttuu `image`-ominaisuuden arvo. (**2 p**)
   - Käytä oletuskuvana osoitetta `https://placehold.co/210x295?text=Not%20Found`.
5. Tee sovellus, joka hakee satunnaisen Chuck Norris -vitsin ja tulostaa sen konsoliin. (**2 p**)
   - Käytettävä rajapinta: [chucknorris.io](https://api.chucknorris.io/)
   - Lähetä pyyntö osoitteeseen `https://api.chucknorris.io/jokes/random` ja tulosta konsoliin pelkkä vitsi (eli `value`-ominaisuuden arvo).
   - Lomaketta ei tarvita.
6. Kehitä sovellusta eteenpäin. (**4 p**)
   - Lisää nyt lomake, johon voit syöttää hakusanan samaan tapaan kuin tehtävissä 1–3.
   - Lähetä hakusana `fetch()`-funktiolla osoitteeseen `https://api.chucknorris.io/jokes/search?query=${value_from_input}`.
   - Tulosta jokainen vitsi tässä muodossa:
   ```html
   <article>
     <p>Vitsi tähän</p>
   </article>
   ```
7. Haastava **lisätehtävä**: reittihaku [Digitransit-rajapinnalla](https://digitransit.fi/en/developers/apis/1-routing-api/) (**16 p**)
   - **Ei heikkohermoisille.** Älä tee tätä, jos se vie aikaa projektityöltä. Se ei kannata.
   - Tee sovellus, joka näyttää reitin käyttäjän antamasta osoitteesta koululle (Karaportti 2).
   - Tarvitset lomakkeen, johon käyttäjä syöttää osoitteen. Kun lomake lähetetään, reitti näytetään kartalla. Näytä myös matkan lähtö- ja saapumisaika. Näytä vain koko matkan alku- ja loppuaika, _ei_ jokaisen osuuden aikoja erikseen.
   - Esimerkki: [JS](../api-examples/js/esim4.js), [HTML](../api-examples/esim4.html)
     - Tarvitset [tämän lisäosan Leaflet-karttakirjastoon](../api-examples/js/Polyline.encoded.js), jotta esimerkki toimii.
   - [Tässä on esimerkki](https://digitransit.fi/en/developers/apis/1-routing-api/itinerary-planning/#basic-route-from-kamppi-helsinki-to-pisa-espoo) siitä, miten reitin paikat tai osoitteet annetaan koordinaatteina.
     - Osoitteen koordinaatit saat [osoitehaulla](https://digitransit.fi/en/developers/apis/2-geocoding-api/address-search/).
   - Jos saat CORS-virheitä (mikä _ei_ todennäköisesti tapahdu), [käytä tätä korjausta](https://github.com/ilkkamtk/corsfix). CORS-virhe tarkoittaa, että selain estää pyynnön, koska rajapinnan palvelin ei salli pyyntöjä sinun sivustoltasi.
