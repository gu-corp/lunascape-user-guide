# AI-indstillinger

Vælg den AI og den model, du overdrager arbejdet til. Denne skærm bruger sine egne rullemenuer, ikke VS Codes hurtigvalg.

1. Tryk på [Dokumentværktøjer] → fanen [AI] → [AI-indstillinger…].
2. Vælg en udbyder under [Udbyder].
   Dem, der ikke kan bruges i dette miljø, vises som ikke-valgbare med en angivelse af årsagen.
3. Vælg en model under [Model]. Valgmulighederne ændrer sig fra udbyder til udbyder.
4. Luk skærmen. Valget gemmes for hver bruger og bruges igen næste gang.

## Udbydere

| Udbyder | Form | Detektion |
|---|---|---|
| Claude Code | Session | Kommandoen `claude` |
| Codex | Session | Kommandoen `codex` |
| VS Codes sprogmodeller | API | Modeller registreret i VS Code Language Model API |
| Anthropic API | API | En registreret API-nøgle |
| OpenAI-kompatibelt API | API | En registreret API-nøgle og et slutpunkt |

En **session**-udbyder læser og skriver filer selv og udfører også dokumentkontrollen selv. Resultaterne skrives direkte i arbejdstræet og gennemgås i Git-diffen.

En **API**-udbyder returnerer ét dokuments Markdown, og udvidelsen viser en diff, før den gemmer.

## Registrering af en API-nøgle

Anthropic API og OpenAI-kompatible API'er kan bruges, når du har registreret en API-nøgle.

1. Vælg under [Udbyder], hvor nøglen skal registreres. Feltet til API-nøglen vises.
2. Indtast [API-nøgle]. For et OpenAI-kompatibelt API skal du også indtaste [Slutpunkt] (for eksempel `https://api.openai.com/v1`).
3. Tryk på [Gem]. »Nøgle registreret« vises.

> **Bemærk**
>
> - Nøgler gemmes i VS Codes SecretStorage og vises aldrig igen. De skrives heller ikke til `settings.json` eller til noget dokument. [Slet nøgle] fjerner en nøgle.
> - Modellisterne hentes fra hver tjeneste med den registrerede nøgle. Indtil det lykkes, vises en kendt liste.
> - En API-udbyder kan kun køre »Oversæt denne side« og »Korrekturlæs denne side«. Gennemgang af flere dokumenter og oprettelse af dokumenter skal køres af en session-udbyder.

> **Tip**
>
> Hvis der ikke findes nogen udbyder, skal du installere Claude Code eller Codex eller registrere en API-nøgle. Åbn [AI-indstillinger…] igen, så registreres den.

## Relaterede emner

- [At overdrage arbejde til en AI](README.md)
- [Oversigt over VS Code-indstillinger](../08-reference/settings.md)
