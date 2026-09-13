# Hovedspesifikasjoner

## Driftsmiljø

| Miljø | Krav |
|---|---|
| VS Code-utvidelse | VS Code 1.90 eller nyere. Funksjoner som skriver til filer, virker i et klarert arbeidsområde |
| Nettleserversjon | Nyere Chrome, Edge, Safari eller Firefox. Visning av en lokal mappe krever en nettleser som støtter mappevalg (File System Access API) |
| Chromium-utvidelse | Manifest V3. Ber ikke om vertstillatelser |

## Støttede dokumenter

| Element | Innhold |
|---|---|
| Filer | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabeller, oppgavelister, kodeblokker, gjennomstreking), lokale bilder, YAML front matter |
| MDX | Bare tillatte komponenter vises. Vilkårlige skript kjøres aldri |
| HTML | Vises etter rensing med DOMPurify 3.4.14 |

## Diagrammer og matematikk

| Type | Språknavn | Merknad |
|---|---|---|
| Matematikk | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Bare innebygde data. Eksterne URL-er og bildemerker støttes ikke |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Bare streng JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Sammenslått kildevisning i distribusjonsversjonen. Grenser: 64 KiB inndata, 15 sekunder, 2 MiB SVG |
| Penrose (eksperimentell) | `penrose` | Bare forhåndsinnstillingen `set-theory` |

## Grenseverdier

| Element | Verdi |
|---|---|
| Resultat av malutvidelse | 4 MiB |
| Referansekontekst for oversettelse | 49 152 tegn som standard, maksimalt 1 048 576 tegn |
| Mål per kjøring med masseoversettelse | 1 000 dokumenter |
| Egendefinert bildebredde | 16–4096px |

## Filer

| Fil | Rolle | Git-styrt |
|---|---|---|
| `lunascape-docs.json` | Innstillinger for dokumentroten | Ja |
| `docs-lint.config.json` | Innstillinger for kontrollregler | Ja |
| `.lunascape-docs/translation-freshness.json` | Registrering av oversettelsens ferskhet (bare bane, språk, hash og tidspunkt) | Ja |
| VS Code-innstillinger og arbeidsområdetilstand | Personlige visningsinnstillinger, valg av leverandør, åpen/lukket tilstand for INDEX | Nei |

## Medfølgende Standard Pack

`builtin:gu-corp-software` — profiler: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Relaterte emner

- [Oversikt over VS Code-innstillinger](settings.md)
- [Sikkerhet og skrivegrenser](security.md)
