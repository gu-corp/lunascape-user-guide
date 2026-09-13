# Ellenőrzési szabályok módosítása

Az egyes ellenőrzési tételek értesítési szintjét (hiba, figyelmeztetés, információ) módosíthatja, vagy kikapcsolhatja őket. A módosítások a dokumentumgyökér `docs-lint.config.json` fájljába kerülnek, és megoszlanak a csapattal.

## Értesítési szint módosítása

1. Nyomja meg az eszköztár [Dokumentumeszközök] gombját, és nyissa meg az [Ellenőrzés] lapot.
2. Nyomja meg a [Szabályok áttekintése és módosítása] gombot.
   Az ellenőrzési tételek listája ugyanabban a kártyában nyílik ki. Minden tételnél látszik a célja és az aktuális beállítás forrása (Project, Profile, Pack, Default).
3. Válassza ki a módosítani kívánt tétel értesítési szintjét.
4. Nyomja meg a [Mentés és újbóli ellenőrzés] gombot.
   A beállítás mentődik, és a rendszer az új beállítással újra ellenőrzi a teljes dokumentumgyökeret.

| Választható érték | Jelentés |
|---|---|
| [Alapértelmezett beállítás (…)] | Eltávolítja a felülbírálatot, és visszatér ahhoz a szabványos beállításhoz, amelyet a profil, a Standard Pack, majd az alapértelmezés határoz meg, ebben a sorrendben |
| [Ki] | Ezt a tételt nem ellenőrzi |
| [Információ] / [Figyelmeztetés] / [Hiba] | Ezen az értesítési szinten jelenti |

> **Megjegyzés**
>
> - A mentéshez megbízható munkaterület szükséges.
> - Csak az egyes tételek értesítési szintje mentődik. A tételenkénti beállítások változatlanul megmaradnak. A Standard Pack és maga a profil ezen a képernyőn nem módosul.
> - Ha a `docs-lint.config.json` fájlt közvetlenül a mentés előtt kívülről módosították, a mentés megszakad. Töltse be a legfrissebb állapotot, majd próbálja meg újra.
> - Ha nincs `docs-lint.config.json`, a mentéskor létrejön.

## A beállítási fájlok közvetlen szerkesztése

- A [Részletes beállítások megnyitása] gomb megnyomásakor a `docs-lint.config.json` megnyílik a VS Code-ban.
- Nyissa meg [A szabályok forrása és a dokumentumbeállítások] részt, és nyomja meg a [Dokumentumbeállítások szerkesztése] gombot: ekkor a `lunascape-docs.json` nyílik meg a VS Code-ban. A Standard Pack és a profil kiválasztása itt történik.

Mindkét fájlnál működik a kiegészítőbe csomagolt JSON Schema szerinti beviteli kiegészítés és leírás.

## Standard Pack és profilok

A Standard Pack olyan dokumentumszabvány, amely összefogja a szükséges dokumentumtípusokat, a fejezetfelépítést, a szakszavakat és a sablonokat. A `lunascape-docs.json` fájl `documentStandards` beállításában választható ki.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

A csomagban lévő `builtin:gu-corp-software` Pack a következő profilokat tartalmazza: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`.

## Kapcsolódó témák

- [Dokumentumok ellenőrzése](check.md)
- [Projektbeállítások](project-configuration.md)
