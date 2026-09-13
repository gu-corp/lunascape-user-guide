# Belangrijkste specificaties

## Systeemvereisten

| Omgeving | Vereisten |
|---|---|
| VS Code-extensie | VS Code 1.90 of hoger. Functies die bestanden schrijven werken in een vertrouwde werkruimte |
| Webbrowserversie | Recente versies van Chrome, Edge, Safari of Firefox. Voor het openen van een lokale map is een browser nodig die mapselectie (File System Access API) ondersteunt |
| Chromium-extensie | Manifest V3. Er worden geen hostrechten gevraagd |

## Ondersteunde documenten

| Onderdeel | Inhoud |
|---|---|
| Bestanden | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabellen, takenlijsten, codeblokken, doorhalen), lokale afbeeldingen, YAML front matter |
| MDX | Alleen toegestane componenten worden weergegeven. Willekeurige scripts worden niet uitgevoerd |
| HTML | Wordt vóór weergave onschadelijk gemaakt met DOMPurify 3.4.14 |

## Diagrammen en formules

| Soort | Taalnaam | Opmerkingen |
|---|---|---|
| Formules | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Alleen ingesloten gegevens. Externe URL's en afbeeldingsmarkeringen zijn niet mogelijk |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Alleen strikte JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | In de distributieversie wordt de bron ingeklapt weergegeven. Limieten: 64 KiB invoer, 15 seconden, 2 MiB SVG |
| Penrose (experimenteel) | `penrose` | Alleen de voorinstelling `set-theory` |

## Limieten

| Onderdeel | Waarde |
|---|---|
| Resultaat van sjabloonverwerking | 4 MiB |
| Referentiecontext voor vertaling | Standaard 49.152 tekens, maximaal 1.048.576 tekens |
| Documenten per bulkvertaling | 1.000 documenten |
| Aangepaste afbeeldingsbreedte | 16–4096px |

## Bestanden

| Bestand | Rol | In Git |
|---|---|---|
| `lunascape-docs.json` | Instellingen van de documentatiehoofdmap | Ja |
| `docs-lint.config.json` | Instellingen van de controleregels | Ja |
| `.lunascape-docs/translation-freshness.json` | Registratie van de actualiteit van vertalingen (alleen paden, talen, hashes en tijdstempels) | Ja |
| Instellingen en werkruimtestatus van VS Code | Persoonlijke weergave-instellingen, keuze van de provider, open/dicht-status van INDEX | Nee |

## Meegeleverde Standard Pack

`builtin:gu-corp-software` — profielen: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Verwante onderwerpen

- [Overzicht van VS Code-instellingen](settings.md)
- [Beveiliging en opslaggrenzen](security.md)
