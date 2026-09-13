# Nem lehet szerkeszteni, menteni vagy átrendezni

## Nincs [Szerkesztés] gomb

- A [Megjelenítési beállítások] alatt a [Szerkesztés gomb] ki van kapcsolva. Kapcsolja be, vagy használja a törzsszöveg jobb felső sarkában a [⋯] → [Szerkesztés] menüpontot, illetve az INDEX elemmenüjében a [Szerkesztés] parancsot.
- Ugyanez a helyzet akkor is, ha a `lunascape-docs.json` fájlban az `editor.showEditButton` értéke `false`.
- A súgó megjelenítése közben nem lehet szerkeszteni. Zárja be a súgót.

## Nem lehet átváltani a vizuális nézetre

„Ez a dokumentum MDX-szintaxist tartalmaz, ezért nem lehet átváltani a szokásos szerkesztőnézetre”: az MDX-specifikus szintaxist (összetevők, `import` és társai) tartalmazó dokumentumok a szintaxis megőrzése érdekében csak Markdown nézetben szerkeszthetők.

## Nem lehet közvetlenül szerkeszteni a képleteket vagy az ábrákat

A vizuális nézet a kirajzolt eredményt mutatja. A szerkesztőnézetben nyomja meg a [Markdown] gombot, és a forrást szerkessze.

## Nem lehet átrendezni vagy húzni

- Szűrés közben, a dokumentum szerkesztése közben, valamint egy másik INDEX-művelet feldolgozása közben nem lehet átrendezni.
- Ha a munkaterület nem megbízható, a létrehozási, rendezési és törlési műveletek nem érhetők el. Jelölje meg a munkaterületet megbízhatóként a VS Code-ban.
- „Az INDEX frissült. Húzza át még egyszer”: éppen most érvényesült egy másik módosítás. Végezze el a műveletet újra.
- A kezdőoldal (a gyökérben lévő `README.md`) nem helyezhető át.

## „Nem mentett módosítások vannak” üzenet jelenik meg

Az adott fájl éppen szerkesztés alatt áll a VS Code szerkesztőjében. Előbb mentse vagy vesse el a módosításokat, majd próbálja újra.

## Nem lehet átnevezni

A következő nevek nem használhatók.

- `.` karakterrel kezdődő nevek, `i18n`, valamint a Windows fenntartott nevei (például `CON`)
- Ponttal vagy szóközzel végződő nevek, illetve vezérlőkaraktert vagy fájlnévben nem használható karaktert tartalmazó nevek
- Az azonos mappában már meglévő nevek (beleértve a csak kis- és nagybetűkben eltérő neveket is)
- Markdown-kiterjesztés nélküli dokumentumnevek

## Mentés után nem jelenik meg a módosítás a Gitben, vagy nem történik commit

A Lunascape Docs csak a fájlba ír, a Git-előkészítést (staging) és a commitot nem végzi el. Ellenőrizze a VS Code forrásvezérlő nézetében, és szükség szerint készítsen commitot.

## Kapcsolódó témák

- [Dokumentum szerkesztése](../03-editing/README.md)
- [Dokumentumok és mappák létrehozása és rendezése](../03-editing/organize.md)
- [A dokumentumok sorrendjének módosítása](../03-editing/reorder.md)
