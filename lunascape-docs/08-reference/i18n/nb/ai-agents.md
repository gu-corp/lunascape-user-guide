# Bruk fra AI

Utvidelsen registrerer det skrivebeskyttede Language Model Tool `lunascape_getDocsSpecification` i VS Code. Når en kompatibel VS Code-agent blir spurt om funksjoner, innstillinger eller dokumentkonvensjoner i Lunascape Docs, kan den hente innholdet i denne hjelpen (den generelle spesifikasjonen) gjennom dette verktøyet.

## Slik bruker du det

Still spørsmål i VS Code-chatten med `#lunascapeDocs`, eller spør ganske enkelt om innstillinger eller dokumentstruktur i Lunascape Docs.

```text
#lunascapeDocs Hvordan aktiverer jeg engelsk oversettelse i lunascape-docs.json?
```

## Verktøyargumenter

| Argument | Innhold |
|---|---|
| `topic` | Kapittelet som skal hentes: `all`, `usage` (Grunnleggende bruk), `structure` (Dokumentrøtter og filkonvensjoner), `editing` (Redigere et dokument), `configuration` (Prosjektinnstillinger), `security` (Sikkerhet og skrivegrenser) eller `ai` (Bruk fra AI) |
| `locale` | Hjelpespråket (en språktag for en medfølgende hjelp, som `ja` eller `en`). Utelates det, brukes visningsspråket i VS Code, og ellers returneres den japanske hjelpen |

> **Merk**
>
> - Verktøyet sender aldri dokumentinnhold ut av maskinen.
> - Verktøyet returnerer aldri navn på arbeidsområder eller lokale stier.
> - Verktøyet endrer aldri filer.
> - Det fungerer fra kompatible VS Code-agenter uten en `AGENTS.md`. Det deles ikke automatisk med andre AI-klienter som ikke bruker utvidelsens verktøy-API.

## Relaterte emner

- [Vise hjelpen](../02-reading/help.md)
- [Sikkerhet og skrivegrenser](security.md)
