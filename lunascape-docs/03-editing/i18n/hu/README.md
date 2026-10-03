# Dokumentum szerkesztése

A dokumentumokat közvetlenül a megjelenítőben szerkesztheti. A szerkesztőnek van egy vizuális nézete, ahol azt szerkeszti, amit lát, és egy Markdown forrásnézete; egyetlen gombbal válthat közöttük.

## A szerkesztés megkezdése

Nyomja meg az alábbiak bármelyikét. Mindegyik ugyanazt a szerkesztőt nyitja meg.

- A dokumentum jobb alsó sarkában lévő [Szerkesztés]
- A dokumentum jobb felső sarkában lévő [⋯] (további műveletek) → [Szerkesztés]
- Az INDEX elemének menüje → [Szerkesztés]

## Szerkesztés

1. Szerkessze közvetlenül a szöveget.
   A szerkesztő tetején lévő eszköztáron a bekezdésformátum (törzsszöveg, 1–4. szintű címsorok, idézet, kód), a [Félkövér], a [Dőlt], a [Felsorolás], a [Számozott lista], a [Hivatkozás], a [Táblázat beszúrása], a [Képméret], a [Visszavonás] és az [Újra] áll rendelkezésre.
2. Ha közvetlenül a Markdown forrást szeretné szerkeszteni, nyomja meg a [Markdown] gombot.
   Nyomja meg újra, hogy visszatérjen a vizuális nézethez. A legutóbb használt nézet megjegyzésre kerül, és a következő alkalommal, amikor a [Szerkesztés] gombot megnyomja, visszaáll.
3. Nyomja meg a [Mentés] gombot (Ctrl+S / ⌘S billentyűkkel is menthet).
   A rendszer beírja a Markdown fájlba, és a megjelenítő visszatér az olvasási nézethez. Ha abba szeretné hagyni a szerkesztést, és vissza szeretne térni a legutóbb mentett tartalomhoz, nyomja meg a [Discard edits] gombot.

## Mindig a szerkesztőben kezdje (szerkesztési mód)

Nyomja meg az eszköztáron a [Szerkesztési mód] gombot a bekapcsoláshoz: ettől kezdve minden dokumentum a szerkesztőben nyílik meg, akárcsak egy jegyzettömb. Akkor használja, amikor ír, nem pedig olvas.

- Amíg be van kapcsolva, a [Mentés] nem zárja be a szerkesztőt. A [Discard edits] visszatér a legutóbb mentett tartalomhoz, és a szerkesztő nyitva marad.
- Nyomja meg újra a kikapcsoláshoz, ekkor visszatér az olvasási nézethez. A be- és kikapcsolt állapotot a rendszer felhasználónként megjegyzi.
- Olyan dokumentumgyökérnél, amelybe nem lehet írni (például csak olvasható GitHub-forrás), nem jelenik meg.

## Nem mentett szerkesztések

A nem mentett szerkesztések automatikusan megmaradnak ezen az eszközön. Nem vesznek el, ha másik dokumentumra vált, vagy ha bezárja a lapot vagy az ablakot.

- A szerkesztőben lévő [Unsaved] azt jelzi, hogy a szöveg eltér a legutóbb mentett tartalomtól.
- Amikor legközelebb megnyitja ugyanazt a dokumentumot, a megmaradt szerkesztésektől folytatódik, és a rendszer erről tájékoztat. Ha az eredeti dokumentum azóta frissült, arról is tájékoztat; a [Discard edits] gombbal visszatérhet a legfrissebb tartalomhoz.
- A megmaradt szerkesztések a [Mentés] vagy a [Discard edits] hatására tűnnek el. Mivel semmi sem lett mentve, nem jelennek meg a Gitben, sem a piszkozatok között.

> **Megjegyzés**
>
> - A mentés csak a fájlba írást végzi el. A Git szerinti előkészítés (staging) és a véglegesítés (commit) soha nem automatikus.
> - A képletek és az ábrák (például Mermaid, TikZ és Vega-Lite) a vizuális nézetben megjelenítve látszanak. A tartalmuk módosításához váltson a [Markdown] nézetre.
> - Az MDX-specifikus szintaxist (komponensek, `import` és hasonlók) tartalmazó dokumentumokat csak a Markdown nézetben lehet szerkeszteni, hogy a szintaxis megmaradjon.
> - A front matter (a dokumentum tetején lévő `---` sorok közé zárt beállítások) a vizuális nézetben végzett szerkesztéskor is megmarad.

> **Tipp**
>
> - A [VS Codeban való megnyitás] a szokásos szövegszerkesztőben nyitja meg a fájlt. Ha ott ment, a megjelenítő is automatikusan frissül.
> - Ha nem szeretné megjeleníteni a [Szerkesztés] gombot, kapcsolja ki a [Szerkesztés gomb] elemet a [Megjelenítési beállítások] között. Ahhoz, hogy az egész projektben elrejtse, állítsa a `lunascape-docs.json` fájlban az `editor.showEditButton` értékét `false` értékre.
> - Az elsőként megnyíló nézet (vizuális vagy Markdown) alapértelmezését a `lunascapeDocEditor.editor.defaultMode` beállítással vagy a `lunascape-docs.json` fájl `editor.defaultMode` értékével módosíthatja.

## Kapcsolódó témák

- [Dokumentumok és mappák létrehozása és rendszerezése](organize.md)
- [Képek méretezése](images.md)
- [Képletek írása](math.md)
- [Ábrák és grafikonok írása](diagrams.md)
