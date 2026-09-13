# VS Code-instellingen

Zoek naar "Lunascape Docs" in de VS Code-instellingen (`⌘,` / `Ctrl+,`) om de volgende items te wijzigen. Het zijn allemaal persoonlijke instellingen; ze worden niet opgeslagen in de documenten van het project.

## Documentatiehoofdmap

| Instelling | Waarden | Standaard | Functie |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` kiest automatisch de documentatiehoofdmap die het dichtst bij het geopende Markdown-bestand ligt en opent tijdelijk de bovenliggende map als het bestand tot geen enkele hoofdmap behoort. `fixed` opent altijd de documentatiehoofdmap in `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Reeks tekenreeksen | `["docs"]` | Mapnamen die in `auto` automatisch als documentatiehoofdmap worden gevonden. Een map met `lunascape-docs.json` wordt gevonden ongeacht de naam. Staat er in de `lunascape-docs.json` direct in de repository een `defaultFolder` of `roots`, dan heeft die voorrang |
| `lunascapeDocEditor.root` | Pad | `docs` | De documentatiehoofdmap ten opzichte van de werkruimte, voor de modus `fixed` of bij openen via de opdracht |
| `lunascapeDocEditor.startPage` | Pad | `README.md` | De beginpagina ten opzichte van de documentatiehoofdmap |
| `lunascapeDocEditor.title` | Tekenreeks | `Lunascape Docs` | Overschrijft de titel van het documenttabblad. Heeft geen invloed op de naam in de keuzelijst van documentatiehoofdmappen |
| `lunascapeDocEditor.ignoredDirectories` | Reeks tekenreeksen | `["99-archive"]` | Mapnamen die uit de INDEX worden weggelaten |

## Weergave

| Instelling | Waarden | Standaard | Functie |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` gebruikt een witte achtergrond, `auto` volgt het kleurenschema van VS Code |
| `lunascapeDocEditor.locale` | Taalcode | Geen | Uw persoonlijke documenttaal, die bij voorrang wordt getoond wanneer die beschikbaar is. De brontaal van het project wordt niet gewijzigd |
| `lunascapeDocEditor.documentMetadata.compact` | Booleaanse waarde | `true` | Vouwt de documentbeheertabel direct onder de H1 samen tot de regel "Documentinformatie" |
| `lunascapeDocEditor.tree.showFileNames` | Booleaanse waarde | `false` | Toont in de INDEX bestandsnamen in plaats van documentnamen |
| `lunascapeDocEditor.tree.showDocumentIcons` | Booleaanse waarde | `false` | Toont documentpictogrammen in de INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Booleaanse waarde | `false` | Toont mappictogrammen in de INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Booleaanse waarde | `false` | Toont in de INDEX het aantal items direct onder elke map |
| `lunascapeDocEditor.tree.showGuides` | Booleaanse waarde | `true` | Toont hulplijnen voor de niveaus in de INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | De regelafstand van de INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Booleaanse waarde | `true` | Sluit de INDEX eenmalig wanneer er maar één document is |

## Bewerken

| Instelling | Waarden | Standaard | Functie |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | De bewerkingsweergave zolang u nog niet hebt gewisseld. De laatst gebruikte weergave heeft voorrang |
| `lunascapeDocEditor.editor.showEditButton` | Booleaanse waarde | `true` | Toont [Bewerken] rechtsonder in het document |

## Diagrammen

| Instelling | Waarden | Standaard | Functie |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | De rendering-runtime voor TikZ. `bundled` gebruikt de meegeleverde goedgekeurde runtime (niet meegeleverd in de huidige distributie), `workspace` gebruikt `node-tikzjax` 1.0.5 direct in een vertrouwde werkruimte (alleen voor ontwikkeling en evaluatie), `disabled` tekent niets |

## Afgeschafte instellingen

| Instelling | Te gebruiken in plaats daarvan |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` in `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` in `lunascape-docs.json` |

Persoonlijke instellingen kunnen de talen van het project niet overschrijven.

## Verwante onderwerpen

- [Weergave-instellingen wijzigen](../02-reading/display-settings.md)
- [Projectconfiguratie](../04-document-tools/project-configuration.md)
