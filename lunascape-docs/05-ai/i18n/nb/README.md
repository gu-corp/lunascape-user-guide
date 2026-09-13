# Overlate arbeid til en AI

Lunascape Docs kaller ikke en språkmodell. Den forbereder **kontekst, verktøy og kontroller**, og overlater oversetting, korrekturlesing og skriving til den AI-en du allerede bruker.

## Tanken bak

| Det produktet stiller til rådighet | Innhold |
|---|---|
| Kontekst | Dokumentkonvensjonene (hvor oversettelser ligger, front matter, dokumentstandarden, ordlisten) og plasseringen av måldokumentet |
| Arbeidsverktøy | Registeret over manglende og utdaterte oversettelser, lesing og skriving av dokumenter, oppretting fra maler |
| Kontroller | docs-lint, samt differansen i dekning og ferskhet |

Instruksjonen inneholder ingen dokumenttekst: AI-en leser filene, skriver dem og verifiserer dem selv.

## Overlat arbeidet

1. Trykk [Dokumentverktøy] på verktøylinjen og åpne fanen [AI].
2. Velg arbeidet under [Arbeid].
3. Fyll inn det som trengs (målspråk, emne).
4. Trykk [Overlat dette arbeidet].
   En VS Code-terminal åpnes, og AI-en du valgte, mottar instruksjonen og starter.

> **Tips**
>
> En Claude Code-økt følges av arbeidsverktøy (MCP-serveren `lunascape-docs`): den kan selv hente listen over manglende/utdaterte oversettelser, kjøre docs-lint og registrere oversettelsesferskhet.

## Kontroll av resultatet

| Leverandørtype | Hvor resultatet havner |
|---|---|
| Øktbasert (Claude Code, Codex) | Skriver direkte til arbeidstreet. **Kontroller det i Git-differansen** |
| API-basert (VS Codes språkmodeller, Anthropic, OpenAI-kompatibel) | Returnerer ett dokument om gangen. Kontroller det med [Åpne differanse], og skriv det så med [Lagre] |

### Kontrollere et API-forslag

Når du kjører med en API-leverandør, leveres et forslag til fanen [AI].

1. Trykk [Åpne differanse] og sammenlign med det nåværende innholdet.
2. Trykk [Lagre] for å skrive det – ved en oversettelse registreres også ferskheten – eller [Forkast] for å droppe det.
   Trykk [Stopp] for å avbryte en generering underveis.

> **Merk**
>
> - Lunascape Docs utfører aldri Git-stage eller commit. Kontroller alltid differansen.
> - Arbeid kan ikke overlates i et arbeidsområde som ikke er klarert, eller mens du blar i en mappe utenfor en dokumentrot.

## Relaterte emner

- [Arbeid som kan overlates](tasks.md)
- [AI-innstillinger](settings.md)
- [Registeret og oppføringene](ledger.md)
