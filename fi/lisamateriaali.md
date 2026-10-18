# Lisämateriaali

Vapaaehtoista lisälukemista ja vinkkejä.

## Rekursio

Rekursiolla (_recursion_) tarkoitetaan tilannetta, jossa funktio kutsuu itseään. Kutsuttu funktio kutsuu taas itseään ja niin edelleen. Keskeneräiset funktiokutsut tallentuvat kutsupinoon (_call stack_), joka syvenee jokaisen kutsun myötä. Kun jokin kutsu lopulta palauttaa arvon kutsumatta enää itseään, rekursio alkaa purkautua.

Tarkastellaan esimerkkinä rekursiivisesta ohjelmasta kertoman (_factorial_) laskemista. Positiivisen kokonaisluvun kertoma on tulo, jonka tekijöinä ovat luku itse ja kaikki sitä pienemmät positiiviset kokonaisluvut. Esimerkiksi luvun 5 kertoma on 5 · 4 · 3 · 2 · 1 = 120.

Luvun 5 kertoma on siis 5 kertaa luvun 4 kertoma. Luvun 4 kertoma puolestaan on 4 kertaa luvun 3 kertoma ja niin edelleen.

Jokainen kertoma ilmaistaan yhtä pienemmän luvun kertoman avulla, kunnes lopulta päädytään luvun 1 kertomaan, joka on 1.

JavaScript-funktiona tämä näyttää seuraavalta:

```javascript
function factorial(number) {
  if (number == 1) return 1;
  else return number * factorial(number - 1);
}

console.log(factorial(5));
```

Rekursiivinen funktio voi olla nokkela, mutta se ei useinkaan ole tehokkain ratkaisu. Suoritusympäristön täytyy nimittäin tallentaa kutsupinoon jokaisen keskeneräisen funktiokutsun tiedot. Kutsupinolle on varattu kooltaan rajallinen muistialue, joka voi syvässä rekursiossa loppua kesken.

# BOM

Selaimen oliomalli (_Browser Object Model_, BOM) tarkoittaa selaimen tarjoamia olioita, kuten `window`-oliota. Niiden avulla JavaScript-koodi voi käyttää selaimen toimintoja, esimerkiksi ajastimia.

## Funktioiden ajastaminen

### [setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setTimeout)

Funktiolla `setTimeout()` voit kutsua funktiota kerran tietyn ajan kuluttua.

```javascript
function printSomething(param) {
  console.log(param);
}

setTimeout(printSomething, 2000, "Tämä tulostetaan");
```

- Yllä oleva koodi määrittelee funktion `printSomething`, jota `setTimeout()` kutsuu kahden sekunnin kuluttua. Aika annetaan millisekunteina. Kolmas argumentti (`'Tämä tulostetaan'`) välitetään argumenttina funktiolle `printSomething`.

### [setInterval](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval)

Funktiolla `setInterval()` voit kutsua funktiota tietyin väliajoin. Funktio `setInterval()` palauttaa ajastimen tunnisteen (_interval ID_), jonka avulla ajastimen voi myöhemmin pysäyttää kutsumalla funktiota `clearInterval()`.

```javascript
function sayHello() {
  console.log("Hei");
}

const interval = setInterval(sayHello, 1000);
```

- Yllä oleva koodi määrittelee funktion `sayHello`, jota `setInterval()` kutsuu sekunnin välein. Aika annetaan millisekunteina. Ajastimen saat pysäytettyä seuraavalla komennolla:

```javascript
clearInterval(interval);
```

# DOM

### Oliokokoelmat

Voit hakea dokumentin elementtejä myös valmiina kokoelmina. Kokoelma (_HTMLCollection_) muistuttaa taulukkoa, mutta se ei ole taulukko, joten kaikki taulukon metodit eivät toimi sillä.

```javascript
document.forms; // kaikki <form>-elementit
document.images; // kaikki <img>-elementit
document.links; // kaikki <area>- ja <a>-elementit, joilla on href-attribuutti
document.scripts; // kaikki <script>-elementit
```

### innerHTML-sisällön puhdistaminen (lisätietoa)

Jos asetat `innerHTML`-ominaisuuden (_property_) arvoksi tekstiä, joka tulee käyttäjältä tai muusta ulkopuolisesta lähteestä, sivustosi altistuu XSS-hyökkäyksille (_Cross-Site Scripting_). XSS-hyökkäyksessä hyökkääjä saa sivulle haitallista JavaScript-koodia, jonka selain suorittaa. [Tässä artikkelissa kerrotaan, miten hyökkäyksiä voi estää.](https://gomakethings.com/how-to-sanitize-third-party-content-with-vanilla-js-to-prevent-cross-site-scripting-xss-attacks/)

# Tapahtumat

### Takaisinkutsufunktiot ja takaisinkutsuhelvetti

Takaisinkutsufunktio (_callback_) on funktio, joka välitetään argumenttina toiselle funktiolle. Toinen funktio kutsuu sitä myöhemmin, esimerkiksi kun jokin tapahtuma on tapahtunut tai tietty tehtävä on valmis. Takaisinkutsufunktioita käytetään usein asynkronisessa (_asynchronous_) koodissa, joka ei jää odottamaan hitaan toiminnon valmistumista. Itse et kutsu takaisinkutsufunktiota, vaan välität sen toiselle funktiolle ilman sulkeita.

Esimerkiksi tapahtumankäsittelijä (_event handler_) on takaisinkutsufunktio, jonka selain kutsuu vasta, kun tietty tapahtuma tapahtuu. Alla olevassa esimerkissä selain kutsuu funktiota `clickHandler` aina, kun käyttäjä klikkaa sivua.

```javascript
function clickHandler() {
  console.log("Käyttäjä klikkasi sivua.");
}
document.addEventListener("click", clickHandler);
```

#### Takaisinkutsuhelvetti

Takaisinkutsuhelvetti (_callback hell_) syntyy, kun takaisinkutsufunktioita kirjoitetaan sisäkkäin niin monta, että sisennykset muodostavat pyramidin. Jokainen takaisinkutsufunktio on riippuvainen edellisen takaisinkutsufunktion tuloksesta ja odottaa sitä. Pyramidirakenne heikentää koodin luettavuutta ja ylläpidettävyyttä.

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

Joskus ongelman voi ratkaista muuttamalla funktiot palauttamaan lupauksen (_promise_, Promise-olio) ja käyttämällä avainsanoja `async` ja `await`.

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

# CORS-virheiden korjaaminen

CORS-virhe syntyy, kun selain estää pyynnön toiselle palvelimelle, koska palvelin ei salli pyyntöjä sinun sivustoltasi. Korjausohje löytyy [tästä linkistä](https://github.com/ilkkamtk/corsfix).
