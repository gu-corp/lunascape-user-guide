# Projektin asetukset

Dokumenttijuuren juuressa sijaitseva `lunascape-docs.json` on tiimin kesken jaettu dokumenttijuuren asetustiedosto. Sitä hallitaan Gitissä.

## Asetustiedoston luominen ja muokkaaminen

- Paina työkalurivin [Dokumenttityökalut] → [Tarkistus]-välilehti → [Sääntöjen lähde ja dokumenttiasetukset] → [Muokkaa dokumenttiasetuksia], niin tiedosto avautuu VS Codessa. Jos tiedostoa ei ole, se luodaan tässä vaiheessa alkusisällöllä.
- Tiedostonimeen `lunascape-docs.json` liitetään automaattisesti mukana toimitettava JSON Schema, joka tarjoaa syötteen täydennyksen ja kuvauksen jokaiselle kentälle. `$schema`-merkintää ei tarvita.

## Asetusesimerkki

```json
{
  "id": "product-docs",
  "title": "Tuotedokumentaatio",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Kenttien kuvaus

| Kenttä | Sisältö | Oletus |
|---|---|---|
| `id` | Avain, jonka alle käyttäjäkohtaiset näyttöasetukset tallennetaan. Anna kiinteä tunnus, kun haluat asetusten säilyvän kansion siirtyessä | Kansion polku |
| `title` | Nimi, joka näkyy työkalurivin vasemmassa reunassa ja dokumenttijuurien luettelossa. Se ei muutu näyttökieltä vaihdettaessa | Juuren README/index-otsikko, muuten kansion nimi |
| `indexTitle` | INDEX-paneelin otsikko | `INDEX` |
| `startPage` | Ensimmäisenä avattava dokumentti (polku dokumenttijuuresta) | `README.md` |
| `appearance` | Väriteema: `light` (aina vaalea) tai `auto` (seuraa VS Coden teemaa) | `light` |
| `defaultLocale` | Oletuskieli (alkuperäisdokumenttien kieli). Ilmoitetaan BCP 47 ‑kielitunnuksena, esimerkiksi `ja`, `en` tai `zh-Hant`. Toimii käännösten lähteenä | Ei asetettu (päätellään tekstistä näyttöä varten) |
| `fallbackLocale` | Kieli, joka näytetään ensimmäisenä lukijalle, jonka ympäristön kieli ei vastaa mitään tuetuista kielistä. Nimeä kieli, joka sisältyy `locales`-luetteloon | Ei asetettu (käytetään `defaultLocale`-arvoa) |
| `locales` | Tuettujen kielten luettelo, johon `defaultLocale` sisältyy. Ne näkyvät kielivalikossa ja ovat käännösten kohteet | Vain `defaultLocale` |
| `ignoredDirectories` | Kansionimet, jotka jätetään pois INDEX-paneelista, hausta ja tarkistuksista. Määrittäminen korvaa oletuksen | `["99-archive"]` |
| `tree` | INDEX-paneelin näytön oletusarvot. Käyttäjä voi ohittaa ne näyttöasetuksissa | Kuten yllä olevassa esimerkissä |
| `editor.defaultMode` | Muokkausnäkymä, jota käytetään kunnes käyttäjä vaihtaa sitä: `visual` tai `source` | `visual` |
| `editor.showEditButton` | Näytetäänkö [Muokkaa] tekstin oikeassa alakulmassa | `true` |
| `documentStandards.pack` | Tarkistuksissa ja malleissa käytettävä Standard Pack: `builtin:<nimi>` tai polku dokumenttijuuresta | Ei mitään |
| `documentStandards.profile` | Pakkauksen määrittelemä profiilin nimi | Ei mitään |
| `translation.enabled` | Ottaa käyttöön käännösehdotukset ja joukkokäännöksen | `true` |
| `translation.contextFiles` | Alkuperäisdokumenttien Markdown-tiedostot (polut dokumenttijuuresta), jotka annetaan käännökselle termistön ja tyylin viitteiksi | `[]` |
| `translation.maxContextCharacters` | Viitedokumenttien yhteispituuden yläraja merkkeinä (enintään 1048576) | `49152` |
| `description` | Yhden rivin kuvaus dokumenttikokonaisuudesta. Näkyy säilön etusivun korteissa. Kuten `title`, se voidaan kirjoittaa merkkijonona tai kielikohtaisena oliona | Ei mitään |

## Kerro, missä säilön dokumentit ovat

Säilön juureen sijoitettuun `lunascape-docs.json`-tiedostoon voi kirjoittaa kyseisen kansion asetusten sijaan **säilön kartan**. Jos kirjoitat jonkin seuraavista kolmesta kentästä, tiedostosta tulee kartta, eikä kansio itse ole enää dokumenttijuuri.

| Kenttä | Sisältö | Oletus |
|---|---|---|
| `defaultFolder` | Missä kansiossa dokumentit ovat (polku tästä kansiosta). Osoitettu kansio ei tarvitse omaa asetustiedostoa | Ei mitään (käytetään `docs`) |
| `roots` | Dokumenttikokonaisuuksien luettelo, kun niitä on useita (polut tästä kansiosta, näyttöjärjestyksessä). Tällöin tästä kansiosta tulee etusivu | Ei mitään |
| `excludes` | Kansiot, jotka jätetään pois dokumenttijuurien etsinnästä (polut tästä kansiosta). Lisätään sisäänrakennettuihin poikkeuksiin, kuten `node_modules` | `[]` |
| `home.cards` | Näytetäänkö etusivun README-tiedoston alla dokumenttikokonaisuuksien kortit. Aseta arvoksi `false`, jos kirjoitat linkit itse README-tiedostoon | `true` |

Dokumenttijuuri määräytyy seuraavassa järjestyksessä. Käyttöön otetaan ylhäältä alkaen ensimmäinen löytynyt.

1. Kansio, jonka asetus tai suoritettu komento nimeää
2. Kohde, johon juuren `lunascape-docs.json`-tiedoston `defaultFolder` tai `roots` osoittaa
3. Kansio, jossa on `lunascape-docs.json` (jos yhteisen ylemmän kansion alla on kaksi tai useampia, siitä ylemmästä kansiosta tulee etusivu)
4. Kansio `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Säilön juuri itse

> **Vinkki**
>
> Jos mitään ei kirjoiteta, kohta 4 astuu voimaan, joten tavallinen säilö, jossa on yksi `docs/`-kansio, toimii kuten ennenkin. Kirjoita `defaultFolder` vain silloin, kun kansion nimi on jokin muu, esimerkiksi `manual`.

### Esimerkki kartasta

```json
{
  "title": "Lunascape-ohje",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Asetusten etusijajärjestys

Näyttöön liittyvät kentät otetaan käyttöön seuraavassa järjestyksessä.

1. Käyttäjän näyttöasetukset ([Näyttöasetukset]-paneeli)
2. VS Coden asetukset (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Tuotteen oletusarvot

Kielet (`defaultLocale`, `fallbackLocale`, `locales`) ovat ainoa poikkeus: `lunascape-docs.json` on määräävä. Projektin kieliä ei voi ohittaa henkilökohtaisilla VS Coden asetuksilla.

> **Huomautus**
>
> Standard Pack voidaan määrittää myös `docs-lint.config.json`-tiedostossa kentällä `standard`. Jos molemmat ovat olemassa, `docs-lint.config.json` on etusijalla.

## Aiheeseen liittyvää

- [Tarkistussääntöjen muuttaminen](rules.md)
- [Näyttöasetusten muuttaminen](../02-reading/display-settings.md)
- [VS Coden asetukset](../08-reference/settings.md)
