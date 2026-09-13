# Endre rekkefølgen på dokumenter

Rekkefølgen som vises i INDEX, kan endres ved dra og slipp eller fra tastaturet. Den nye rekkefølgen lagres i dokumentets front matter som `navigation.order`.

## Sortere med dra og slipp

1. Dra et dokument eller en mappe i INDEX.
2. Slipp det foran eller bak et element på samme nivå, eller oppå en mappe.
   Innenfor samme nivå endres rekkefølgen. Slipper du oppå en annen mappe, flyttes elementet til den mappen.

## Sortere med tastaturet eller menyen

- Sett fokus på et element i INDEX og trykk `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Velg [Flytt opp] / [Flytt ned] i elementmenyen.

## Hva som lagres

- Når du sorterer innenfor samme nivå, oppdateres `navigation.order` i front matter til originaldokumentet. For en mappe skrives den til mappens `README.md`. Hvis mappen ikke har noen, opprettes en `README.md` med bare front matter.
- Når du flytter til en annen mappe, flyttes originaldokumentet sammen med de tilhørende oversettelsene. Før flyttingen får du en bekreftelse om at relative lenker kan bli påvirket.
- Git-staging og commit utføres aldri.

> **Merk**
>
> - Du kan ikke sortere mens du filtrerer, mens du redigerer et dokument, eller i et arbeidsområde som ikke er klarert.
> - Når «INDEXが更新されています» (INDEX er oppdatert) vises, er en annen endring nettopp tatt i bruk. Gjenta handlingen.
> - Startsiden kan ikke flyttes til en annen mappe.

> **Tips**
>
> Hvis du angir `navigation.order` i trinn på 100, for eksempel 100, 200, 300, blir det enkelt å sette inn dokumenter mellom dem senere. Se [Angi navigasjonsinformasjon](../04-document-tools/navigation-metadata.md) for mer informasjon.

## Relaterte emner

- [Opprette og organisere dokumenter og mapper](organize.md)
- [Angi navigasjonsinformasjon](../04-document-tools/navigation-metadata.md)
