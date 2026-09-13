# Opprette de første dokumentene dine

I et prosjekt som ennå ikke har en dokumentasjonsmappe, kan du opprette et første sett med dokumenter fra kommandopaletten.

1. Åpne prosjektmappen i VS Code og klarer arbeidsområdet.
2. Kjør «Lunascape Docs: Opprett dokumentasjon fra mal» fra kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).
   Hvis arbeidsområdet har flere mapper, velger du arbeidsområdet der dokumentene skal opprettes.
3. Velg strukturen du vil opprette.
   - [Enkeltsidedokument]: bare en `README.md`. Passer til en kort spesifikasjon, notater eller et frittstående forklaringsdokument.
   - [Dokumentasjonssett]: en toppside pluss inngangssider for `specification/` (spesifikasjon), `manual/` (manual) og `help/` (hjelp).
4. Skriv inn dokumenttittelen. Den brukes til README-filen og overskriftene i hvert dokument.
5. Skriv inn dokumentmappen som skal opprettes, relativt til arbeidsområdet. Standard er `docs`.
6. Se gjennom listen over filer som skal opprettes, og trykk på [Opprett].
   Når opprettelsen er fullført, åpnes den nye `README.md` i viseren.

> **Merk**
>
> - Eksisterende filer overskrives aldri. Hvis bare én av filene som skal opprettes allerede finnes, opprettes ingenting, og operasjonen avbrytes.
> - Opprettelse er ikke tilgjengelig i et arbeidsområde som ikke er klarert.

> **Tips**
>
> - Hvis du allerede har en dokumentmappe, hopper du over dette og går til [Grunnleggende bruk](../02-reading/README.md).
> - Etter hvert som dokumentasjonen vokser, kan du legge til dokumenter ett om gangen fra maler i [Opprett]-fanen i Dokumentverktøy.

## Relaterte emner

- [Opprette et dokument fra en mal](../04-document-tools/templates.md)
- [Dokumentrøtter og filkonvensjoner](../04-document-tools/structure.md)
