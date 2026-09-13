# Lese på et annet språk

Når et dokument har oversettelser, kan du bytte språk fra språkmenyen (globusen) på verktøylinjen.

## Bytt språk

1. Trykk på språkmenyen på verktøylinjen.
   Den viser språket til siden som vises nå, og grunnlaget for det (banen til oversettelsen, automatisk gjenkjenning eller prosjektets standardspråk).
2. Velg språket du vil lese.
   Oversettelsen av det samme dokumentet åpnes. Det valgte språket huskes, og neste dokument du åpner, vises på det språket når det finnes en oversettelse.

Listen viser om det finnes en oversettelse av dokumentet på hvert språk.

| Visning | Betydning |
|---|---|
| Oversatt | En oversettelse finnes og kan åpnes |
| Ikke oversatt | Språket støttes av prosjektet, men dokumentet har ennå ingen oversettelse |
| Utdatert | En oversettelse finnes, men originaldokumentet er endret etter at den ble oversatt |

> **Merk**
>
> - Å velge et språk åpner bare en oversettelse som allerede finnes. Det genererer aldri en oversettelse og oppretter aldri en fil. For å lage en oversettelse bruker du [Opprett eller administrer oversettelser…] i den samme menyen.
> - Når språket til siden som vises nå, ser ut til å avvike fra prosjektets standardspråk, vises en advarsel. Innstillingene blir aldri skrevet om.

## Språket som vises først

Når du åpner et dokument, avgjøres det første visningsspråket i denne rekkefølgen.

1. Språket du selv har valgt tidligere i denne dokumentroten. Valget ditt lagres (også når du velger standardspråket, lagres det som et valg).
2. Visningsspråket i VS Code (i nettleserutgaven, nettleserens språkinnstillinger). Et støttet språk som stemmer overens, velges automatisk. Et språk med regiontillegg (som `en-US`) stemmer også overens med grunnspråket (`en`).
3. Prosjektets reservespråk (`fallbackLocale` i `lunascape-docs.json`).
4. Prosjektets standardspråk.

> **Tips**
>
> - Når språket ble valgt automatisk, vises «automatisk valgt» ved gjeldende språk i språkmenyen. Hold pekeren over merket for å se grunnen.
> - `fallbackLocale` er språket som vises til lesere hvis miljøspråk ikke stemmer overens med noen av de støttede språkene. I et prosjekt der japansk er originalen og som har en engelsk utgave, vil `"en"` gjøre at den engelske utgaven åpnes for lesere i for eksempel et spanskspråklig miljø. Når det ikke er satt, brukes standardspråket.

## Hvor oversettelsene ligger

Dokumenter på standardspråket blir liggende der de er, mens en oversettelse legges i **mappen `i18n/<språk>/` ved siden av dokumentet**, med samme filnavn.

```text
docs/
  README.md                  ← standardspråk (for eksempel japansk)
  i18n/en/README.md          ← den engelske utgaven
  guide/
    setup.md
    i18n/en/setup.md         ← den engelske utgaven
```

> **Merk**
>
> - Å bygge opp mappestrukturen på nytt under `i18n/` (`i18n/en/guide/setup.md`) gjenkjennes ikke. Mappen `i18n/` skal alltid ligge ved siden av dokumentet den oversetter.
> - Det ene stedet er det eneste stedet en oversettelse hentes fra. Å legge den samme oversettelsen i en overordnet mappes `i18n/` i tillegg gir ingen konflikt om «hvilken som har forrang»: kopien i den overordnede mappen blir bare en foreldreløs fil som verken språkmenyen eller registeret noen gang ser (og som aldri slettes automatisk). Ikke legg den samme oversettelsen to steder.

## Lese i nettleserutgaven

Nettleserutgaven bytter språk på samme måte når det finnes oversettelser. Vil du lese et språk som ikke har en oversettelse, kan du bruke nettleserens sideoversettelse. Kode, matematikk og diagrammer holdes utenfor nettleseroversettelsen.

## Relaterte emner

- [Overlate arbeid til en AI](../05-ai/README.md)
- [Arbeid som kan overlates](../05-ai/tasks.md)
- [Endre visningsinnstillinger](../02-reading/display-settings.md)
