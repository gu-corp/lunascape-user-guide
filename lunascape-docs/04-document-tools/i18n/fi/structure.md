# Dokumenttijuuret ja tiedostokäytännöt

Säännöt, joiden mukaan Lunascape Docs löytää dokumentit ja kokoaa INDEX-luettelon. Tiedostojärjestelmä itsessään on alkuperäislähde, joten erillistä luetteloa tai käännösasetuksia ei tarvita.

## Dokumenttijuuri

- Lähin `docs`-kansio tai kansio, jossa on `lunascape-docs.json`, on dokumenttijuuri.
- Kun kansiossa on `lunascape-docs.json`, sen nimen ei tarvitse olla `docs`.
- Kun avaat Markdown-tiedoston, joka ei kuulu mihinkään dokumenttijuureen, sen kansio näytetään väliaikaisena dokumenttijuurena.

## INDEX-luettelossa näkyvät tiedostot

- Näytetään tiedostot `.md`, `.markdown` ja `.mdx`. Uudet tiedostot näkyvät aina, vaikka niissä ei olisi front matter -osaa eikä navigointitietoja.
- Kansioita, joiden nimi alkaa merkillä `.`, kansiota `node_modules` ja asetuksessa `ignoredDirectories` lueteltuja kansioita (oletus `99-archive`) ei näytetä.
- Kaikki kansion `i18n/` alla oleva käsitellään käännöksinä, eikä sitä näytetä INDEX-luettelossa erikseen.

## Kansion aloitussivu

- `README.md` (tai `index.md`, jos README-tiedostoa ei ole), jossa on leipätekstiä, on kansionsa aloitussivu. Kun painat kansion nimeä INDEX-luettelossa, aloitussivu avautuu.
- `README.md`, jossa on vain front matter eikä lainkaan leipätekstiä, käsitellään pelkkänä asetuskuvauksena eikä sitä näytetä sivuna. Käytä sitä, kun kansiolle riittää pelkkä otsikko tai järjestys.
- Jos sekä `README.md` että `index.md` ovat olemassa, `README.md` on ensisijainen.

## Oletuskieli ja käännökset

- Oletuskielen dokumentit (alkuperäisdokumentit) pysyvät paikoillaan.
- Käännös sijoitetaan alkuperäisdokumentin kanssa samassa kansiossa olevaan kansioon `i18n/<kieli>/` samalla tiedostonimellä. Kansiorakenteen uudelleenrakentamista kansion `i18n/` alle ei tunnisteta.
- Käännös haetaan vain tästä yhdestä paikasta. Muualle sijoitettu samanniminen tiedosto jää irralliseksi, eikä mikään dokumentti tunnista sitä käännöksekseen.

```text
docs/
  lunascape-docs.json
  README.md                  ← dokumenttijuuren aloitussivu (aloitussivu)
  i18n/en/README.md          ← sen englanninkielinen käännös
  01-product/
    README.md                ← kansion aloitussivu
    requirements.md
    i18n/en/README.md        ← kahden edellisen englanninkieliset käännökset
    i18n/en/requirements.md
  99-archive/                ← oletuksena INDEX-luettelon ulkopuolella
```

## Tietoja tiedostosta `_meta.json`

Nextran `_meta.json` ei ole käytössä navigoinnissa. Olemassa olevia tiedostoja ei muuteta eikä poisteta. Jatkossa niitä käsitellään vain erillisellä tuonti- ja vientitoiminnolla.

## Aiheeseen liittyvää

- [Navigointitietojen määrittäminen](navigation-metadata.md)
- [Projektiasetukset](project-configuration.md)
- [Dokumenttijuuren vaihtaminen](../02-reading/roots.md)
