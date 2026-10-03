# GitHub-adattár megnyitása

A webes változatban és a Lunascape-ben a GitHub-adattárakat másolat készítése nélkül, közvetlenül megnyithatja és olvashatja. Nyilvános adattárakhoz nincs szükség bejelentkezésre.

## Megnyitás a képernyőről

1. Nyomja meg az eszköztáron a [Dokumentumok megnyitása] gombot (mappa ikon). Megnyílik a „Dokumentumok megnyitása” képernyő.
2. A bal oldali sávban válassza ki, honnan szeretne megnyitni.

   | Hely | Ami megjelenik |
   |---|---|
   | Mind | Az alábbiak mindegyike. A legutóbb megnyitottak állnak elöl |
   | Legutóbb megnyitott | Az eddig megnyitott adattárak és mappák |
   | Ajánlott | A webhely által ajánlott kézikönyvek |
   | GitHub-adattárak | Ha be van jelentkezve a GitHubra, azok az adattárak, amelyeket olvashat |
   | Ez a számítógép | Az eszköz mappái. A Lunascape-ben a lemásolt adattárak is itt jelennek meg |

3. Nyomja meg a megnyitni kívánt sorban a [Megnyitás] gombot. A felül lévő [Szűrés dokumentum- vagy adattárnév szerint] mezőbe írva szűkítheti a sorokat.

A listában nem szereplő adattárat a bal oldali sáv [owner/repo megadása és megnyitása] elemével adhatja meg.

> **Tipp**
>
> - A listában azok a GitHub-adattárak jelennek meg, amelyekre telepítve van a „Lunascape Docs” GitHub-alkalmazás, és amelyekhez olvasási joga van. Ha egy adattár hiányzik, kérje meg a tulajdonosát, hogy adja hozzá az alkalmazást.

## A dokumentum helyének ellenőrzése

Az eszköztár bal oldalán lévő kis ikon (helyjelző) mutatja, hol található az éppen olvasott dokumentum.

| Ikon | Hely |
|---|---|
| GitHub-logó | A GitHubról olvassa. Ezen az eszközön nincs mentve |
| Számítógép | A Lunascape által kezelt mappa ezen az eszközön. A Git-ág neve és a módosított fájlok száma is megjelenik |
| Mappa | Mappa ezen az eszközön |

Az ikont megnyomva megjelenik a hely, az állapot és az onnan elérhető műveletek (például [Megtekintés a GitHubon], [Hivatkozás másolása]).

## Adattár másolása a Lunascape-ben

A Lunascape-ben a GitHub-adattárat lemásolhatja erre az eszközre, majd a Gittel szerkesztheti és véglegesítheti a változtatásokat.

- A „Dokumentumok megnyitása” képernyőn nyomja meg az adattár sorában a [Másolat készítése] gombot.
- Ha a GitHubról megnyitott adattárat olvas, nyomja meg a helyjelzőt, majd a [Másolat készítése erre a számítógépre] gombot. A másolás végeztével ugyanaz a dokumentum nyílik meg az eszközön lévő példányból.

A lemásolt adattár mellett a listában „Ezen a számítógépen” felirat jelenik meg, és a [Megnyitás ezen a számítógépen] áll elöl.

## Megnyitás URL-lel

A cím az adattárat és a dokumentum helyét egymás után sorolja fel. Az elérési út az adattáron belüli helyet jelöli, így a sorrend megegyezik a GitHub URL-jével.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Megadás | Formátum |
|---|---|
| Csak az adattár (alapértelmezett ág) | `/github/owner/repo` |
| Dokumentum az adattáron belül | `/github/owner/repo/docs/01-product/vision.md` |
| Ág vagy címke megadása | Fűzze a végére: `?ref=v1.2.0` |

Oldalváltáskor a cím is megváltozik. Az eszköztár [A dokumentum megosztása] gombjával továbbadhatja az éppen olvasott oldal hivatkozását. A böngésző [Vissza] és [Előre] gombja is használható.

A korábbi `?source=` formátumú címek továbbra is megnyithatók. Megnyitás után a cím az új formátumra változik.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Figyelem**
>
> - Bejelentkezés nélkül a GitHub API használati korlátja (óránként 60 kérés) érvényes. Sok dokumentumot tartalmazó adattárak vagy ismételt olvasás esetén jelentkezzen be a [Bejelentkezés GitHubbal] gombbal.
> - A `/` karaktert tartalmazó ágnevek (például `feature/xxx`) a fenti címformátumban a `?ref=` paraméterrel adhatók meg. A `?source=` formátumban nem írhatók le.
> - A dokumentumok az olvasó saját GitHub-jogosultságaival töltődnek be. Akinek nincs olvasási joga, annak nem jelennek meg.

## Dokumentumok megnyitása helyi mappából

Nyomja meg az eszköztáron a [Dokumentumok megnyitása] gombot, majd a bal oldali sáv [Dokumentumok megnyitása helyi mappából] elemével válasszon ki egy mappát az eszközön. A fájlok feldolgozása a böngészőn belül történik, és semmi sem kerül külső helyre. Olyan böngészőben használható, amely támogatja a mappaválasztást (például Chrome, Edge).

## Kapcsolódó témakörök

- [Privát adattár megtekintése](private-repository.md)
- [A webes változat nem nyílik meg, vagy nem lehet bejelentkezni](../07-troubleshooting/web.md)
