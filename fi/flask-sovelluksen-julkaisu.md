# Flask-pohjaisen verkkosovelluksen julkaiseminen verkossa

## Flask-sovelluksen julkaiseminen Renderissä

Tässä ohjeessa julkaiset (_deploy_) Flask-sovelluksesi verkossa **Render**-palvelun avulla. Julkaisun jälkeen sovelluksesi on käytettävissä julkisessa `onrender.com`-osoitteessa.

Render on pilvialusta, jolla voi julkaista verkkosovelluksia ja -palveluita. Sen maksuton palvelutaso (_free tier_) sopii pieniin projekteihin ja kurssitehtäviin.

Flask-sovelluksia voi julkaista myös muilla pilvialustoilla, kuten **Herokussa** ja **PythonAnywheressa**. Jos pilvipalvelut ovat sinulle tuttuja, voit käyttää myös **AWS**:ää, **Google Cloudia** tai **Microsoft Azurea**. Alustan valinta on sinun päätettävissäsi, mutta tämä ohje keskittyy Renderiin.

### 1. Varmista, että projektisi toimii paikallisesti

Varmista ennen julkaisua, että Flask-sovelluksesi toimii omalla tietokoneellasi.

Projektin kansiorakenne voi olla esimerkiksi tällainen:

```dir
my-project-app/
├── app.py
├── requirements.txt
└── static/
    ├── index.html
    ├── style.css
    └── script.js
```

Python-päätiedostossa `app.py` pitää olla Flask-sovellusolio, joka on tallennettu muuttujaan `app`, esimerkiksi:

```python
from flask import Flask, send_from_directory

app = Flask(__name__)

@app.route('/')
def home():
    return send_from_directory('static', 'index.html')

@app.route('/<path:filename>')
def serve_static(filename):
    return send_from_directory('static', filename)

@app.route('/hello')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(use_reloader=True, host='127.0.0.1', port=3000)
```

Tässä esimerkissä Flask-sovellus tarjoaa staattisia tiedostoja `static`-kansiosta, ja siinä on yksinkertainen reitti (_route_) eli päätepiste `/hello`. Kun suoritat sovellusta paikallisesti, voit avata sen esimerkiksi seuraavista osoitteista:

```text
http://localhost:3000/ -> näyttää index.html-tiedoston
http://localhost:3000/index.html -> näyttää index.html-tiedoston
http://localhost:3000/style.css -> näyttää style.css-tiedoston
http://localhost:3000/script.js -> näyttää script.js-tiedoston
http://localhost:3000/hello -> näyttää tekstin "Hello, World!"
```

### 2. Luo `requirements.txt`

Renderin täytyy tietää, mitä Python-paketteja sovelluksesi käyttää.

Luo projektin juurikansioon tiedosto `requirements.txt`. Yksinkertaista Flask-sovellusta varten siihen tarvitaan seuraavat rivit:

```text
Flask
gunicorn
```

Gunicorn on tuotantokäyttöön tarkoitettu palvelinohjelma, joka käynnistää Flask-sovelluksesi Renderissä. Flaskin oma `app.run`-palvelin on tarkoitettu vain kehityskäyttöön.

Jos projektisi käyttää muita paketteja, lisää myös ne, esimerkiksi:

```text
Flask
gunicorn
requests
```

Voit myös luoda tiedoston automaattisesti terminaalikomennolla, joka listaa koneellesi asennetut Python-paketit:

```sh
pip freeze > requirements.txt
```

Huomaa, että komento listaa kaikki ympäristöön asennetut paketit, ei vain projektisi tarvitsemia. Lisäksi `gunicorn` on listassa vain, jos olet asentanut sen.

Varmista, että `requirements.txt` on lisätty ja commitoitu Git-repositorioosi.

### 3. Vie projektisi GitHubiin

Luo GitHubiin repositorio ja vie (push) Flask-projektisi sinne.

Varmista, että repositoriossa on vähintään:

```text
app.py
requirements.txt
static/
```

**Älä** lataa GitHubiin salasanoja, API-avaimia tai muita salaisuuksia.

### 4. Luo Render-tili ja julkaise sovelluksesi

