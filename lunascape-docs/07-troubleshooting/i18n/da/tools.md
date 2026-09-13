# Kontrol, oprettelse eller oversættelse mislykkes

## Kontrol

### "docs-lint er ikke tilgængelig" vises

- Kørselsmiljøet for docs-lint mangler i udvidelsen, eller der er et problem med konfigurationen. Geninstaller udvidelsen.
- "Hav tillid til dette arbejdsområde i VS Code for at indlæse den lokale Pack og konfigurationen sikkert": for at bruge en lokal Standard Pack kræves der en browser, du har tillid til.

### Resultatet forbliver på "genkontrol påkrævet"

Når du ændrer et dokument eller en indstilling, bliver det forrige resultat ugyldigt. Tryk på [Kontrollér dokumentroden] igen. Ændringer, du ikke har gemt, medtages ikke.

### Et fund åbner ikke, når du trykker på det

Elementer under "Hele dokumentroden" er ikke knyttet til et bestemt dokument og har derfor ingen position. Følg indholdet af fundet, og kontrollér det relevante dokument.

### Regler kan ikke gemmes

- Der kræves en browser, du har tillid til.
- "Lint-konfigurationen blev ændret af en anden handling": `docs-lint.config.json` er blevet ændret eksternt. Genindlæs den nyeste tilstand, og prøv igen.
- Konfigurationsfiler, der er symbolske links eller ligger uden for dokumentroden, kan ikke redigeres.

## Oprettelse fra en skabelon

- "Skabelonens forhåndsvisning er udløbet" / "De indtastede oplysninger er ændret": tryk på [Forhåndsvisning] igen, før du opretter.
- "Der findes allerede et dokument på destinationen": eksisterende filer overskrives aldrig. Vælg en anden destination.
- Destinationen skal bruge en sti relativ til dokumentroden og en `.md`/`.mdx`-filendelse. Der kan ikke oprettes noget under `i18n`.
- "Hav tillid til arbejdsområdet for at oprette dokumenter": hav tillid til arbejdsområdet i VS Code.

<!-- ai-only:start -->
## Oversættelse

### Oversættelsesknapperne er deaktiverede

- "AI-oversættelse er ikke aktiveret for denne dokumentrod": sæt `translation.enabled` til `true` i `lunascape-docs.json`.
- "Projektets standardsprog er ikke angivet": gem standardsproget som beskrevet i [Ændring af visningsindstillinger](../02-reading/display-settings.md).
- "Tilføj destinationen til de understøttede sprog": tilføj destinationssproget til `locales`.
- "Der blev ikke fundet et originaldokument at oversætte": du har en oversat side åben. Skift til siden på standardsproget.
- Samlet oversættelse kan ikke bruges i en midlertidig mappevisning. Læg en `lunascape-docs.json` i mappen for at gøre den til en dokumentrod.

### Et forslag afvises eller skal genereres på ny

- "Originaldokumentet er blevet ændret. Generér forslaget på ny": originaldokumentet eller destinationen blev ændret, efter at forslaget blev oprettet. Oversæt igen.
- Et svar fra sprogmodellen, der mangler identifikatorer eller kode, som skulle have været beskyttet, accepteres ikke. Du kan se svarets indhold i outputpanelet "Lunascape Docs Oversættelse".
- "Samlet oversættelse behandler op til 1000 dokumenter ad gangen": opdel omfanget efter mappe eller ved eksplicit markering.
<!-- ai-only:end -->

## Relaterede emner

- [Kontrollér dokumenter](../04-document-tools/check.md)
- [Opret et dokument fra en skabelon](../04-document-tools/templates.md)
- [Overdrag arbejde til en AI](../05-ai/README.md)
