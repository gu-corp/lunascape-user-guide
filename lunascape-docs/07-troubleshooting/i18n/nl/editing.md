# Bewerken, opslaan of herschikken lukt niet

## De knop [Bewerken] ontbreekt

- [Bewerkknop] in [Weergave-instellingen] staat uit. Zet deze aan, of gebruik [⋯] → [Bewerken] rechtsboven in het document, of het itemmenu in INDEX → [Bewerken].
- Hetzelfde geldt wanneer `editor.showEditButton` in `lunascape-docs.json` op `false` staat.
- Terwijl de Help wordt weergegeven, kunt u niet bewerken. Sluit de Help.

## Overschakelen naar de visuele weergave lukt niet

"Dit document bevat MDX-syntaxis en kan daarom niet in het gewone bewerkingsscherm worden geopend": documenten met MDX-specifieke syntaxis (componenten, `import` en dergelijke) bewerkt u alleen in de Markdown-weergave, om die syntaxis te behouden.

## Formules of diagrammen rechtstreeks bewerken lukt niet

De visuele weergave toont het weergaveresultaat. Druk in het bewerkingsscherm op [Markdown] en bewerk de bron.

## Herschikken of slepen lukt niet

- Tijdens het filteren, tijdens het bewerken van een document en terwijl een andere INDEX-bewerking wordt uitgevoerd, kunt u niet herschikken.
- Als u de werkruimte niet vertrouwt, zijn de acties voor maken, ordenen en verwijderen niet beschikbaar. Vertrouw de werkruimte in VS Code.
- "INDEX is bijgewerkt. Sleep het item opnieuw": er is zojuist een andere wijziging verwerkt. Voer de handeling opnieuw uit.
- De startpagina (de `README.md` in de hoofdmap) kan niet worden verplaatst.

## Er verschijnt "Er zijn niet-opgeslagen wijzigingen"

Het betreffende bestand wordt bewerkt in de editor van VS Code. Sla de wijzigingen eerst op of verwerp ze en probeer het opnieuw.

## De naam wijzigen lukt niet

De volgende namen kunnen niet worden gebruikt.

- Namen die met `.` beginnen, `i18n` en gereserveerde namen van Windows (zoals `CON`)
- Namen die eindigen op een punt of een spatie, en namen met stuurtekens of tekens die niet zijn toegestaan in bestandsnamen
- Namen die al voorkomen in dezelfde map (ook namen die alleen in hoofdletters of kleine letters verschillen)
- Documentnamen zonder Markdown-extensie

## Opgeslagen wijzigingen verschijnen niet in Git of worden niet vastgelegd

Lunascape Docs schrijft alleen naar het bestand en voert geen staging of commit uit in Git. Controleer dit in de weergave Broncodebeheer van VS Code en leg de wijzigingen zo nodig vast.

## Verwante onderwerpen

- [Een document bewerken](../03-editing/README.md)
- [Documenten en mappen maken en ordenen](../03-editing/organize.md)
- [De volgorde van documenten wijzigen](../03-editing/reorder.md)
