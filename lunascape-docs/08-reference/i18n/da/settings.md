# VS Code-indstillinger

Søg efter »Lunascape Docs« i VS Code-indstillingerne (`⌘,` / `Ctrl+,`) for at ændre følgende. Alle er personlige indstillinger og gemmes aldrig i projektets dokumenter.

## Dokumentrod

| Indstilling | Værdier | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` vælger den dokumentrod, der er tættest på den åbnede Markdown-fil, og åbner midlertidigt dens overordnede mappe, når den ikke hører til nogen. `fixed` åbner altid roden i `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Række af strenge | `["docs"]` | Mappenavne, der opdages som dokumentrødder i tilstanden `auto`. En mappe med `lunascape-docs.json` opdages uanset dens navn. En `defaultFolder` eller `roots` i `lunascape-docs.json` øverst i lageret har forrang |
| `lunascapeDocEditor.root` | Sti | `docs` | Den dokumentrod, der er relativ til arbejdsområdet, for tilstanden `fixed` og for åbn-kommandoen |
| `lunascapeDocEditor.startPage` | Sti | `README.md` | Startsiden relativt til dokumentroden |
| `lunascapeDocEditor.title` | Streng | `Lunascape Docs` | Overskriver titlen på dokumentfanen. Det påvirker ikke vælgeren af dokumentrod |
| `lunascapeDocEditor.ignoredDirectories` | Række af strenge | `["99-archive"]` | Mappenavne, der udelukkes fra INDEX |

## Visning

| Indstilling | Værdier | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` bruger en hvid baggrund; `auto` følger VS Code-temaet |
| `lunascapeDocEditor.locale` | Sprogtag | Ingen | Dit foretrukne dokumentsprog, som bruges, når det er tilgængeligt. Det ændrer aldrig projektets originalsprog |
| `lunascapeDocEditor.documentMetadata.compact` | Boolesk | `true` | Folder dokumentstyringstabellen lige efter H1 sammen til rækken »Dokumentinformation« |
| `lunascapeDocEditor.tree.showFileNames` | Boolesk | `false` | Viser filnavne i stedet for dokumenttitler i INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Boolesk | `false` | Viser dokumentikoner i INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Boolesk | `false` | Viser mappeikoner i INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Boolesk | `false` | Viser antallet af elementer direkte under hver mappe |
| `lunascapeDocEditor.tree.showGuides` | Boolesk | `true` | Viser guidelinjer for hierarkiet |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Rækkeafstanden i INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Boolesk | `true` | Lukker INDEX én gang, når der kun er ét dokument |

## Redigering

| Indstilling | Værdier | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Redigeringsvisningen, der bruges, indtil du skifter. Den senest brugte visning har forrang |
| `lunascapeDocEditor.editor.showEditButton` | Boolesk | `true` | Viser [Rediger] nederst til højre i dokumentet |

## Diagrammer

| Indstilling | Værdier | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ-gengivelsesruntimen. `bundled` bruger en godkendt, medfølgende runtime (ikke inkluderet i den aktuelle distribuerede version), `workspace` bruger `node-tikzjax` 1.0.5 i roden af en browser, du har tillid til (kun til udvikling og evaluering), `disabled` gengiver ingenting |

## Forældede indstillinger

| Indstilling | Brug i stedet |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` i `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` i `lunascape-docs.json` |

Personlige indstillinger kan ikke tilsidesætte projektets sprog.

## Relaterede emner

- [Ændring af visningsindstillinger](../02-reading/display-settings.md)
- [Projektkonfiguration](../04-document-tools/project-configuration.md)
