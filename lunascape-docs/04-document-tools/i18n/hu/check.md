# Dokumentumok ellenőrzése

A docs-lint segítségével ellenőrizheti a címsorok felépítését, a törött hivatkozásokat, a kötelező dokumentumok és fejezetek hiányát, a szóhasználat ingadozását, a követelményazonosítók egyezését és így tovább. Az ellenőrzés mindig a teljes dokumentumgyökérre vonatkozik.

## Ellenőrzés futtatása

1. Nyomja meg az eszköztáron a [Dokumentumeszközök] gombot, és nyissa meg az [Ellenőrzés] lapot.
2. Nyomja meg a [Dokumentumgyökér ellenőrzése] gombot.
   A parancskatalógusból a „Lunascape Docs: Dokumentumgyökér ellenőrzése” paranccsal is futtatható.
3. Tekintse át a találatok listáját.

## Az eredmények értelmezése

- A lista fölötti [Ez a dokumentum] / [Összes] kapcsolóval válthatja a megjelenített tartományt. Magának az ellenőrzésnek a hatóköre mindig a teljes dokumentumgyökér.
- A találatoknak négy szintje van: „hiba”, „figyelmeztetés”, „információ” és „javaslat”. Az eszköztáron a [Dokumentumeszközök] gombon a hibák és a figyelmeztetések száma látszik.
- Egy találatra kattintva a hozzá tartozó Markdown forrás megfelelő helye nyílik meg a VS Code szerkesztőjében.
- A teljes dokumentumgyökeret érintő találatok (például egy hiányzó tesztdokumentum) a „Teljes dokumentumgyökér” tétel alatt jelennek meg, és nincs hozzájuk pozíció.
- Ugyanezek a találatok a VS Code „Problémák” paneljén is megjelennek.

## Mit ellenőriz a program

A [Szabályok áttekintése és módosítása] gomb megnyomásával megjelenik az érvényben lévő ellenőrzések listája és mindegyik célja. A főbb tételek a következők.

| Tétel | Tartalom |
|---|---|
| Címsorok felépítése | Pontosan egy H1 van-e, és nem ugranak-e át a címsorszintek |
| Belső hivatkozások | Létezik-e a hivatkozott dokumentum, és nem mutat-e a dokumentumgyökéren kívülre |
| Kódblokkok nyelve | Meg van-e adva a kódblokkok nyelve |
| Szükséges mappák és dokumentumok | Megvan-e minden mappa és dokumentum, amelyet a Standard Pack profilja megkövetel |
| A dokumentum kötelező fejezetei | Megvannak-e az egyes dokumentumtípusokhoz szükséges fejezetek |
| Szóhasználat egységesítése | Felismeri a kerülendő kifejezéseket, és az ajánlott szakkifejezések használatára ösztönöz |
| Követelményazonosítók elnevezése és ismétlődése | Megfelelnek-e a követelményazonosítók az elnevezési szabálynak, és nincsenek-e kétszer meghatározva |
| Követelményazonosítók hivatkozási egyezése | Léteznek-e azok a követelményazonosítók, amelyekre a tervezési, a teszt- és az állapotdokumentumok hivatkoznak |
| Követelmények és tesztek megfelelése | Hivatkoznak-e a tesztdokumentumok a követelményazonosítókra |

Azt, hogy mely tételek lépnek érvénybe, a `lunascape-docs.json` fájlban kiválasztott Standard Pack és profil, valamint a `docs-lint.config.json` fájl határozza meg.

> **Megjegyzés**
>
> - Ha módosít egy dokumentumot vagy egy beállítást, az előző eredmény „újraellenőrzés szükséges” állapotba kerül. Semmi sem minősül automatikusan megfelelőnek: nyomja meg újra a [Dokumentumgyökér ellenőrzése] gombot.
> - A nem mentett módosítások nem kerülnek bele az ellenőrzésbe. Előbb mentsen.
> - Az ellenőrzés az eszközön, helyben és determinisztikus módon fut. Az AI értékelésének vagy fordításának eredménye soha nem keveredik az ellenőrzés eredményébe.

## Kapcsolódó témák

- [Ellenőrzési szabályok módosítása](rules.md)
- [Projektbeállítások](project-configuration.md)
- [Az ellenőrzés, a létrehozás vagy a fordítás nem sikerül](../07-troubleshooting/tools.md)
