# Wat Lunascape Docs is

Lunascape Docs behandelt de Markdown-documenten in een Git-repository zonder meer als een "specificatiesite". Een voorafgaande build, een documentserver of een aparte database is niet nodig.

## Wat u ermee kunt doen

| Doel | Belangrijkste functies |
|---|---|
| Lezen | INDEX (inhoudsopgave), links in de tekst, broodkruimels, Vorige en Volgende, overzicht van de pagina, filterzoekopdracht |
| Bekijken | Tabellen, codeblokken, automatisch passend gemaakte afbeeldingen, KaTeX-formules, diagrammen van Mermaid, Vega-Lite, Markmap, WaveDrom en Svgbob, ingeklapte documentbeheertabellen |
| Schrijven | Wisselen tussen visueel bewerken en het bewerken van de Markdown-bron; maken, dupliceren, hernoemen en herschikken vanuit de INDEX |
| Controleren | Documentcontrole met docs-lint, nagaan van verplichte documenten, hoofdstukken en termen op basis van een Standard Pack, aanmaken vanuit een sjabloon |
| Vertalen | Vertaalvoorstellen genereren per pagina of in één keer. Eerst controleren, dan opslaan <!-- ai-only --> |
| Gebruiken vanuit AI | Een alleen-lezen specificatiehulpmiddel dat agents in VS Code kunnen raadplegen <!-- ai-only --> |

## Waar u het kunt gebruiken

| Omgeving | Gebruik |
|---|---|
| VS Code-extensie | De repository op uw computer lezen, bewerken, controleren en vertalen. Deze Help gaat hier vooral over |
| Webversie | Documenten op GitHub (openbaar of privé) lezen, concepten op uw apparaat, een lokale map bekijken |
| Chromium-extensie | Opent de webversie op een tabblad van de browser |
| Lunascape-browser | Krijgt hetzelfde documentmodel ingebouwd |

## Uitgangspunten

- **Markdown is het origineel.** Documenten blijven de Markdown-bestanden die met Git worden beheerd. Lunascape Docs zet ze niet om in een andere indeling om ze zo te bewaren.
- **U bepaalt wanneer er wordt opgeslagen.** Wat u bewerkt, wordt pas naar het bestand geschreven wanneer u op [Opslaan] drukt. Stagen en vastleggen in Git gebeurt niet automatisch.
- **Documenten worden op uw apparaat verwerkt.** Om te lezen of te bewerken wordt een document nergens naartoe gestuurd. Alleen bij het vertalen worden de bestemming en de inhoud vooraf getoond en wordt er pas na uw goedkeuring verzonden.
- **Vertalingen komen in `i18n/<taal>/` te staan.** Documenten in de standaardtaal blijven op hun plaats; vertalingen krijgen hetzelfde relatieve pad onder bijvoorbeeld `i18n/en/`.
- **AI doet niet meer dan voorstellen.** Vertaalvoorstellen slaat u op nadat u de verschillen hebt bekeken. Documenten worden nooit stilzwijgend herschreven. <!-- ai-only -->

## Verwante onderwerpen

- [Namen en functies van de schermonderdelen](screen.md)
- [De extensie installeren](install.md)
- [Basishandelingen](../02-reading/README.md)
