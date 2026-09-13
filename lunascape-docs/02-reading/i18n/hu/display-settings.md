# A megjelenítési beállítások módosítása

Az eszköztár [Megjelenítési beállítások] (fogaskerék) gombjával felhasználónként módosítható, hogyan jelenik meg az INDEX, és látszik-e a szerkesztés gomb.

1. Nyomja meg az eszköztár [Megjelenítési beállítások] gombját.
2. Kapcsolja át a módosítani kívánt elemeket. A változások azonnal érvénybe lépnek.
3. A bezáráshoz nyomja meg ismét a [Megjelenítési beállítások] gombot, vagy kattintson a panelen kívülre.

## Beállítható elemek

| Csoport | Elem | Működés |
|---|---|---|
| Dokumentum nyelve | (jelenlegi állapot) | Megjeleníti a projekt alapértelmezett nyelvét és az éppen megjelenített nyelvet. A [Projektnyelvek beállítása…] paranccsal nyithatja meg a projekt nyelvi beállításait |
| Tartalom | [Fájlnevek] | A dokumentum neve helyett a fájlnevet jeleníti meg |
| | [Dokumentumikonok] | Ikont jelenít meg a dokumentumelemek mellett |
| | [Mappaikonok] | Ikont jelenít meg a mappaelemek mellett |
| | [Mappák elemszáma] | Megjeleníti a mappában lévő dokumentumok számát |
| | [Szintjelző vonalak] | A szinteket jelző vonalakat jelenít meg |
| | [Elrejtés, ha csak egy dokumentum van] | Az egyetlen dokumentumot tartalmazó dokumentumgyökérben az első alkalommal automatikusan bezárja az INDEX panelt |
| | [A dokumentum adatainak összecsukása] | A dokumentum elején lévő kezelőtáblázatot a „Dokumentumadatok” sorba csukja össze. Kikapcsolva a táblázat változatlanul jelenik meg |
| | [Megjelenítési sűrűség] | Az INDEX sorközét választja ki: [Normál] vagy [Kompakt] |
| | [Szerkesztés gomb] | Megjeleníti a [Szerkesztés] gombot a szöveg jobb alsó sarkában |
| Műveletek | [Visszaállítás a projekt alapértelmezéseire] | Törli a felhasználó összes módosítását, és visszaáll a projekt beállításaira |
| | [Bővítménybeállítások megnyitása] | Megnyitja a Lunascape Docs beállításait a VS Code beállítási képernyőjén |

> **Tipp**
>
> - A megjelenítési beállítások felhasználónként és dokumentumgyökerenként tárolódnak, és nem íródnak be a Git által kezelt fájlokba.
> - A beállítások a következő sorrendben érvényesülnek: „a felhasználó megjelenítési beállításai → VS Code beállítások → `lunascape-docs.json` → termékalapértelmezések”. A csapat közös alapértelmezéseit a `lunascape-docs.json` `tree` és `editor` szakaszában adhatja meg.

## A színösszeállítás váltása

Az eszköztár témaváltó gombjával (nap/hold) válthat a fehér háttér és a VS Code színösszeállítása között. A megnyitáskor használt színösszeállítást a `lunascapeDocEditor.appearance` beállítás (`light` vagy `auto`) határozza meg.

## Kapcsolódó témák

- [Az INDEX használata](index-panel.md)
- [Projektbeállítások](../04-document-tools/project-configuration.md)
- [VS Code beállítások listája](../08-reference/settings.md)
