# Tärkeimmät määrittelyt

## Käyttöympäristö

| Ympäristö | Vaatimukset |
|---|---|
| VS Code ‑laajennus | VS Code 1.90 tai uudempi. Tiedostoja kirjoittavat toiminnot vaativat luotetun työtilan |
| Verkkoselainversio | Tuore Chrome, Edge, Safari tai Firefox. Paikallisen kansion selaaminen vaatii selaimen, joka tukee kansion valintaa (File System Access API) |
| Chromium-laajennus | Manifest V3. Isäntäoikeuksia ei pyydetä |

## Tuetut dokumentit

| Kohde | Sisältö |
|---|---|
| Tiedostot | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (taulukot, tehtävälistat, koodilohkot, yliviivaus), paikalliset kuvat, YAML front matter |
| MDX | Vain sallitut komponentit näytetään. Mielivaltaisia skriptejä ei suoriteta |
| HTML | Puhdistetaan DOMPurify 3.4.14:llä ennen näyttämistä |

## Kaaviot ja matematiikka

| Tyyppi | Kielen nimi | Huomautuksia |
|---|---|---|
| Matematiikka | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Vain upotettu data. Ulkoiset URL-osoitteet ja kuvamerkinnät eivät ole mahdollisia |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Vain tiukka JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Jakeluversiossa lähdekoodi näkyy tiivistettynä. Rajat: syöte 64 KiB, 15 sekuntia, SVG 2 MiB |
| Penrose (kokeellinen) | `penrose` | Vain `set-theory`-esiasetus |

## Rajat

| Kohde | Arvo |
|---|---|
| Mallin muodostama tulos | 4 MiB |
| Käännöksen viitekonteksti | oletuksena 49 152 merkkiä, enintään 1 048 576 merkkiä |
| Dokumentteja yhdessä joukkokäännöksessä | 1 000 |
| Kuvan vapaavalintainen leveys | 16–4096 px |

## Tiedostot

| Tiedosto | Tehtävä | Git-hallinnassa |
|---|---|---|
| `lunascape-docs.json` | Dokumenttijuuren asetukset | Kyllä |
| `docs-lint.config.json` | Tarkistussääntöjen asetukset | Kyllä |
| `.lunascape-docs/translation-freshness.json` | Käännösten tuoreustiedot (vain polut, kielet, tiivisteet ja aikaleimat) | Kyllä |
| VS Coden asetukset ja työtilan tila | Henkilökohtaiset näyttöasetukset, palveluntarjoajan valinta, INDEX-paneelin avaustila | Ei |

## Mukana toimitettava Standard Pack

`builtin:gu-corp-software` — profiilit: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Aiheeseen liittyvää

- [VS Coden asetukset](settings.md)
- [Tietoturva ja tallennusrajat](security.md)
