# Wichtigste Spezifikationen

## Systemvoraussetzungen

| Umgebung | Anforderungen |
|---|---|
| VS Code-Erweiterung | VS Code 1.90 oder neuer. Funktionen, die schreiben, arbeiten in einem vertrauenswürdigen Arbeitsbereich |
| Web-Browser-Version | Aktuelles Chrome, Edge, Safari oder Firefox. Zum Anzeigen eines lokalen Ordners ein Browser, der die Ordnerauswahl (File System Access API) unterstützt |
| Chromium-Erweiterung | Manifest V3. Es werden keine Host-Berechtigungen angefordert |

## Unterstützte Dokumente

| Punkt | Inhalt |
|---|---|
| Dateien | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (Tabellen, Aufgabenlisten, Codeblöcke, Durchstreichung), lokale Bilder, YAML-Front-Matter |
| MDX | Es werden nur zugelassene Komponenten angezeigt. Beliebige Skripte werden nicht ausgeführt |
| HTML | Wird mit DOMPurify 3.4.14 bereinigt und dann angezeigt |

## Diagramme und Formeln

| Art | Sprachname | Hinweise |
|---|---|---|
| Formeln | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Nur eingebettete Daten. Externe URLs und Bildmarken sind nicht möglich |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Nur striktes JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | In der ausgelieferten Version eingeklappte Quelltextanzeige. Obergrenzen: 64 KiB Eingabe, 15 Sekunden, 2 MiB SVG |
| Penrose (experimentell) | `penrose` | Nur die Voreinstellung `set-theory` |

## Obergrenzen

| Punkt | Wert |
|---|---|
| Ergebnis der Vorlagenexpansion | 4 MiB |
| Referenzkontext der Übersetzung | Standardmäßig 49.152 Zeichen, höchstens 1.048.576 Zeichen |
| Dokumente je Durchlauf der Sammelübersetzung | 1.000 Dokumente |
| Freie Bildbreite | 16–4096 px |

## Dateien

| Datei | Aufgabe | In Git |
|---|---|---|
| `lunascape-docs.json` | Einstellungen der Dokumentwurzel | Ja |
| `docs-lint.config.json` | Einstellungen der Prüfregeln | Ja |
| `.lunascape-docs/translation-freshness.json` | Aufzeichnung der Aktualität von Übersetzungen (nur Pfad, Sprache, Hash und Zeitstempel) | Ja |
| Einstellungen und Arbeitsbereichsstatus von VS Code | Persönliche Anzeigeeinstellungen, Wahl des Anbieters, Auf- und Zuklappzustand von INDEX | Nein |

## Mitgeliefertes Standard Pack

`builtin:gu-corp-software` — Profile: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Verwandte Themen

- [Übersicht der VS Code-Einstellungen](settings.md)
- [Sicherheit und Speichergrenzen](security.md)
