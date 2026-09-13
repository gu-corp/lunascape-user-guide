# Biztonság és írási határok

A Lunascape Docs ezekkel a határokkal védi a dokumentumokat és a készüléket.

## Megjelenítés

- A Markdownból előállított HTML-t és az ábrákból előállított SVG-t a megjelenítés előtt a DOMPurify 3.4.14 tisztítja meg.
- Az MDX-ben található tetszőleges parancsfájlokat nem futtatja.
- A KaTeX `trust: false`, `maxSize: 50` és `maxExpand: 1000` beállítással fut, és nem bízik meg sem külső HTML-ben, sem tetszőleges parancsokban.
- A Markmap, a WaveDrom, a Svgbob, a Vega-Lite és a Penrose megjelenítő programkönyvtára csak akkor töltődik be a készüléken, rögzített változatban, ha az adott blokk jelen van. Külső erőforrásokra való hivatkozás, nyers HTML és futtatható jelölés nem engedélyezett, az előállított SVG-ből pedig eltávolítja a parancsfájlokat, a külső képeket, valamint a `link`, `style` és `foreignObject` elemeket.
- A TikZ megjelenítése nem indítja el a gazdagép LaTeX programját. Egy memóriabeli fájlrendszerrel rendelkező WebAssembly TeX-munkavégzőben fut, egymás után, a bemenetre, a várakozási sorra, a memóriára, a futási időre (15 másodperc) és az SVG-kimenetre vonatkozó korlátokkal, a fájlműveleti utasításokat pedig elutasítja.

## Hozzáférés a dokumentumokhoz és a fájlokhoz

- A dokumentumok hivatkozásai és a fájlműveletek nem léphetnek ki a dokumentumgyökérből.
- Az INDEX-ből indított létrehozást, átnevezést, áthelyezést és törlést a bővítmény az alkalmazás előtt újra ellenőrzi: a dokumentumgyökeret, az INDEX változatát, a hiteles dokumentum útvonalát, a cél típusát, a szimbolikus hivatkozások határait és a nem mentett dokumentumokat. Elavult menüből vagy másik dokumentumgyökérből érkező műveleti kérést nem alkalmaz.
- Amíg egy dokumentum szerkesztés alatt áll, vagy amíg egy másik INDEX-művelet alkalmazása folyik, az INDEX módosító műveletei le vannak tiltva.
- A sablonból való létrehozás az előnézet után újra ellenőrzi a munkaterület megbízhatóságát, a dokumentumgyökér valódiságát, az INDEX változatát, a Standard Packet és az előállított tartalmat, a mentés helyét és a szimbolikus hivatkozások határait. Meglévő fájlt nem ír felül, és nem hoz létre az előnézettől eltérő tartalmat, sem 4 MiB-nál nagyobb eredményt.
- A beállításfájl mentése közvetlenül a mentés előtt ellenőrzi a változatot, és külső módosítás észlelésekor megszakad.

## Küldés kifelé

- Megtekintéshez, szerkesztéshez vagy ellenőrzéshez a dokumentumok soha nem kerülnek ki a készülékről. A dokumentumellenőrzés a készüléken, determinisztikusan fut.
- Csak a fordítás (ezen oldal fordítása, kötegelt fordítás) küld dokumentumot nyelvi modellnek: előzetesen megjeleníti a címzettet és a küldés körét, és csak kifejezett jóváhagyás esetén küld. <!-- ai-only -->
- A fordítási javaslatot különbségként mutatja meg, újra ellenőrzi a hiteles dokumentum és a fordítás célváltozatát, és csak akkor alkalmazza, ha egy ember kifejezetten menti. <!-- ai-only -->
- Az AI-ügynököknek szánt specifikációs eszköz nem ad vissza dokumentumszöveget, munkaterületnevet vagy helyi útvonalat. <!-- ai-only -->

## Git

- A mentés csak a fájlba ír. A Git előkészítését vagy véglegesítését egyetlen funkció sem végzi el automatikusan.
- A meglévő fájlokat, például a `_meta.json` fájlt, soha nem törli vagy módosítja észrevétlenül. Az árván maradt fordításokat sem törli vagy helyezi át automatikusan.

## Kapcsolódó témák

- [Fő specifikációk](README.md)
- [Használat AI-ból](ai-agents.md)
