# Mi az a Lunascape Docs

A Lunascape Docs olyan eszköz, amellyel a Git adattárban elhelyezett Markdown dokumentumok úgy, ahogy vannak, „specifikációs webhelyként” kezelhetők. Nincs szükség előzetes fordítási lépésre, dokumentumkiszolgálóra vagy külön adatbázisra.

## Mire használható

| Cél | Fő funkciók |
|---|---|
| Olvasás | INDEX (tartalomjegyzék), szövegközi hivatkozások, morzsamenü, vissza és előre, oldalon belüli tartalomjegyzék, szűrő kereséssel |
| Megjelenítés | Táblázatok, kódblokkok, automatikusan illesztett képek, KaTeX képletek, Mermaid, Vega-Lite, Markmap, WaveDrom és Svgbob ábrák, összecsukva megjelenő dokumentumkezelési táblázatok |
| Írás | Váltás a vizuális szerkesztés és a Markdown-forrás szerkesztése között; létrehozás, másolás, átnevezés és átrendezés az INDEX felől |
| Ellenőrzés | Dokumentumellenőrzés a docs-lint eszközzel, a Standard Pack szerinti kötelező dokumentumok, fejezetek és szakkifejezések ellenőrzése, létrehozás sablonból |
| Fordítás | Fordítási javaslat készítése egy-egy oldalhoz vagy több oldalhoz egyszerre. Mentés csak ellenőrzés után <!-- ai-only --> |
| Használat AI-ból | Csak olvasható specifikációs eszköz, amelyet a VS Code ügynökei is elérnek <!-- ai-only --> |

## Hol használható

| Környezet | Felhasználás |
|---|---|
| VS Code bővítmény | A gépen lévő adattár olvasása, szerkesztése, ellenőrzése és fordítása. Ez a súgó erre összpontosít |
| Webes böngészőváltozat | A GitHubon lévő dokumentumok (nyilvános és nem nyilvános) olvasása, piszkozatok a készüléken, helyi mappa megnyitása |
| Chromium bővítmény | A webes böngészőváltozatot nyitja meg egy böngészőlapon |
| Lunascape böngésző | Ugyanezt a dokumentummodellt fogja beépíteni |

## Alapelvek

- **A Markdown a hiteles dokumentum.** A dokumentumok maradnak azok a Markdown fájlok, amelyeket a Git kezel. A Lunascape Docs nem tart fenn más formátumra alakított másolatot.
- **A mentés a felhasználó dolga.** A szerkesztett tartalom csak akkor kerül a fájlba, amikor megnyomja a [Mentés] gombot. A Git-előkészítés és a véglegesítés soha nem történik meg automatikusan.
- **A dokumentumok feldolgozása a készüléken történik.** Az olvasáshoz és a szerkesztéshez semmi nem kerül ki külső helyre. Csak a fordítás küld ki dokumentumot, és csak azután, hogy megjelenítette a címzettet és a tartalmat, és Ön jóváhagyta.
- **A fordítások az `i18n/<nyelv>/` alatt vannak.** Az alapértelmezett nyelvű dokumentumok a helyükön maradnak, a fordítások pedig ugyanazzal a viszonylagos útvonallal az `i18n/en/` és hasonló mappákba kerülnek.
- **Az AI csak javaslatot tesz.** A fordítási javaslat mentése az eltérések ellenőrzése után történik. A dokumentumokat semmi nem írja át észrevétlenül. <!-- ai-only -->

## Kapcsolódó témák

- [A képernyő részei és szerepük](screen.md)
- [A bővítmény telepítése](install.md)
- [Alapműveletek](../02-reading/README.md)
