# GitHub-tárház megnyitása

A webes változatban egy GitHub-tárház megadásával nyithatja meg a dokumentumokat. Nyilvános tárházhoz nincs szükség bejelentkezésre.

## Megnyitás a képernyőről

1. Nyissa meg a <https://docs.lunascape.org/> címet.
2. Nyomja meg az eszköztáron a [Dokumentumok megnyitása] gombot (mappa ikon).
3. Írja be a tárházat a [Tárház közvetlen megadása] mezőbe, majd nyomja meg a [Megnyitás] gombot.
   Ha be van jelentkezve a GitHubra, a [Választás az olvasható tárházak közül] listából is kiválaszthatja.

> **Tipp**
>
> - A mellette lévő GitHub ikon az éppen olvasott dokumentumot nyitja meg a github.com oldalon. Ez nem dokumentummegnyitó művelet.

## Megnyitás URL-lel

A cím a tárházat és a dokumentum helyét ugyanabban a sorrendben tartalmazza. Az útvonal a tárházon belüli hely, ezért ugyanúgy épül fel, mint a GitHub URL-je.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Megadás | Írásmód |
|---|---|
| Csak a tárház (alapértelmezett ág) | `/github/owner/repo` |
| A tárházon belüli dokumentum | `/github/owner/repo/docs/01-product/vision.md` |
| Ág vagy címke megadása | a végére írja: `?ref=v1.2.0` |

Ahogy másik oldalra lép, a cím is változik. Az eszköztár [A dokumentum megosztása] gombjával továbbadhatja az éppen olvasott oldal hivatkozását. A böngésző [Vissza] és [Előre] gombja is működik.

A korábbi `?source=` alak is megnyitható, mint eddig. Megnyitás után átíródik az új alakra.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Megjegyzés**
>
> - Bejelentkezés nélkül a GitHub API használati korlátja (óránként 60 kérés) érvényes. Sok dokumentumot tartalmazó tárháznál vagy ismételt olvasásnál jelentkezzen be a [Bejelentkezés GitHubbal] gombbal.
> - A `/` jelet tartalmazó ágnevek (például `feature/xxx`) a fenti címformátum `?ref=` részével adhatók meg. A `?source=` alakban nem írhatók le.
> - A dokumentumok az olvasó saját GitHub-jogosultságaival töltődnek be. Akinek nincs olvasási joga, annak nem jelennek meg.

## Dokumentumok megnyitása helyi mappából

Nyomja meg az eszköztáron a [Dokumentumok megnyitása] gombot, majd a lista alján a [Dokumentumok megnyitása helyi mappából] lehetőséget, és válasszon egy mappát a készülékén. A fájlok feldolgozása a böngészőn belül történik, és nem kerülnek ki sehová. Azokban a böngészőkben működik, amelyek támogatják a mappaválasztást (Chrome, Edge és egyebek).

## Kapcsolódó témák

- [Nem nyilvános tárház olvasása](private-repository.md)
- [A webes változat nem nyílik meg, vagy nem lehet bejelentkezni](../07-troubleshooting/web.md)
