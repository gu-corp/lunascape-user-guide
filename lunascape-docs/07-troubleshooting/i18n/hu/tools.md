# Az ellenőrzés, a létrehozás vagy a fordítás nem sikerül

## Ellenőrzés

### Megjelenik „A docs-lint nem érhető el" üzenet

- A bővítményből hiányzik a docs-lint futtatókörnyezete, vagy a beállításokkal van gond. Telepítse újra a bővítményt.
- „A helyi Pack és a beállítások biztonságos betöltéséhez tekintse megbízhatónak ezt a munkaterületet a VS Code-ban": a helyi Standard Pack használatához megbízható munkaterület szükséges.

### Az eredmény „újraellenőrzés szükséges" állapotban marad

A dokumentum vagy a beállítások módosítása érvényteleníti az előző eredményt. Nyomja meg újra a [Dokumentumgyökér ellenőrzése] gombot. A nem mentett módosítások nem kerülnek bele.

### A megállapításra kattintva nem nyílik meg semmi

A „teljes dokumentumgyökér" tételei nem kapcsolódnak egy adott dokumentumhoz, ezért nincs helyük. A megállapítás tartalma szerint ellenőrizze az érintett dokumentumot.

### A szabályok nem menthetők

- Megbízható munkaterület szükséges.
- „A Lint beállításait egy másik művelet módosította": a `docs-lint.config.json` fájlt kívülről módosították. Töltse be a legfrissebb állapotot, majd próbálja újra.
- A szimbolikus hivatkozások és a dokumentumgyökéren kívüli beállításfájlok nem szerkeszthetők.

## Létrehozás sablonból

- „A sablon előnézete lejárt", „A megadott adatok megváltoztak": nyomja meg újra az [Előnézet] gombot, majd hozza létre a dokumentumot.
- „A célhelyen már létezik dokumentum": a meglévő fájlokat a program nem írja felül. Adjon meg másik célhelyet.
- A célhelyhez a dokumentumgyökérhez viszonyított útvonal és `.md` / `.mdx` kiterjesztés szükséges. Az `i18n` alatt nem hozható létre dokumentum.
- „Dokumentum létrehozásához tekintse megbízhatónak a munkaterületet": tekintse megbízhatónak a munkaterületet a VS Code-ban.

<!-- ai-only:start -->
## Fordítás

### A fordítás gombjai nem nyomhatók meg

- „Ebben a dokumentumgyökérben nincs engedélyezve az AI-fordítás": állítsa a `lunascape-docs.json` fájlban a `translation.enabled` értékét `true` értékre.
- „A projekt alapértelmezett nyelve nincs beállítva": mentse az alapértelmezett nyelvet a [Megjelenítési beállítások módosítása](../02-reading/display-settings.md) szerint.
- „Vegye fel a célnyelvet a támogatott nyelvek közé": adja hozzá a célnyelvet a `locales` listához.
- „Nem található a fordítandó hiteles dokumentum": fordítási oldal van megnyitva. Váltson az alapértelmezett nyelvű oldalra.
- Ideiglenes mappanézetben nem használható a kötegelt fordítás. Helyezzen `lunascape-docs.json` fájlt a mappába, hogy dokumentumgyökér legyen belőle.

### A fordítási javaslatot a program elutasítja, vagy újrakészítést kér

- „A hiteles dokumentum megváltozott. Készítse el újra a fordítási javaslatot": a javaslat elkészítése után a hiteles dokumentum vagy a célfájl megváltozott. Fordítsa le újra.
- Ha a nyelvi modell válaszából hiányoznak a védendő azonosítók vagy kódrészletek, a program nem fogadja el. A válasz tartalma a kimeneti panel „Lunascape Docs Fordítás" csatornáján tekinthető meg.
- „A kötegelt fordítás alkalmanként legfeljebb 1000 dokumentumot kezel": ossza fel a hatókört mappákra vagy kijelöléssel.
<!-- ai-only:end -->

## Kapcsolódó témák

- [Dokumentumok ellenőrzése](../04-document-tools/check.md)
- [Dokumentum létrehozása sablonból](../04-document-tools/templates.md)
- [Munka átadása az AI-nak](../05-ai/README.md)
