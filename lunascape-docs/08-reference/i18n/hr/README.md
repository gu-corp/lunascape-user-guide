# Glavne specifikacije

## Radno okruženje

| Okruženje | Zahtjevi |
|---|---|
| VS Code proširenje | VS Code 1.90 ili noviji. Značajke koje zapisuju datoteke rade u pouzdanom radnom prostoru |
| Web preglednik | Noviji Chrome, Edge, Safari ili Firefox. Za pregled lokalne mape potreban je preglednik koji podržava odabir mape (File System Access API) |
| Chromium proširenje | Manifest V3. Ne traže se dopuštenja za pristup poslužiteljima |

## Podržani dokumenti

| Stavka | Sadržaj |
|---|---|
| Datoteke | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tablice, popisi zadataka, blokovi koda, precrtani tekst), lokalne slike, YAML front matter |
| MDX | Prikazuju se samo dopuštene komponente. Proizvoljne skripte se ne izvršavaju |
| HTML | Prikazuje se nakon pročišćavanja pomoću DOMPurify 3.4.14 |

## Dijagrami i matematički izrazi

| Vrsta | Naziv jezika | Napomene |
|---|---|---|
| Matematički izrazi | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Samo ugrađeni podaci. Vanjski URL-ovi i oznake slika nisu dopušteni |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Samo strogi JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | U distribuiranoj verziji izvorni kod je prikazan sklopljeno. Ograničenja: 64 KiB ulaza, 15 sekundi, 2 MiB SVG |
| Penrose (eksperimentalno) | `penrose` | Samo `set-theory` predložak postavki |

## Ograničenja

| Stavka | Vrijednost |
|---|---|
| Rezultat razrješavanja predloška | 4 MiB |
| Referentni kontekst prijevoda | Zadano 49.152 znaka, najviše 1.048.576 znakova |
| Broj dokumenata po skupnom prijevodu | 1.000 dokumenata |
| Proizvoljna širina slike | 16–4096 px |

## Datoteke

| Datoteka | Uloga | U Gitu |
|---|---|---|
| `lunascape-docs.json` | Postavke korijena dokumentacije | Da |
| `docs-lint.config.json` | Postavke pravila provjere | Da |
| `.lunascape-docs/translation-freshness.json` | Zapis o svježini prijevoda (samo putanje, jezici, hashovi i vremenske oznake) | Da |
| Postavke VS Codea i stanje radnog prostora | Osobne postavke prikaza, odabir pružatelja usluge, stanje otvorenosti INDEX-a | Ne |

## Priloženi Standard Pack

`builtin:gu-corp-software` — profili: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Povezane teme

- [Popis postavki VS Codea](settings.md)
- [Sigurnost i granice zapisivanja](security.md)
