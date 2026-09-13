# Használat AI-ból

A bővítmény regisztrálja a csak olvasható `lunascape_getDocsSpecification` Language Model Tool eszközt a VS Code-ban. Ha egy kompatibilis VS Code-ügynököt a Lunascape Docs funkcióiról, beállításairól vagy dokumentumkonvencióiról kérdeznek, ezzel az eszközzel lekérheti ennek a súgónak a tartalmát (az általános specifikációt).

## Használat

Kérdezzen a VS Code csevegésében a `#lunascapeDocs` megadásával, vagy egyszerűen kérdezzen a Lunascape Docs beállításairól vagy a dokumentumok felépítéséről.

```text
#lunascapeDocs Hogyan engedélyezem az angol fordítást a lunascape-docs.json fájlban?
```

## Az eszköz argumentumai

| Argumentum | Jelentés |
|---|---|
| `topic` | A lekérendő fejezet: `all`, `usage` (Alapműveletek), `structure` (Dokumentumgyökér és fájlkonvenciók), `editing` (Dokumentum szerkesztése), `configuration` (Projektbeállítások), `security` (Biztonság és írási határok), `ai` (Használat AI-ból) |
| `locale` | A súgó nyelve (a mellékelt súgó egyik nyelvcímkéje, például `ja` vagy `en`). Ha elhagyja, a VS Code megjelenítési nyelve érvényes, ennek hiányában a japán súgót adja vissza |

> **Megjegyzés**
>
> - Az eszköz nem küldi ki a dokumentumok szövegét sehová.
> - Az eszköz nem ad vissza munkaterületneveket vagy helyi elérési utakat.
> - Az eszköz nem módosít fájlokat.
> - `AGENTS.md` nélkül is működik a kompatibilis VS Code-ügynökökből. Azokkal az AI-kliensekkel, amelyek nem használják a bővítmény eszköz-API-ját, nem oszlik meg automatikusan.

## Kapcsolódó témák

- [A súgó megjelenítése](../02-reading/help.md)
- [Biztonság és írási határok](security.md)
