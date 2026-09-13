# Specifiche principali

## Requisiti di sistema

| Ambiente | Requisiti |
|---|---|
| Estensione VS Code | VS Code 1.90 o successivo. Le funzioni che scrivono file richiedono un'area di lavoro attendibile |
| Versione per browser web | Versioni recenti di Chrome, Edge, Safari o Firefox. Per aprire una cartella locale serve un browser che supporti la selezione di cartelle (File System Access API) |
| Estensione Chromium | Manifest V3. Non richiede autorizzazioni host |

## Documenti supportati

| Voce | Contenuto |
|---|---|
| File | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabelle, elenchi di attività, blocchi di codice, testo barrato), immagini locali, front matter YAML |
| MDX | Vengono visualizzati solo i componenti consentiti. Non viene eseguito alcuno script arbitrario |
| HTML | Viene visualizzato dopo la sanificazione con DOMPurify 3.4.14 |

## Diagrammi e formule

| Tipo | Nome del linguaggio | Note |
|---|---|---|
| Formule | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Solo dati incorporati. Non sono ammessi URL esterni né marchi immagine |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Solo JSON rigoroso |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Nella versione distribuita il sorgente è mostrato compresso. Limiti: 64 KiB di input, 15 secondi, 2 MiB di SVG |
| Penrose (sperimentale) | `penrose` | Solo preset `set-theory` |

## Valori limite

| Voce | Valore |
|---|---|
| Risultato dell'espansione del modello | 4 MiB |
| Contesto di riferimento della traduzione | 49.152 caratteri per impostazione predefinita, massimo 1.048.576 |
| Documenti per ogni traduzione in blocco | 1.000 |
| Larghezza personalizzata delle immagini | 16–4096px |

## File

| File | Ruolo | In Git |
|---|---|---|
| `lunascape-docs.json` | Impostazioni della radice della documentazione | Sì |
| `docs-lint.config.json` | Impostazioni delle regole di controllo | Sì |
| `.lunascape-docs/translation-freshness.json` | Registro dell'aggiornamento delle traduzioni (solo percorsi, lingue, hash e date) | Sì |
| Impostazioni di VS Code e stato dell'area di lavoro | Impostazioni di visualizzazione personali, scelta del provider, stato di apertura di INDEX | No |

## Standard Pack incluso

`builtin:gu-corp-software` — profili: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Argomenti correlati

- [Elenco delle impostazioni di VS Code](settings.md)
- [Sicurezza e limiti di salvataggio](security.md)
