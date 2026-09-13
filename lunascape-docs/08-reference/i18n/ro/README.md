# Specificații principale

## Cerințe de sistem

| Mediu | Cerințe |
|---|---|
| Extensia VS Code | VS Code 1.90 sau mai nou. Funcțiile care scriu fișiere necesită un spațiu de lucru de încredere |
| Vizualizatorul web | Chrome, Edge, Safari sau Firefox recente. Deschiderea unui folder local necesită un browser care acceptă selectarea folderelor (File System Access API) |
| Extensia Chromium | Manifest V3. Nu solicită permisiuni de gazdă |

## Documente acceptate

| Element | Detalii |
|---|---|
| Fișiere | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabele, liste de sarcini, blocuri de cod, text tăiat), imagini locale, front matter YAML |
| MDX | Se afișează numai componentele permise. Scripturile arbitrare nu sunt executate |
| HTML | Se afișează după igienizarea cu DOMPurify 3.4.14 |

## Diagrame și formule matematice

| Tip | Numele limbajului | Observații |
|---|---|---|
| Formule matematice | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Numai date încorporate. Nu sunt permise adrese URL externe și marcaje de imagine |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Numai JSON strict |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | În versiunea distribuită, sursa este afișată restrânsă. Limite: 64 KiB la intrare, 15 secunde, 2 MiB SVG |
| Penrose (experimental) | `penrose` | Numai presetarea `set-theory` |

## Valori maxime

| Element | Valoare |
|---|---|
| Rezultatul expandării unui șablon | 4 MiB |
| Contextul de referință al traducerii | 49.152 de caractere în mod implicit, maximum 1.048.576 |
| Documente per rulare a traducerii în bloc | 1.000 de documente |
| Lățimea personalizată a imaginii | 16–4096px |

## Fișiere

| Fișier | Rol | În Git |
|---|---|---|
| `lunascape-docs.json` | Configurarea rădăcinii documentației | Da |
| `docs-lint.config.json` | Configurarea regulilor de verificare | Da |
| `.lunascape-docs/translation-freshness.json` | Evidența prospețimii traducerilor (numai căi, limbi, sume de control și date/ore) | Da |
| Setările VS Code și starea spațiului de lucru | Setări personale de afișare, furnizorul ales, starea de deschidere a panoului INDEX | Nu |

## Standard Pack inclus

`builtin:gu-corp-software` — profiluri: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Subiecte conexe

- [Lista setărilor VS Code](settings.md)
- [Securitatea și limitele de salvare](security.md)
