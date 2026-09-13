# VS Code-innstillinger

Søk etter «Lunascape Docs» i VS Code-innstillingene (`⌘,` / `Ctrl+,`) for å endre følgende. Alle er personlige innstillinger og lagres aldri i prosjektets dokumenter.

## Dokumentrot

| Innstilling | Verdier | Standard | Funksjon |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` velger dokumentroten nærmest den åpnede Markdown-filen og åpner overordnet mappe midlertidig når filen ikke tilhører noen. `fixed` åpner alltid dokumentroten i `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Tabell med strenger | `["docs"]` | Mappenavn som oppdages som dokumentrøtter i `auto`-modus. En mappe med `lunascape-docs.json` oppdages uansett navn. En `defaultFolder` eller `roots` i `lunascape-docs.json` øverst i repositoriet har forrang |
| `lunascapeDocEditor.root` | Sti | `docs` | Den arbeidsområderelative dokumentroten for `fixed`-modus og for åpne-kommandoen |
| `lunascapeDocEditor.startPage` | Sti | `README.md` | Startsiden relativt til dokumentroten |
| `lunascapeDocEditor.title` | Streng | `Lunascape Docs` | Overstyrer tittelen på dokumentfanen. Den påvirker ikke valgnavnet for dokumentroten |
| `lunascapeDocEditor.ignoredDirectories` | Tabell med strenger | `["99-archive"]` | Mappenavn som utelates fra INDEX |

## Visning

| Innstilling | Verdier | Standard | Funksjon |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` bruker hvit bakgrunn; `auto` følger fargeoppsettet i VS Code |
| `lunascapeDocEditor.locale` | Språktagg | Ingen | Ditt personlige dokumentspråk, som foretrekkes når det er tilgjengelig. Det endrer ikke prosjektets originalspråk |
| `lunascapeDocEditor.documentMetadata.compact` | Boolsk | `true` | Slår sammen dokumentbehandlingstabellen rett etter H1 til raden «Dokumentinformasjon» |
| `lunascapeDocEditor.tree.showFileNames` | Boolsk | `false` | Viser filnavn i stedet for dokumentnavn i INDEX |
| `lunascapeDocEditor.tree.showDocumentIcons` | Boolsk | `false` | Viser dokumentikoner i INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Boolsk | `false` | Viser mappeikoner i INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Boolsk | `false` | Viser antall elementer rett under hver mappe |
| `lunascapeDocEditor.tree.showGuides` | Boolsk | `true` | Viser hjelpelinjer for hierarkinivåene i INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Radavstanden i INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Boolsk | `true` | Lukker INDEX én gang når det bare finnes ett dokument |

## Redigering

| Innstilling | Verdier | Standard | Funksjon |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Redigeringsvisningen som brukes til du bytter. Visningen du brukte sist, har forrang |
| `lunascapeDocEditor.editor.showEditButton` | Boolsk | `true` | Viser [Rediger] nederst til høyre i dokumentet |

## Diagram

| Innstilling | Verdier | Standard | Funksjon |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | TikZ-tegneruntime. `bundled` bruker en godkjent medfølgende runtime (ikke inkludert i den nåværende distribuerte versjonen), `workspace` bruker `node-tikzjax` 1.0.5 rett under et klarert arbeidsområde (kun for utvikling og evaluering), `disabled` tegner ingenting |

## Utfasede innstillinger

| Innstilling | Bruk i stedet |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` i `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` i `lunascape-docs.json` |

Personlige innstillinger kan ikke overstyre prosjektets språk.

## Relaterte emner

- [Endre visningsinnstillinger](../02-reading/display-settings.md)
- [Prosjektkonfigurasjon](../04-document-tools/project-configuration.md)
