# Átadható munkák

Az [AI] lapon a [Feladat] alatt választhat. Minden munkához más átadott utasítás és más utólagos ellenőrzés tartozik.

| Munka | Tartalom | Szükséges hozzá | API-típus |
|---|---|---|---|
| Ezen oldal fordítása | A megjelenített dokumentumot lefordítja a választott nyelvre | A dokumentum meg van nyitva, célnyelv | ○ |
| Hiányzó fordítások együtt | A választott nyelv hiányzó fordítású és elavult dokumentumait sorban lefordítja | Célnyelv | Csak munkamenet típusú |
| Ezen oldal korrektúrája | Ellenőrzi és javítja a terminológiát, a stílust és a dokumentumszabvány által megkövetelt fejezetbeosztást | A dokumentum meg van nyitva | ○ |
| Új dokumentum létrehozása | A dokumentumszabvány és a sablonok szerint új dokumentumot hoz létre | Téma (elhagyható) | Csak munkamenet típusú |

## Mit tartalmaz az utasítás

| Sorszám | Tartalom |
|---|---|
| 1 | A Dokumentumgyökér helye. Az utasítás szerint ezen kívül semmit nem szabad módosítani |
| 2 | Az Alapértelmezett nyelv (Hiteles dokumentum), és a fordítások helye (a dokumentum mellett lévő `i18n/<nyelv>/` mappa) |
| 3 | Hogy a `navigation.order` csak a Hiteles dokumentumé, és hogy a fordítás egyedül a `navigation.title` értéket írhatja felül |
| 4 | Hogy a követelményazonosítók, a hivatkozások, a kód, a Mermaid, a TeX és a front matter szerkezete nem változhat |
| 5 | A dokumentumszabvány és a szójegyzék (a `docs-lint.config.json` `terminology` része) |
| 6 | Hogy a végén futtassa le a dokumentum-ellenőrzést, jelentse a módosított fájlokat, és ne végezzen Git-műveletet |

> **Tipp**
>
> A „Hiányzó fordítások együtt” munka célpontjai a nyilvántartásból készülnek, alkalmanként legfeljebb 200 dokumentum. Ha ennél több van, futtassa többször.

## Kapcsolódó témák

- [Munka átadása az AI-nak](README.md)
- [A nyilvántartás és a feljegyzések](ledger.md)
