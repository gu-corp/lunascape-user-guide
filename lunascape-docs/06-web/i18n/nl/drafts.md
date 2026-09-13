# Concepten opslaan

Wanneer u een document bewerkt in de webviewer, worden de wijzigingen niet naar de repository geschreven. Ze worden in uw browser bewaard als "concept".

## Een concept maken

1. Open een document en druk rechtsonder op [Bewerken].
2. Bewerk het document en druk op [Opslaan].
   "Opgeslagen als concept" verschijnt en de wijziging wordt in de browser bewaard.

- Documenten met een concept krijgen een badge in de INDEX. Boven de tekst staat "Dit document is een concept op dit apparaat (niet gepubliceerd)".
- [Concepten] in de werkbalk toont het aantal en opent de lijst met concepten.

## Een concept verwerpen

- Druk op [Concept verwerpen] boven de tekst om het concept van één document te verwerpen.
- Gebruik de lijst met concepten om alle concepten te verwerpen.

## Concepten in de repository verwerken

Het "publicatieverzoek", dat concepten als pull request verstuurt, is geïmplementeerd maar niet ingeschakeld in de openbare viewer. Bewerk het document met de VS Code-extensie of in een lokale kloon om de repository te wijzigen.

> **Let op**
>
> - Concepten worden in de browser bewaard (IndexedDB). Ze gaan niet mee naar een andere browser of een ander apparaat, en als u de sitegegevens van de browser wist, verdwijnen ook de concepten.
> - Wanneer het document in de repository verandert nadat u een concept hebt gemaakt, verschijnt "De bron is bijgewerkt". Controleer de inhoud en beslis of u het concept verwerpt of gebruikt.
> - Wanneer u een lokale map bewerkt die u via [Documenten openen] hebt geopend, worden de wijzigingen rechtstreeks in het bestand opgeslagen als de browser dat ondersteunt. Bij browsers zonder die ondersteuning blijven ze alleen tijdens de huidige sessie bewaard.

## Verwante onderwerpen

- [Wat de webviewer kan](README.md)
- [Een document bewerken](../03-editing/README.md)
