# Olvasás másik nyelven

Ha egy dokumentumnak van fordítása, az eszköztár nyelvmenüjéből (földgömb) válthat nyelvet.

## Nyelvváltás

1. Nyomja meg az eszköztár nyelvmenüjét.
   Megjelenik az aktuális oldal nyelve és annak alapja (a fordítás útvonala, automatikus felismerés vagy a projekt alapértelmezett nyelve).
2. Válassza ki az olvasni kívánt nyelvet.
   Megnyílik ugyanannak a dokumentumnak a fordítása. A program megjegyzi a választott nyelvet, és a következő megnyitott dokumentumot is ezen a nyelven jeleníti meg, ha van hozzá fordítás.

A nyelvek listája azt is mutatja, hogy az adott dokumentumnak van-e fordítása.

| Jelzés | Jelentése |
|---|---|
| Van fordítás | Létezik fordítás, és megnyitható |
| Nincs fordítás | A projekt támogatja ezt a nyelvet, de ehhez a dokumentumhoz még nincs fordítás |
| Frissítendő | Van fordítás, de a forrásdokumentum a fordítás óta megváltozott |

> **Megjegyzés**
>
> - A nyelv kiválasztása csak egy meglévő fordítást nyit meg. Fordítást nem hoz létre, és fájlt sem készít. Fordítás létrehozásához használja ugyanennek a menünek a [Fordítások létrehozása és kezelése…] pontját.
> - Ha a program úgy ítéli meg, hogy az aktuális oldal nyelve eltér a projekt alapértelmezett nyelvétől, figyelmeztetés jelenik meg. A beállítások soha nem íródnak felül.

## Az elsőként megjelenő nyelv

Dokumentum megnyitásakor az első megjelenítési nyelvet a következő sorrend határozza meg.

1. Az a nyelv, amelyet korábban ebben a dokumentumgyökérben saját maga választott. A választás mentésre kerül (az alapértelmezett nyelv kiválasztása is választásként mentődik).
2. A VS Code megjelenítési nyelve (webböngészős változatban a böngésző nyelvi beállítása). A program automatikusan kiválasztja az ezzel egyező támogatott nyelvet. A régiójelöléssel ellátott nyelvek (például `en-US`) az alapnyelvvel (`en`) is egyezésnek számítanak.
3. A projekt tartaléknyelve (`lunascape-docs.json` fájl `fallbackLocale` beállítása).
4. A projekt alapértelmezett nyelve.

> **Tipp**
>
> - Automatikus kiválasztás esetén a nyelvmenü aktuális nyelvénél „automatikus kiválasztás” felirat jelenik meg. Ha a jelzés fölé viszi a mutatót, megjelenik az indoklás.
> - A `fallbackLocale` az a nyelv, amelyet azoknak az olvasóknak mutat a program, akiknek a környezeti nyelve egyik támogatott nyelvvel sem egyezik. Ha egy japán hiteles dokumentumokból és angol fordításokból álló projektben `"en"` értéket ad meg, a például spanyol nyelvű környezetben olvasók az angol változatot kapják. Ha nincs beállítva, az alapértelmezett nyelv érvényesül.

## A fordítások helye

Az alapértelmezett nyelvű dokumentumok a helyükön maradnak, a fordítások pedig **ugyanannak a mappának az `i18n/<nyelv>/` almappájába** kerülnek, azonos fájlnévvel.

```text
docs/
  README.md                  ← alapértelmezett nyelv (például japán)
  i18n/en/README.md          ← ennek az angol fordítása
  guide/
    setup.md
    i18n/en/setup.md         ← ennek az angol fordítása
```

> **Megjegyzés**
>
> - A mappaszerkezet `i18n/` alatti újraépítését (`i18n/en/guide/setup.md`) a program nem ismeri fel. Az `i18n/` mappa mindig a lefordított dokumentummal azonos mappában áll.
> - A fordítások feloldása kizárólag ezen az egy helyen történik. Ha ugyanannak a dokumentumnak a fordítását a szülőmappa `i18n/` mappájába is elhelyezi, abból nem lesz elsőbbségi ütközés: az ottani példány egyszerűen árva fájllá válik, amely sem a nyelvmenüben, sem a nyilvántartásban nem jelenik meg (és a program nem is törli automatikusan). Ne tartson egy fordítást két helyen.

## Olvasás a webböngészős változatban

A webböngészős változatban is ugyanígy válthat nyelvet, ha van fordítás. Ha olyan nyelven szeretne olvasni, amelyhez nincs fordítás, használhatja a böngésző oldalfordító funkcióját. A kód, a képletek és az ábrák ki vannak zárva a fordításból.

## Kapcsolódó témák

- [Munka átadása az AI-nak](../05-ai/README.md)
- [Átadható munkák](../05-ai/tasks.md)
- [Megjelenítési beállítások módosítása](../02-reading/display-settings.md)
