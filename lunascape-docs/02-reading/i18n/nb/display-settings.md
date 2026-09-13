# Endre visningsinnstillinger

Fra [Visningsinnstillinger] (tannhjul) på verktøylinjen kan hver bruker endre hvordan INDEX ser ut og om redigeringsknappen vises.

1. Trykk på [Visningsinnstillinger] på verktøylinjen.
2. Slå av eller på elementene du vil endre. Endringene trer i kraft umiddelbart.
3. Trykk på [Visningsinnstillinger] én gang til, eller trykk utenfor panelet, for å lukke det.

## Innstillinger du kan endre

| Kategori | Element | Funksjon |
|---|---|---|
| Dokumentspråk | (gjeldende tilstand) | Viser prosjektets standardspråk og språket som vises nå. [Angi prosjektspråk …] åpner prosjektets språkinnstillinger |
| Innhold | [Filnavn] | Viser filnavnet i stedet for dokumentnavnet |
| | [Dokumentikoner] | Viser et ikon ved hvert dokumentelement |
| | [Mappeikoner] | Viser et ikon ved hvert mappeelement |
| | [Antall i mappen] | Viser antall dokumenter i mappen |
| | [Nivåhjelpelinjer] | Viser hjelpelinjer som angir nivåene |
| | [Skjul når det bare finnes ett dokument] | Lukker INDEX automatisk, bare første gang, i en dokumentrot med bare ett dokument |
| | [Slå sammen dokumentopplysningene] | Slår sammen administrasjonstabellen øverst i dokumentet til raden «Dokumentopplysninger». Når den er av, vises tabellen som den er |
| | [Visningstetthet] | Velg linjeavstanden i INDEX mellom [Normal] / [Kompakt] |
| | [Redigeringsknappen] | Viser [Rediger] nede til høyre i teksten |
| Handlinger | [Tilbakestill til prosjektets standardverdier] | Fjerner alle brukerens endringer og går tilbake til prosjektets innstillinger |
| | [Åpne innstillingene for utvidelsen] | Åpner innstillingene for Lunascape Docs i innstillingsvinduet i VS Code |

> **Tips**
>
> - Visningsinnstillingene lagres per bruker og per dokumentrot, og skrives ikke til filer som er under Git-styring.
> - Innstillingene prioriteres i rekkefølgen «brukerens visningsinnstillinger → VS Code-innstillinger → `lunascape-docs.json` → produktets standardverdier». Felles standardverdier for teamet bestemmes med `tree` og `editor` i `lunascape-docs.json`.

## Bytte fargevalg

Trykk på temavalgeren (sol/måne) på verktøylinjen for å veksle mellom hvit bakgrunn og fargevalget i VS Code. Fargevalget ved oppstart bestemmes av innstillingen `lunascapeDocEditor.appearance` (`light` eller `auto`).

## Relaterte emner

- [Bruke INDEX](index-panel.md)
- [Prosjektinnstillinger](../04-document-tools/project-configuration.md)
- [Oversikt over VS Code-innstillinger](../08-reference/settings.md)
