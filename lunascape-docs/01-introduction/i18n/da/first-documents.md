# Opret dine første dokumenter

I et projekt, der endnu ikke har en dokumentmappe, kan du oprette et første sæt dokumenter fra kommandopaletten.

1. Åbn projektmappen i VS Code, og angiv, at du har tillid til arbejdsområdet.
2. Kør »Lunascape Docs: Opret dokumentation ud fra skabelon« fra kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).
   Hvis arbejdsområdet indeholder flere mapper, skal du vælge den, dokumenterne skal oprettes i.
3. Vælg den struktur, der skal oprettes.
   - [Enkeltsidet dokument]: kun en `README.md`. Egner sig til en kort specifikation, noter eller et enkeltstående forklarende dokument.
   - [Dokumentsæt]: en forside samt indgangssider til `specification/` (specifikation), `manual/` (manual) og `help/` (hjælp).
4. Indtast dokumentets titel. Den bruges til README og til overskrifterne i hvert dokument.
5. Indtast den dokumentmappe, der skal oprettes. Stien er relativ i forhold til arbejdsområdet, og standarden er `docs`.
6. Gennemse listen over de filer, der oprettes, og tryk på [Opret].
   Når oprettelsen er færdig, åbnes den nye `README.md` i fremviseren.

> **Bemærk**
>
> - Eksisterende filer overskrives ikke. Hvis blot én af de filer, der skal oprettes, allerede findes, oprettes intet, og handlingen afbrydes.
> - Der kan ikke oprettes dokumenter i et arbejdsområde, du ikke har tillid til.

> **Tip**
>
> - Hvis du allerede har en dokumentmappe, kan du springe dette over og gå videre til [Grundlæggende betjening](../02-reading/README.md).
> - Efterhånden som antallet af dokumenter vokser, kan du tilføje ét dokument ad gangen ud fra en skabelon på fanen [Opret] i Dokumentværktøjer.

## Relaterede emner

- [Opret et dokument ud fra en skabelon](../04-document-tools/templates.md)
- [Dokumentrødder og filkonventioner](../04-document-tools/structure.md)
