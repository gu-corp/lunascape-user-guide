# Mikä Lunascape Docs on

Lunascape Docs on työkalu, jolla Git-säilöön tallennettuja Markdown-dokumentteja käsitellään sellaisinaan ”määrittelysivustona”. Etukäteen tehtävää koontia, dokumenttipalvelinta tai erillistä tietokantaa ei tarvita.

## Mitä voit tehdä

| Tarkoitus | Tärkeimmät toiminnot |
|---|---|
| Lukeminen | INDEX (sisällysluettelo), tekstin linkit, navigointipolku, siirtyminen taakse- ja eteenpäin, sivun sisällysluettelo, suodatushaku |
| Katselu | Taulukot, koodilohkot, kuvien automaattinen sovitus, KaTeX-matematiikka, Mermaid-, Vega-Lite-, Markmap-, WaveDrom- ja Svgbob-kaaviot, dokumentinhallintataulukoiden kokoontaitettu näyttö |
| Kirjoittaminen | Vaihto visuaalisen muokkauksen ja Markdown-lähdekoodin muokkauksen välillä, luonti, monistaminen, uudelleennimeäminen ja järjestyksen muuttaminen INDEX-paneelista |
| Tarkistaminen | docs-lint-tarkistukset, pakollisten dokumenttien, lukujen ja termien tarkistus Standard Packin perusteella, luonti mallista |
| Kääntäminen | Käännösehdotusten luonti sivu kerrallaan tai useille sivuille kerralla. Tarkistus ennen tallentamista <!-- ai-only --> |
| Käyttö tekoälystä | Vain luku -tilassa toimiva määrittelytyökalu, jota VS Coden agentit voivat käyttää <!-- ai-only --> |

## Käyttöympäristöt

| Ympäristö | Käyttötarkoitus |
|---|---|
| VS Code -laajennus | Omalla koneella olevan säilön lukeminen, muokkaus, tarkistus ja kääntäminen. Tämä ohje keskittyy siihen |
| Verkkoselainversio | GitHubissa olevien dokumenttien (julkisten ja yksityisten) lukeminen, luonnokset laitteella, paikallisen kansion lukeminen |
| Chromium-laajennus | Avaa verkkoselainversion selaimen välilehteen |

## Perusperiaatteet

- **Markdown on ensisijainen lähde.** Dokumentit pysyvät Gitillä hallittuina Markdown-tiedostoina. Lunascape Docs ei muunna niitä toiseen muotoon eikä säilytä niitä sellaisena.
- **Käyttäjä tallentaa itse.** Muokkaukset kirjoitetaan tiedostoon vain, kun painat [Tallenna]. Muutoksia ei lisätä Gitin valmistelualueelle eikä commitoida automaattisesti.
- **Dokumentit käsitellään laitteellasi.** Dokumentteja ei lähetetä minnekään lukemista tai muokkausta varten. Vain käännettäessä vastaanottaja ja sisältö näytetään etukäteen, ja dokumentti lähetetään vasta hyväksyntäsi jälkeen.
- **Käännökset sijoitetaan kansioon `i18n/<kieli>/`.** Oletuskielen dokumentit pysyvät paikallaan, ja käännökset sijoitetaan samaan suhteelliseen polkuun esimerkiksi kansioon `i18n/en/`.
- **Tekoäly vain ehdottaa.** Käännösehdotukset tallennetaan vasta, kun olet tarkistanut erot. Dokumentteja ei koskaan muuteta huomaamatta. <!-- ai-only -->

## Aiheeseen liittyvää

- [Näytön osien nimet ja toiminnot](screen.md)
- [Laajennuksen asentaminen](install.md)
- [Perustoiminnot](../02-reading/README.md)
