# Opprette og organisere dokumenter og mapper

Fra elementmenyen i INDEX kan du opprette, duplisere, endre navn på og slette dokumenter og mapper. Inndataene skrives i en liten dialog inne i viseren, uten å avbryte lesingen.

> **Merk**
>
> Disse handlingene er bare tilgjengelige når arbeidsområdet er klarert i VS Code. De kan ikke kjøres mens et dokument redigeres, mens en annen operasjon pågår, eller når målet har ulagrede endringer.

## Opprette et dokument eller en mappe

1. Åpne elementmenyen ([⋯] eller høyreklikk) til målmappen.
   For å opprette direkte under dokumentroten bruker du [⋯] ytterst til høyre i INDEX-overskriften, eller høyreklikker på et tomt område i INDEX.
2. Velg [Nytt dokument] eller [Ny mappe].
3. Skriv inn et navn og trykk [Opprett].
   Et dokumentnavn trenger en Markdown-filendelse (`.md`, `.markdown`, `.mdx` og så videre).

Nye dokumenter opprettes som dokumenter på standardspråket (originaldokument).

## Duplisere et dokument

1. Åpne elementmenyen til dokumentet og velg [Dupliser].
2. Skriv inn et nytt navn og trykk [Opprett].

Bare originaldokumentet dupliseres; oversettelsene dupliseres ikke.

## Endre tittelen

Endrer dokumentets overskrift (H1). Filnavnet forblir det samme.

1. Åpne elementmenyen til et dokument eller en mappe og velg [Endre tittelen].
2. Skriv inn den nye tittelen på én linje og trykk [Endre].

For en mappe endres overskriften i mappens `README.md`. Når en oversettelse vises, endres tittelen på dokumentet for det språket.

## Endre dokumentnavnet

Endrer dokumentnavnet som vises i verktøylinjen (navnet på dokumentroten).

1. Høyreklikk på dokumentnavnet i verktøylinjen. [⋯] ytterst til høyre i INDEX-overskriften åpner den samme menyen.
2. Velg [Endre dokumentnavnet] og skriv inn et nytt navn.

Så lenge ingenting er konfigurert, vises mappenavnet slik det er.

Et navn du angir, skrives til **det stedet som for øyeblikket leverer dokumentnavnet**, slik at en overskrift du kan se, aldri blir ignorert.

| Nåværende tilstand | Skrives til |
|---|---|
| `lunascape-docs.json` inneholder et navn | `lunascape-docs.json` oppdateres |
| Ingen navn, men dokumentroten har en README | READMEs overskrift (H1) skrives om |
| Ingen av delene | `lunascape-docs.json` opprettes og navnet lagres der |

Meldingen som vises etter endringen, sier hvilket sted som ble skrevet til.

> **Tips**
>
> Dokumentnavnet bestemmes i denne rekkefølgen: navnet i `lunascape-docs.json`, deretter overskriften i dokumentrotens README, deretter mappenavnet.

## Endre et fil- eller mappenavn

1. Åpne elementmenyen og velg [Endre filnavnet] eller [Endre mappenavnet].
2. Skriv inn det nye navnet og trykk [Endre].

De tilsvarende oversettelsene (samme sti under `i18n/<språk>/`) endres samtidig.

## Slette

1. Åpne elementmenyen og velg [Flytt til papirkurven].
2. Kontroller bekreftelsesmeldingen og godkjenn flyttingen.

Målet flyttes til operativsystemets papirkurv, så det kan gjenopprettes ved behov. Oversettelsene slettes ikke og blir værende.

## Navn som ikke kan brukes

- Navn som begynner med `.` (de vil ikke vises i INDEX)
- `i18n` (reservert for oversettelsesfiler)
- Navn som er reservert av Windows (`CON`, `PRN` og så videre)
- Navn som ender med et punktum eller et mellomrom
- Navn som inneholder kontrolltegn eller tegn som ikke er tillatt i filnavn
- Navn som allerede finnes i den samme mappen (inkludert navn som bare skiller seg i store og små bokstaver)

> **Merk**
>
> Startsiden (vanligvis rotens `README.md`) kan ikke få nytt navn eller flyttes. Endre `startPage` i `lunascape-docs.json` først.

## Relaterte emner

- [Endre rekkefølgen på dokumenter](reorder.md)
- [Bruke INDEX](../02-reading/index-panel.md)
