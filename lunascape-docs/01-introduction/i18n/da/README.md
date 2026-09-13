# Hvad Lunascape Docs er

Lunascape Docs gør Markdown-dokumenterne i et Git-lager til et "specifikationssted", som de er. Der kræves ingen byggetrin, ingen dokumentserver og ingen særskilt database.

## Det kan du gøre

| Formål | Vigtigste funktioner |
|---|---|
| Læse | INDEX (indholdsfortegnelse), links i teksten, brødkrummesti, Tilbage/Frem, sideoversigt, filtrerende søgning |
| Se | Tabeller, kodeblokke, automatisk tilpassede billeder, KaTeX-matematik, diagrammer fra Mermaid, Vega-Lite, Markmap, WaveDrom og Svgbob, sammenfoldede dokumentstyringstabeller |
| Skrive | Skift mellem visuel redigering og redigering af Markdown-kilden; opret, kopier, omdøb og omarrangér fra INDEX |
| Kontrollere | Dokumentkontrol med docs-lint, kontrol af påkrævede dokumenter, kapitler og termer efter en Standard Pack, oprettelse ud fra skabeloner |
| Oversætte | Generér oversættelsesforslag for én side ad gangen eller samlet. Gennemse dem, før du gemmer <!-- ai-only --> |
| Bruge fra AI | Et skrivebeskyttet specifikationsværktøj, som agenter i VS Code kan slå op i <!-- ai-only --> |

## Hvor du kan bruge det

| Miljø | Formål |
|---|---|
| VS Code-udvidelse | Læs, redigér, kontrollér og oversæt lageret på din egen maskine. Denne hjælp handler først og fremmest om den |
| Webvisning | Læs dokumenter på GitHub (offentlige og private), hold kladder på enheden, åbn en lokal mappe |
| Chromium-udvidelse | Åbner webvisningen i en browserfane |
| Lunascape-browseren | Får den samme dokumentmodel indbygget |

## Grundtanken

- **Markdown er originalen.** Dokumenterne bliver ved med at være de Markdown-filer, Git styrer. Lunascape Docs beholder dem aldrig i et andet format.
- **Du bestemmer, hvornår der gemmes.** Det, du har redigeret, skrives kun til filen, når du trykker på [Gem]. Der sker aldrig automatisk staging eller commit i Git.
- **Dokumenterne behandles på din enhed.** Intet sendes ud af huset, for at du kan læse eller redigere et dokument. Kun ved oversættelse sendes noget, og først efter at modtager og indhold er vist, og du har godkendt det.
- **Oversættelserne ligger under `i18n/<sprog>/`.** Dokumenterne på standardsproget bliver liggende, hvor de er; oversættelserne får den samme relative sti under fx `i18n/en/`.
- **AI foreslår kun.** Oversættelsesforslag gemmes, efter at du har gennemset forskellene. Dokumenter bliver aldrig ændret i stilhed. <!-- ai-only -->

## Relaterede emner

- [Skærmens dele og deres funktion](screen.md)
- [Installér udvidelsen](install.md)
- [Grundlæggende betjening](../02-reading/README.md)
