# Dokumentumgyökér váltása

A dokumentumgyökér egy dokumentumkészlet legfelső mappája. Az INDEX, a szűrés, az ellenőrzés és a fordítás mind dokumentumgyökerenként működik.

## Hogyan találja meg a program a dokumentumgyökeret

A Lunascape Docs a megnyitott Markdown-fájltól felfelé haladva a szülőmappákat járja végig, és az alábbiak egyikére illeszkedő legközelebbi mappát tekinti dokumentumgyökérnek.

- `lunascape-docs.json` fájlt tartalmazó mappa (a mappa neve tetszőleges)
- `docs` nevű mappa (további nevek a `lunascapeDocEditor.rootDirectoryNames` beállítással adhatók meg)

A „Lunascape Docs: Specifikációnézet megnyitása” parancs futtatásakor a `lunascapeDocEditor.root` beállításban megadott dokumentumgyökér nyílik meg (alapértelmezés: `docs`).

## Váltás másik dokumentumgyökérre

Ha a munkaterületen több dokumentumgyökér van, az eszköztár bal szélén látható dokumentumgyökérnév legördülő listává válik.

1. Nyomja meg az eszköztár bal szélén a dokumentumgyökér nevét.
2. Válasszon egy dokumentumgyökeret a listából.
   Megjelenik a kiválasztott dokumentumgyökér kezdőoldala, és az INDEX átvált.

> **Tipp**
>
> A listában megjelenő nevek a következő sorrendben dőlnek el. A megjelenítési nyelv váltásakor nem változnak.
>
> 1. A `lunascape-docs.json` `title` mezője
> 2. A gyökérben lévő `README.md` `navigation.title` mezője, ennek hiányában a H1 címsora
> 3. A gyökérben lévő `index.md` `navigation.title` mezője, ennek hiányában a H1 címsora
> 4. A mappa neve (szabványos `docs` mappa esetén a szülőmappa neve)

## Dokumentumgyökérhez nem tartozó Markdown megnyitása

Ha olyan Markdown-fájlt nyit meg, amely nem tartozik dokumentumgyökérhez, a program a fájlt tartalmazó mappát ideiglenes dokumentumgyökérként jeleníti meg. Az INDEX az adott mappában és az alatta lévő Markdown-fájlokat sorolja fel.

- Az eszköztár [Egy mappával feljebb] gombjával a megjelenítés hatóköre kiterjeszthető a munkaterületen belüli szülőmappára.
- Ebben a nézetben a projekt nyelvi beállításai és a kötegelt fordítás nem használható. Helyezzen `lunascape-docs.json` fájlt a mappába, hogy dokumentumgyökérré váljon, és így elérhetővé váljanak.

## Mindig egy meghatározott dokumentumgyökér megnyitása

Ha a `lunascapeDocEditor.rootMode` beállítás értéke `fixed`, akkor bármely Markdown-fájl megnyitásakor mindig a `lunascapeDocEditor.root` beállításban megadott dokumentumgyökér nyílik meg.

## Kapcsolódó témák

- [Dokumentumgyökerek és fájlkonvenciók](../04-document-tools/structure.md)
- [Projektbeállítások](../04-document-tools/project-configuration.md)
- [VS Code beállítások listája](../08-reference/settings.md)
