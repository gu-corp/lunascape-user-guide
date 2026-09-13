# Documentatiehoofdmappen wisselen

Een documentatiehoofdmap is de bovenste map van één set documenten. De INDEX, het filteren, de controles en de vertaling werken allemaal per documentatiehoofdmap.

## Hoe een documentatiehoofdmap wordt gevonden

Lunascape Docs loopt vanaf het geopende Markdown-bestand omhoog langs de bovenliggende mappen en gebruikt de dichtstbijzijnde map die aan een van de volgende voorwaarden voldoet als documentatiehoofdmap.

- Een map met `lunascape-docs.json` (de mapnaam maakt niet uit)
- Een map met de naam `docs` (met de instelling `lunascapeDocEditor.rootDirectoryNames` voegt u namen toe)

Wanneer u "Lunascape Docs: Specificatieviewer openen" uitvoert, wordt de documentatiehoofdmap uit de instelling `lunascapeDocEditor.root` (standaard `docs`) geopend.

## Naar een andere documentatiehoofdmap overschakelen

Wanneer de werkruimte meerdere documentatiehoofdmappen bevat, wordt de naam van de documentatiehoofdmap uiterst links op de werkbalk een vervolgkeuzelijst.

1. Druk op de naam van de documentatiehoofdmap uiterst links op de werkbalk.
2. Kies een documentatiehoofdmap uit de lijst.
   De startpagina van de gekozen documentatiehoofdmap wordt weergegeven en de INDEX wisselt mee.

> **Tip**
>
> De namen in de lijst worden in deze volgorde bepaald. Ze veranderen niet wanneer u de weergavetaal wijzigt.
>
> 1. `title` in `lunascape-docs.json`
> 2. `navigation.title` van de `README.md` in de hoofdmap, anders de H1 daarvan
> 3. `navigation.title` van de `index.md` in de hoofdmap, anders de H1 daarvan
> 4. De mapnaam (bij een standaardmap `docs` de naam van de bovenliggende map)

## Markdown openen die niet bij een documentatiehoofdmap hoort

Wanneer u een Markdown-bestand opent dat niet in een documentatiehoofdmap staat, wordt de map van dat bestand tijdelijk als documentatiehoofdmap weergegeven. In de INDEX staan de Markdown-bestanden in die map en daaronder.

- Druk op [Naar bovenliggende map] op de werkbalk om het weergavebereik uit te breiden tot de bovenliggende map binnen de werkruimte.
- In deze weergave zijn de taalinstellingen van het project en het in bulk vertalen niet beschikbaar. Plaats een `lunascape-docs.json` in die map om er een documentatiehoofdmap van te maken; dan zijn ze wel beschikbaar.

## Altijd een vaste documentatiehoofdmap openen

Zet de instelling `lunascapeDocEditor.rootMode` op `fixed` om altijd de documentatiehoofdmap uit `lunascapeDocEditor.root` te openen, welk Markdown-bestand u ook opent.

## Verwante onderwerpen

- [Documentatiehoofdmappen en bestandsconventies](../04-document-tools/structure.md)
- [Projectinstellingen](../04-document-tools/project-configuration.md)
- [Overzicht van VS Code-instellingen](../08-reference/settings.md)
