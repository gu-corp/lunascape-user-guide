# Arbejde, du kan overdrage

Vælg under [Opgave] i fanen [AI]. Hver opgave ændrer den instruktion, der overdrages, og den kontrol, der følger.

| Arbejde | Indhold | Kræver | API-type |
|---|---|---|---|
| Oversæt denne side | Oversætter det viste dokument til det valgte sprog | At måldokumentet er åbent, et målsprog | ○ |
| Oversæt alt ikke oversat | Oversætter de ikke oversatte og forældede dokumenter for det valgte sprog, i rækkefølge | Et målsprog | Kun sessionstype |
| Korrekturlæs denne side | Kontrollerer og retter terminologi, stil og den kapitelinddeling, som dokumentstandarden kræver | At måldokumentet er åbent | ○ |
| Opret et nyt dokument | Opretter et nyt dokument efter dokumentstandarden og dens skabeloner | Et emne (valgfrit) | Kun sessionstype |

## Hvad instruktionen indeholder

| Nr. | Indhold |
|---|---|
| 1 | Placeringen af dokumentroden med en instruktion om ikke at ændre noget uden for den |
| 2 | Standardsproget (originaldokumentet) og hvor oversættelserne ligger (en `i18n/<sprog>/`-mappe ved siden af dokumentet) |
| 3 | At `navigation.order` kun tilhører originaldokumentet, og at en oversættelse kun må overskrive `navigation.title` |
| 4 | At krav-ID'er, links, kode, Mermaid, TeX og strukturen i front matter ikke må ændres |
| 5 | Dokumentstandarden og ordlisten (`terminology` i `docs-lint.config.json`) |
| 6 | At køre dokumentkontrollen bagefter, rapportere de ændrede filer og ikke udføre nogen Git-handlinger |

> **Tip**
>
> Målene for "Oversæt alt ikke oversat" kommer fra hovedbogen, op til 200 dokumenter pr. kørsel. Kør den igen, hvis der er flere.

## Relaterede emner

- [At overdrage arbejde til en AI](README.md)
- [Hovedbogen og dens registreringer](ledger.md)
