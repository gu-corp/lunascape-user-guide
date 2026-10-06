# Vad är Lunascape Docs?

Lunascape Docs är ett verktyg som låter dig använda Markdown-dokument i en Git-lagringsplats direkt som en ”specifikationswebbplats”. Inget byggsteg i förväg, ingen dokumentserver och ingen särskild databas behövs.

## Det här kan du göra

| Syfte | Huvudfunktioner |
|---|---|
| Läsa | INDEX (innehållsförteckning), länkar i texten, sökväg, bakåt och framåt, innehållsförteckning för sidan, filtersökning |
| Visa | Tabeller, kodblock, automatiskt anpassade bilder, KaTeX-matematik, diagram i Mermaid, Vega-Lite, Markmap, WaveDrom och Svgbob, hopfällda tabeller för dokumentstyrning |
| Skriva | Växla mellan visuell redigering och redigering av Markdown-källan; skapa, duplicera, byta namn och ändra ordning från INDEX |
| Kontrollera | Kontroll av dokument med docs-lint, kontroll av obligatoriska dokument, avsnitt och termer enligt ett Standard Pack, skapande från mallar |
| Översätta | Översättningsförslag för en sida i taget eller för flera på en gång. Du granskar innan du sparar <!-- ai-only --> |
| Använda från AI | Ett skrivskyddat specifikationsverktyg som agenter i VS Code kan använda <!-- ai-only --> |

## Tillgängliga miljöer

| Miljö | Användning |
|---|---|
| VS Code-tillägg | Läsa, redigera, kontrollera och översätta en lagringsplats på datorn. Den här hjälpen handlar främst om tillägget |
| Webbläsarversion | Läsa dokument på GitHub (offentliga och privata), spara utkast på enheten, läsa en lokal mapp |
| Chromium-tillägg | Öppnar webbläsarversionen i en flik i webbläsaren |

## Grundprinciper

- **Markdown-filerna är originaldokumenten.** Dokumenten förblir Markdown-filer som hanteras i Git. Lunascape Docs konverterar dem aldrig till ett annat format för att lagra dem.
- **Du sparar själv.** Ändringar skrivs till filen endast när du trycker på [Spara]. Ingen staging eller commit i Git görs automatiskt.
- **Dokumenten bearbetas på enheten.** Inga dokument skickas någonstans för att läsas eller redigeras. Endast vid översättning skickas ett dokument, och först efter att mottagaren och innehållet har visats och du har godkänt det.
- **Översättningar placeras i `i18n/<språk>/`.** Dokument på standardspråket ligger kvar där de är, och översättningarna placeras med samma relativa sökväg under `i18n/en/` och så vidare.
- **AI ger bara förslag.** Översättningsförslag sparas först när du har granskat skillnaderna. Dokument skrivs aldrig om i det tysta. <!-- ai-only -->

## Relaterade avsnitt

- [Skärmens delar och deras funktioner](screen.md)
- [Installera tillägget](install.md)
- [Grundläggande användning](../02-reading/README.md)
