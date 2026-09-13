# Dokumentumgyökér és fájlkonvenciók

Ezek azok a szabályok, amelyeket a Lunascape Docs követ a dokumentumok megtalálásakor és az INDEX felépítésekor. Maga a fájlrendszer a hiteles forrás, ezért nincs szükség nyilvántartásra vagy build-beállításokra.

## Dokumentumgyökér

- A legközelebbi `docs` mappa vagy az a mappa, amelyben a `lunascape-docs.json` található, lesz a dokumentumgyökér.
- Ha elhelyez egy `lunascape-docs.json` fájlt, a mappa neve nem kell, hogy `docs` legyen.
- Ha olyan Markdown fájlt nyit meg, amely egyetlen dokumentumgyökérhez sem tartozik, a program a fájl mappáját ideiglenes dokumentumgyökérként jeleníti meg.

## Az INDEX-ben megjelenő fájlok

- A `.md`, `.markdown` és `.mdx` fájlok jelennek meg. Az új fájlok mindig megjelennek, front matter és navigációs információ nélkül is.
- A `.` karakterrel kezdődő mappák, a `node_modules`, valamint az `ignoredDirectories` beállításban megadott mappák (alapértelmezés szerint `99-archive`) nem jelennek meg.
- Az `i18n/` alatti fájlok fordításnak számítanak, és nem jelennek meg külön az INDEX-ben.

## Mappák címlapja

- A törzsszöveget tartalmazó `README.md` (ennek hiányában az `index.md`) az adott mappa címlapja. Ha az INDEX-ben a mappa nevére kattint, a címlap nyílik meg.
- Az a `README.md`, amely csak front mattert tartalmaz, törzsszöveget nem, „kizárólag beállítást leíró fájlnak” számít, és nem jelenik meg oldalként. Akkor használja, ha a mappának csak címet vagy sorrendet szeretne adni.
- Ha a `README.md` és az `index.md` is létezik, a `README.md` élvez elsőbbséget.

## Alapértelmezett nyelv és fordítások

- Az alapértelmezett nyelvű dokumentumok (a hiteles dokumentumok) a helyükön maradnak.
- A fordítás a hiteles dokumentummal azonos mappában lévő `i18n/<nyelv>/` mappába kerül, ugyanazzal a fájlnévvel. Ha a mappaszerkezetet építi újra az `i18n/` alatt, azt a program nem ismeri fel.
- A feloldás kizárólag erről az egy helyről történik. A máshová helyezett, azonos nevű fordítás árva fájl marad, amelyet egyetlen dokumentum sem tekint a fordításának.

```text
docs/
  lunascape-docs.json
  README.md                  ← a dokumentumgyökér címlapja (kezdőoldal)
  i18n/en/README.md          ← ennek angol változata
  01-product/
    README.md                ← a mappa címlapja
    requirements.md
    i18n/en/README.md        ← a fenti két dokumentum angol változata
    i18n/en/requirements.md
  99-archive/                ← alapértelmezés szerint kizárva az INDEX-ből
```

## A `_meta.json` fájlról

A Nextra `_meta.json` fájlját a program nem használja a navigációhoz. A meglévő fájlokat sem módosítja, sem törli. A jövőben csak egy kifejezett importáló és exportáló funkció fogja kezelni őket.

## Kapcsolódó témák

- [Navigációs információk beállítása](navigation-metadata.md)
- [Projektbeállítások](project-configuration.md)
- [Váltás másik dokumentumgyökérre](../02-reading/roots.md)
