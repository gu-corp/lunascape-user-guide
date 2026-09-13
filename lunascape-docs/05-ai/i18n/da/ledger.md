# Regnskabet og dets registreringer

Regnskabet øverst på fanen [AI] er oversættelsestilstanden for hvert understøttet sprog. Det er nyttigt uden en AI: det viser, hvad der mangler.

| Visning | Betydning |
|---|---|
| Ikke oversat | Antal dokumenter uden en oversættelse endnu |
| Forældet | Antal dokumenter, hvis oversættelse findes, men hvis originaldokument er nyere end registreringen |
| Oversat | Antal oversættelser, der følger deres originaldokument |

Regnskabet beregnes ved at gennemgå dokumentroden. Ingen AI og ingen sprogmodel er involveret.

## Opdater oversættelsesregistreringerne

For at afgøre "forældet" kræves der en registrering af originaldokumentet og oversættelsen, som de var på oversættelsestidspunktet. En sessionsbaseret AI skriver filer direkte, så der oprettes ingen registrering automatisk.

1. Når oversættelsen er færdig, og du har gennemgået den, skal du trykke på [Opdater oversættelsesregistreringer].
2. Oversættelser uden en registrering registreres som svarende til det nuværende originaldokument.

Claude Code-sessioner og API-baserede gemninger registrerer dette automatisk (en session bliver instrueret i at bruge MCP-værktøjet `record_translation_freshness`). Denne knap er nødvendig, når du har oversat med Codex eller VS Code-chatten.

Herefter vil ændring af et originaldokument markere dets oversættelse som "forældet".

> **Bemærk**
>
> - Oversættelser, der allerede har en registrering, overskrives ikke, så en eksisterende "forældet"-tilstand slettes aldrig.
> - Registreringerne gemmes i `.lunascape-docs/translation-freshness.json` og indeholder kun relative stier, sprog, indholds-hashes og et tidsstempel — aldrig dokumentets tekst.

## Relaterede emner

- [Arbejde, der kan overdrages](tasks.md)
- [Læsning på et andet sprog](../02-reading/languages.md)
