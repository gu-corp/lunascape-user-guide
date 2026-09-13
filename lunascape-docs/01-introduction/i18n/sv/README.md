# Vad Lunascape Docs är

Lunascape Docs är ett verktyg som låter dig hantera Markdown-dokument i en Git-lagringsplats som en "specifikationswebbplats" precis som de är. Det behövs inget byggsteg, ingen dokumentserver och ingen särskild databas.

## Det här kan du göra

| Syfte | Huvudfunktioner |
|---|---|
| Läsa | INDEX (innehållsförteckning), länkar i texten, sökväg, bakåt och framåt, innehåll på sidan, filtrerad sökning |
| Visa | Tabeller, kodblock, automatiskt anpassade bilder, KaTeX-matematik, diagram med Mermaid, Vega-Lite, Markmap, WaveDrom och Svgbob, hopfällda dokumenthanteringstabeller |
| Skriva | Växla mellan visuell redigering och redigering av Markdown-källa; skapa, duplicera, byta namn och ändra ordning från INDEX |
| Kontrollera | Dokumentkontroll med docs-lint, kontroll av obligatoriska dokument, kapitel och termer enligt Standard Pack, skapa från mall |
| Översätta | Skapa översättningsförslag för en sida i taget eller flera samtidigt. Granska innan du sparar <!-- ai-only --> |
| Använda från AI | Ett skrivskyddat specifikationsverktyg som agenter i VS Code kan använda <!-- ai-only --> |

## Miljöer du kan använda

| Miljö | Användning |
|---|---|
| VS Code-tillägg | Läsa, redigera, kontrollera och översätta lagringsplatsen på din dator. Den här hjälpen handlar främst om detta |
| Webbläsarversion | Läsa dokument på GitHub (offentliga och privata), utkast på enheten, läsa en lokal mapp |
| Chromium-tillägg | Öppnar webbläsarversionen på en flik i webbläsaren |
| Lunascape-webbläsaren | Samma dokumentmodell är planerad att byggas in |

## Grundprinciper

- **Markdown är originalet.** Dokumenten förblir de Markdown-filer som hanteras i Git. Lunascape Docs konverterar dem inte till något annat format och behåller ingen sådan kopia.
- **Du sparar själv.** Det du redigerar skrivs till filen först när du trycker på [Spara]. Git-stegning och incheckning sker aldrig automatiskt.
- **Dokumenten behandlas på enheten.** Inget dokument skickas utanför enheten för att läsas eller redigeras. Endast vid översättning skickas något, och då visas mottagare och innehåll i förväg och sändningen sker efter ditt godkännande.
- **Översättningarna ligger under `i18n/<språk>/`.** Dokument på standardspråket ligger kvar på sin plats, och översättningarna läggs med samma relativa sökväg under `i18n/en/` och så vidare.
- **AI ger bara förslag.** Översättningsförslagen sparas först när du har granskat skillnaderna. Dokument skrivs aldrig om i tysthet. <!-- ai-only -->

## Relaterade ämnen

- [Skärmens delar och funktioner](screen.md)
- [Installera tillägget](install.md)
- [Grundläggande användning](../02-reading/README.md)
