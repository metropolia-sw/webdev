# Ohjelmointiprojekti 2: Pelillinen verkkosovellus

## Tavoite

Suunnitelkaa ja toteuttakaa **neljän opiskelijan** tiimeissä pieni **pelillinen verkkosovellus**.

Projektissa osoitat, että ymmärrät kurssilla käsitellyt web-kehityksen perusteet ja osaat yhdistää ne toimivaksi sovellukseksi.

Projektissa on käytettävä seuraavia teknologioita:

- **HTML** – rakenne ja sisältö
- **CSS** – tyylit ja responsiivinen asettelu
- **Vanilla JavaScript** (pelkkä JavaScript ilman sovelluskehyksiä) – vuorovaikutus ja dynaaminen toiminnallisuus
- **Python + Flask** – taustapalvelun (_backend_) toiminnallisuus
- **HTTP- ja rajapintaviestintä** – viestintä käyttöliittymän (_frontend_) ja taustapalvelun välillä
- **Tietojen tallennus** palvelimelle – esimerkiksi tekstitiedostoihin tai JSON-tiedostoihin
- Vähintään yksi selkeä **pelimekaniikka**, jossa käyttäjän toiminta vaikuttaa pelin tilaan

- Reactin kaltaisten sovelluskehysten (_framework_) käyttö on kielletty.

## Projektin idea

Tiimi saa valita teeman ja peli-idean itse.

Pohjana voi käyttää myös jotakin edellisen kurssin tekstipohjaisen pelin ideaa.

Pelillä on oltava selkeä tavoite ja pelattava mekaniikka. Se voi olla vuoropohjainen tai reaaliaikainen, yksin- tai moninpeli, mutta sitä on voitava pelata selaimessa.

Peli-idean on liityttävä jollakin tavalla johonkin YK:n kestävän kehityksen tavoitteista (_Sustainable Development Goals_), ja pelin on sovelluttava alaikäisille (ikäraja K-12).

Projektin ei tarvitse olla suuri tai hienostunut peli. **Pieni, valmis ja hyvin toimiva sovellus on parempi kuin suuri ja keskeneräinen.**

### Sovelluksen suunnittelu

Ensin tiimi suunnittelee sovelluksen sekä sen rakenteen ja toiminnallisuuden. Suunnittelussa käytetään [paperiprototypointia](https://en.wikipedia.org/wiki/Paper_prototyping) (_paper prototyping_). Tämän vaiheen tehtävä ja ohjeet löytyvät OMA-palautustehtävistä.

## Vähimmäisvaatimukset

Sovelluksen on täytettävä seuraavat vaatimukset:

1. Sovelluksella on selkeä peli-idea ja tavoite.
2. Sovelluksessa on pelattava pelimekaniikka.
3. Taustapalvelu toteutetaan Flaskilla.
4. Käyttöliittymä viestii taustapalvelun kanssa JavaScriptillä, ja tiedot siirretään JSON-muodossa.
5. Sovellus tallentaa ja päivittää olennaiset pelitiedot.
6. Sovelluksella on selkeä ja johdonmukainen käyttöliittymä.
7. Sovellus toimii kokonaisuutena alusta loppuun.
8. Koodi on siistiä, hyvin jäsenneltyä ja kommentoitua.

## Tiimityö

Projekti tehdään neljän hengen tiimeissä.

Jokaisella tiimin jäsenellä voi olla selkeä vastuualue, esimerkiksi:

- taustapalvelu / Flask
- HTML / käyttöliittymän rakenne
- CSS / visuaalinen suunnittelu
- JavaScript / rajapintaviestintä.

Voitte myös jakaa työn jollakin muulla tavalla, joka sopii tiimillenne.

**Kaikkien tiimin jäsenten odotetaan kuitenkin osallistuvan koko projektin kehittämiseen.**

Käyttäkää versionhallintaan Gitiä. Jokaisen tiimin jäsenen on tehtävä projektiin merkityksellistä työtä.

## Palautettavat tuotokset

Tiimi palauttaa:

- linkin projektin Git-repositorioon (_repository_), jossa on
  - kaikki projektin tiedostot (HTML, CSS, JS, Python jne.)
  - `README.md`-tiedosto, jossa on projektin kuvaus:
    - peli-idea ja tavoite
    - tärkeimmät ominaisuudet ja toiminnallisuus
    - tiimin jäsenet
    - käytetyt teknologiat
    - ohjeet sovelluksen käynnistämiseen
    - lyhyt kuvaus työnjaosta
- linkin julkaistuun verkkosovellukseen
  - Varmistakaa ennen lopullista palautusta, että linkki ja kaikki sovelluksen ominaisuudet toimivat myös verkossa.

Tiimi pitää lisäksi lyhyen, **10–15 minuutin esityksen ja demon** sovelluksesta.

Lopullisen palautuksen ja esityksen ohjeet löytyvät OMA-palautustehtävistä.

---

# Arviointi

Projekti arvioidaan asteikolla **0–5**.

Loppuarvosana perustuu sekä projektin laatuun että opiskelijan **henkilökohtaiseen osallistumiseen ja aktiivisuuteen**.

### 5 – Erinomainen

Sovellus on valmis, toimiva ja hyvin jäsennelty. Toteutuksesta näkyy, että käyttöliittymän ja taustapalvelun kehittäminen hallitaan hyvin. Opiskelija on osallistunut aktiivisesti koko projektin ajan, tehnyt merkittävää työtä ja osaa selittää sekä oman työnsä että kokonaisratkaisun.

### 4 – Kiitettävä

Sovellus toimii hyvin ja täyttää keskeiset vaatimukset. Toteutuksesta näkyy, että käytetyt teknologiat ymmärretään hyvin. Opiskelija on osallistunut aktiivisesti ja tehnyt selkeää, merkityksellistä työtä.

### 3 – Hyvä

Keskeiset vaatimukset täyttyvät ja sovellus toimii. Sovelluksessa voi olla joitakin teknisiä tai käytettävyyteen liittyviä ongelmia. Opiskelija on osallistunut riittävästi ja tehnyt osansa projektista.

### 2 – Tyydyttävä

Vain perusvaatimukset täyttyvät. Sovelluksessa on huomattavia rajoituksia tai keskeneräisiä osia. Opiskelija on osallistunut vähän mutta kuitenkin riittävästi osoittaakseen jonkin verran oppimista.

### 1 – Välttävä

Projekti on merkittävästi keskeneräinen tai siinä on suuria toiminnallisia ongelmia. Opiskelijan henkilökohtainen panos ja aktiivisuus ovat olleet hyvin vähäisiä.

### 0 – Hylätty

Projekti ei täytä vähimmäisvaatimuksia tai ei toimi, tai opiskelija ei ole osoittanut riittävää henkilökohtaista osallistumista tai projektin ymmärrystä.

## Henkilökohtainen osallistuminen

Henkilökohtaisessa arvioinnissa otetaan huomioon:

- aktiivinen osallistuminen projektiin
- merkityksellinen panos koodiin tai muuhun projektityöhön
- osallistuminen suunnitteluun ja ongelmanratkaisuun
- kyky selittää oma panos
- kyky osoittaa ymmärtävänsä sovelluksen kokonaisuutena
- yhteistyö ja viestintä tiimin sisällä
- Git-commitit ja muut näytöt kehitystyöstä
- muiden tiimin jäsenten antama anonyymi palaute.

**Kaikkien tiimin jäsenten on pystyttävä selittämään, miten sovellus toimii – ei vain omaa osuuttaan.**
