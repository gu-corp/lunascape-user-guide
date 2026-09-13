# Sikkerhet og skrivegrenser

Grensene Lunascape Docs opprettholder for å beskytte dokumentene dine og enheten din.

## Visning

- HTML generert fra Markdown og SVG generert fra diagrammer renses med DOMPurify 3.4.14 før de vises.
- Vilkårlige skript i MDX kjøres aldri.
- KaTeX kjører med `trust: false`, `maxSize: 50` og `maxExpand: 1000`, og stoler verken på ekstern HTML eller vilkårlige kommandoer.
- Kjøremiljøene for Markmap, WaveDrom, Svgbob, Vega-Lite og Penrose lastes lokalt, i låste versjoner, bare når den tilsvarende blokken finnes. Referanser til eksterne ressurser, rå HTML og kjørbare notasjoner tillates ikke, og skript, eksterne bilder, `link`, `style` og `foreignObject` fjernes fra generert SVG.
- TikZ-tegning starter aldri vertens LaTeX. Den kjøres sekvensielt i en WebAssembly-TeX-arbeider med et minnebasert filsystem, med grenser for inndata, kø, minne, kjøretid (15 sekunder) og SVG-utdata, og avviser fil-I/O-instruksjoner.

## Tilgang til dokumenter og filer

- Dokumentlenker og filoperasjoner kan ikke gå utenfor dokumentroten.
- Å opprette, gi nytt navn til, flytte og slette fra INDEX kontrolleres på nytt på utvidelsens side – dokumentrot, INDEX-revisjon, originaldokumentets sti, måltype, grensene for symbolske lenker og ulagrede dokumenter – før de utføres. Forespørsler fra en utdatert meny eller en annen dokumentrot utføres ikke.
- Endringer i INDEX deaktiveres mens et dokument redigeres eller mens en annen INDEX-operasjon utføres.
- Å opprette fra en mal kontrollerer på nytt om arbeidsområdet er klarert, dokumentrotens identitet, INDEX-revisjonen, Standard Pack og det genererte innholdet, målplasseringen og grensene for symbolske lenker etter forhåndsvisningen. Den overskriver aldri en eksisterende fil og oppretter aldri innhold som avviker fra forhåndsvisningen eller overstiger 4 MiB.
- Lagring av en konfigurasjonsfil kontrollerer revisjonen umiddelbart før lagring og avbrytes når en ekstern endring oppdages.

## Sending av data ut

- Dokumenter sendes aldri noe sted for lesing, redigering eller kontroll. Dokumentkontroller kjøres lokalt og deterministisk.
- Bare oversettelse (av denne siden eller i grupper) sender dokumenter til en språkmodell, etter å ha vist mål og omfang på forhånd og bare med uttrykkelig godkjenning. <!-- ai-only -->
- Oversettelsesforslag presenteres som en forskjell, revisjonene av originaldokumentet og oversettelsesmålet kontrolleres på nytt, og et forslag utføres bare når en person lagrer det uttrykkelig. <!-- ai-only -->
- Spesifikasjonsverktøyet for AI-agenter returnerer verken dokumentinnhold, navn på arbeidsområder eller lokale stier. <!-- ai-only -->

## Git

- Lagring skriver bare til filen. Ingen funksjon utfører staging eller commit i Git automatisk.
- Eksisterende filer som `_meta.json` slettes eller endres aldri i det stille. Forlatte oversettelser slettes eller flyttes aldri automatisk.

## Relaterte emner

- [Hovedspesifikasjoner](README.md)
- [Bruk fra AI](ai-agents.md)
