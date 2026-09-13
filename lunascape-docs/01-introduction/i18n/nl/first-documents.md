# Uw eerste documenten maken

In een project dat nog geen documentenmap heeft, kunt u vanuit het opdrachtenpalet een eerste set documenten maken.

1. Open de projectmap in VS Code en vertrouw de werkruimte.
2. Voer in het opdrachtenpalet (`⇧⌘P` / `Ctrl+Shift+P`) "Lunascape Docs: Documentatie maken op basis van een sjabloon" uit.
   Als de werkruimte meerdere mappen bevat, kiest u de werkruimte waarin de documenten worden gemaakt.
3. Kies de structuur die u wilt maken.
   - [Document van één pagina]: alleen een `README.md`. Geschikt voor een korte specificatie, notities of een losstaand uitlegdocument.
   - [Volledige documentatie]: een startpagina plus ingangen voor `specification/` (specificaties), `manual/` (handleiding) en `help/` (help).
4. Voer de titel van de documentatie in. Deze wordt gebruikt voor de README en voor de koppen van elk document.
5. Voer de documentenmap in die moet worden gemaakt. Dit is een pad ten opzichte van de werkruimte; de standaardwaarde is `docs`.
6. Controleer de lijst met bestanden die worden gemaakt en druk op [Maken].
   Zodra het maken is voltooid, wordt de nieuwe `README.md` in de viewer geopend.

> **Opmerking**
>
> - Bestaande bestanden worden niet overschreven. Als ook maar één van de te maken bestanden al bestaat, wordt er niets gemaakt en wordt de bewerking afgebroken.
> - In een niet-vertrouwde werkruimte kunt u niets maken.

> **Tip**
>
> - Hebt u al een documentenmap, dan slaat u deze stappen over en gaat u verder met [Basishandelingen](../02-reading/README.md).
> - Naarmate de documentatie groeit, kunt u op het tabblad [Maken] van Documenthulpmiddelen een sjabloon kiezen en documenten één voor één toevoegen.

## Verwante onderwerpen

- [Een document maken op basis van een sjabloon](../04-document-tools/templates.md)
- [Documentatiehoofdmappen en bestandsconventies](../04-document-tools/structure.md)
