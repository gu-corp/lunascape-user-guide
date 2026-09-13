# VS Code-inställningar

Sök efter ”Lunascape Docs” i VS Code-inställningarna (`⌘,` / `Ctrl+,`) för att ändra följande. Samtliga är personliga inställningar och sparas aldrig i projektets dokument.

## Dokumentrot

| Inställning | Värden | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` väljer automatiskt den dokumentrot som ligger närmast den öppnade Markdown-filen och öppnar tillfälligt den överordnade mappen om filen inte hör till någon. `fixed` öppnar alltid dokumentroten i `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Array med strängar | `["docs"]` | Mappnamn som upptäcks som dokumentrötter i läget `auto`. En mapp med `lunascape-docs.json` upptäcks oavsett namn. Om `lunascape-docs.json` direkt under lagringsplatsen innehåller `defaultFolder` eller `roots` har de företräde |
| `lunascapeDocEditor.root` | Sökväg | `docs` | Dokumentroten relativt arbetsytan, i läget `fixed` eller när dokumentroten öppnas via kommandot |
| `lunascapeDocEditor.startPage` | Sökväg | `README.md` | Startsidan relativt dokumentroten |
| `lunascapeDocEditor.title` | Sträng | `Lunascape Docs` | Skriver över titeln på dokumentfliken. Den påverkar inte namnet i väljaren för dokumentrot |
| `lunascapeDocEditor.ignoredDirectories` | Array med strängar | `["99-archive"]` | Mappnamn som utesluts från INDEX |

## Visning

| Inställning | Värden | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` ger vit bakgrund, `auto` följer färgtemat i VS Code |
| `lunascapeDocEditor.locale` | Språktagg | Inget | Ditt personliga dokumentspråk, som visas i första hand när det finns. Det ändrar inte projektets originalspråk |
| `lunascapeDocEditor.documentMetadata.compact` | Booleskt | `true` | Fäller ihop dokumenthanteringstabellen direkt efter H1 till raden ”Dokumentinformation” |
| `lunascapeDocEditor.tree.showFileNames` | Booleskt | `false` | Visar filnamn i stället för dokumentnamn i INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Booleskt | `false` | Visar dokumentikoner i INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Booleskt | `false` | Visar mappikoner i INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Booleskt | `false` | Visar antalet objekt direkt under varje mapp i INDEX |
| `lunascapeDocEditor.tree.showGuides` | Booleskt | `true` | Visar hjälplinjer för nivåerna i INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Radavstånd i INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Booleskt | `true` | Stänger INDEX första gången när det bara finns ett dokument |

## Redigering

| Inställning | Värden | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Redigeringsvyn som används innan du har växlat. Den vy du använde senast har företräde |
| `lunascapeDocEditor.editor.showEditButton` | Booleskt | `true` | Visar [Redigera] längst ned till höger i dokumentet |

## Diagram

| Inställning | Värden | Standard | Funktion |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Körmiljön som ritar TikZ. `bundled` använder den medföljande godkända körmiljön (ingår inte i den nuvarande distributionen), `workspace` använder `node-tikzjax` 1.0.5 direkt under en betrodd arbetsyta (endast för utveckling och utvärdering), `disabled` ritar ingenting |

## Inaktuella inställningar

| Inställning | Använd i stället |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` i `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` i `lunascape-docs.json` |

Personliga inställningar kan inte skriva över projektets språk.

## Relaterade ämnen

- [Ändra visningsinställningar](../02-reading/display-settings.md)
- [Projektinställningar](../04-document-tools/project-configuration.md)
