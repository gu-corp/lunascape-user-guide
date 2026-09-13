# Læs på et andet sprog

Når et dokument har oversættelser, kan du skifte sprog i sprogmenuen (globussen) på værktøjslinjen.

## Skift sprog

1. Tryk på sprogmenuen på værktøjslinjen.
   Den viser sproget på den aktuelle side og grundlaget for det (stien til oversættelsen, automatisk registrering eller projektets standardsprog).
2. Vælg det sprog, du vil læse på.
   Oversættelsen af det samme dokument åbnes. Det valgte sprog huskes, og det næste dokument, du åbner, vises på det sprog, hvis der findes en oversættelse.

Listen viser, om hvert sprog har en oversættelse af dokumentet.

| Visning | Betydning |
|---|---|
| Oversat | Der findes en oversættelse, og den kan åbnes |
| Ikke oversat | Sproget understøttes af projektet, men dokumentet har endnu ingen oversættelse |
| Forældet | Der findes en oversættelse, men originaldokumentet er ændret, efter at den blev lavet |

> **Bemærk**
>
> - Når du vælger et sprog, åbnes kun en oversættelse, der allerede findes. Der bliver hverken genereret en oversættelse eller oprettet en fil. Brug [Opret og administrer oversættelser…] i den samme menu for at lave en oversættelse.
> - Hvis sproget på den aktuelle side vurderes at være et andet end projektets standardsprog, vises en advarsel. Indstillingerne bliver ikke ændret.

## Det sprog, der vises først

Når du åbner et dokument, afgøres det første visningssprog i denne rækkefølge.

1. Det sprog, du tidligere selv har valgt i denne dokumentrod. Valget gemmes (også hvis du vælger standardsproget, gemmes det som et valg).
2. Visningssproget i VS Code (i webbrowserversionen browserens sprogindstillinger). Et understøttet sprog, der passer, vælges automatisk. Et sprog med region (for eksempel `en-US`) passer også til grundsproget (`en`).
3. Projektets reservesprog (`fallbackLocale` i `lunascape-docs.json`).
4. Projektets standardsprog.

> **Tip**
>
> - Når sproget er valgt automatisk, står der »Valgt automatisk« ved det aktuelle sprog i sprogmenuen. Hold markøren over mærkatet for at se begrundelsen.
> - `fallbackLocale` er det sprog, der vises til læsere, hvis miljøsprog ikke passer til nogen af de understøttede sprog. I et projekt med japansk som originalsprog og en engelsk udgave åbner `"en"` den engelske udgave for læsere i for eksempel et spansksproget miljø. Er den ikke angivet, bruges standardsproget.

## Hvor oversættelserne ligger

Dokumenter på standardsproget bliver liggende, hvor de er, og oversættelsen lægges i **`i18n/<sprog>/` i den samme mappe** under det samme filnavn.

```text
docs/
  README.md                  ← standardsprog (for eksempel japansk)
  i18n/en/README.md          ← den engelske udgave
  guide/
    setup.md
    i18n/en/setup.md         ← den engelske udgave
```

> **Bemærk**
>
> - Hvis mappestrukturen bygges op igen under `i18n/` (`i18n/en/guide/setup.md`), genkendes den ikke. `i18n/` skal altid ligge i den samme mappe som dokumentet.
> - Oversættelser slås kun op dette ene sted. Lægger du den samme oversættelse i en overordnet mappes `i18n/`, opstår der ingen konflikt om, hvad der har forrang: kopien deroppe bliver blot en forældreløs fil, som hverken sprogmenuen eller registret nogensinde ser (og den slettes ikke automatisk). Læg ikke den samme oversættelse to steder.

## Hvis du læser i webbrowserversionen

I webbrowserversionen kan du skifte sprog på samme måde, når der findes en oversættelse. Vil du læse på et sprog, der ikke er oversat til, kan du bruge browserens sideoversættelse. Kode, matematik og diagrammer holdes uden for oversættelsen.

## Relaterede emner

- [Giv arbejde videre til en AI](../05-ai/README.md)
- [Arbejde, du kan give videre](../05-ai/tasks.md)
- [Skift visningsindstillinger](../02-reading/display-settings.md)
