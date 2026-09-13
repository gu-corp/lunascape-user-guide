# Overdrag arbejde til en AI

Lunascape Docs kalder ikke en sprogmodel. Den forbereder **kontekst, værktøjer og kontroller** og overlader oversættelse, korrekturlæsning og forfatning til den AI, du allerede bruger.

## Idéen

| Hvad produktet leverer | Indhold |
|---|---|
| Kontekst | Dokumentkonventionerne (hvor oversættelser ligger, front matter, dokumentstandarden, ordlisten) og placeringen af måldokumentet |
| Arbejdsværktøjer | Registret over ikke oversatte og forældede oversættelser, læsning og skrivning af dokumenter, oprettelse fra skabeloner |
| Kontroller | docs-lint samt forskellen i dækning og friskhed |

Instruktionen indeholder ikke dokumentets tekst: AI'en læser selv filerne, skriver dem og verificerer dem.

## Overdrag arbejdet

1. Tryk på [Dokumentværktøjer] i værktøjslinjen, og åbn fanen [AI].
2. Vælg det arbejde, du vil overdrage, under [Opgave].
3. Udfyld de nødvendige felter (målsprog, emne).
4. Tryk på [Overdrag denne opgave].
   En terminal i VS Code åbnes, og den valgte AI modtager instruktionen og går i gang.

> **Tip**
>
> En Claude Code-session ledsages af arbejdsværktøjer (MCP-serveren `lunascape-docs`): den kan selv hente listen over ikke oversatte og forældede dokumenter, køre docs-lint og registrere oversættelsens friskhed.

## Gennemgang af resultatet

| Udbyderens form | Hvor resultatet lander |
|---|---|
| Session (Claude Code, Codex) | Skriver direkte til arbejdstræet. **Gennemgå det i Git-diffen** |
| API (VS Codes sprogmodeller, Anthropic, OpenAI-kompatibel) | Returnerer ét dokument ad gangen. Gennemgå det med [Åbn diff], og skriv det med [Gem] |

### Gennemgå et API-forslag

Når du kører med en API-udbyder, ankommer et forslag i fanen [AI].

1. Tryk på [Åbn diff], og sammenlign med det nuværende indhold.
2. Tryk på [Gem], hvis det er i orden – ved en oversættelse registreres friskheden også. Tryk på [Kassér] for at droppe det.
   Tryk på [Stop] for at afbryde en generering undervejs.

> **Bemærk**
>
> - Lunascape Docs udfører aldrig staging eller commit i Git. Gennemgå altid ændringerne i diffen.
> - Du kan ikke overdrage arbejde i en browser, du ikke har tillid til, eller mens du gennemser en midlertidig mappe uden for en dokumentrod.

## Relaterede emner

- [Tilgængeligt arbejde](tasks.md)
- [AI-indstillinger](settings.md)
- [Registret og dets optegnelser](ledger.md)
