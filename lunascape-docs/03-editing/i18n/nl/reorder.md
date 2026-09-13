# De volgorde van documenten wijzigen

De volgorde in de INDEX kunt u wijzigen met slepen en neerzetten of met het toetsenbord. De gewijzigde volgorde wordt als `navigation.order` opgeslagen in de front matter van het document.

## Volgorde wijzigen met slepen en neerzetten

1. Sleep een document of map in de INDEX.
2. Zet het vóór of na een item op hetzelfde niveau neer, of op een map.
   Binnen hetzelfde niveau verandert de volgorde. Zet u het op een andere map neer, dan wordt het naar die map verplaatst.

## Volgorde wijzigen met het toetsenbord of het menu

- Plaats de focus op een item in de INDEX en druk op `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Kies [Eén plaats omhoog] / [Eén plaats omlaag] in het menu van het item.

## Wat er wordt opgeslagen

- Wijzigt u de volgorde binnen hetzelfde niveau, dan wordt `navigation.order` in de front matter van het brondocument bijgewerkt. Bij een map wordt dit weggeschreven naar de `README.md` van die map. Heeft de map geen `README.md`, dan wordt er een `README.md` met alleen front matter aangemaakt.
- Verplaatst u een item naar een andere map, dan worden het brondocument en de bijbehorende vertalingen samen verplaatst. Vóór het verplaatsen wordt om een bevestiging gevraagd, omdat dit gevolgen kan hebben voor relatieve koppelingen.
- Er wordt niet gestaged of gecommit in Git.

> **Let op**
>
> - De volgorde kan niet worden gewijzigd tijdens het filteren, tijdens het bewerken van een document en in een niet-vertrouwde werkruimte.
> - Verschijnt de melding "De INDEX is bijgewerkt", dan is zojuist een andere wijziging doorgevoerd. Voer de handeling opnieuw uit.
> - De startpagina kan niet naar een andere map worden verplaatst.

> **Tip**
>
> Geeft u `navigation.order` waarden in stappen van 100, zoals 100, 200 en 300, dan kunt u er later gemakkelijk documenten tussen plaatsen. Zie [Navigatiegegevens instellen](../04-document-tools/navigation-metadata.md) voor meer informatie.

## Verwante onderwerpen

- [Documenten en mappen maken en ordenen](organize.md)
- [Navigatiegegevens instellen](../04-document-tools/navigation-metadata.md)
