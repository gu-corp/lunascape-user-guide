# AI-innstillinger

Velg AI-en og modellen som mottar arbeidet ditt. Denne skjermen bruker sine egne nedtrekksmenyer, ikke hurtigvalget i VS Code.

1. Trykk på [Dokumentverktøy] → fanen [AI] → [AI-innstillinger…].
2. Velg en leverandør under [Leverandør].
   Leverandører denne maskinen ikke kan bruke, vises som ikke-valgbare, med begrunnelsen.
3. Velg en modell under [Modell]. Valgene endrer seg per leverandør.
4. Lukk skjermen. Valget lagres per bruker og gjenbrukes neste gang.

## Leverandører

| Leverandør | Form | Registrering |
|---|---|---|
| Claude Code | Økt | Kommandoen `claude` |
| Codex | Økt | Kommandoen `codex` |
| Språkmodeller i VS Code | API | Modeller registrert med VS Code Language Model API |
| Anthropic API | API | En registrert API-nøkkel |
| OpenAI-kompatibelt API | API | En registrert API-nøkkel og et endepunkt |

En **økt**-leverandør leser og skriver filer selv og kjører dokumentkontrollen selv. Resultatene havner i arbeidstreet og gjennomgås i Git-diffen.

En **API**-leverandør returnerer ett dokument med Markdown, og utvidelsen viser en diff før lagring.

## Registrere en API-nøkkel

Anthropic API og OpenAI-kompatible API-er blir tilgjengelige når en nøkkel er registrert.

1. Velg leverandøren under [Leverandør]. Nøkkelfeltet vises.
2. Skriv inn nøkkelen under [API-nøkkel]. For et OpenAI-kompatibelt API må du også skrive inn [Endepunkt] (for eksempel `https://api.openai.com/v1`).
3. Trykk på [Lagre]. «Nøkkel registrert» vises.

> **Merk**
>
> - Nøkler ligger i VS Codes SecretStorage og vises aldri igjen – og skrives aldri til `settings.json` eller noe dokument. [Slett nøkkel] fjerner en nøkkel.
> - Modellistene hentes fra hver tjeneste med den registrerte nøkkelen; en kjent liste vises inntil svaret kommer.
> - En API-leverandør kan bare kjøre «Oversett denne siden» og «Korrekturles denne siden». Å gå gjennom mange dokumenter og å opprette dokumenter er øktarbeid.

> **Tips**
>
> Når ingen leverandør finnes, installer Claude Code eller Codex, eller registrer en API-nøkkel. Åpne [AI-innstillinger…] på nytt, så oppdages den.

## Relaterte emner

- [Overlate arbeid til en AI](README.md)
- [VS Code-innstillinger](../08-reference/settings.md)
