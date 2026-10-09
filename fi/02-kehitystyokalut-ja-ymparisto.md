# Kehitystyökalut ja -ympäristö

## Koodieditori tai IDE

Koodieditorin tai IDE:n (_integrated development environment_, integroitu kehitysympäristö) valinta on viime kädessä sinun. Opettaja käyttää VSCodea.

### [Visual Studio Code (VSCode)](https://code.visualstudio.com/download)

- Microsoftin ilmainen avoimen lähdekoodin koodieditori (**!=** Visual Studio IDE)
- paljon laajennuksia
- kevyt, toimii Windowsissa, macOS:ssä ja Linuxissa
- hyvä [dokumentaatio ja ohjeet](https://code.visualstudio.com/docs/editor/codebasics)
- monen web-kehittäjän valinta

#### Laajennusten asentaminen

Paina _ctrl-shift-x_ tai napsauta vasemman reunan paneelissa laajennusten kuvaketta.

Etsi ja asenna seuraavat laajennukset:

- Prettier
- Live Server (tekijä Ritwick Dey)

#### VSCoden peruskäyttö

Katso: [Visual Studio Code tips and tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)

VSCodessa **projekti** on kansio, jonka avaat komennolla _File -> Open folder..._. Avatun kansion tiedostot näkyvät vasemmassa sivupaneelissa.

Käteviä pikanäppäimiä suomalaisella näppäimistöllä (lisää löydät kohdasta _File -> Preferences -> Keyboard shortcuts_):

- Valittujen rivien kommentointi ja kommentin poisto: _ctrl-'_
- Rivin poistaminen: _ctrl-shift-k_
- Rivi(e)n siirtäminen: _alt-up/down_
- Rivi(e)n kopioiminen: _alt-shift-up/down_
- Koodin automaattinen muotoilu: _alt-shift-f_
- Integroidun päätteen (terminaalin) avaaminen: _ctrl-ö_
- Tiedostojen pikahaku ja -avaus: _ctrl-p_
- Editorin jakaminen: _ctrl-§_

### WebStorm/PyCharm (valinnainen)

- ilmainen Metropolian opiskelijoille. [Hae lisenssiä täältä](https://www.jetbrains.com/student/)
  - ilmaiseen lisenssiin tarvitset _@metropolia.fi_-sähköpostiosoitteen
  - asenna sen jälkeen [ToolBox-sovellus](https://www.jetbrains.com/toolbox-app/)
- monipuolinen IDE
- toimii hyvin heti asennuksen jälkeen ilman laajennuksia
- perustuu IntelliJ IDEAan, kuten myös PyCharm

## Selain ja virheenjäljitys

- Chrome ja [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/)
  - Myös Firefox, Safari, Edge ja muut modernit selaimet tarjoavat kehittäjätyökaluja.
- Selain piirtää sivun näytölle HTML- ja CSS-koodin perusteella ja suorittaa sivun JavaScript-koodin.
- Kehittäjätyökaluilla (_developer tools_, DevTools) voit tarkastella sivun rakennetta ja tyylejä, etsiä virheitä JavaScript-koodista (_debugging_) ja seurata selaimen lähettämiä verkkopyyntöjä.
- Pidä kehittäjätyökalut _aina_ auki, kun teet sivua. Näet silloin muutokset heti ja huomaat virheet nopeasti.
  > Toistetaan yhdessä: _Lupaan pitää kehittäjätyökalut auki koko ajan tämän kurssin aikana ja loppuelämäni ajan aina, kun teen web-kehitystä._
  <!-- https://fullstackopen.com/en/part1/introduction_to_react -->

## Paikallinen web-palvelin

- Web-palvelin on ohjelma, joka lähettää sivun tiedostot selaimelle. Paikallinen web-palvelin toimii omalla tietokoneellasi.
- Koodi toimii samoin kuin internetiin julkaistuna, mutta sivu näkyy vain omalla tietokoneellasi.
- Live Server on suosittu VSCode-laajennus, jonka voit asentaa suoraan editorin laajennusvälilehdeltä.
- Tämän jälkeen sivusto avautuu selaimessa osoitteessa <http(s)://localhost:[PORT]>. Nimi `localhost` tarkoittaa omaa tietokonettasi, ja `[PORT]` on palvelimen porttinumero (Live Serverillä yleensä 5500).

## Julkinen web-palvelin

- Jotta voit julkaista verkkosivustosi internetissä, tarvitset web-palvelimen, johon muut pääsevät verkon kautta.
- Metropolia tarjoaa opiskelijoille palvelimen verkkosivustoja varten. Voit julkaista sen avulla tehtäväsi.
- Voit käyttää myös muita ilmaisia ylläpitopalveluita, kuten GitHub Pagesia, Netlifyä tai Verceliä.

---

<!-- add mermaid support for gh pages -->
<script type="module">
    Array.from(document.getElementsByClassName("language-mermaid")).forEach(element => {
      element.classList.add("mermaid");
    });
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
    mermaid.initialize({startOnLoad: true});
</script>
