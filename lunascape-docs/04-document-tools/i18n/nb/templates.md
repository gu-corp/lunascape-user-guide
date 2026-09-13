# Opprette et dokument fra en mal

I fanen [Opprett] i Dokumentverktøy velger du en mal, forhåndsviser innholdet og oppretter deretter et nytt dokument.

1. Trykk på [Dokumentverktøy] i verktøylinjen og åpne fanen [Opprett].
2. Trykk på [Opprett fra en mal] og velg en mal.
3. Fyll ut inndatafeltene (tittel, sammendrag og så videre). Obligatoriske felter er merket med «obligatorisk».
4. Angi lagringsplassen som en bane relativt til dokumentroten (for eksempel `03-design/api.md`).
5. Trykk på [Forhåndsvisning] og kontroller den genererte Markdown.
6. Trykk på [Opprett med dette innholdet].
   Dokumentet opprettes og vises i visningsprogrammet. Deretter kjøres en kontroll av hele dokumentroten.

## Maler du kan velge

| Mal | Innhold |
|---|---|
| Ettsidesdokument | Oppretter en kort spesifikasjon, et notat eller et frittstående forklaringsdokument i én fil |
| Spesifikasjon, manual, hjelp | Oppretter én fil med en generell kapittelinndeling som passer for en spesifikasjon, manual eller hjelp |
| Maler fra Standard Pack | Når Standard Pack er valgt i `lunascape-docs.json`, legges dokumenttypene som profilen tillater (kravdokument, designdokument og så videre), til |

> **Merk**
>
> - Oppretting krever et klarert arbeidsområde.
> - Eksisterende filer overskrives ikke. Du kan ikke opprette et dokument hvis det allerede finnes et dokument med samme navn på lagringsplassen.
> - Lagringsplassen må ha filtypen `.md` eller `.mdx`. Du kan ikke opprette dokumenter under `i18n` (der oversettelsene ligger).
> - Etter at du har endret inndataene, trykker du på [Forhåndsvisning] én gang til før du oppretter.

> **Tips**
>
> I et prosjekt som ennå ikke har en dokumentmappe, kan du opprette det første settet med «Lunascape Docs: Opprett dokument fra mal» i kommandopaletten. Se [Opprette dine første dokumenter](../01-introduction/first-documents.md).

## Relaterte emner

- [Bruke Dokumentverktøy](README.md)
- [Endre kontrollregler](rules.md)
