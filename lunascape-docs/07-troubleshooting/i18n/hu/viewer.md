# A dokumentumok nem jelennek meg

## „Nem található megnyitható Markdown- vagy docs mappa” üzenet jelenik meg

- A munkaterületen nincs `docs` mappa, vagy attól eltérő nevet használ.
  - Ha a mappába helyezi a `lunascape-docs.json` fájlt, a program a nevétől függetlenül dokumentumgyökérként ismeri fel.
  - Vagy vegye fel a mappa nevét a `lunascapeDocEditor.rootDirectoryNames` beállításba.
- Ha még nincs dokumentum, hozza létre a „Lunascape Docs: Dokumentum létrehozása sablonból” paranccsal.
- Megnyithat egy Markdown-fájlt a szerkesztőben, majd futtathatja a „Lunascape Docs: Megnyitás a specifikációnézőben” parancsot is.

## Egy dokumentum nem jelenik meg az INDEX-ben

- Ellenőrizze, hogy a kiterjesztés `.md`, `.markdown` vagy `.mdx`.
- A következő mappák nem jelennek meg: a `.` karakterrel kezdődő mappák, a `node_modules`, valamint az `ignoredDirectories` beállításban megadott mappák (alapértelmezés szerint `99-archive`).
- Az `i18n/` alatti fordítások nem jelennek meg külön az INDEX-ben. A nyelvi menüből válthat rájuk.
- Ha egy most hozzáadott fájl nem jelenik meg, nyomja meg az [Újratöltés] gombot.
- Lehet, hogy másik dokumentumgyökeret néz. Ellenőrizze az eszköztár bal szélén a dokumentumgyökér nevét.

## A mappára nyomva semmi nem jelenik meg

Az adott mappa `README.md` fájlja „csak beállításokat tartalmazó leíró”: csak front mattert tartalmaz, törzsszöveget nem. Nyissa ki a mappát az INDEX-ben, és válasszon benne egy dokumentumot.

## Nem a kívánt dokumentumgyökér nyílik meg

- Ha a `lunascapeDocEditor.rootMode` beállítás értéke `fixed`, mindig a `lunascapeDocEditor.root` nyílik meg.
- `auto` esetén a megnyitott Markdown-fájlhoz legközelebbi dokumentumgyökér lesz kiválasztva. Az eszköztár bal szélén lévő legördülő listával válthat.

## A dokumentumgyökér neve eltér a várttól

A nevet a következő sorrend határozza meg: a `lunascape-docs.json` `title` mezője → a gyökér `README.md` fájljának `navigation.title` mezője → annak H1 címsora → `index.md` → a mappa neve. Ha rögzíteni szeretné, állítsa be a `title` mezőt.

## Eltűnt az INDEX

- Az olyan dokumentumgyökérben, amely csak egy dokumentumot tartalmaz, az INDEX az első alkalommal automatikusan bezárul. Az eszköztár oszlopmegjelenítés ikonjával nyithatja meg újra. A [Megjelenítési beállítások] alatt az [Elrejtés, ha csak egy dokumentum van] kapcsolóval kikapcsolhatja.
- Keskeny képernyőn a [Vissza] gombtól balra lévő [INDEX megnyitása] (három vonal) gombbal nyithatja meg.

## A hivatkozásra nyomva nem nyílik meg semmi

- „A hivatkozás célja nem található”: a hivatkozott fájl nem létezik. A belső hivatkozásokat a Dokumentumeszközök [Ellenőrzés] funkciójával ellenőrizheti.
- „Nem biztonságos vagy nem támogatott hivatkozás – a megnyitás elmaradt”: a dokumentumgyökéren kívülre mutató, illetve a `https://` és `mailto:` sémáktól eltérő hivatkozások nem nyílnak meg.

## Nem a kívánt nyelv jelenik meg

- A nyelvi menüben ellenőrizze a megjelenített oldal nyelvét és annak okát.
- A program megjegyzi a legutóbb választott megjelenítési nyelvet. A nyelvi menüben válassza ki újra az alapértelmezett nyelvet.
- Ha a személyes `lunascapeDocEditor.locale` beállítás meg van adva, az adott nyelvű fordítás élvez elsőbbséget.

## Kapcsolódó témák

- [Dokumentumgyökér váltása](../02-reading/roots.md)
- [Dokumentumgyökerek és fájlkonvenciók](../04-document-tools/structure.md)
