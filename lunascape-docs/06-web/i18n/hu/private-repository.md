# Nem nyilvános adattár megtekintése

A nem nyilvános adattárak dokumentumait a GitHubbal való bejelentkezés után, csak azoknál az adattáraknál tekintheted meg, amelyekhez olvasási jogosultságod van. A Lunascape Docs soha nem rendelkezik saját fiókkal vagy jogosultságokkal.

## Bejelentkezés és megnyitás

1. Nyisd meg a <https://docs.lunascape.org/> címet.
   Ha nem nyilvános dokumentumot adtál meg, vagy még nem jelentkeztél be, megjelenik a bejelentkezési képernyő.
2. Nyomd meg a [Bejelentkezés GitHubbal] gombot.
   A GitHub hitelesítési képernyője felugró ablakban nyílik meg.
3. A bejelentkezés után nyomd meg a [Dokumentumok megnyitása] gombot az eszköztáron, majd a [Választás az olvasható tárházak közül] pontban válaszd ki a megnyitni kívánt adattárat.

> **Tipp**
>
> - A bejelentkezett fiók neve az eszköztáron látható. A [Kijelentkezés] és a [Bejelentkezés másik fiókkal] műveletek is innen érhetők el.
> - A listában azoknak a fiókoknak (szervezet vagy egyéni) az adattárai jelennek meg, amelyekre a „Lunascape Docs” GitHub App telepítve van, azok közül is csak azok, amelyekhez olvasási jogosultságod van.

## Az adattár tulajdonosa által elvégzendő beállítások

Ha a keresett adattár nem jelenik meg a listában, az adattár tulajdonosának vagy a szervezet rendszergazdájának telepítenie kell a „Lunascape Docs” GitHub Appot.

- A kért jogosultságok a Contents (olvasás és írás) és a Pull requests (olvasás és írás). Az olvasás a megtekintéshez, az írás a webről küldött közzétételi kéréshez (Pull Request) szükséges. A Lunascape Docs soha nem tárolja a dokumentumok tartalmát.
- A telepítés fiókonként (szervezet vagy egyéni) történik. Beállíthatod, hogy az „All repositories” lehetőségre vonatkozzon (amely a később létrehozott adattárakat is automatikusan tartalmazza), vagy csak a kiválasztott adattárakra.

| Helyzet | Lépések |
|---|---|
| Bevezetés új szervezeti vagy egyéni fiókon | Végezd el a [telepítési oldalról](https://github.com/apps/lunascape-docs/installations/new) |
| Adattárak hozzáadása egy már bevezetett szervezetben | A szervezet Settings → GitHub Apps → Lunascape Docs → Configure → Repository access pontjában állítható be |

Még ha az egész szervezetre telepíted is, minden tag csak azokat az adattárakat tekintheti meg, amelyekhez olvasási jogosultsága van. Közzétételi kérést is csak azokhoz az adattárakhoz küldhet, amelyekhez írási jogosultsága van.

> **Tipp**
> - Új telepítés esetén a kért jogosultságok listája megjelenik a telepítési képernyőn, és az „Install” megnyomásával jóváhagyod azokat. További teendő nincs.
> - Annak a szervezetnek, amely a jogosultság bővítése előtt telepítette az appot, a rendszergazdái e-mailt kapnak, és jóváhagyó gomb jelenik meg a szervezet Settings → GitHub Apps → Lunascape Docs → Configure oldalának tetején. A jóváhagyásig az adott szervezetben csak megtekintés lehetséges, és közzétételi kérés küldésekor az „írási jogosultság megadása szükséges” üzenet jelenik meg.
> - Hogy éppen milyen jogosultságokkal van telepítve, ugyanezen a Configure oldalon ellenőrizheted. Egyéni fiók esetén ez a Settings → Applications → Installed GitHub Apps.
> - Ha véletlenül eltávolítottad az adott adattárat, vagy eltávolítottad az appot, a [telepítési oldalról](https://github.com/apps/lunascape-docs/installations/new) újratelepítve visszaáll az eredeti állapot. A közzétételi kérés elutasítási üzenete tartalmaz egy hivatkozást a javítás képernyőjére.
> - Ha az adattár oldalán nem szeretnél közzétételi kéréseket fogadni, írd be a `lunascape-docs.json` fájlba a `"publish": { "enabled": false }` beállítást. A megtekintés továbbra is működik.

## Kapcsolódó témák

- [GitHub-adattár megnyitása](open-repository.md)
- [A webes verzió nem nyílik meg, vagy nem lehet bejelentkezni](../07-troubleshooting/web.md)
