# Mikä Lunascape Docs on

Lunascape Docs on työkalu, jolla Git-säilössä olevia Markdown-dokumentteja käsitellään sellaisinaan "määrittelysivustona". Erillistä käännösvaihetta, dokumenttipalvelinta tai omaa tietokantaa ei tarvita.

## Mitä sillä voi tehdä

| Tarkoitus | Päätoiminnot |
|---|---|
| Lukeminen | INDEX (sisällysluettelo), tekstin linkit, navigointipolku, takaisin ja eteenpäin, sivun sisältöluettelo, rajaava haku |
| Katselu | Taulukot, koodilohkot, kuvien automaattinen sovitus, KaTeX-matematiikka, Mermaid-, Vega-Lite-, Markmap-, WaveDrom- ja Svgbob-kaaviot, dokumentinhallintataulukoiden tiivistetty näyttö |
| Kirjoittaminen | Vaihto visuaalisen muokkauksen ja Markdown-lähdemuokkauksen välillä, luonti, monistus, uudelleennimeäminen ja järjestäminen INDEX-paneelista |
| Tarkistaminen | docs-lint-dokumenttitarkistus, Standard Packin mukaisten pakollisten dokumenttien, lukujen ja termien tarkistus, luonti mallista |
| Kääntäminen | Käännösehdotusten luonti sivu kerrallaan tai erässä. Tallennus vasta tarkistuksen jälkeen <!-- ai-only --> |
| Käyttö tekoälystä | Vain luku -muotoinen määrittelytyökalu, jota VS Coden agentit voivat käyttää <!-- ai-only --> |

## Käytettävissä olevat ympäristöt

| Ympäristö | Käyttötarkoitus |
|---|---|
| VS Code -laajennus | Oman koneen säilön lukeminen, muokkaus, tarkistus ja kääntäminen. Tämä ohje keskittyy siihen |
| Selainversio | GitHubissa olevien dokumenttien (julkisten ja yksityisten) lukeminen, luonnokset laitteessa, paikallisen kansion selaus |
| Chromium-laajennus | Avaa selainversion selaimen välilehdellä |
| Lunascape-selain | Samaa dokumenttimallia ollaan liittämässä siihen |

## Perusperiaatteet

- **Markdown on alkuperäisdokumentti.** Dokumentit pysyvät Gitillä hallittuina Markdown-tiedostoina. Lunascape Docs ei säilytä niistä muuhun muotoon muunnettua kopiota.
- **Tallennuksen tekee käyttäjä.** Muokkaukset kirjoitetaan tiedostoon vasta, kun painat [Tallenna]. Gitin stagingia tai committeja ei tehdä automaattisesti.
- **Dokumentit käsitellään laitteessa.** Dokumentteja ei lähetetä ulkopuolelle lukemista tai muokkausta varten. Vain kääntäminen lähettää dokumentin, ja silloinkin vastaanottaja ja sisältö näytetään etukäteen ja lähetys tapahtuu vasta hyväksynnän jälkeen.
- **Käännökset sijaitsevat kansiossa `i18n/<kieli>/`.** Oletuskielen dokumentit pysyvät paikallaan, käännökset tulevat samalla suhteellisella polulla kansioon `i18n/en/` ja vastaaviin.
- **Tekoäly vain ehdottaa.** Käännösehdotukset tallennetaan vasta, kun olet tarkistanut erot. Dokumentteja ei muuteta huomaamatta. <!-- ai-only -->

## Aiheeseen liittyvää

- [Näytön osat ja niiden tehtävät](screen.md)
- [Laajennuksen asentaminen](install.md)
- [Perustoiminnot](../02-reading/README.md)
