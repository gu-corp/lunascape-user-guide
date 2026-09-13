# Huvudsakliga specifikationer

## Systemkrav

| Miljö | Krav |
|---|---|
| VS Code-tillägg | VS Code 1.90 eller senare. Funktioner som skriver filer kräver en betrodd arbetsyta |
| Webbläsarversion | Senare versioner av Chrome, Edge, Safari och Firefox. För att visa en lokal mapp krävs en webbläsare som stöder mappval (File System Access API) |
| Chromium-tillägg | Manifest V3. Inga värdbehörigheter begärs |

## Dokument som stöds

| Post | Innehåll |
|---|---|
| Filer | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabeller, uppgiftslistor, kodblock, genomstrykning), lokala bilder, YAML front matter |
| MDX | Endast tillåtna komponenter visas. Godtyckliga skript körs inte |
| HTML | Visas efter rensning med DOMPurify 3.4.14 |

## Diagram och matematik

| Typ | Språknamn | Anmärkning |
|---|---|---|
| Matematik | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Endast inbäddade data. Externa URL:er och bildmarkeringar stöds inte |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Endast strikt JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | I den distribuerade versionen visas källan hopfälld. Gränser: 64 KiB indata, 15 sekunder, 2 MiB SVG |
| Penrose (experimentellt) | `penrose` | Endast förinställningen `set-theory` |

## Gränsvärden

| Post | Värde |
|---|---|
| Resultatet av en expanderad mall | 4 MiB |
| Referenskontext för översättning | 49 152 tecken som standard, högst 1 048 576 tecken |
| Antal dokument per samlad översättningskörning | 1 000 |
| Valfri bildbredd | 16–4096 px |

## Filer

| Fil | Roll | I Git |
|---|---|---|
| `lunascape-docs.json` | Inställningar för dokumentroten | Ja |
| `docs-lint.config.json` | Inställningar för kontrollregler | Ja |
| `.lunascape-docs/translation-freshness.json` | Registrering av översättningarnas färskhet (endast sökvägar, språk, hashvärden och tidsstämplar) | Ja |
| Inställningar och arbetsytans tillstånd i VS Code | Personliga visningsinställningar, val av leverantör, om INDEX är öppet eller stängt | Nej |

## Medföljande Standard Pack

`builtin:gu-corp-software` — profiler: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Relaterade avsnitt

- [Lista över VS Code-inställningar](settings.md)
- [Säkerhet och skrivgränser](security.md)
