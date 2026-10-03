# Wat is Lunascape Docs?

Lunascape Docs is een hulpmiddel waarmee je de Markdown-documenten in een Git-repository direct als “specificatiesite” gebruikt. Er is geen voorafgaande build, documentserver of aparte database nodig.

## Wat je kunt doen

| Doel | Belangrijkste functies |
|---|---|
| Lezen | INDEX (inhoudsopgave), koppelingen in de tekst, broodkruimels, terug en vooruit, inhoudsopgave van de pagina, zoeken met filter |
| Bekijken | Tabellen, codeblokken, automatisch passend gemaakte afbeeldingen, KaTeX-formules, diagrammen met Mermaid, Vega-Lite, Markmap, WaveDrom en Svgbob, ingeklapte weergave van documentbeheertabellen |
| Schrijven | Wisselen tussen visueel bewerken en bewerken van de Markdown-bron; aanmaken, dupliceren, hernoemen en de volgorde wijzigen vanuit de INDEX |
| Controleren | Documentcontrole met docs-lint, controle van verplichte documenten, hoofdstukken en termen op basis van een Standard Pack, aanmaken vanuit een sjabloon |
| Vertalen | Vertaalvoorstellen genereren, per pagina of in één keer. Pas opslaan na controle <!-- ai-only --> |
| Gebruiken vanuit AI | Een alleen-lezen specificatiehulpmiddel dat agents in VS Code kunnen raadplegen <!-- ai-only --> |

## Waar je het kunt gebruiken

| Omgeving | Gebruik |
|---|---|
| VS Code-extensie | Een repository op je computer lezen, bewerken, controleren en vertalen. Deze Help gaat vooral hierover |
| Webbrowserversie | Documenten op GitHub lezen (openbaar en privé), concepten op je apparaat, een lokale map lezen |
| Chromium-extensie | Opent de webbrowserversie in een browsertabblad |

## Uitgangspunten

- **Markdown is het brondocument.** Documenten blijven de Markdown-bestanden die met Git worden beheerd. Lunascape Docs bewaart ze nooit in een ander, omgezet formaat.
- **Opslaan doe je zelf.** Wijzigingen worden alleen naar het bestand geschreven wanneer je op [Opslaan] drukt. Stagen en committen in Git gebeurt niet automatisch.
- **Documenten worden op je apparaat verwerkt.** Voor lezen of bewerken wordt geen document naar buiten verstuurd. Alleen bij vertalen worden de bestemming en de inhoud vooraf getoond, en wordt er pas na je goedkeuring verstuurd.
- **Vertalingen staan in `i18n/<taal>/`.** Documenten in de standaardtaal blijven op hun plaats; vertalingen staan onder hetzelfde relatieve pad in `i18n/en/` enzovoort.
- **AI doet alleen voorstellen.** Vertaalvoorstellen sla je pas op nadat je de verschillen hebt gecontroleerd. Documenten worden nooit ongemerkt herschreven. <!-- ai-only -->

## Verwante onderwerpen

- [Namen en functies van de schermonderdelen](screen.md)
- [De extensie installeren](install.md)
- [Basisbediening](../02-reading/README.md)
