# AI-inställningar

Välj den AI och den modell som ska ta emot ditt arbete. Använd inte VS Codes snabbval, utan listrutorna på den här skärmen.

1. Tryck på [Dokumentverktyg] → fliken [AI] → [AI-inställningar…].
2. Välj [Leverantör].
   De som inte kan användas i den här miljön visas som omöjliga att välja, med en angiven orsak.
3. Välj [Modell]. Alternativen skiljer sig åt mellan leverantörer.
4. Stäng skärmen. Valet sparas per användare och används även nästa gång.

## Leverantörer

| Leverantör | Form | Identifiering |
|---|---|---|
| Claude Code | Sessionstyp | Om kommandot `claude` finns |
| Codex | Sessionstyp | Om kommandot `codex` finns |
| VS Codes språkmodeller | API-typ | Modeller som registrerats i VS Code Language Model API |
| Anthropic API | API-typ | Registrerad API-nyckel |
| OpenAI-kompatibelt API | API-typ | Registrerad API-nyckel och slutpunkt |

**Sessionstyp** läser och skriver filer själv och kör även dokumentkontrollen själv. Resultatet skrivs direkt i arbetsträdet och granskas i Gits differens.

**API-typ** returnerar Markdown för ett dokument, och tillägget visar en differens innan det sparas.

## Registrera en API-nyckel

Anthropic API och OpenAI-kompatibla API:er kan användas när en API-nyckel har registrerats.

1. Välj registreringsmål under [Leverantör]. Fältet för API-nyckeln visas.
2. Ange [API-nyckel]. För ett OpenAI-kompatibelt API anger du även [Slutpunkt] (till exempel `https://api.openai.com/v1`).
3. Tryck på [Spara]. ”Nyckel registrerad” visas.

> **Obs!**
>
> - Nyckeln sparas i VS Codes SecretStorage och visas inte igen. Den skrivs inte heller till `settings.json` eller till något dokument. Du kan ta bort den med [Ta bort nyckel].
> - Modellistan hämtas från respektive tjänst med den registrerade nyckeln. Tills den kan hämtas visas en känd lista.
> - Med API-typ kan endast ”Översätt den här sidan” och ”Korrekturläs den här sidan” utföras. Genomgång av flera dokument och skapande av dokument utförs med sessionstyp.

> **Tips**
>
> Om ingen leverantör hittas installerar du Claude Code eller Codex, eller registrerar en API-nyckel. Öppna [AI-inställningar…] igen så identifieras den.

## Relaterade ämnen

- [Lämna arbete till en AI](README.md)
- [Lista över VS Code-inställningar](../08-reference/settings.md)
