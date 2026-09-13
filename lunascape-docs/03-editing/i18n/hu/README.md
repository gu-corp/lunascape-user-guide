# Dokumentum szerkesztése

A dokumentumokat közvetlenül a megjelenítőben lehet szerkeszteni. A szerkesztőnek van egy vizuális nézete, ahol azt szerkeszti, amit lát, és egy Markdown forrásnézete; egyetlen gombbal válthat közöttük.

## A szerkesztés megkezdése

Nyomja meg az alábbiak bármelyikét. Mindegyik ugyanazt a szerkesztőt nyitja meg.

- A dokumentum jobb alsó sarkában a [Szerkesztés]
- A dokumentum jobb felső sarkában a [⋯] (további műveletek) → [Szerkesztés]
- Az INDEX elemmenüje → [Szerkesztés]

## Szerkesztés

1. Szerkessze közvetlenül a szöveget.
   A szerkesztő tetején lévő eszköztáron a bekezdésformátum (törzsszöveg, 1–4. szintű címsor, idézet, kód), a [Félkövér], a [Dőlt], a [Felsorolás], a [Számozott lista], a [Hivatkozás], a [Táblázat beszúrása], a [Képméret], a [Visszavonás] és az [Újra] érhető el.
2. Ha közvetlenül a Markdown forrást szeretné szerkeszteni, nyomja meg a [Markdown] gombot.
   Ismételt megnyomásával visszatér a vizuális nézetbe. A program megjegyzi a legutóbb használt nézetet, és a következő [Szerkesztés] gombnyomáskor visszaállítja.
3. Nyomja meg a [Mentés] gombot.
   A program a Markdown fájlba írja a változásokat, és visszatér az olvasónézetbe. Ha mégsem szeretné menteni, nyomja meg a [Mégse] gombot.

> **Megjegyzés**
>
> - A mentés csak a fájlba írást végzi el. A Git-előkészítés (staging) és a véglegesítés (commit) soha nem történik meg automatikusan.
> - A képleteket és az ábrákat – például a Mermaid, a TikZ és a Vega-Lite ábrákat – a vizuális nézet megjelenített formában mutatja. A tartalmuk módosításához váltson a [Markdown] nézetre.
> - Az MDX-re jellemző szintaxist (összetevőket, `import` utasítást és hasonlókat) tartalmazó dokumentumok csak a Markdown nézetben szerkeszthetők, hogy a szintaxis épen maradjon.
> - A front matter (a dokumentum elején a `---` sorok közötti beállítások) a vizuális nézetben végzett szerkesztés után is megmarad.

> **Tipp**
>
> - A [Megnyitás a VS Code-ban] gombbal a fájlt a szokásos szövegszerkesztőben nyithatja meg. Ha ott menti, a megjelenítő is automatikusan frissül.
> - Ha nem szeretné látni a [Szerkesztés] gombot, kapcsolja ki a [Szerkesztés gomb] beállítást a [Megjelenítési beállítások] között. Ha az egész projektben el kívánja rejteni, állítsa az `editor.showEditButton` értékét `false` értékre a `lunascape-docs.json` fájlban.
> - Az először megnyíló nézet (vizuális vagy Markdown) alapértelmezését a `lunascapeDocEditor.editor.defaultMode` beállítással, illetve a `lunascape-docs.json` fájl `editor.defaultMode` értékével módosíthatja.

## Kapcsolódó témák

- [Dokumentumok és mappák létrehozása és rendezése](organize.md)
- [Képek méretének beállítása](images.md)
- [Képletek írása](math.md)
- [Ábrák és diagramok készítése](diagrams.md)
