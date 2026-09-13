# Tilgjengelige oppgaver

Velg under [Oppgave] i [AI]-fanen. Hver oppgave endrer instruksjonen som overleveres, og kontrollen som følger etter.

| Oppgave | Innhold | Krever | API-type |
|---|---|---|---|
| Oversett denne siden | Oversetter det viste dokumentet til det valgte språket | At dokumentet er åpent, et målspråk | Ja |
| Oversett alt som mangler | Oversetter dokumentene på det valgte språket som er ikke oversatt eller utdaterte, i rekkefølge | Et målspråk | Kun økt |
| Korrekturles denne siden | Kontrollerer og retter terminologi, stil og kapittelinndelingen som dokumentstandarden krever | At dokumentet er åpent | Ja |
| Opprett et nytt dokument | Oppretter et nytt dokument i tråd med dokumentstandarden og malene | Emne (valgfritt) | Kun økt |

## Hva instruksjonen inneholder

| Nr. | Innhold |
|---|---|
| 1 | Plasseringen av dokumentroten, med beskjed om å ikke endre noe utenfor den |
| 2 | Standardspråket (originaldokumentet) og hvor oversettelsene ligger (en `i18n/<språk>/`-mappe ved siden av dokumentet) |
| 3 | At `navigation.order` bare tilhører originaldokumentet, og at en oversettelse bare kan overstyre `navigation.title` |
| 4 | At struktur for krav-ID-er, lenker, kode, Mermaid, TeX og front matter ikke må endres |
| 5 | Dokumentstandarden og ordlisten (`terminology` i `docs-lint.config.json`) |
| 6 | Å kjøre dokumentkontrollen etterpå, rapportere filene som ble endret, og ikke utføre noen Git-operasjoner |

> **Tips**
>
> Målene for «Oversett alt som mangler» lages fra loggboken, opptil 200 dokumenter per kjøring. Kjør den på nytt for resten.

## Relaterte emner

- [Overlate arbeid til en AI](README.md)
- [Loggboken og oppføringene](ledger.md)
