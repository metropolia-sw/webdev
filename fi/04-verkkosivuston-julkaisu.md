# Verkkosivuston julkaisu

## Metropolian opiskelijoiden kotisivupalvelun käyttö (users.metropolia.fi)

Voit julkaista verkkosivustosi Metropolian palvelimella users.metropolia.fi-palvelun avulla seuraavasti:

1. Siirrä verkkosivustosi tiedostot (kaikki HTML-, CSS- ja kuvatiedostot jne.) palvelimella olevan kotihakemistosi `public_html`-hakemistoon (HUOM! Älä missään tapauksessa poista tätä hakemistoa).
   - Pääset kotihakemistoosi kirjautumalla palvelimelle `shell.metropolia.fi` esimerkiksi SSH-yhteydellä (salattu etäyhteys palvelimelle). Tiedostot voit siirtää scp- tai sftp-ohjelmalla. Ennen kirjautumista sinun täytyy luoda SSH-avainpari (katso alla olevat linkit).
   - Aloittelijalle helpompi vaihtoehto on Webdisk-palvelu, jota käytetään selaimella: <https://webdisk.metropolia.fi/>

2. Julkaistu verkkosivustosi löytyy osoitteesta <https://users.metropolia.fi/~yourusername>, jossa `yourusername` korvataan omalla Metropolian käyttäjätunnuksellasi.
   - Jos käyttäjätunnuksesi on esimerkiksi ”janedoe”, sivustosi osoite on <https://users.metropolia.fi/~janedoe>

Lisätietoa löydät Metropolian Helpdeskin wikistä:

- [Home Page, Shell and MySQL Services](https://wiki.metropolia.fi/spaces/itservices/pages/8552770/Home+Page+Shell+and+MySQL+Services)
- [Creating an SSH Key Pair and Logging in on a Linux Server (shell.metropolia.fi)](https://wiki.metropolia.fi/spaces/itservices/pages/307791540/Creating+an+SSH+Key+Pair+and+Logging+in+on+a+Linux+Server+shell.metropolia.fi)
- [Webdisk Service Quick Instructions](https://wiki.metropolia.fi/spaces/itservices/pages/181375282/Webdisk+Service+Quick+Instructions)

Voit pyytää apua myös Helpdeskin tekoälypalvelulta: <https://mikko.metropolia.fi/>

## Muut palvelut (Metropolia tai opettaja ei tue)

Verkkosivustojen ylläpitopalveluita (_hosting_) on tarjolla myös muualla. Osassa on ilmainen versio tai opiskelijatarjous. Esimerkkejä:

- Render: <https://render.com/>
- Azure Static Web Apps: <https://azure.microsoft.com/en-us/services/app-service/static/>
- GitHub Pages: <https://pages.github.com/>
- Netlify: <https://www.netlify.com/>
- Vercel: <https://vercel.com/>
- Firebase Hosting: <https://firebase.google.com/products/hosting>
- Heroku: <https://www.heroku.com/>

Nämä ovat ulkopuolisten yritysten palveluita, ja niiden käyttöön tarvitset käyttäjätilin. Jokaisella palvelulla on omat ohjeensa verkkosivuston julkaisemiseen, joten katso tarkemmat tiedot palvelun dokumentaatiosta.

Metropolia tai opettaja ei tue näitä palveluita. Jos kohtaat ongelmia, pyydä apua palvelun omasta tuesta.