Mene osoitteeseen [Render.com](https://render.com/) ja luo tili. Voit rekisteröityä GitHub-tililläsi tai luoda uuden tilin sähköpostiosoitteellasi.

Huomaa: jos rekisteröidyt GitHub-tililläsi, Render pyytää lupaa käyttää repositorioitasi. Lupa tarvitaan, jotta Render voi hakea Flask-sovelluksesi koodin julkisesta GitHub-repositoriosta ja julkaista sen.

Tee Renderin hallintapaneelissa (_Dashboard_) seuraavat vaiheet:

1. Valitse _New Web Service_
1. Yhdistä GitHub-repositoriosi
1. Tarkista asetukset
   - valitse maksuton palvelutaso (_Free_)
   - muuten oletusarvojen pitäisi riittää tämän esimerkin kaltaiselle yksinkertaiselle projektille
1. Napsauta **Deploy web service**

Odota julkaisun valmistumista. Render tekee nyt seuraavat asiat:

1. Hakee projektisi koodin GitHub-repositoriosta
1. Asentaa Python-riippuvuudet (`requirements.txt`-tiedoston luettelon perusteella)
1. Käynnistää Flask-sovelluksesi
1. Antaa sovelluksellesi julkisen URL-osoitteen

URL-osoite on muotoa `https://my-flask-game.onrender.com`. Avaa osoite selaimessa ja testaa sovellustasi.

### 5. Sovelluksen päivittäminen

**Varmista aina ennen päivittämistä, että sovellus toimii omalla tietokoneellasi!**

Yksi Renderin hyödyllisistä ominaisuuksista on automaattinen julkaisu. Kun olet yhdistänyt GitHub-repositoriosi, Render julkaisee automaattisesti uuden version aina, kun viet uusia committeja valittuun haaraan.

Kun suoritat esimerkiksi `main`-haarassa seuraavat komennot:

```bash
git add .
git commit -m "Add new game feature"
git push
```

Render havaitsee uuden commitin ja aloittaa uuden julkaisun. Voit seurata julkaisua Render-palvelusi **Deploys**-osiosta.

Jos automaattinen julkaisu on poistettu käytöstä tai se ei toimi, voit julkaista myös käsin. Napsauta vain _Deploys_-välilehden _Manual Deploy_ -painiketta.

---

## Yleisiä ongelmia

### Tärkeää: tiedostojärjestelmän käyttö Renderissä

Jos projektisi käyttää tiedostoja pysyvään tiedon tallentamiseen, huomaa, että julkaistun verkkopalvelun tiedostojärjestelmää **ei pidä käsitellä kuin oman tietokoneesi pysyvää tiedostojärjestelmää**. Tiedostoja voi kyllä lukea ja kirjoittaa, mutta muutokset voivat kadota ilman varoitusta milloin tahansa, esimerkiksi kun sovellus julkaistaan uudelleen.

Yksinkertaisessa kurssiprojektissa tiedon tallentaminen tiedostoihin riittää, mutta älä oleta, että tiedot säilyvät maksuttomassa julkaisussa pysyvästi.

### `ModuleNotFoundError`

Jos Render ilmoittaa:

```text
ModuleNotFoundError: No module named ...
```

paketti puuttuu todennäköisesti `requirements.txt`-tiedostosta. Lisää puuttuva paketti tiedostoon ja vie muutokset GitHubiin.

Render asentaa vain ne Python-paketit, jotka on lueteltu projektin riippuvuustiedostossa.

### `gunicorn: command not found`

Varmista, että `gunicorn` on mukana `requirements.txt`-tiedostossa.

Julkaise sitten uudelleen.

### Sovellus käynnistyy paikallisesti mutta ei Renderissä

Tarkista Renderin julkaisuloki (**Deploy Logs**).

Yleinen ongelma on virheellinen käynnistyskomento eli komento, jolla Render käynnistää sovelluksesi.

Jos Python-päätiedostosi on `app.py` ja se sisältää rivin:

```python
app = Flask(__name__)
```

käynnistyskomennon pitäisi yleensä olla: `gunicorn app:app`.

Muoto on:

```text
gunicorn <python_file>:<flask_app_variable>
```

Jos sinulla on esimerkiksi tiedosto `server.py` ja Flask-sovellus on tallennettu muuttujaan näin:

```python
application = Flask(__name__)
```

komento olisi: `gunicorn server:application`

Korjaa virhe joko muuttamalla tiedoston tai muuttujan nimeä sovelluksessasi tai muuttamalla käynnistyskomentoa Renderin asetuksissa (_Start Command_).

### Sovellus käyttää väärää Python-versiota

Render käyttää uusille palveluille oletuksena tiettyä Python-versiota. Jos projektisi vaatii jonkin toisen version, voit määrittää sen `.python-version`-tiedostolla tai `PYTHON_VERSION`-ympäristömuuttujalla (_environment variable_), jonka voit asettaa palvelun asetuksissa Renderissä.

Kurssiprojektissa oletusversion pitäisi riittää, mutta jos kohtaat ongelmia, kannattaa määrittää versio, jolla olet testannut sovelluksen paikallisesti.

---
