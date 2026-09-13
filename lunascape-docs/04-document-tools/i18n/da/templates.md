# Opret et dokument ud fra en skabelon

På fanen [Opret] i Dokumentværktøjer vælger du en skabelon, ser indholdet i forhåndsvisning og opretter derefter et nyt dokument.

1. Tryk på [Dokumentværktøjer] på værktøjslinjen, og åbn fanen [Opret].
2. Tryk på [Opret ud fra en skabelon], og vælg en skabelon.
3. Udfyld felterne (titel, resumé og så videre). Ved obligatoriske felter vises "Påkrævet".
4. Indtast destinationen som en sti i forhold til dokumentroden (for eksempel `03-design/api.md`).
5. Tryk på [Forhåndsvisning], og kontrollér den Markdown, der dannes.
6. Tryk på [Opret med dette indhold].
   Dokumentet oprettes og vises i fremviseren. Derefter kontrolleres hele dokumentroden.

## Skabeloner, du kan vælge

| Skabelon | Indhold |
|---|---|
| Dokument på én side | Opret en kort specifikation, en note eller et selvstændigt forklarende dokument i én fil |
| Specifikation, manual, hjælp | Opret én fil med en generel kapitelstruktur, der kan bruges til specifikationer, manualer og hjælp |
| Skabeloner fra Standard Pack | Når Standard Pack er valgt i `lunascape-docs.json`, føjes de dokumenttyper, som profilen tillader (kravspecifikation, designdokument og så videre), til listen |

> **Bemærk**
>
> - Oprettelse kræver en browser, du har tillid til.
> - Eksisterende filer overskrives ikke. Hvis der findes et dokument med samme navn på destinationen, kan dokumentet ikke oprettes.
> - Destinationen skal have filtypen `.md` eller `.mdx`. Der kan ikke oprettes dokumenter under `i18n` (hvor oversættelserne ligger).
> - Når du har ændret indtastningen, skal du trykke på [Forhåndsvisning] igen, før du opretter.

> **Tip**
>
> I et projekt, der endnu ikke har en dokumentmappe, kan du oprette det første sæt med "Lunascape Docs: Opret dokumentation ud fra en skabelon" i kommandopaletten. Se [Opret dine første dokumenter](../01-introduction/first-documents.md).

## Relaterede emner

- [Brug Dokumentværktøjer](README.md)
- [Ændr kontrolreglerne](rules.md)
