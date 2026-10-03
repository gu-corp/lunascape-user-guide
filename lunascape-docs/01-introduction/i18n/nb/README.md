# Hva er Lunascape Docs?

Lunascape Docs er et verktøy for å bruke Markdown-dokumentene i et Git-repositorium direkte som et «spesifikasjonsnettsted». Det trengs ingen forhåndsbygging, dokumentserver eller egen database.

## Hva du kan gjøre

| Formål | Hovedfunksjoner |
|---|---|
| Lese | INDEX (innholdsfortegnelse), lenker i teksten, brødsmuler, tilbake og fremover, innholdsfortegnelse for siden, filtersøk |
| Vise | Tabeller, kodeblokker, automatisk tilpassede bilder, KaTeX-matematikk, diagrammer i Mermaid, Vega-Lite, Markmap, WaveDrom og Svgbob, sammenfoldet visning av dokumentkontrolltabeller |
| Skrive | Bytte mellom visuell redigering og redigering av Markdown-kilden, opprette, duplisere, gi nytt navn og endre rekkefølge fra INDEX |
| Kontrollere | Kontroll av dokumenter med docs-lint, kontroll av påkrevde dokumenter, kapitler og termer etter en Standard Pack, opprettelse fra maler |
| Oversette | Lage oversettelsesforslag for én side om gangen eller samlet. Gjennomgå før du lagrer <!-- ai-only --> |
| Bruke fra KI | Et skrivebeskyttet spesifikasjonsverktøy som agenter i VS Code kan slå opp i <!-- ai-only --> |

## Hvor du kan bruke det

| Miljø | Bruk |
|---|---|
| VS Code-utvidelse | Lese, redigere, kontrollere og oversette repositoriet på maskinen din. Denne hjelpen handler hovedsakelig om dette |
| Nettleserversjon | Lese dokumenter på GitHub (offentlige og private), utkast på enheten, lese en lokal mappe |
| Chromium-utvidelse | Åpner nettleserversjonen i en fane i nettleseren |

## Grunnprinsipper

- **Markdown er originalen.** Dokumentene forblir Markdown-filer som administreres i Git. Lunascape Docs konverterer dem aldri til et annet format for lagring.
- **Du lagrer selv.** Endringer skrives til filen bare når du trykker [Lagre]. Staging og commit i Git skjer aldri automatisk.
- **Dokumenter behandles på enheten.** Dokumenter sendes aldri ut for å leses eller redigeres. Bare ved oversettelse vises mottaker og innhold på forhånd, og sendingen skjer først etter at du har godkjent.
- **Oversettelser ligger i `i18n/<språk>/`.** Dokumenter på standardspråket blir liggende der de er, og oversettelser legges med samme relative bane under `i18n/en/` og så videre.
- **KI kommer bare med forslag.** Oversettelsesforslag lagres etter at du har sett gjennom forskjellene. Dokumenter blir aldri skrevet om uten at du vet det. <!-- ai-only -->

## Relaterte emner

- [Navn og funksjoner for delene av skjermen](screen.md)
- [Installere utvidelsen](install.md)
- [Grunnleggende bruk](../02-reading/README.md)
