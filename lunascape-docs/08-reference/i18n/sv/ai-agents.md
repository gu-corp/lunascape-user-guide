# Användning från AI

Tillägget registrerar det skrivskyddade Language Model Tool `lunascape_getDocsSpecification` i VS Code. När en VS Code-agent som stöder detta får frågor om funktioner, inställningar eller dokumentkonventioner i Lunascape Docs kan den hämta innehållet i den här hjälpen (den allmänna specifikationen) med verktyget.

## Så använder du det

Ställ frågan i VS Code-chatten med `#lunascapeDocs`, eller fråga om inställningar eller dokumentstruktur i Lunascape Docs.

```text
#lunascapeDocs Hur aktiverar jag engelsk översättning i lunascape-docs.json?
```

## Verktygets argument

| Argument | Innehåll |
|---|---|
| `topic` | Kapitlet som ska hämtas. `all`, `usage` (Grundläggande användning), `structure` (Dokumentrot och filkonventioner), `editing` (Redigera dokument), `configuration` (Projektinställningar), `security` (Säkerhet och skrivgränser), `ai` (Användning från AI) |
| `locale` | Hjälpens språk (språktaggen för en medföljande hjälp, till exempel `ja` eller `en`). Om det utelämnas används visningsspråket i VS Code, annars returneras hjälpen på japanska |

> **Obs!**
>
> - Verktyget skickar aldrig dokumentens innehåll utanför datorn.
> - Verktyget returnerar aldrig namn på arbetsytor eller lokala sökvägar.
> - Verktyget ändrar inga filer.
> - Det fungerar från VS Code-agenter som stöder detta även utan `AGENTS.md`. Det delas inte automatiskt med andra AI-klienter som inte använder tilläggets verktygs-API.

## Relaterade ämnen

- [Visa hjälpen](../02-reading/help.md)
- [Säkerhet och skrivgränser](security.md)
