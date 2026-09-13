# Kontroll, skapande eller översättning fungerar inte

## Kontroll

### ”docs-lint är inte tillgängligt” visas

- Körmiljön för docs-lint saknas i tillägget, eller så är något fel i inställningarna. Installera om tillägget.
- ”Lita på den här arbetsytan i VS Code för att läsa in lokala Pack och inställningar på ett säkert sätt”: för att använda ett lokalt Standard Pack krävs en betrodd arbetsyta.

### Resultatet står kvar på ”omvalidering krävs”

När du ändrar ett dokument eller en inställning blir det tidigare resultatet ogiltigt. Tryck på [Kontrollera dokumentroten] igen. Ändringar som inte är sparade tas inte med.

### Det händer inget när du trycker på en anmärkning

Poster av typen ”hela dokumentroten” hör inte till något bestämt dokument och har därför ingen position. Kontrollera det dokument som anmärkningen gäller.

### Det går inte att spara regler

- En betrodd arbetsyta krävs.
- ”Lint-inställningarna har ändrats av en annan åtgärd”: `docs-lint.config.json` har ändrats utifrån. Läs in det senaste tillståndet och försök igen.
- Inställningsfiler som är symboliska länkar, eller som ligger utanför dokumentroten, går inte att redigera.

## Skapa från en mall

- ”Förhandsgranskningen av mallen har upphört att gälla” / ”Det du har angett har ändrats”: tryck på [Förhandsgranska] en gång till innan du skapar dokumentet.
- ”Det finns redan ett dokument på målplatsen”: befintliga filer skrivs aldrig över. Ange en annan målplats.
- Målplatsen behöver en sökväg relativt dokumentroten och filändelsen `.md` eller `.mdx`. Det går inte att skapa dokument under `i18n`.
- ”Lita på arbetsytan för att skapa dokument”: lita på arbetsytan i VS Code.

<!-- ai-only:start -->
## Översättning

### Det går inte att trycka på översättningsknapparna

- ”AI-översättning är inte aktiverad för den här dokumentroten”: ange `true` för `translation.enabled` i `lunascape-docs.json`.
- ”Projektets standardspråk är inte angivet”: spara standardspråket enligt [Ändra visningsinställningar](../02-reading/display-settings.md).
- ”Lägg till målspråket bland de språk som stöds”: lägg till målspråket i `locales`.
- ”Det finns inget originaldokument att översätta”: du har en översatt sida öppen. Växla till sidan på standardspråket.
- Massöversättning går inte att använda när en mapp visas tillfälligt. Lägg en `lunascape-docs.json` i mappen så att den blir en dokumentrot.

### Ett översättningsförslag avvisas eller måste göras om

- ”Originaldokumentet har ändrats. Gör om översättningsförslaget”: originalet eller målet ändrades efter att förslaget skapades. Översätt en gång till.
- Om svaret från språkmodellen saknar identifierare eller kod som ska skyddas, godtas det inte. Du kan se svarets innehåll i utdatapanelen under ”Lunascape Docs Översättning”.
- ”Massöversättning hanterar högst 1 000 dokument åt gången”: dela upp omfånget per mapp eller genom att välja dokument.
<!-- ai-only:end -->

## Relaterade avsnitt

- [Kontrollera dokument](../04-document-tools/check.md)
- [Skapa ett dokument från en mall](../04-document-tools/templates.md)
- [Lämna över arbete till en AI](../05-ai/README.md)
