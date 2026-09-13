# Projektbeállítások

A dokumentumgyökér alatt közvetlenül elhelyezett `lunascape-docs.json` az adott dokumentumgyökér csapaton belül megosztott beállításait tartalmazza. Kezelése Git-ben történik.

## A beállítási fájl létrehozása vagy szerkesztése

- Az eszköztáron nyomja meg a [Dokumentumeszközök] gombot → az [Ellenőrzés] fület → [A szabályok forrása és a dokumentumbeállítások] → [Dokumentumbeállítások szerkesztése] elemet, és a fájl megnyílik a VS Code-ban. Ha a fájl nem létezik, ekkor létrejön egy kiinduló fájl.
- A `lunascape-docs.json` fájlnévhez a rendszer automatikusan hozzárendeli a mellékelt JSON Schema-t, amely kiegészítést és az egyes mezők leírását nyújtja. A `$schema` megadására nincs szükség.

## Példa a beállításokra

```json
{
  "id": "product-docs",
  "title": "Termékdokumentáció",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## A mezők leírása

| Mező | Jelentés | Alapértelmezés |
|---|---|---|
| `id` | Az a kulcs, amely alatt a felhasználónkénti megjelenítési beállítások tárolódnak. Adjon neki rögzített értéket, ha a beállításokat a mappa áthelyezése után is meg szeretné tartani | A mappa útvonala |
| `title` | Az eszköztár bal szélén és a dokumentumgyökerek listájában megjelenő név. A megjelenítési nyelv váltásakor sem változik | A gyökér README/index címsora, ennek hiányában a mappa neve |
| `indexTitle` | Az INDEX címsora | `INDEX` |
| `startPage` | Az elsőként megnyíló dokumentum (a dokumentumgyökérhez képest megadott relatív útvonal) | `README.md` |
| `appearance` | A színösszeállítás: `light` (mindig világos) vagy `auto` (a VS Code témáját követi) | `light` |
| `defaultLocale` | Az alapértelmezett nyelv (a hiteles dokumentumok nyelve), BCP 47 nyelvi címkeként megadva, például `ja`, `en` vagy `zh-Hant`. Ez a fordítás forrása | Nincs megadva (a szövegből következtetve jelenik meg) |
| `fallbackLocale` | Az a nyelv, amelyet elsőként látnak azok az olvasók, akiknek a környezeti nyelve egyik támogatott nyelvvel sem egyezik. A `locales` listában szereplő nyelvet adjon meg | Nincs megadva (a `defaultLocale` értéke érvényes) |
| `locales` | A támogatott nyelvek listája, beleértve a `defaultLocale` értékét is. Ezek jelennek meg a nyelvi menüben, és ezek a fordítás céljai | Csak a `defaultLocale` |
| `ignoredDirectories` | Az INDEX-ből, a keresésből és az ellenőrzésekből kihagyott mappanevek. Megadása felülírja az alapértelmezést | `["99-archive"]` |
| `tree` | Az INDEX megjelenítésének alapértelmezései. A felhasználók a megjelenítési beállításokban felülírhatják ezeket | A fenti példa szerint |
| `editor.defaultMode` | A szerkesztési nézet mindaddig, amíg a felhasználó nem vált: `visual` vagy `source` | `visual` |
| `editor.showEditButton` | Megjelenjen-e a [Szerkesztés] a dokumentum jobb alsó sarkában | `true` |
| `documentStandards.pack` | Az ellenőrzésekhez és a sablonokhoz használt Standard Pack: `builtin:<név>` vagy a dokumentumgyökérhez képest megadott relatív útvonal | Nincs |
| `documentStandards.profile` | A Pack által meghatározott profil neve | Nincs |
| `translation.enabled` | Engedélyezi a fordítási javaslatok készítését és a kötegelt fordítást | `true` |
| `translation.contextFiles` | Azok a hiteles Markdown fájlok (a dokumentumgyökérhez képest megadott relatív útvonallal), amelyeket a fordítás a terminológia és a stílus referenciájaként kap meg | `[]` |
| `translation.maxContextCharacters` | A referenciadokumentumok összesített karakterszámának felső határa (legfeljebb 1048576) | `49152` |
| `description` | Egysoros leírás a dokumentumkészletről. Az adattár kezdőlapjának kártyáin jelenik meg. A `title` mezőhöz hasonlóan karakterláncként vagy nyelvenkénti objektumként írható | Nincs |

## Annak megadása, hogy hol találhatók a dokumentumok az adattárban

Az adattár gyökerében elhelyezett `lunascape-docs.json` nem az adott mappa beállításait, hanem az **adattár térképét** is tartalmazhatja. Ha az alábbi három mező bármelyikét megadja, a fájl térképpé válik, és maga a mappa nem lesz dokumentumgyökér.

| Mező | Jelentés | Alapértelmezés |
|---|---|---|
| `defaultFolder` | Melyik mappa tartalmazza a dokumentumokat (a gyökérhez képest megadott relatív útvonal). A megnevezett mappának nincs szüksége saját beállítási fájlra | Nincs (a `docs` érvényes) |
| `roots` | Több dokumentumkészlet esetén azok listája (a gyökérhez képest megadott relatív útvonalak, megjelenítési sorrendben). Ilyenkor a gyökér lesz a kezdőlap | Nincs |
| `excludes` | A dokumentumgyökerek felderítéséből kihagyott mappák (a gyökérhez képest megadott relatív útvonalak). Az olyan beépített kizárásokhoz adódik hozzá, mint a `node_modules` | `[]` |
| `home.cards` | Megjelenjenek-e a dokumentumkészletek kártyái a kezdőlap README-je alatt. Állítsa `false` értékre, ha a hivatkozásokat maga írja meg a README-ben | `true` |

A dokumentumgyökér a következő sorrendben dől el. Felülről haladva az elsőként megtalált érvényes.

1. A beállításban vagy a parancsban megadott mappa
2. Az, amire a gyökérben lévő `lunascape-docs.json` `defaultFolder` vagy `roots` mezője mutat
3. Az a mappa, amelyben `lunascape-docs.json` található (ha egy közös szülő alatt kettő vagy több van, akkor az a szülő lesz a kezdőlap)
4. A `docs` mappa (`lunascapeDocEditor.rootDirectoryNames`)
5. Maga az adattár gyökere

> **Tipp**
>
> Ha semmit sem ír be, a 4. lépés érvényesül, így az egyetlen `docs/` mappát tartalmazó szokásos adattár ugyanúgy működik, mint eddig. A `defaultFolder` mezőt csak akkor írja be, ha a mappa neve más, például `manual`.

### Példa a térképre

```json
{
  "title": "Lunascape Súgó",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## A beállítások sorrendje

A megjelenítéssel kapcsolatos mezők a következő sorrendben érvényesülnek.

1. A felhasználó megjelenítési beállításai (a [Megjelenítési beállítások] panel)
2. A VS Code beállításai (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. A termék alapértelmezései

Egyedül a nyelvek (`defaultLocale`, `fallbackLocale`, `locales`) jelentenek kivételt: ezekre nézve a `lunascape-docs.json` a mérvadó. A projekt nyelveit a személyes VS Code-beállításokkal nem lehet felülírni.

> **Megjegyzés**
>
> A Standard Pack a `docs-lint.config.json` fájlban is megadható `standard` néven. Ha mindkettőben szerepel, a `docs-lint.config.json` élvez elsőbbséget.

## Kapcsolódó témák

- [Az ellenőrzési szabályok módosítása](rules.md)
- [A megjelenítési beállítások módosítása](../02-reading/display-settings.md)
- [VS Code-beállítások listája](../08-reference/settings.md)
