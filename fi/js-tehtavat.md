# Tehtävät

Luo jokaiselle moduulille oma kansio ja luo jokaisen moduulin sisälle kansio jokaiselle tehtävälle. Luo jokaiselle tehtävälle yksi HTML- ja JavaScript-tiedosto. Tiedostonimien tulee sisältää tehtävän numero. Kaiken HTML:n tulee olla validia. Palauta linkit, jotka osoittavat users.metropolia.fi-palvelussa moduulin kansioon (ei yksittäisiin tiedostoihin), sekä JavaScript-tehtäviesi GitHub-repositorioon.

- [YouTube-ohjeet lataamiseen](https://www.youtube.com/watch?v=CDXEu4piXRA&list=PLKenVLUxjmH-y89AiiI2xcXDy5QG83D4K&index=8)
- [webdisk.metropolia.fi](https://webdisk.metropolia.fi/) -palvelua voidaan myös käyttää tehtävien lataamiseen

---

### Esimerkkipalautus:

[Linkki users.metropolia.fi-palveluun](https://users.metropolia.fi/~username/folder)

[Linkki GitHubiin](https://github.com/username/repository)

Tehdyt tehtävät:

1, 2p<br>
4, 3p<br>
5, 6p

**Yhteensä 11p**

---

## Lue tämä ennen jatkamista

Voit valita taitotasosi perusteella, mitkä tehtävät haluat tehdä. Pyri tekemään vähintään noin 10 pisteen edestä tehtäviä (eli vähintään 40 %). Mitä enemmän pisteitä tehtävästä on saatavilla, sitä haastavampi se on.

## Moduuli 1. Interaktiiviset ohjelmat + ehtolausekkeet ja silmukat

1. Kirjoita ohjelma, joka [tulostaa konsoliin](05-js1-interactive-programs.md#console-log) tekstin: `I'm printing to console!` (**1p**)

2. Kirjoita ohjelma, joka [kysyy](05-js1-interactive-programs.md#feed-reading) käyttäjän nimeä ja tervehtii sitten käyttäjää. Tulosta tulos [HTML-dokumenttiin](05-js1-interactive-programs.md#printing-into-a-web-page): `Hello, Name!` (**2p**)
3. Kirjoita ohjelma, joka pyytää kolme kokonaislukua. Ohjelma tulostaa lukujen summan, tulon ja keskiarvon [HTML-dokumenttiin](05-js1-interactive-programs.md#printing-into-a-web-page). (**3p**)

- muista [muuntaa merkkijonot luvuiksi](05-js1-interactive-programs.md#changing-the-type), kun lasket niitä yhteen.

4. Harry Potter -lastenkirjoissa lajitteluhattu sijoittaa uuden opiskelijan Tylypahkan noitien ja velhojen kouluun yhteen neljästä tuvasta, jotka ovat Gryffindor, Slytherin, Hufflepuff ja Ravenclaw. Kirjoita sähköinen lajitteluhattu, joka kysyy opiskelijan nimen ja arpoo hänelle tuvan. Jos esimerkiksi nimeksi annetaan Anna, ohjelma tulostaa HTML-dokumenttiin "Anna, you are Ravenclaw." (**3p**)

- Käytä [math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)-funktiota arvomaan arvo (1, 2, 3 tai 4)
- Kun numero on arvottu, sinun tulee käyttää monivalintarakennetta ([if, else if, ..., else tai switch](06-js2-control-structures.md#conditional-expressions)).

5. Kirjoita ohjelma, joka pyytää käyttäjää syöttämään vuoden ja ilmoittaa, onko syötetty vuosi karkausvuosi. Vuosi on karkausvuosi, jos se on jaollinen neljällä. Kuitenkin sadalla jaolliset vuodet ovat karkausvuosia vain, jos ne ovat myös jaollisia 400:lla. Tulosta tulos HTML-dokumenttiin. (**3p**)
6. Kirjoita ohjelma, joka tulostaa vahvistusikkunaan tekstin "Should I calculate the square root?". Jos käyttäjä valitsee OK, ohjelma pyytää luvun ja laskee ja tulostaa sen neliöjuuren HTML-dokumenttiin. Jos käyttäjä valitsee Cancel, ohjelma tulostaa tekstin "The square root is not calculated." HTML-dokumenttiin (**3p**)

- Vahvistusikkuna voidaan näyttää [confirm()](08-js4-dom-events.md#confirm)-funktiolla. Funktio palauttaa true, jos käyttäjä valitsee OK. Jos käyttäjä valitsee Cancel, funktio palauttaa false.
- Negatiivisen luvun neliöjuurta ei voi laskea. Jos käyttäjän syöttämä luku on negatiivinen, ohjelma tulostaa HTML-dokumenttiin "The square root of a negative number is not defined".

7. Tee ohjelma, joka heittää käyttäjän määrittelemän määrän noppia ja näyttää nopanheittojen tulosten summan.(**2p**)

- Ensin ohjelma kysyy käyttäjältä nopanheittojen määrän.
- Sen jälkeen ohjelma heittää noppaa niin monta kertaa kuin käyttäjä määritteli.
- Tulosta tulosten summa konsoliin tai HTML-dokumenttiin.

8. Kirjoita ohjelma, joka pyytää käyttäjältä alku- ja loppuvuoden. Ohjelma tulostaa kaikki käyttäjän antaman aikavälin karkausvuodet. Tulostus tehdään järjestämättömänä listana HTML-dokumenttiin. (**3p**)

- Esimerkki tulostettavasta HTML-koodista:

```html
<ul>
  <li>1992</li>
  <li>1996</li>
  <li>2000</li>
  <li>2004</li>
  <li>2008</li>
</ul>
```

9. Kirjoita ohjelma, joka pyytää käyttäjältä kokonaisluvun ja kertoo, onko luku alkuluku. (**2p**)

- Alkuluvut ovat lukuja, jotka ovat jaollisia vain yhdellä ja itsellään.
- Esimerkiksi luku 13 on alkuluku, koska se voidaan jakaa vain luvulla 1 tai 13 siten, että tulos on kokonaisluku.
- Toisaalta esimerkiksi luku 21 ei ole alkuluku, koska se voidaan jakaa myös luvuilla 3 ja 7.
- Tulosta tulos HTML-dokumenttiin.

10. Tee ohjelma, joka kysyy käyttäjältä noppien määrän ja käyttäjää kiinnostavan silmälukujen summan. Ohjelman tarkoituksena on selvittää, millä todennäköisyydellä käyttäjän antama noppien määrä tuottaa käyttäjän antaman silmälukujen summan. Jos käyttäjä esimerkiksi syöttää noppien määräksi 3 ja silmälukujen summaksi 17, ohjelma laskee todennäköisyyden sille, että kolmen nopan silmälukujen summa on 17. (**5p**)

- Ratkaise ongelma simuloimalla: anna ohjelman heittää annettua määrää noppia for-silmukassa (esimerkiksi 10 000 kertaa) ja laskea, kuinka suuri osuus toistoista tuotti käyttäjän haluaman silmälukujen summan.
- Tulosta tulos HTML-dokumenttiin:

```text
Probability to get sum 7 with 2 dice is 15.64%
```

```
\- voit rajoittaa desimaalien määrää [toFixed()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed)-funktiolla
\- testiarvot:
  \- 2 noppaa, summa 7, todennäköisyys noin 15–17 %
  \- 3 noppaa, summa 15, todennäköisyys noin 5 %
```

## Moduuli 2. Taulukot ja funktiot

1. Kirjoita ohjelma, joka pyytää käyttäjältä viisi lukua ja tulostaa ne käänteisessä järjestyksessä kuin ne syötettiin (ei käänteisessä järjestyksessä lajiteltuna). Tulosta tulos konsoliin.(**2p**)

- Tallenna luvut taulukkoon ja käytä sitten for-silmukkaa niiden läpikäymiseen käänteisessä järjestyksessä.
- Älä käytä array.reverse()-funktiota.

2. Kirjoita ohjelma, joka kysyy käyttäjältä osallistujien määrän. Tämän jälkeen ohjelma kysyy kaikkien osallistujien nimet. Lopuksi ohjelma tulostaa osallistujien nimet verkkosivulle aakkosjärjestyksessä järjestettynä listana (`<ol>`). (**2p**)
3. Kirjoita ohjelma, joka kysyy kuuden koiran nimet. Ohjelma tulostaa koirien nimet järjestämättömään listaan `<ul>` käänteisessä aakkosjärjestyksessä. (**2p**)
4. Kirjoita ohjelma, joka kysyy käyttäjältä lukuja, kunnes käyttäjä antaa nollan. Annetut luvut tulostetaan konsoliin suurimmasta pienimpään. (**2p**)
5. Kirjoita ohjelma, joka pyytää käyttäjältä lukuja. Kun käyttäjä syöttää jonkin aiemmin syötetyistä luvuista, ohjelma ilmoittaa, että luku on jo annettu, ja lopettaa toimintansa. Tämän jälkeen kaikki annetut luvut tulostetaan konsoliin nousevassa järjestyksessä. (**2p**)
6. Kirjoita funktio, joka palauttaa satunnaisen nopanheiton väliltä 1–6. Funktiolla ei saa olla parametreja. Kirjoita pääohjelma, joka heittää noppaa, kunnes tulos on 6. Pääohjelman tulee tulostaa jokaisen heiton tulos järjestämättömään listaan (`<ul>`). (**2p**)
7. Muokkaa yllä olevaa funktiota siten, että se saa nopan sivujen määrän parametrina. Muokatulla funktiolla voit esimerkiksi heittää 21-sivuista roolipelinoppaa. Erona edelliseen tehtävään on se, että pääohjelman nopanheitto jatkuu, kunnes ohjelma saa nopan suurimman mahdollisen silmäluvun, joka kysytään käyttäjältä ohjelman alussa. (**2p**)
8. Kirjoita funktio nimeltä `concat()`, joka vastaanottaa merkkijonojen taulukon parametrina. Funktio palauttaa merkkijonon, joka muodostetaan yhdistämällä taulukon alkiot. (**2p**)

- Esimerkki: Neljän alkion taulukossa ovat alkiot Johnny, DeeDee, Joey ja Marky. Funktio palauttaa merkkijonon JohnnyDeeDeeJoeyMarky.
- Älä käytä `array.join()`-funktiota
- Voit määritellä taulukon suoraan koodiin, `prompt()`-funktiota ei tarvitse käyttää.
- Tulosta tulos HTML-dokumenttiin.

9. Kirjoita funktio nimeltä `even()`, joka vastaanottaa parametrina lukuja sisältävän taulukon. Funktio palauttaa toisen (yleensä pienemmän) taulukon, joka sisältää alkuperäisen taulukon parilliset luvut. Funktio ei saa tehdä muutoksia alkuperäiseen taulukkoon. (**3p**)

- Esimerkki: Kolmen alkion taulukossa ovat alkiot 2, 7 ja 4. Funktio palauttaa kahden alkion taulukon, jonka alkiot ovat 2 ja 4.
- Tulosta pääohjelmassa sekä alkuperäinen taulukko että uusi taulukko konsoliin funktion kutsumisen jälkeen.
- Voit määritellä taulukon suoraan koodiin, `prompt()`-funktiota ei tarvitse käyttää.

10. Tee alla kuvatun kaltainen äänestysohjelma pienimuotoista kokouskäyttöä varten. (**8p**)

- Ohjelma kysyy ehdokkaiden määrän.
- Sen jälkeen ohjelma kysyy ehdokkaiden nimet: `Ehdokkas 1:`, `Ehdokas 2:` jne.
- Tallenna ehdokkaiden nimet ja alustava äänimäärä tämän kaltaisiin olioihin:

```javascript
[
  {
    name: "maija",
    votes: 0,
  },
  {
    name: "matti",
    votes: 0,
  },
  {
    name: "liisa",
    votes: 0,
  },
];
```

- Ohjelma kysyy äänestäjien määrän.
- Ohjelma kysyy jokaiselta äänestäjältä vuorollaan, ketä he äänestävät. Äänestäjän tulee syöttää ehdokkaan nimi. Jos äänestäjä syöttää tyhjän arvon äänestysnumeron sijaan, se tulkitaan tyhjäksi ääneksi.
- Ohjelma ilmoittaa voittajan nimen ja tulokset tulostamalla ne konsoliin:

```text
Voittaja: liisa, äänimäärä: 3

Tulokset:
liisa: 3 äänestäjää
matti: 1 äänestäjä
maija: 1 äänestäjää
```

- Tässä hieman apua:

```javascript
// You need to compare votes so console log a and b to see how to get the correct property.
someArray.sort((a, b) => {
  console.log(a, b);
  return b - a;
});
```

## Moduuli 3. BOM, DOM ja tapahtumat

[Lataa tämä ZIP-tiedosto](https://github.com/ilkkamtk/module3-starters), pura se ja siirrä sisältö kansioon, jossa sinulla on muut tämän kurssin tiedostot.

1. Avaa IDE:ssä/editorissa `t1`-kansio. Lisää HTML:ää innerHTML-ominaisuudella (**2p**)

- Lisää seuraava HTML-koodi elementtiin, jonka `id="target"`

```html
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
```

- Lisää luokka `my-list` elementtiin, jonka `id="target"`

2. Avaa IDE:ssä/editorissa `t2`-kansio. Lisää HTML:ää `createElement()`- ja `appendChild`-metodeilla. (**2p**)

- Lisää seuraava HTML-koodi elementtiin, jonka `id="target"`

```html
<li>First item</li>
<li>Second item</li>
<li>Third item</li>
```

- Lisää luokka `my-item` toiseen listaelementtiin

3. Avaa IDE:ssä/editorissa `t3`-kansio. Lisää HTML:ää innerHTML-ominaisuudella. (**2p**)

- Lisää seuraava HTML-koodi elementtiin, jonka `id="target"`. Lisää `names`-taulukon arvot `<li>`-elementteihin for-silmukassa.

```html
<li>John</li>
<li>Paul</li>
<li>Jones</li>
```

4. Avaa IDE:ssä/editorissa `t4`-kansio. Lisää HTML:ää `createElement()`- ja `appendChild`-metodeilla. (**2p**)

- Lisää seuraava HTML-koodi elementtiin, jonka `id="target"`. Lisää `students`-taulukon arvot `<option>`-elementteihin for-silmukassa.

```html
<option value="2345768">John</option>
<option value="2134657">Paul</option>
<option value="5423679">Jones</option>
```

- avaa Element Inspector DevTools-kehittäjätyökaluista nähdäksesi koko tuloksen. (napsauta hiiren oikealla painikkeella ja valitse Inspect...)

5. Avaa IDE:ssä/editorissa `t5`-kansio. Luo useita `<article>`-elementtejä, jotka sisältävät otsikon, kuvan, kuvatekstin ja tekstin, ja täytä ne `picArray`-taulukon tiedoilla. Lisää artikkelit `<section>`-elementtiin. (**5p**)

- Artikkelien rakenteen tulee olla seuraava:

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

6. Avaa IDE:ssä/editorissa `t6`-kansio. Tee skripti, joka avaa hälytysikkunan tekstillä 'Button Clicked', kun `<button>`-elementtiä napsautetaan. (**1p**)
7. Avaa IDE:ssä/editorissa `t7`-kansio. Tee hover-efekti JavaScriptillä. (**2p**)

- kun käyttäjä vie hiiren `<p id="trigger">`-elementin päälle, vaihda `<img id="target">`-elementin kuva `picA.jpg`:stä `picB.jpg`:ksi
- kun käyttäjä vie hiiren pois elementin päältä, vaihda kuva takaisin alkuperäiseksi

8. Avaa IDE:ssä/editorissa `t8`-kansio. Tee yksinkertainen laskin. (**4p**)

- Käyttäjä syöttää kaksi lukua kahteen syötekenttään. Laskin suorittaa näiden kahden luvun yhteenlaskun, vähennyslaskun, kertolaskun tai jakolaskun pudotusvalikon perusteella.
- Käytä `<option>`-elementtien value-attribuuttia määrittämään, minkä laskutoimituksen laskimen tulee suorittaa. [Esimerkki.](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_select_value2)
- Näytä tulos `<p id="result">`-elementissä, kun painiketta napsautetaan.

9. Avaa IDE:ssä/editorissa `t9`-kansio. Tämä on jatkoa edelliseen tehtävään. Jäljellä on vain yksi tekstikenttä, johon käyttäjä kirjoittaa laskutoimituksen (yhteenlasku, vähennyslasku, kertolasku tai jakolasku) (**4p**)

- Voit käyttää [includes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes)- ja [split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)-metodeja.
- eval()-funktion käyttö on kielletty
- Desimaalilukuja ei tarvitse tukea, kokonaislukujen laskeminen riittää.
- Esimerkkisyötteitä: `3+5`, `2-78`, `3/6` jne.

10. Avaa IDE:ssä/editorissa `t10`-kansio. Lue lomakkeesta etunimen ja sukunimen arvot ja tulosta ne `<p id="target">`-elementtiin (**2p**)

- muista estää lomakkeen oletustoiminto
- voit käyttää [attribuuttivalitsimia](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) `querySelector()`-funktiossa `<input>`-elementtien valitsemiseen
- esimerkkituloste: `Your name is Luke Skywalker`

11. Jatka tehtävää 5. `t11`-kansio on jo olemassa. Noudata `t11.txt`-tiedoston ohjeita. Muokkaa ohjelmaa siten, että suuri kuva avataan [modaalissa](#modal), kun `<article>`-elementtiä napsautetaan. (**6p**) - toru itseäsi tässä vaiheessa, jos käytit innerHTML:ää `<article>`-elementin ja sen sisällön luomiseen. - lisää seuraava HTML-koodi manuaalisesti HTML-dokumenttiin `</div>`- ja `</body>`-tagien väliin (ei JavaScriptillä)
`html
<dialog>
<span>✕</span>
<img>
</dialog>
` - `picArray` sisältää jokaiselle kohteelle kaksi kuvaa: medium ja large. Medium-kuvaa käytetään `<article>`-elementin sisällä olevassa `<img>`-elementissä ja large-kuvaa `<dialog>`-elementin sisällä olevassa `<img>`-elementissä. - käytä [showModal()- ja close()-funktioita](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement#instance_methods) `<dialog>`-elementin näyttämiseen ja piilottamiseen - samalla kun avaat modaalin, sinun tulee asettaa suuri kuva modaalissa olevaan `<img>`-elementtiin. - Älä unohda lisätä `alt`-attribuuttia. - käytä `<dialog>`-elementin sisällä olevaa `<span>`-elementtiä modaalin sulkemiseen.
<hr>
<sub id="modal"><sup>- Modaali on valintaikkuna/popup-ikkuna, joka näytetään nykyisen sivun päällä</sup></sub>

## Moduuli 4. AJAX

1. Tee sovellus, joka hakee syöttämäsi televisiosarjan tiedot ja näyttää ne konsolissa. (**2p**)

- Käytettävä API: [TVMaze API](http://www.tvmaze.com/api#show-search)
- Tee ensin validi HTML-sivu, jossa on hakulomake. Esimerkkilomake:

```html
<form action="[https://api.tvmaze.com/search/shows">
  ](https://api.tvmaze.com/search/shows%22>)
  <input id="query" name="q" type="text" />
  <input type="submit" value="Search" />
</form>
```

- Testaa lomake. Tuloksen pitäisi olla sivu täynnä JSON-muotoista dataa.

2. Kehitä sovellusta edelleen.

- Lisää JavaScript, joka lukee lomakkeeseen syötetyn arvon ja lähettää pyynnön [fetch](apit-ajax.md#here-is-the-same-example-but-this-time-the-airport-code-is-entered-by-using-a-form)-funktiolla osoitteeseen `[https://api.tvmaze.com/search/shows?q=${value\_from\_input](https://api.tvmaze.com/search/shows?q=${value_from_input)}`. Tulosta hakutulos konsoliin. (**3p**)

3. Kehitä sovellusta edelleen. Tulosta seuraavat tiedot kaikista hakutuloksessa olevista sarjoista verkkosivulle. (**7p**)

- vaaditut tiedot: nimi, linkki tietoihin (url), keskikokoinen kuva ja yhteenveto
- näytä nimi `<h2>`-elementissä
- näytä url `<a>`-elementissä. Lisää linkkiin myös `target="\_blank"`.
- näytä keskikokoinen kuva `<img src="" alt="">`-elementillä. Lisää keskikokoinen kuva `src`-attribuuttiin ja name-ominaisuus `alt`-attribuuttiin.
- joillakin televisiosarjoilla ei ole kuvia. Tämä aiheuttaa virheen. Voit korjata tämän lisäämällä ?-operaattorin `image`-ominaisuuteen. Esimerkki: `tvShow\.show\.image?.medium;`. Tätä kutsutaan [optional chainingiksi](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining).
- näytä yhteenveto `<div>`-elementissä (ei `<p>`-elementissä). Tämä johtuu siitä, että yhteenveto on jo `<p>`-elementissä ja tulos ei olisi validi, jos `<p>` olisi toisen `<p>`-elementin sisällä.
- kokoa elementit `<article>`-elementteihin ja lisää `<article>`-elementit HTML-dokumenttiin.
- lisää HTML-dokumenttiin `<div id="results">`-elementti, johon lisäät `<article>`-elementit.
- tyhjennä vanhat tulokset komennolla `innerHTML = ''` ennen uusien tulosten lisäämistä.

4. Kehitä sovellusta vielä pidemmälle. Optional chaining ei ole paras tapa käsitellä puuttuvaa kuvaa. Käytä [ternary operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)-operaattoria tai if/else-rakennetta oletuskuvan lisäämiseen, jos televisiosarjalta puuttuu image-ominaisuus. (**2p**)

- Käytä oletuskuvana `[https://placehold.co/210x295?text=Not%20Found](https://placehold.co/210x295?text=Not%20Found)`.

5. Tee sovellus, joka hakee satunnaisen Chuck Norris -vitsin ja näyttää sen konsolissa. (**2p**)

- Käytettävä API: [chucknorris.io](https://api.chucknorris.io/)
- Lähetä pyyntö osoitteeseen `[https://api.chucknorris.io/jokes/random](https://api.chucknorris.io/jokes/random)` ja tulosta konsoliin vain vitsi (eli `value`-ominaisuus)
- Lomaketta ei tarvitse lisätä.

6. Kehitä sovellusta edelleen (**4p**).

- Lisää nyt lomake, johon voit syöttää hakutermin kuten tehtävissä 1–3
- Lähetä hakutermi osoitteeseen `[https://api.chucknorris.io/jokes/search?query=${value\_from\_input](https://api.chucknorris.io/jokes/search?query=${value_from_input)}` käyttäen `fetch()`-funktiota
- Tulosta jokainen vitsi tässä muodossa:

```html
<article>
  <p>Joke here</p>
  <p></p>
</article>
```

7. Edistynyt. Reititys [digitransit](https://digitransit.fi/en/developers/apis/1-routing-api/)-palvelulla (**16p**)

- **Ei heikkohermoisille**. Älä tee tätä, jos se häiritsee projektia. Se ei ole sen arvoista.
- Luo sovellus, joka näyttää reitin käyttäjän määrittämästä osoitteesta koululle (Karaportti 2).
- Sinulla tulee olla lomake, johon käyttäjä lisää osoitteen. Kun lomake on lähetetty, reitti näytetään kartalla. Näytä myös matkan alkamis- ja päättymisaika. _*Ei*_ jokaista matkan osaa, vaan ainoastaan alku- ja loppuajat.
- Esimerkki: [JS](api-examples/js/esim4.js), [HTML](api-examples/esim4.html)
- Tarvitset [tämän Leaflet-laajennuksen](api-examples/js/Polyline.encoded.js), jotta esimerkki toimii.
- [Tässä on esimerkki](https://digitransit.fi/en/developers/apis/1-routing-api/itinerary-planning/#basic-route-from-kamppi-helsinki-to-pisa-espoo) siitä, kuinka paikkoja/osoitteita käytetään koordinaattien kanssa.
- Koordinaattien hakemiseen osoitteesta voit käyttää [osoitehakua](https://digitransit.fi/en/developers/apis/2-geocoding-api/address-search/).
- Jos saat CORS-virheitä (mikä _*ei*_ todennäköisesti tule tapahtumaan), [käytä tätä korjausta](https://github.com/ilkkamtk/corsfix).
