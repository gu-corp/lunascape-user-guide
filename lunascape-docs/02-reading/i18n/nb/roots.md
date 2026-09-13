# Bytte dokumentrot

En dokumentrot er den øverste mappen for ett sett med dokumenter. INDEX, filtrering, kontroll og oversettelse fungerer alle per dokumentrot.

## Hvordan en dokumentrot finnes

Lunascape Docs følger de overordnede mappene oppover fra den åpnede Markdown-filen og bruker den nærmeste mappen som samsvarer med ett av følgende, som dokumentrot.

- En mappe som inneholder `lunascape-docs.json` (uansett mappenavn)
- En mappe med navnet `docs` (legg til flere navn med innstillingen `lunascapeDocEditor.rootDirectoryNames`)

Når du kjører «Lunascape Docs: Åpne spesifikasjonsviser», åpnes dokumentroten fra innstillingen `lunascapeDocEditor.root` (standard `docs`).

## Bytte til en annen dokumentrot

Når arbeidsområdet har flere dokumentrøtter, blir dokumentrotnavnet ytterst til venstre på verktøylinjen en nedtrekksliste.

1. Trykk på dokumentrotnavnet ytterst til venstre på verktøylinjen.
2. Velg en dokumentrot fra listen.
   Startsiden for den valgte dokumentroten vises, og INDEX byttes.

> **Tips**
>
> Navnene som vises i listen, bestemmes i denne rekkefølgen. De endres ikke selv om du bytter visningsspråk.
>
> 1. `title` i `lunascape-docs.json`
> 2. `navigation.title` i rotens `README.md`, ellers dens H1
> 3. `navigation.title` i rotens `index.md`, ellers dens H1
> 4. Mappenavnet (for en standard `docs`-mappe: navnet på den overordnede mappen)

## Åpne Markdown utenfor en dokumentrot

Når du åpner en Markdown-fil som ikke ligger i en dokumentrot, vises mappen som filen ligger i, som en midlertidig dokumentrot. INDEX viser Markdown-filene i den samme mappen og under den.

- Trykk på [Opp én mappe] på verktøylinjen for å utvide omfanget til den overordnede mappen i arbeidsområdet.
- I denne visningen er prosjektets språkinnstillinger og samlet oversettelse utilgjengelige. Legg en `lunascape-docs.json` i mappen for å gjøre den til en dokumentrot og aktivere dem.

## Alltid åpne en fast dokumentrot

Sett innstillingen `lunascapeDocEditor.rootMode` til `fixed` for alltid å åpne dokumentroten i `lunascapeDocEditor.root`, uansett hvilken Markdown-fil du åpner.

## Relaterte emner

- [Dokumentrøtter og filkonvensjoner](../04-document-tools/structure.md)
- [Prosjektkonfigurasjon](../04-document-tools/project-configuration.md)
- [VS Code-innstillinger](../08-reference/settings.md)
