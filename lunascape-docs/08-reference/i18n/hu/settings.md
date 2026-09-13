# VS Code-beállítások

A VS Code beállításaiban (`⌘,` / `Ctrl+,`) a „Lunascape Docs” kifejezésre keresve a következő elemeket módosíthatja. Mindegyik felhasználónkénti beállítás, és nem kerül mentésre a projekt dokumentumaiba.

## Dokumentumgyökér

| Beállítás | Érték | Alapértelmezés | Működés |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | Az `auto` a megnyitott Markdown fájlhoz legközelebbi dokumentumgyökeret választja ki automatikusan, és ha a fájl egyikhez sem tartozik, ideiglenesen a szülőmappát nyitja meg. A `fixed` mindig a `root` beállításban megadott dokumentumgyökeret nyitja meg |
| `lunascapeDocEditor.rootDirectoryNames` | Karakterláncok tömbje | `["docs"]` | Azok a mappanevek, amelyeket az `auto` mód dokumentumgyökérként automatikusan felismer. A `lunascape-docs.json` fájlt tartalmazó mappát a nevétől függetlenül felismeri. Ha az adattár gyökerében lévő `lunascape-docs.json` fájlban van `defaultFolder` vagy `roots`, akkor az élvez elsőbbséget |
| `lunascapeDocEditor.root` | Útvonal | `docs` | A munkaterülethez viszonyított dokumentumgyökér `fixed` módban, illetve a parancsból való megnyitáskor |
| `lunascapeDocEditor.startPage` | Útvonal | `README.md` | A dokumentumgyökérhez viszonyított kezdőoldal |
| `lunascapeDocEditor.title` | Karakterlánc | `Lunascape Docs` | Felülírja a dokumentumlap címét. A dokumentumgyökér választójában megjelenő névre nincs hatással |
| `lunascapeDocEditor.ignoredDirectories` | Karakterláncok tömbje | `["99-archive"]` | Az INDEX panelről kizárt mappanevek |

## Megjelenítés

| Beállítás | Érték | Alapértelmezés | Működés |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | A `light` fehér hátteret használ, az `auto` a VS Code színösszeállítását követi |
| `lunascapeDocEditor.locale` | Nyelvi címke | Nincs | Az Ön személyes dokumentumnyelve, amely elérhetőség esetén elsőbbséget élvez a megjelenítéskor. A projekt hiteles nyelvét nem változtatja meg |
| `lunascapeDocEditor.documentMetadata.compact` | Logikai érték | `true` | A H1 után álló dokumentumkezelő táblázatot a „Dokumentuminformációk” sorba csukja össze |
| `lunascapeDocEditor.tree.showFileNames` | Logikai érték | `false` | Az INDEX panelen a dokumentum neve helyett a fájlnevet jeleníti meg |
| `lunascapeDocEditor.tree.showDocumentIcons` | Logikai érték | `false` | Dokumentumikonokat jelenít meg az INDEX panelen |
| `lunascapeDocEditor.tree.showFolderIcons` | Logikai érték | `false` | Mappaikonokat jelenít meg az INDEX panelen |
| `lunascapeDocEditor.tree.showItemCounts` | Logikai érték | `false` | Megjeleníti az egyes mappák közvetlen elemeinek számát az INDEX panelen |
| `lunascapeDocEditor.tree.showGuides` | Logikai érték | `true` | Megjeleníti a szintek vezetővonalait az INDEX panelen |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Az INDEX panel sorköze |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Logikai érték | `true` | Ha csak egy dokumentum van, első alkalommal bezárja az INDEX panelt |

## Szerkesztés

| Beállítás | Érték | Alapértelmezés | Működés |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | A szerkesztési nézet mindaddig, amíg nem vált. A legutóbb használt nézet élvez elsőbbséget |
| `lunascapeDocEditor.editor.showEditButton` | Logikai érték | `true` | Megjeleníti a [Szerkesztés] gombot a szövegtörzs jobb alsó sarkában |

## Ábra

| Beállítás | Érték | Alapértelmezés | Működés |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | A TikZ megjelenítési futtatókörnyezete. A `bundled` a mellékelt jóváhagyott futtatókörnyezetet használja (a jelenlegi terjesztett változat nem tartalmazza), a `workspace` a megbízható munkaterület gyökerében lévő `node-tikzjax` 1.0.5 verziót (csak fejlesztéshez és kiértékeléshez), a `disabled` pedig nem rajzol ki semmit |

## Elavult beállítások

| Beállítás | Használja helyette |
|---|---|
| `lunascapeDocEditor.defaultLocale` | a `lunascape-docs.json` fájl `defaultLocale` beállítását |
| `lunascapeDocEditor.locales` | a `lunascape-docs.json` fájl `locales` beállítását |

A projekt nyelvei személyes beállításokkal nem írhatók felül.

## Kapcsolódó témák

- [Megjelenítési beállítások módosítása](../02-reading/display-settings.md)
- [Projektbeállítások](../04-document-tools/project-configuration.md)
