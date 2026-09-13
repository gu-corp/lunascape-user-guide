# Setări VS Code

Căutați „Lunascape Docs” în setările VS Code (`⌘,` / `Ctrl+,`) pentru a modifica următoarele elemente. Toate sunt setări personale și nu se salvează niciodată în documentele proiectului.

## Rădăcina documentației

| Setare | Valori | Implicit | Rol |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` alege automat rădăcina documentației cea mai apropiată de fișierul Markdown deschis, iar dacă acesta nu aparține niciuneia, deschide temporar folderul părinte. `fixed` deschide întotdeauna rădăcina din `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Matrice de șiruri | `["docs"]` | Numele folderelor descoperite automat ca rădăcini ale documentației în modul `auto`. Un folder care conține `lunascape-docs.json` este descoperit indiferent de nume. Dacă fișierul `lunascape-docs.json` din rădăcina depozitului conține `defaultFolder` sau `roots`, acestea au prioritate |
| `lunascapeDocEditor.root` | Cale | `docs` | Rădăcina documentației, relativă la spațiul de lucru, folosită în modul `fixed` sau la deschiderea prin comandă |
| `lunascapeDocEditor.startPage` | Cale | `README.md` | Pagina de pornire, relativă la rădăcina documentației |
| `lunascapeDocEditor.title` | Șir | `Lunascape Docs` | Înlocuiește titlul filei documentului. Nu afectează numele afișat la selectarea rădăcinii documentației |
| `lunascapeDocEditor.ignoredDirectories` | Matrice de șiruri | `["99-archive"]` | Numele folderelor excluse din INDEX |

## Afișare

| Setare | Valori | Implicit | Rol |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` folosește fundal alb, iar `auto` urmează schema de culori din VS Code |
| `lunascapeDocEditor.locale` | Etichetă de limbă | Niciuna | Limba documentului preferată de dumneavoastră, folosită atunci când este disponibilă. Nu modifică limba canonică a proiectului |
| `lunascapeDocEditor.documentMetadata.compact` | Boolean | `true` | Restrânge tabelul de gestionare a documentului de după H1 într-un rând „Informații despre document” |
| `lunascapeDocEditor.tree.showFileNames` | Boolean | `false` | Afișează în INDEX numele fișierelor în locul titlurilor documentelor |
| `lunascapeDocEditor.tree.showDocumentIcons` | Boolean | `false` | Afișează pictogramele documentelor în INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Boolean | `false` | Afișează pictogramele folderelor în INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Boolean | `false` | Afișează în INDEX numărul de elemente aflate direct sub fiecare folder |
| `lunascapeDocEditor.tree.showGuides` | Boolean | `true` | Afișează în INDEX liniile de ghidare ale ierarhiei |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Spațierea rândurilor în INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Boolean | `true` | Închide INDEX o singură dată, atunci când există un singur document |

## Editare

| Setare | Valori | Implicit | Rol |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Vizualizarea de editare folosită cât timp nu ați comutat încă. Vizualizarea folosită ultima dată are prioritate |
| `lunascapeDocEditor.editor.showEditButton` | Boolean | `true` | Afișează [Editează] în partea din dreapta jos a documentului |

## Diagrame

| Setare | Valori | Implicit | Rol |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Mediul de execuție pentru randarea TikZ. `bundled` folosește mediul aprobat inclus în pachet (neinclus în versiunea distribuită în prezent), `workspace` folosește `node-tikzjax` 1.0.5 aflat direct în spațiul de lucru de încredere (numai pentru dezvoltare și evaluare), iar `disabled` nu randează nimic |

## Setări nerecomandate

| Setare | De folosit în schimb |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` din `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` din `lunascape-docs.json` |

Setările personale nu pot înlocui limbile proiectului.

## Subiecte conexe

- [Modificarea setărilor de afișare](../02-reading/display-settings.md)
- [Configurarea proiectului](../04-document-tools/project-configuration.md)
