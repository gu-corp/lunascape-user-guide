# Säkerhet och skrivgränser

De gränser som Lunascape Docs upprätthåller för att skydda dina dokument och din enhet.

## Visning

- HTML som genereras från Markdown och SVG som genereras från diagram saneras med DOMPurify 3.4.14 innan de visas.
- Godtyckliga skript i MDX körs aldrig.
- KaTeX körs med `trust: false`, `maxSize: 50` och `maxExpand: 1000` och litar varken på extern HTML eller godtyckliga kommandon.
- Ritbiblioteken Markmap, WaveDrom, Svgbob, Vega-Lite och Penrose läses in lokalt, i fasta versioner, endast när motsvarande block finns. Referenser till externa resurser, rå HTML och körbara notationer tillåts inte, och skript, externa bilder, `link`, `style` och `foreignObject` tas bort från genererad SVG.
- TikZ-ritning startar aldrig värdens LaTeX. Den körs sekventiellt i en WebAssembly-TeX-arbetare med ett filsystem i minnet, med gränser för indata, kö, minne, körtid (15 sekunder) och SVG-utdata, och avvisar fil-I/O-instruktioner.

## Åtkomst till dokument och filer

- Dokumentlänkar och filoperationer kan inte gå utanför dokumentroten.
- Att skapa, byta namn på, flytta och ta bort från INDEX kontrolleras på nytt av tillägget – dokumentrot, INDEX-version, originaldokumentets sökväg, målets typ, gränserna för symboliska länkar och osparade dokument – innan det tillämpas. Begäranden från en föråldrad meny eller från en annan dokumentrot tillämpas inte.
- Ändringar i INDEX är inaktiverade medan ett dokument redigeras eller medan en annan INDEX-åtgärd tillämpas.
- Att skapa från en mall kontrollerar på nytt efter förhandsgranskningen att arbetsytan är betrodd, dokumentrotens identitet, INDEX-versionen, Standard Pack och det genererade innehållet, målplatsen och gränserna för symboliska länkar. Befintliga filer skrivs aldrig över, och innehåll som skiljer sig från förhandsgranskningen eller vars resultat överstiger 4 MiB skapas inte.
- När en konfigurationsfil sparas kontrolleras dess version omedelbart innan, och åtgärden avbryts om en extern ändring upptäcks.

## Sändning till externa tjänster

- Dokument skickas aldrig utanför enheten för läsning, redigering eller kontroll. Dokumentkontroller körs lokalt och deterministiskt.
- Endast översättning (av den här sidan eller i grupp) skickar dokument till en språkmodell, efter att mottagare och omfattning har visats i förväg och endast med uttryckligt godkännande. <!-- ai-only -->
- Översättningsförslag presenteras som en skillnad, versionerna av originaldokumentet och måldokumentet kontrolleras på nytt, och ett förslag tillämpas endast när en person sparar det uttryckligen. <!-- ai-only -->
- Specifikationsverktyget för AI-agenter returnerar varken dokumentens innehåll, arbetsytenamn eller lokala sökvägar. <!-- ai-only -->

## Git

- När du sparar skrivs endast filen. Ingen funktion utför automatisk staging eller commit i Git.
- Befintliga filer som `_meta.json` tas aldrig bort eller ändras i tysthet. Föräldralösa översättningar tas aldrig bort eller flyttas automatiskt.

## Relaterade avsnitt

- [Huvudsakliga specifikationer](README.md)
- [Användning från AI](ai-agents.md)
