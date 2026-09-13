# A nyilvántartás és a rekordok

Az [AI] lap tetején lévő nyilvántartás az egyes támogatott nyelvek fordítási állapotát mutatja. AI nélkül is megnézheti benne, hogy mi hiányzik.

| Megjelenítés | Jelentés |
|---|---|
| Hiányzó fordítás | Azoknak a dokumentumoknak a száma, amelyekhez még nincs fordítás |
| Elavult | Azoknak a dokumentumoknak a száma, amelyekhez van fordítás, de a hiteles dokumentum újabb a rögzítés időpontjánál |
| Lefordítva | A hiteles dokumentumot követő fordítások száma |

A nyilvántartást a program a dokumentumgyökér bejárásával számítja ki. Sem AI, sem nyelvi modell nem vesz részt benne.

## A fordítási rekordok frissítése

Az „elavult” állapot megállapításához rögzíteni kell a hiteles dokumentumot és a fordítást abban az állapotban, ahogyan a fordítás idején voltak. A munkamenet típusú AI közvetlenül írja a fájlokat, ezért rekord nem jön létre automatikusan.

1. Ha a fordítás elkészült, és ellenőrizte a tartalmát, nyomja meg a [Fordítási rekordok frissítése] gombot.
2. A rekord nélküli fordítások a jelenlegi hiteles dokumentumnak megfelelőként kerülnek rögzítésre.

A Claude Code munkamenetei és az API típusú mentés automatikusan rögzíti ezt (a munkamenet utasítást kap arra, hogy a `record_translation_freshness` MCP eszközt használja). Erre a gombra akkor van szükség, ha Codexszel vagy a VS Code csevegőjével fordított.

Ettől kezdve a hiteles dokumentum módosítása a hozzá tartozó fordítást „elavultként” jelöli meg.

> **Megjegyzés**
>
> - A már rekorddal rendelkező fordításokat nem írja felül, hogy a meglévő „elavult” állapot ne vesszen el.
> - A rekordok a `.lunascape-docs/translation-freshness.json` fájlba kerülnek, és csak relatív útvonalakat, nyelveket, tartalomhasheket és időbélyeget tartalmaznak – a dokumentum szövegét soha.

## Kapcsolódó témák

- [Átadható munka](tasks.md)
- [Olvasás másik nyelven](../02-reading/languages.md)
