# Alapműveletek

A dokumentumok megnyitásától a kívánt oldal eléréséig tartó alapműveletek.

## A dokumentumok megnyitása

1. Nyissa meg az adattárat a VS Code-ban.
2. A parancskatalógusban (`⇧⌘P` / `Ctrl+Shift+P`) futtassa a „Lunascape Docs: Specifikációnézegető megnyitása” parancsot.
   A program megkeresi a legközelebbi dokumentumgyökeret (alapértelmezés szerint a `docs` mappát), és megjeleníti annak kezdőoldalát.

> **Tipp**
>
> - Az Explorer nézetben kattintson a jobb gombbal egy Markdown fájlra, és válassza a [Lunascape Docs: Megnyitás a specifikációnézegetőben] parancsot; ekkor az a fájl nyílik meg elsőként.
> - Ha olyan Markdown fájlt nyit meg, amely egyetlen dokumentumgyökérhez sem tartozik, a program a fájl mappáját jeleníti meg ideiglenes dokumentumgyökérként.

## Váltás az oldalak között

| Művelet | Hogyan |
|---|---|
| Megnyitás a tartalomjegyzékből | Nyomja meg a dokumentum nevét a bal oldali INDEX panelen |
| Hivatkozás követése | Nyomjon meg egy hivatkozást a szövegben. Ugyanabban a nézetben nyílik meg |
| Az előzmények bejárása | Az eszköztáron a [Vissza] és az [Előre] gomb, vagy `Alt`+`←` / `Alt`+`→` |
| Vissza a kezdőoldalra | Az eszköztáron [A specifikáció kezdőlapja] |
| Egy szinttel feljebb | Az eszköztáron a [Szülő INDEX], vagy a morzsamenü egyik eleme |
| Mozgás az oldalon belül | Nyomjon meg egy címsort a jobb oldali „Ezen az oldalon” panelen |

## Dokumentum keresése

Ha szót ír az INDEX fölötti [Dokumentumok szűrése] mezőbe, csak azok a tételek jelennek meg, amelyek neve illeszkedik. A beírt szöveg törlésekor ismét minden megjelenik.

## A tartalom frissítése

Ha Markdown fájlt ment a VS Code szerkesztőjében, a megjelenítés automatikusan frissül. Ha külső eszközzel módosította a fájlokat, nyomja meg az eszköztáron az [Újratöltés] gombot.

> **Megjegyzés**
>
> - A szövegben lévő külső hivatkozások (például `https://`) az alapértelmezett böngészőben nyílnak meg. A dokumentumgyökéren kívüli fájlokra mutató hivatkozások nem nyílnak meg.
> - A megtekintett dokumentumok feldolgozása a készüléken történik. A program olvasás céljából semmit sem küld ki.

## Kapcsolódó témák

- [Az INDEX használata](index-panel.md)
- [Dokumentumgyökér váltása](roots.md)
- [Dokumentum szerkesztése](../03-editing/README.md)
