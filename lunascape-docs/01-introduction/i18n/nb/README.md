# Hva Lunascape Docs er

Lunascape Docs gjør Markdown-dokumentene i et Git-repositorium om til et «spesifikasjonssted» slik de er. Det trengs ingen byggetrinn, dokumentserver eller egen database.

## Hva du kan gjøre

| Formål | Hovedfunksjoner |
|---|---|
| Lese | INDEX (innholdsfortegnelse), lenker i teksten, brødsmuler, Tilbake/Fram, sideoversikt, filtreringssøk |
| Vise | Tabeller, kodeblokker, automatisk tilpassede bilder, KaTeX-matematikk, diagrammer med Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, sammenfoldet visning av dokumentkontrolltabeller |
| Skrive | Veksle mellom visuell redigering og Markdown-kilderedigering; opprette, duplisere, gi nytt navn og endre rekkefølge fra INDEX |
| Kontrollere | Dokumentkontroll med docs-lint, sjekk av påkrevde dokumenter, kapitler og termer basert på en Standard Pack, oppretting fra maler |
| Oversette | Generere oversettelsesforslag per side eller samlet. Kontroller før du lagrer <!-- ai-only --> |
| Bruke fra AI | Et skrivebeskyttet spesifikasjonsverktøy som VS Code-agenter kan slå opp i <!-- ai-only --> |

## Hvor du kan bruke det

| Miljø | Bruk |
|---|---|
| VS Code-utvidelse | Lese, redigere, kontrollere og oversette repositoriet på maskinen din. Denne hjelpen handler mest om dette |
| Nettleserversjon | Lese dokumenter på GitHub (offentlige og private), utkast på enheten din, lese en lokal mappe |
| Chromium-utvidelse | Åpner nettleserversjonen i en nettleserfane |
| Lunascape-nettleseren | Skal bygge inn den samme dokumentmodellen |

## Grunnleggende tankegang

- **Markdown er originalen.** Dokumentene forblir Markdown-filene som forvaltes av Git. Lunascape Docs konverterer dem ikke til et annet format for lagring.
- **Du velger når du lagrer.** Det du redigerer, skrives til filen bare når du trykker [Lagre]. Git-staging og commit skjer aldri automatisk.
- **Dokumentene behandles på enheten din.** Ingenting sendes ut for å lese eller redigere et dokument. Bare ved oversettelse sendes noe, og først etter at mottaker og innhold er vist på forhånd og du har godkjent.
- **Oversettelser ligger under `i18n/<språk>/`.** Dokumenter på standardspråket blir liggende på samme sted, og oversettelsene legges med samme relative sti under `i18n/en/` og lignende.
- **AI foreslår bare.** Oversettelsesforslag lagres etter at du har kontrollert diffen. Dokumenter blir aldri skrevet om i det stille. <!-- ai-only -->

## Relaterte emner

- [Navn på og funksjon til skjermens deler](screen.md)
- [Installere utvidelsen](install.md)
- [Grunnleggende betjening](../02-reading/README.md)
