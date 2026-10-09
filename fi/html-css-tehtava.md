# Tehtävä 1: Yrityksen verkkosivusto HTML:llä ja CSS:llä

**Tee oma versiosi [annetusta layoutista](../assets/assignment-1-layout.pdf). Huom.: useita sivuja!**

> Mikä ihmeen layout? Layoutilla tarkoitetaan verkkosivun visuaalista ilmettä ja rakennetta. Välillä käytämme tästä myös termiä leiska, tai virallisemmin ehkä sivun asettelu.

- Annetussa layoutissa on suunnitelmat kolmelle sivulle: Home, Products ja Contact.
- Tehtäväsi on tehdä yksinkertainen verkkosivusto annetun layoutin mukaan.
- Lopputuloksen ei tarvitse olla pikselintarkka. Riittää, että visuaalinen rakenne on lähellä annettua layoutia.
- Voit tehdä kaikki kolme sivua yhteen dokumenttiin tai jokaisen sivun omaan dokumenttiinsa.
- Keksi versioosi oma väripaletti ja valitse fontti (tai fontit).
- Lisää sivu(i)lle myös omia kuvia.
- Voit käyttää tekstisisältönä [lorem ipsum](https://en.wikipedia.org/wiki/Lorem_ipsum) -tekstiä. Mikä tahansa teksti käy.
  - [lipsum generaattori](https://www.lipsum.com/)
- Tekijänoikeuksia ei tarvitse huomioida, koska kyseessä on koulutehtävä.
- Tehtävä kuvataan tarkemmin OMAssa olevassa videossa.
- Tässä tehtävässä verkkosivujen ei tarvitse olla responsiivisia eli mukautua erikokoisille näytöille. Toisessa tehtävässä teet kuitenkin responsiivisen verkkosivuston, joten voit jo nyt miettiä, miten layoutista saisi responsiivisen.

### Palauttaminen

Palauta OMAan `klikattava` linkki kansioon, jossa tehtäväsi on. Palauta myös `klikattava` linkki HTML-dokumenttiin, jossa ovat tarkistusten kuvakaappaukset ja CSS-koodi, jolla otit fontin käyttöön. Katso tarkemmat ohjeet [videosta](https://www.youtube.com/watch?v=u7mjd5Vi6lk&list=PLKenVLUxjmH-y89AiiI2xcXDy5QG83D4K&index=6).

Esimerkkipalautus:

[Sivusto](https://users.metropolia.fi/~username/foldername)

[Kuvakaappaukset](https://users.metropolia.fi/~username/foldername/screenshots.html)

### Arviointi

Arviointiasteikko on **hyväksytty/hylätty**. Tehtävä hyväksytään, jos seuraavat vaatimukset täyttyvät pääosin:

- Versiosi muistuttaa annettua layoutia.
- CSS on käytössä.
- Navigointi toimii.
- Kuvat näkyvät sivulla.
- Kontrastitarkistus menee läpi (tekstin ja taustan värien välillä on riittävä kontrasti).
  - _PÄIVITYS_: https://color.a11y.com/Contrast/ ei ole enää käytettävissä. Käytä sen sijaan palvelua https://wave.webaim.org/. [Esimerkkikuvakaappaus täällä](../assets/wave.png).
  - Kontrastivirheitä ei saa olla yhtään. Työkalun muita huomautuksia ei arvioida tässä, koska ne tarkistetaan alla mainitulla validoinnilla ja Lighthouse-tarkistuksella.
- Validointi menee läpi (validaattori tarkistaa, että HTML-koodi noudattaa HTML-standardia).
  - Ei virheitä.
  - Varoitukset, kuten otsikon puuttuminen `<article>`- tai `<section>`-elementistä, ovat sallittuja.
- Lighthouse-tarkistuksen pistemäärän on oltava vähintään 90 tai selaimesta riippuen 3/4 tai 4/5. Lighthouse on Chromen kehittäjätyökaluihin sisältyvä työkalu, joka arvioi sivun laatua, esimerkiksi saavutettavuutta.
  - _PÄIVITYS_: jos lisäät Google-kartan `<iframe>`-elementillä, Lighthouse vähentää pisteitä. Tämä ei vaikuta arviointiin, mutta harkitse silti pelkän karttakuvan käyttämistä.
- Älä käytä oletusfonttia (Times New Roman).
- Sisämarginaalia (_padding_) on käytetty riittävästi (teksti ei ole liian lähellä elementtien reunoja tai muita elementtejä).

**Huom.: Testaa tehtäväsi toisella tietokoneella ja varmista, että kaikki tiedostot latautuvat!**

Esimerkki kuvakaappaussivun HTML-koodista:

```html
<!DOCTYPE html>
<html lang="fi">
  <head>
    <meta charset="UTF-8" />
    <title>Tulokset</title>
  </head>
  <body>
    <h2>Fontti</h2>
    <p>
      Fontti on palvelusta
      <a href="https://fonts.google.com/specimen/Whatever"
        >Google Fonts. Nimi: Whatever</a
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
    <h2>Validointi</h2>
    <p>
      <img src="img/validator.png" alt="validointi" />
    </p>
    <h2>Lighthouse</h2>
    <p>
      <img src="img/lighthouse.png" alt="lighthouse" />
    </p>
    <h2>Kontrasti</h2>
    <p>
      <img src="img/contrast.png" alt="kontrasti" />
    </p>
  </body>
</html>
```
