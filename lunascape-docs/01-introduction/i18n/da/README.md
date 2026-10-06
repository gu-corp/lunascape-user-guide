# Hvad er Lunascape Docs

Lunascape Docs er et værktøj, der behandler Markdown-dokumenter i et Git-lager som et »specifikationswebsted«, præcis som de er. Der er ikke brug for et forudgående byggetrin, en dokumentserver eller en særlig database.

## Hvad du kan gøre

| Formål | Vigtigste funktioner |
|---|---|
| Læse | INDEX (indholdsfortegnelse), links i teksten, brødkrummesti, Tilbage/Frem, indholdsfortegnelse for siden, filtersøgning |
| Se | Tabeller, kodeblokke, automatisk tilpassede billeder, KaTeX-matematik, Mermaid-, Vega-Lite-, Markmap-, WaveDrom- og Svgbob-diagrammer, sammenklappet visning af dokumentstyringstabeller |
| Skrive | Skift mellem visuel redigering og redigering af Markdown-kilden; opret, dupliker, omdøb og omarranger fra INDEX |
| Kontrollere | Kontrol af dokumenter med docs-lint, kontrol af påkrævede dokumenter, afsnit og termer ud fra en Standard Pack, oprettelse ud fra skabeloner |
| Oversætte | Oversættelsesforslag for én side ad gangen eller for flere på én gang. Gennemse dem, før de gemmes <!-- ai-only --> |
| Bruge fra AI | Et skrivebeskyttet specifikationsværktøj, som agenter i VS Code kan slå op i <!-- ai-only --> |

## Hvor du kan bruge det

| Miljø | Anvendelse |
|---|---|
| VS Code-udvidelse | Læse, redigere, kontrollere og oversætte et lager på din egen computer. Denne hjælp handler primært om den |
| Webbrowserversion | Læse dokumenter på GitHub (offentlige og private), kladder på enheden, læse en lokal mappe |
| Chromium-udvidelse | Åbner webbrowserversionen i en fane i browseren |

## Grundprincipper

- **Markdown-filerne er originaldokumenterne.** Dokumenterne forbliver de Markdown-filer, der styres med Git. Lunascape Docs konverterer dem aldrig til et andet format for at gemme dem.
- **Du gemmer selv.** Redigeringer skrives kun til filen, når du trykker på [Gem]. Git-staging og commits sker aldrig automatisk.
- **Dokumenterne behandles på din enhed.** Dokumenter sendes aldrig ud for at blive læst eller redigeret. Kun ved oversættelse vises modtager og indhold på forhånd, og der sendes først, når du har godkendt det.
- **Oversættelser placeres i `i18n/<sprog>/`.** Dokumenter på standardsproget bliver, hvor de er; oversættelser placeres med samme relative sti under `i18n/en/` osv.
- **AI kommer kun med forslag.** Oversættelsesforslag gemmes, efter at du har gennemset forskellene. Dokumenter omskrives aldrig i det skjulte. <!-- ai-only -->

## Relaterede emner

- [Skærmens dele og deres funktion](screen.md)
- [Installer udvidelsen](install.md)
- [Grundlæggende betjening](../02-reading/README.md)
