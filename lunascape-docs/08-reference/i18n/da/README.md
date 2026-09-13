# Vigtigste specifikationer

## Driftsmiljø

| Miljø | Krav |
|---|---|
| VS Code-udvidelse | VS Code 1.90 eller nyere. Funktioner, der skriver filer, virker i en browser, du har tillid til |
| Webbrowserversion | Nyere Chrome, Edge, Safari eller Firefox. Visning af en lokal mappe kræver en browser, der understøtter mappevalg (File System Access API) |
| Chromium-udvidelse | Manifest V3. Der anmodes ikke om værtstilladelser |

## Understøttede dokumenter

| Element | Indhold |
|---|---|
| Filer | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabeller, opgavelister, kodeblokke, gennemstregning), lokale billeder, YAML front matter |
| MDX | Kun tilladte komponenter vises. Vilkårlige scripts køres ikke |
| HTML | Vises efter uskadeliggørelse med DOMPurify 3.4.14 |

## Diagrammer og matematik

| Type | Sprognavn | Bemærkninger |
|---|---|---|
| Matematik | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Kun indlejrede data. Eksterne URL'er og billedmærker er ikke tilladt |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Kun streng JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Kilden vises sammenklappet i distributionsversionen. Grænser: 64 KiB input, 15 sekunder, 2 MiB SVG |
| Penrose (eksperimentel) | `penrose` | Kun forudindstillingen `set-theory` |

## Grænseværdier

| Element | Værdi |
|---|---|
| Resultatet af skabelonudvidelse | 4 MiB |
| Referencekontekst for oversættelse | 49.152 tegn som standard, højst 1.048.576 tegn |
| Mål pr. samlet oversættelse | 1.000 dokumenter |
| Vilkårlig billedbredde | 16-4096px |

## Filer

| Fil | Rolle | Git-styret |
|---|---|---|
| `lunascape-docs.json` | Konfiguration af dokumentroden | Ja |
| `docs-lint.config.json` | Konfiguration af kontrolregler | Ja |
| `.lunascape-docs/translation-freshness.json` | Registrering af oversættelsens friskhed (kun sti, sprog, hash og tidsstempel) | Ja |
| VS Code-indstillinger og arbejdsområdets tilstand | Personlige visningsindstillinger, valg af udbyder, INDEX' åbne/lukkede tilstand | Nej |

## Medfølgende Standard Pack

`builtin:gu-corp-software` — profiler: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Relaterede emner

- [VS Code-indstillinger](settings.md)
- [Sikkerhed og lagringsgrænser](security.md)
