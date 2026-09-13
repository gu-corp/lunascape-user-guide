# Dokumentumadatok megjelenítése

A dokumentum elején elhelyezett „dokumentumkezelési táblázat” (dokumentumazonosító, verzió, frissítés dátuma, állapot és hasonlók) olvasáskor egyetlen kis „dokumentumadatok” sorba összevonva jelenik meg. Maga a Markdown továbbra is közönséges táblázat marad, így a GitHubon is ugyanúgy olvasható.

## A megjelenítés feltételei

A címsor (H1) után közvetlenül helyezzen el egy kétoszlopos táblázatot az alábbi módon.

```markdown
# Funkcionális követelmények

| 項目 | 内容 |
|---|---|
| 文書ID | REQ-001 |
| 版 | 1.0 |
| 更新日 | 2026-08-31 |
| 状態 | 承認済み |
| 文書責任者 | G.U.Corp |
```

- Feltétel, hogy legyen benne dokumentumazonosító sor, és több kezelési tétel is szerepeljen.
- A `## 文書管理` vagy `## Document information` címsor alá helyezett táblázat is ide tartozik.
- A szöveg közepén álló táblázatok és a szokásos „tétel/tartalom” táblázatok nem alakulnak át.

## A megjelenítés módja

- Olvasáskor csak az állapot és a frissítés dátuma látszik kis betűvel.
- A sorra kattintva minden tétel megjelenik.
- Nyomtatáskor minden tétel megjelenik.
- A szerkesztőben közönséges táblázatként jelenik meg, és úgy is szerkeszthető.

> **Tipp**
>
> Ha a táblázatot összecsukás nélkül mindig táblázatként szeretné látni, kapcsolja ki a [Megjelenítési beállítások] alatt [A dokumentum adatainak összecsukása] lehetőséget.

## Kapcsolódó témák

- [Dokumentum szerkesztése](README.md)
- [Megjelenítési beállítások módosítása](../02-reading/display-settings.md)
