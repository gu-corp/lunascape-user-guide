# Documenten en mappen maken en ordenen

Via het itemmenu van de INDEX kunt u documenten en mappen maken, dupliceren, hernoemen en verwijderen. Invoer gebeurt in een klein dialoogvenster binnen de viewer, zonder het lezen te onderbreken.

> **Opmerking**
>
> Deze bewerkingen zijn alleen beschikbaar als u de werkruimte in VS Code hebt vertrouwd. Ze kunnen niet worden uitgevoerd terwijl een document wordt bewerkt, terwijl een andere bewerking wordt verwerkt of wanneer het doel niet-opgeslagen wijzigingen heeft.

## Een document of map maken

1. Open het itemmenu ([⋯] of rechtermuisklik) van de map waarin u wilt maken.
   Om rechtstreeks onder de documentatiehoofdmap te maken, gebruikt u [⋯] rechts van de INDEX-kop of klikt u met de rechtermuisknop op een leeg gedeelte van de INDEX.
2. Kies [Nieuw document] of [Nieuwe map].
3. Voer een naam in en druk op [Maken].
   Een documentnaam heeft een Markdown-extensie nodig (`.md`, `.markdown`, `.mdx` enzovoort).

Nieuwe documenten worden gemaakt als documenten in de standaardtaal (brondocument).

## Een document dupliceren

1. Open het itemmenu van het document en kies [Dupliceren].
2. Voer een nieuwe naam in en druk op [Maken].

Alleen het brondocument wordt gedupliceerd. De vertalingen worden niet gedupliceerd.

## De titel wijzigen

Wijzigt de kop (H1) van het document. De bestandsnaam blijft ongewijzigd.

1. Open het itemmenu van een document of map en kies [Titel wijzigen].
2. Voer de nieuwe titel op één regel in en druk op [Wijzigen].

Bij een map wordt de kop van de `README.md` van die map gewijzigd. Wanneer de weergegeven taal een vertaling is, wordt de titel van het document in die taal gewijzigd.

## De documentnaam wijzigen

Wijzigt de documentnaam die in de werkbalk wordt getoond (de naam van de documentatiehoofdmap).

1. Klik met de rechtermuisknop op de documentnaam in de werkbalk. U kunt het menu ook openen via [⋯] rechts van de INDEX-kop.
2. Kies [Documentnaam wijzigen] en voer een nieuwe naam in.

Zolang er niets is ingesteld, wordt de mapnaam ongewijzigd weergegeven.

De gewijzigde naam wordt geschreven naar **de plaats die op dat moment als documentnaam wordt gebruikt**. Er wordt niet naar een plaats geschreven die niet voor de weergave wordt gebruikt, zodat een zichtbare kop nooit wordt genegeerd.

| Huidige situatie | Wordt geschreven naar |
|---|---|
| `lunascape-docs.json` bevat een naam | `lunascape-docs.json` wordt bijgewerkt |
| Geen naam, maar de documentatiehoofdmap heeft een README | De kop (H1) van de README wordt herschreven |
| Geen van beide | `lunascape-docs.json` wordt gemaakt en de naam wordt daarin opgeslagen |

In het bericht na de wijziging staat waarnaar is geschreven.

> **Tip**
>
> De documentnaam wordt in deze volgorde bepaald: de naam in `lunascape-docs.json`, dan de kop van de README in de documentatiehoofdmap, dan de mapnaam.

## Een bestandsnaam of mapnaam wijzigen

1. Open het itemmenu en kies [Bestandsnaam wijzigen] of [Mapnaam wijzigen].
2. Voer de nieuwe naam in en druk op [Wijzigen].

De bijbehorende vertalingen (hetzelfde pad onder `i18n/<taal>/`) worden mee hernoemd.

## Verwijderen

1. Open het itemmenu en kies [Naar prullenbak verplaatsen].
2. Controleer de inhoud van het bevestigingsbericht en keur de verplaatsing goed.

Het item wordt naar de prullenbak van het besturingssysteem verplaatst, zodat u het zo nodig kunt herstellen. Vertalingen worden niet verwijderd en blijven staan.

## Namen die niet zijn toegestaan

- Namen die met `.` beginnen (die verschijnen niet in de INDEX)
- `i18n` (gereserveerd voor vertaalbestanden)
- Namen die in Windows zijn gereserveerd (`CON`, `PRN` enzovoort)
- Namen die eindigen op een punt of een spatie
- Namen met stuurtekens of tekens die niet in bestandsnamen zijn toegestaan
- Namen die al in dezelfde map bestaan (inclusief namen die alleen in hoofdlettergebruik verschillen)

> **Opmerking**
>
> De startpagina (normaal gesproken de `README.md` in de hoofdmap) kan niet worden hernoemd of verplaatst. Wijzig eerst `startPage` in `lunascape-docs.json`.

## Verwante onderwerpen

- [De volgorde van documenten wijzigen](reorder.md)
- [De INDEX gebruiken](../02-reading/index-panel.md)
