# Tehtävä 1: HTML + CSS -yrityssivusto

**Tee oma versiosi [annetusta asettelusta](../assets/assignment-1-layout.pdf). Huomaa: useita sivuja!**

- Annetusta asettelusta löydät suunnitelmat kolmelle sivulle: Home, Products ja Contact.
- Tehtäväsi on tehdä yksinkertainen verkkosivusto annetun asettelun perusteella.
- Tuloksen ei tarvitse olla pikselintarkka. Riittää, että visuaalinen rakenne on lähellä annettua asettelua.
- Voit tehdä kolme sivua yhteen dokumenttiin tai voit sijoittaa jokaisen sivun omaan dokumenttiinsa.
- Sinun tulee keksiä oma väripalettisi ja valita versiollesi fontti (tai fontteja).
- Lisää sivulle/sivuille myös omia kuvia.
- Voit käyttää tekstisisältönä [lorem ipsumia](https://en.wikipedia.org/wiki/Lorem_ipsum). Mikä tahansa teksti käy.
- Tekijänoikeuksia ei tarvitse huomioida, koska kyseessä on opetustehtävä.
- Tarkempi kuvaus löytyy Omassa olevasta videosta.
- Verkkosivun/sivujen ei tarvitse olla tässä tehtävässä responsiivisia, mutta toisessa tehtävässä teet responsiivisen verkkosivuston, joten voit jo nyt alkaa miettiä, kuinka asettelusta tehdään responsiivinen.

### Palauttaminen

Anna Omassa `clickable`-linkki kansioon, jossa tehtäväsi on. Anna lisäksi `clickable`-linkki HTML-dokumenttiin, jossa ovat kuvakaappaukset ja fonttisi CSS-esimerkki. Katso [video](https://www.youtube.com/watch?v=u7mjd5Vi6lk&list=PLKenVLUxjmH-y89AiiI2xcXDy5QG83D4K&index=6) saadaksesi lisätietoja. Esimerkki palautuksesta:

[Sivusto](https://users.metropolia.fi/~username/foldername)

[Kuvakaappaukset](https://users.metropolia.fi/~username/foldername/screenshots.html)

### Arviointi

Palautuksen yhteydessä saat automaattisesti arvosanan 5. Jos jotkin tehtävän osa-alueet puuttuvat tai ovat puutteellisia, arvosanaa vähennetään seuraavasti:

- Versiosi ei muistuta annettua asettelua tai CSS puuttuu -1 - -3
- Navigointi ei toimi -1 - -3
- Kuvia ei löydy -1 - -3
- Kontrastitarkistus ei mene läpi -1
  - _PÄIVITYS_: [https://color.a11y.com/Contrast/](https://color.a11y.com/Contrast/) ei ole enää saatavilla. Käytä sen sijaan [https://wave.webaim.org/](https://wave.webaim.org/). [Esimerkkikuvakaappaus täällä](../assets/wave.png).
  - Kontrastivirheitä pitää olla 0. Muut kohdat tarkistetaan validoinnilla ja alla olevalla Lighthousella.
- Validointi ei mene läpi -3
  - Ei virheitä
  - Varoitukset, kuten otsikon puuttuminen `<article>`- tai `<section>`-elementistä jne., ovat sallittuja
- Lighthouse-tarkistuksen tulos on alle 90 -1, alle 70 -2
  - jotkin Chromen versiot näyttävät tuloksen muodossa 5/5 tai 4/4, jolloin kustakin puuttuvasta pisteestä vähennetään tässä tapauksessa -1. Esimerkiksi 3/4 = -1. Vähennys on kuitenkin enintään -2
  - Päivitys: Jos käytät `<iframe>`-elementtiä Google Maps -kartan lisäämiseen, Lighthouse vähentää pisteitä. Tämä ei vaikuta arviointiin. Sinun kannattaa kuitenkin harkita pelkän karttakuvan käyttämistä.
- Oletusfontti (Times New Roman) -1
- Padding puuttuu (teksti on liian lähellä reunoja tai muita elementtejä) -1 - -3

**Huom! Testaa tehtäväsi toisella tietokoneella varmistaaksesi, että kaikki tiedostot latautuvat!**

Kuvakaappaussivun esimerkki-HTML:

```html id="jy6l3u"
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Results</title>
  </head>
  <body>
    <h2>Font</h2>
    <p>
      Font is from
      <a href="https://fonts.google.com/specimen/Whatever"
        >Google Fonts. Name: Whatever</a
      >
    </p>
    <pre>
    @font-face {
      font-family: whatEver;
      src: url(sansation_light.woff) format(woff);
    }

    body {
       font-family: whatEver;
    }
</pre
    >
    <h2>Validation</h2>
    <p>
      <img src="img/validator.png" alt="valid" />
    </p>
    <h2>Lighthouse</h2>
    <p>
      <img src="img/lighthouse.png" alt="lighthouse" />
    </p>
    <h2>Contrast</h2>
    <p>
      <img src="img/contrast.png" alt="contrast" />
    </p>
  </body>
</html>
```
