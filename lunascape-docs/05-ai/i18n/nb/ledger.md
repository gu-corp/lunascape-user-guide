# Registeret og oppføringene

Registeret øverst på [AI]-fanen er oversettelsesstatusen for hvert språk som støttes. Det er nyttig også uten en AI: det viser hva som mangler.

| Visning | Betydning |
|---|---|
| Ikke oversatt | Antall dokumenter som ennå ikke har en oversettelse |
| Utdatert | Antall dokumenter der oversettelsen finnes, men originaldokumentet er nyere enn oppføringen |
| Oversatt | Antall oversettelser som følger originaldokumentet sitt |

Registeret beregnes ved å gjennomsøke dokumentroten. Ingen AI og ingen språkmodell er involvert.

## Oppdater oversettelsesoppføringene

For å kunne rapportere «Utdatert» trengs en oppføring av originaldokumentet og oversettelsen slik de var da oversettelsen ble laget. En AI av økttypen skriver filer direkte, så det opprettes ingen oppføring automatisk.

1. Når oversettelsen er ferdig og du har gått gjennom den, trykker du [Oppdater oversettelsesoppføringer].
2. Oversettelser uten oppføring registreres som samsvarende med det nåværende originaldokumentet.

Claude Code-økter og lagringer fra API-leverandører oppretter denne oppføringen automatisk (en økt blir bedt om å bruke MCP-verktøyet `record_translation_freshness`). Knappen betyr noe når du har oversatt med Codex eller VS Code-chatten.

Fra da av vil endring av et originaldokument merke oversettelsen som «Utdatert».

> **Merk**
>
> - Oversettelser som allerede har en oppføring, blir ikke rørt, slik at en eksisterende «Utdatert»-tilstand aldri slettes.
> - Oppføringene lagres i `.lunascape-docs/translation-freshness.json` og inneholder bare relative baner, språk, innholdshasher og et tidsstempel – aldri dokumentteksten.

## Relaterte emner

- [Arbeid som kan overleveres](tasks.md)
- [Lese på et annet språk](../02-reading/languages.md)
