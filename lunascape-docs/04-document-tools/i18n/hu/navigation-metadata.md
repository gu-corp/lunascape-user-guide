# Navigációs adatok beállítása

Az INDEX panelen megjelenő név és sorrend az egyes dokumentumok YAML front matter részében szerepel. A dokumentumok e nélkül is megjelennek, ilyenkor a címsor (H1) és a fájlnév szerinti sorrend érvényesül.

## A dokumentum neve és sorrendje

Írja a következőt a dokumentum elejére.

```yaml
---
navigation:
  title: Bevezetés
  order: 200
---
```

| Mező | Jelentés |
|---|---|
| `navigation.title` | Az INDEX panelen megjelenő név. Ha elhagyja, a H1, ennek híján a fájlnév szerepel |
| `navigation.order` | Egész szám, amely a sorrendet határozza meg, növekvő irányban. Ha elhagyja, az állandó alapértelmezett sorrend (fájlnév szerint) érvényes |

> **Tipp**
>
> - Az `order` értékeit 100-as lépésekben adja meg, például 100, 200, 300, így később beszúrhat közéjük egy 150-est.
> - A hiányzó, érvénytelen vagy ismétlődő `order` érték sosem rejti el a dokumentumot.
> - Az INDEX panelen végzett átrendezés magától beírja a `navigation.order` értéket; nem kell kézzel megadnia.

## A mappa neve és sorrendje

A mappa neve és sorrendje a mappa `README.md` fájljának (illetve `index.md` fájljának, ha nincs README) front matter részéhez tartozik. A nyitóoldalnak nem kell törzsszöveget tartalmaznia.

```yaml
---
navigation:
  title: Terméktervezés
  order: 100
---
```

A nyitóoldal nélküli mappa a mappanevével és az alapértelmezett sorrenddel jelenik meg. Ha az INDEX panelen végzett átnevezés vagy átrendezés megkívánja, egy csak front mattert tartalmazó `README.md` jön létre. A puszta olvasás sosem hoz létre fájlt.

## Kezelés a fordításokban

- A sorrendet és a mappa szerepét (nyitóoldal vagy csak beállítás) kizárólag az alapértelmezett nyelvű dokumentum határozza meg.
- A fordítás csak a `navigation.title` értéket írhatja felül. Ha a hiteles dokumentumnak van törzsszövege, a fordítás H1 címsora is névként szolgál.
- Önmagában álló fordítástól sosem lesz több oldal.

## Gyermekelemek rendezése és összecsukása

A mappa nyitóoldalán szereplő `navigation.children.sort` és `navigation.children.defaultCollapsed` mező azt szabályozza, hogyan rendeződnek a közvetlen gyermekelemek, és összecsukva induljanak-e. Ezek olvasása és szerkesztése a VS Code felületén később válik elérhetővé.

## Kapcsolódó témák

- [A dokumentumok sorrendjének módosítása](../03-editing/reorder.md)
- [Dokumentumgyökerek és fájlszabályok](structure.md)
