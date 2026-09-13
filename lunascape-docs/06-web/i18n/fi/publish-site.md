# Omien dokumenttien julkaiseminen verkossa

Voit julkaista oman säilösi dokumentit verkkosivustona GitHub Pagesissa tai missä tahansa staattisessa palvelussa. Julkaisuun on kaksi tapaa. Nämä ohjeet on tarkoitettu kehittäjille, jotka voivat kloonata Lunascape Docsin säilön ja käyttää `npm`-komentoa.

## Tapa 1: sijoita katselimen kaksi tiedostoa

Julkaise vain katselin (`index.html` ja `lsdoc.js`) ja anna sen ladata dokumentit GitHubista. Dokumentit itsessään eivät kuulu sivustoon, joten tapa on turvallinen myös yksityisille säilöille (lukijat kirjautuvat sisään GitHubilla).

1. Suorita seuraava komento Lunascape Docsin säilössä.

   ```sh
   npm run build:viewer
   ```

   Kansioon `dist/viewer/` luodaan tiedostot `index.html` ja `lsdoc.js`.
2. Sijoita nämä kaksi tiedostoa julkaistavan säilön kansioon `docs/`.
3. Ota GitHub Pages käyttöön.

Näytettävä dokumenttijuuri määräytyy seuraavassa järjestyksessä.

1. Tiedoston `index.html` sisältämä asetus `source`
2. Samassa kansiossa olevan `lunascape-docs.json`-tiedoston `repository`
3. Päättely `*.github.io`-osoitteesta ja haararakenteesta

## Tapa 2: kirjoita ulos staattinen sivusto dokumentteineen

Kirjoita katselin ja dokumenttitiedostot yhdessä ulos ja julkaise tulos sellaisenaan.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Tuloksena ovat katselimen tiedostot, kansion `docs/` alla olevat dokumentit, luettelotiedosto `lunascape-docs-manifest.json` sekä `.nojekyll`. Julkaise sijoittamalla tuloshakemisto S3:een tai GitHub Pagesiin. Esimerkki automaattisesta julkaisusta GitHub Actionsilla on säilön tiedostossa `examples/workflows/publish-docs-pages.yml`.

> **Huomautus**
>
> - **Älä koskaan kirjoita yksityisen säilön dokumentteja ulos ja sijoita niitä GitHub Pagesiin.** Enterprise Cloudin ulkopuolella GitHub Pages on kaikkien luettavissa. Jos julkaisua on rajoitettava, käytä tapaa 1 ja anna lukijoiden kirjautua sisään GitHubilla.
> - Tiedoston `index.html` avaaminen suoraan `file://`-osoitteesta ei toimi, koska selaimet estävät viereisten tiedostojen lataamisen ja ES-moduulien suorittamisen näin. Tarkista sivusto paikallisesti VS Code -laajennuksella tai HTTP-palvelimella.
> - TikZ-, Vega-Lite-, Markmap-, WaveDrom-, Svgbob- ja Penrose-piirtokirjastot ladataan vasta näytettäessä. Sijoita ulos kirjoitetun sivuston mukana myös kansio `vendor/`.

## Aiheeseen liittyvää

- [Mihin verkkokatselin pystyy](README.md)
- [Yksityisen säilön lukeminen](private-repository.md)
