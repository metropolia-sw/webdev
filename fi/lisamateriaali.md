## Rekursio

Rekursiolla tarkoitetaan tilannetta, jossa funktio kutsuu itseään, minkä seurauksena kutsuttu funktio kutsuu jälleen itseään ja niin edelleen. Jossain vaiheessa kutsupinon syveneminen päättyy ja rekursio alkaa purkautua.

Tarkastellaan esimerkkinä rekursiivista ohjelmaa, joka laskee kertoman. Kertoma tarkoittaa kertolaskua, jossa kertomiseen käytetään luvun lisäksi kaikkia sitä pienempiä positiivisia kokonaislukuja yksi kerrallaan. Esimerkiksi luvun 5 kertoma on 120.

Näin ollen luvun 5 kertoman laskemiseksi on tarpeen selvittää luvun 4 kertoma, joka puolestaan on 4 kertaa luvun 3 kertoma ja niin edelleen.

Jokainen kertoma voidaan aina ilmaista yhtä pienemmän luvun kertoman avulla, kunnes lopulta päädytään luvun 1 kertomaan, jonka tiedetään olevan yksi.

Ohjelmana tämä voidaan ilmaista seuraavasti:

```javascript
function factorial(number) {
  if (number == 1) return 1;
  else return number * factorial(number - 1);
}

console.log(factorial(5));
```

Vaikka rekursiivinen funktio vaikuttaa kekseliäältä, se ei useinkaan ole tehokkain ratkaisu. Tämä johtuu siitä, että suoritusympäristön täytyy tallentaa suorituksen aikana väliin jääneiden funktiokutsujen tiedot. Syvässä rekursiossa tälle kutsupinolle varattu kiinteän kokoinen osa keskusmuistista voi loppua.

# BOM

## Funktioiden ajoitus

### [setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setTimeout)

`setTimeout ()`-funktiolla voidaan kutsua funktiota kerran tietyn ajan kuluttua.

```javascript
function printSomething(param) {
  console.log(param);
}

setTimeout(printSomething, 2000, "This will be printed");
```

- yllä oleva koodi luo `printSomething`-funktion, joka suoritetaan kahden sekunnin kuluttua käyttämällä `setTimeout ()`-metodia. Aika annetaan millisekunteina.

### [setInterval](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval)

`setInterval()`-funktiolla voidaan kutsua funktiota määritetyin väliajoin. `setInterval()`-funktio palauttaa `interval ID`:n, jonka avulla väli voidaan pysäyttää myöhemmin kutsumalla `clearInterval ()`-funktiota.

```javascript
function sayHello() {
  console.log("Hello");
}

const interval = setInterval(sayHello, 1000);
```

- yllä oleva koodi luo `sayHello`-funktion, joka suoritetaan joka sekunti käyttämällä `setInterval()`-funktiota. Aika annetaan millisekunteina. Pysäytä kyseinen väli seuraavalla komennolla:

```javascript
clearInterval(interval);
```

# DOM

### Olioiden kokoelmat

Voit myös valita dokumentista elementtikokoelmia:

```javascript
document.forms; // retrieves all form elements
document.images; // retrieves all image elements
document.links; // retrieves all area and a elements with the href attribute
document.scripts; // retrieves all script elements
```

### innerHTML:n puhdistaminen (lisätehtävä)

`innerHTML`-ominaisuutta voidaan käyttää Cross Site Scripting -hyökkäyksiin. [Tässä on artikkeli siitä, kuinka ne voidaan estää.](https://gomakethings.com/how-to-sanitize-third-party-content-with-vanilla-js-to-prevent-cross-site-scripting-xss-attacks/)

# Tapahtumat

### Callback-funktiot ja callback-helvetti

Callbackit ovat funktioita, jotka välitetään argumenttina toiselle funktiolle suoritettavaksi, kun tapahtuma on tapahtunut tai tietty tehtävä on suoritettu. Niitä käytetään usein asynkronisessa koodissa. Koodinpätkä kutsuu callback-funktioita myöhemmin, mutta ne voidaan määritellä alustuksen yhteydessä ilman, että niitä kutsutaan.

Esimerkiksi tapahtumankuuntelijat ovat asynkronisia callback-funktioita, jotka suoritetaan vain, kun tietty tapahtuma tapahtuu.

```javascript
function clickHandler() {
  console.log("The user clicked on the page.");
}
document.addEventListener("click", clickHandler);
```

#### Callback-helvetti

Callback-helvetti tarkoittaa käytännössä sisäkkäisiä callback-funktioita, jotka on pinottu toistensa alle pyramidimaiseksi rakenteeksi. Jokainen callback riippuu edellisestä callbackista tai odottaa sen suorittamista, jolloin muodostuu pyramidimainen rakenne, joka vaikuttaa koodin luettavuuteen ja ylläpidettävyyteen.

```javascript
getData(function (a) {
  getMoreData(a, function (b) {
    getMoreData(b, function (c) {
      getMoreData(c, function (d) {
        getMoreData(d, function (e) {
          // ...
        });
      });
    });
  });
});
```

Funktioiden muokkaaminen palauttamaan promiseja ja async/awaitin käyttäminen voi joskus olla ratkaisu.

```javascript
async function asyncAwaitVersion() {
  const a = await getData();
  const b = await getMoreData(a);
  const c = await getMoreData(b);
  const d = await getMoreData(c);
  const e = await getMoreData(d);
  // ...
}
```

# HTTP-protokolla

Useimmat avoimet API-rajapinnat on toteutettu HTTP-protokollaan perustuvalla REST-arkkitehtuurimallilla, minkä vuoksi niihin viitataan usein RESTful-verkkopalveluina.
REST-arkkitehtuuri käyttää HTTP-metodeja kertomaan järjestelmälle esimerkiksi, haluatko lukea, lisätä tai muokata tietoja. Jotta voit käyttää avoimia rajapintoja / RESTful-palveluita, on hyvä tuntea HTTP-protokollan perusteet:

[HTTP:n yleiskatsaus](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)

### HTTP-metodit

HTTP määrittelee kyselymetodeja, jotka kertovat palvelimelle, millaisen toiminnon se haluaa suorittaa.
Yleisimmin käytetyt metodit ovat:

- GET
  - käytetään yleensä tietyn resurssin tai tietojen pyytämiseen

- POST
  - käytetään tietojen tai esimerkiksi tiedoston lisäämiseen

- PUT
  - käytetään vanhan tietueen korvaamiseen uudella

- DELETE
  - käytetään tietueen poistamiseen

- PATCH
  - käytetään tietueen tietojen osan päivittämiseen

Käytetyn API-rajapinnan dokumentaatio kertoo, mitä metodia sekä mitä parametreja ja HTTP-otsakkeita tulee käyttää eri tilanteissa.

# CORS-virheiden korjaaminen

[Tässä linkissä](https://github.com/ilkkamtk/corsfix)
