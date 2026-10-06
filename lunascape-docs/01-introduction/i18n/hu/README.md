# Mi a Lunascape Docs?

A Lunascape Docs olyan eszköz, amellyel a Git-adattárban tárolt Markdown-dokumentumok átalakítás nélkül, „specifikációs webhelyként” használhatók. Nincs szükség előzetes buildelésre, dokumentumkiszolgálóra vagy külön adatbázisra.

## Lehetőségek

| Cél | Fő funkciók |
|---|---|
| Olvasás | INDEX (tartalomjegyzék), szövegközi hivatkozások, morzsamenü, vissza és előre lépés, oldalon belüli tartalomjegyzék, keresés szűréssel |
| Megtekintés | Táblázatok, kódblokkok, képek automatikus méretezése, KaTeX-képletek, Mermaid-, Vega-Lite-, Markmap-, WaveDrom- és Svgbob-ábrák, dokumentumkezelési táblázatok összecsukott megjelenítése |
| Írás | Váltás a vizuális szerkesztés és a Markdown-forrás szerkesztése között; létrehozás, másolás, átnevezés és átrendezés az INDEX-ből |
| Ellenőrzés | Dokumentumok ellenőrzése a docs-linttel; a kötelező dokumentumok, fejezetek és kifejezések ellenőrzése a Standard Pack alapján; létrehozás sablonból |
| Fordítás | Fordítási javaslatok készítése oldalanként vagy egyszerre több oldalra; mentés csak ellenőrzés után <!-- ai-only --> |
| Használat AI-val | Csak olvasható specifikációs eszköz, amelyet a VS Code ügynökei használhatnak <!-- ai-only --> |

## Használati környezetek

| Környezet | Felhasználás |
|---|---|
| VS Code-bővítmény | A helyi adattár megtekintése, szerkesztése, ellenőrzése és fordítása. Ez a súgó főként ezzel foglalkozik |
| Webböngészős változat | A GitHubon tárolt (nyilvános és privát) dokumentumok megtekintése, piszkozatok az eszközön, helyi mappák megtekintése |
| Chromium-bővítmény | Böngészőlapon nyitja meg a webböngészős változatot |

## Alapelvek

- **A Markdown a hiteles dokumentum.** A dokumentumok a Gitben kezelt Markdown-fájlok maradnak. A Lunascape Docs nem alakítja át és nem tárolja őket más formátumban.
- **A mentésről Ön dönt.** A szerkesztett tartalom csak akkor kerül a fájlba, amikor megnyomja a [Mentés] gombot. A Gitben az előkészítés és a véglegesítés nem történik automatikusan.
- **A dokumentumok feldolgozása az eszközön történik.** A megtekintéshez és a szerkesztéshez a dokumentumok nem kerülnek külső helyre. Csak fordításkor történik küldés: a program előtte megmutatja a címzettet és a tartalmat, és csak jóváhagyás után küldi el.
- **A fordítások helye: `i18n/<locale>/`.** Az alapértelmezett nyelvű dokumentumok a helyükön maradnak, a fordítások pedig ugyanazzal a relatív elérési úttal az `i18n/en/` és hasonló mappákba kerülnek.
- **Az AI csak javasol.** A fordítási javaslatot a különbségek ellenőrzése után lehet menteni. A program soha nem írja át a dokumentumokat észrevétlenül. <!-- ai-only -->

## Kapcsolódó témakörök

- [A képernyő részei és funkcióik](screen.md)
- [A bővítmény telepítése](install.md)
- [Alapműveletek](../02-reading/README.md)
