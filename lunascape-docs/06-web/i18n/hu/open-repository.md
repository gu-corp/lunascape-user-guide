# GitHub-adattár megnyitása

A webes változatban a GitHub-adattárakat klónozás nélkül, közvetlenül megnyithatja és olvashatja. Nyilvános adattárakhoz nem kell bejelentkezni.

## Megnyitás a képernyőről

1. Nyomja meg az eszköztáron a [Dokumentumok megnyitása] gombot (a mappa ikont). Megnyílik a „Dokumentumok megnyitása” képernyő.
2. A bal oldali sávban válassza ki, honnan nyit meg.

   | Hely | Ami megjelenik |
   |---|---|
   | Összes | Az alábbiak mindegyike. A legutóbb megnyitottak állnak elöl |
   | Legutóbb megnyitott | Az eddig megnyitott adattárak és mappák |
   | Ajánlott | A webhely által bemutatott kézikönyvek |
   | GitHub-adattárak | Ha be van jelentkezve a GitHubra, az Ön által olvasható adattárak |
   | Ez a számítógép | Az eszközön lévő mappák |

3. Nyomja meg a [Megnyitás] gombot abban a sorban, amelyet meg szeretne nyitni. Ha a felső [Szűrés dokumentum- vagy adattárnév szerint] mezőbe gépel, szűkítheti a sorokat.

A listában nem szereplő adattárat a bal oldali sáv [owner/repo beírása és megnyitása] elemével adhatja meg.

> **Tipp**
>
> - A listában azok a GitHub-adattárak jelennek meg, amelyekre telepítve van a „Lunascape Docs” nevű GitHub App, és amelyekhez Önnek olvasási jogosultsága van. Ha egy adattár nem látható, kérje meg a tulajdonosát, hogy adja hozzá az alkalmazást.

## A dokumentum helyének ellenőrzése

Az eszköztár bal oldalán található kis ikon (helyjelző) mutatja, hol van az éppen olvasott dokumentum.

| Ikon | Hely |
|---|---|
| A GitHub-logó | A GitHubról olvassa. Ezen az eszközön nincs mentve |
| Mappa | Az eszközön lévő mappa |

Ha megnyomja az ikont, megjelenik a hely, az állapot, és az onnan elérhető műveletek (például [Megtekintés a GitHubon], [Hivatkozás másolása]).

## Megnyitás URL-címmel

A cím egymás után sorolja fel az adattárat és a dokumentum helyét. Az elérési út az adattáron belüli helyet jelöli, ezért a sorrend megegyezik a GitHub URL-címével.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Megadás | Írásmód |
|---|---|
| Csak az adattár (alapértelmezett ág) | `/github/owner/repo` |
| Dokumentum az adattáron belül | `/github/owner/repo/docs/01-product/vision.md` |
| Ág vagy címke megadása | Fűzze a végére: `?ref=v1.2.0` |

Ha másik oldalra lép, a cím is megváltozik. Az eszköztár [A dokumentum megosztása] gombjával elküldheti az éppen olvasott oldal hivatkozását. A böngésző [Vissza] és [Előre] gombja is használható.

A korábbi `?source=` formátum továbbra is megnyílik. Megnyitás után a cím az új formátumra íródik át.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Megjegyzés**
>
> - Bejelentkezés nélkül a GitHub API használati korlátja érvényes (óránként 60 kérés). Sok dokumentumot tartalmazó adattárakhoz vagy ismételt olvasáshoz használja a [Bejelentkezés GitHubbal] gombot.
> - A `/` karaktert tartalmazó ágnevek (például `feature/xxx`) a fenti címformátumban a `?ref=` paraméterrel adhatók meg. A `?source=` formátumban nem írhatók le.
> - A dokumentumok az olvasó saját GitHub-jogosultságaival töltődnek be. Akinek nincs olvasási jogosultsága, annak nem jelennek meg.

## Dokumentumok megnyitása helyi mappából

Nyomja meg az eszköztáron a [Dokumentumok megnyitása] gombot, majd a bal oldali sáv [Dokumentumok megnyitása helyi mappából] elemével válasszon ki egy mappát az eszközön. A fájlok feldolgozása a böngészőn belül történik, és semmi nem kerül külső helyre. Olyan böngészőkben használható, amelyek támogatják a mappa kiválasztását (Chrome, Edge stb.).

## Kapcsolódó témakörök

- [Nem nyilvános adattár megtekintése](private-repository.md)
- [A webes változat nem nyílik meg, vagy nem lehet bejelentkezni](../07-troubleshooting/web.md)
