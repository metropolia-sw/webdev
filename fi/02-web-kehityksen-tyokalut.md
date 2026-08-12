# Kehitystyökalut ja -ympäristö

## Koodieditori tai IDE

Lopulta valinta on sinun. Opettaja käyttää VSCodea.

### [Visual Studio Code (VSCode)](https://code.visualstudio.com/download)

- ilmainen ja avoimen lähdekoodin koodieditori Microsoftilta (**!=** Visual Studio IDE)
- laaja laajennustuki
- kevyt, monialustainen tuki
- hyvät [dokumentaatiot ja ohjeet](https://code.visualstudio.com/docs/editor/codebasics)
- monien web-kehittäjien valinta

#### Laajennusten asentaminen

Paina _ctrl-shift-x_ tai napsauta vasemman paneelin laajennuskuvaketta.

Hae ja asenna:

- Prettier
- Live Server (by Ritwick Dey)

#### VSCode – perusteet

Katso: [Visual Studio Coden vinkit ja niksit](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)

Aktiivinen **projekti** on vasemman paneelin puolella avoinna oleva kansio (_File -> Open folder..._)

Hyödyllisiä pikanäppäimiä (suomalainen näppäimistöasettelu, katso _File -> Preferences -> Keyboard shortcuts_ saadaksesi lisätietoja)

- Monirivinen kommentti: _ctrl-'_
- Poista rivi: _ctrl-shift-k_
- Siirrä rivi(t): _alt-up/down_
- Kopioi rivi(t): _alt-shift-up/down_
- Muotoile koodi automaattisesti: _alt-shift-f_
- Avaa integroitu konsoli: _ctrl-ö_
- Etsi/avaa tiedostoja nopeasti: _ctrl-p_
- Jaa editori: _ctrl-§_

### WebStorm/PyCharm (valinnainen)

- ilmainen Metropolian opiskelijoille. [Hae lisenssi täältä](https://www.jetbrains.com/student/)
  - _@metropolia.fi_-sähköpostiosoite tarvitaan ilmaiseen lisenssiin
  - asenna sitten [ToolBox-sovellus](https://www.jetbrains.com/toolbox-app/)
- monipuolinen IDE
- varsin käyttövalmis sellaisenaan. Lisäosia ei tarvita.
- perustuu IntelliJ IDEAan, kuten PyCharm

## Selain ja virheenkorjaus

- Chrome & [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)
- Selain renderöi sivun HTML:n ja CSS:n perusteella ja suorittaa JavaScript-koodin.
- DevToolsin avulla voit tarkastella sivua ja nähdä, miten se renderöidään, korjata JavaScript-koodin virheitä, tarkistaa verkkopyyntöjä jne.
- Pidä DevTools _aina_ avoinna kehityksen aikana, jotta näet muutokset reaaliajassa ja voit korjata mahdollisia ongelmia.

## Paikallinen web-palvelin

- Koodi toimii samalla tavalla kuin jos se olisi julkaistu internetissä, mutta sivu näkyy vain paikallisesti omalla tietokoneellasi.
- Ritwick Deyn Live Server on suosittu VSCode-laajennus, jonka voit asentaa suoraan editorin laajennukset-välilehdeltä.
- Tämän jälkeen sivusto avautuu selaimessa osoitteessa <http(s)://localhost:[PORT]>

## Julkinen web-palvelin

- Julkaistaksesi sivustosi internetissä tarvitset web-palvelimen.
- Metropolia tarjoaa opiskelijoille ilmaisen web-hotellipalvelun. Voit käyttää sitä tehtäviesi ja portfoliosi julkaisemiseen.
- Voit myös käyttää muita ilmaisia hosting-palveluita, kuten GitHub Pagesia, Netlifyä, Verceliä jne.
- Käymme seuraavien viikkojen aikana läpi sivustosi julkaisemisen Metropolian web-hosting-palvelussa.

---

<!-- add mermaid support for gh pages -->
<script type="module">
    Array.from(document.getElementsByClassName("language-mermaid")).forEach(element => {
      element.classList.add("mermaid");
    });
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
    mermaid.initialize({startOnLoad: true});
</script>
