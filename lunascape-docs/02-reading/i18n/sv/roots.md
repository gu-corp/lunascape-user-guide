# Byta dokumentrot

Dokumentroten är den översta mappen för en uppsättning dokument. INDEX, filtrering, kontroll och översättning fungerar alla per dokumentrot.

## Så hittas dokumentroten

Lunascape Docs går uppåt från den öppnade Markdown-filen och använder den närmaste mapp som stämmer med något av följande som dokumentrot.

- En mapp som innehåller `lunascape-docs.json` (mappnamnet spelar ingen roll)
- En mapp som heter `docs` (fler namn kan läggas till med inställningen `lunascapeDocEditor.rootDirectoryNames`)

När du kör ”Lunascape Docs: Öppna specifikationsvisaren” öppnas dokumentroten i inställningen `lunascapeDocEditor.root` (standard `docs`).

## Byta till en annan dokumentrot

När arbetsytan har flera dokumentrötter blir dokumentrotens namn längst till vänster i verktygsfältet en listruta.

1. Tryck på dokumentrotens namn längst till vänster i verktygsfältet.
2. Välj en dokumentrot i listan.
   Startsidan för den valda dokumentroten visas och INDEX byts ut.

> **Tips**
>
> Namnen i listan bestäms i följande ordning. De ändras inte när du byter visningsspråk.
>
> 1. `title` i `lunascape-docs.json`
> 2. `navigation.title` i rotens `README.md`, annars dess H1
> 3. `navigation.title` i rotens `index.md`, annars dess H1
> 4. Mappnamnet (för en vanlig `docs`-mapp namnet på dess överordnade mapp)

## Öppna Markdown utanför en dokumentrot

När du öppnar en Markdown-fil som inte ligger i en dokumentrot visas filens mapp som en tillfällig dokumentrot. I INDEX listas Markdown-filerna i den mappen och under den.

- Tryck på [Upp en mapp] i verktygsfältet för att utvidga omfånget till den överordnade mappen inom arbetsytan.
- I den här vyn går projektets språkinställningar och samlad översättning inte att använda. Lägg en `lunascape-docs.json` i mappen så att den blir en dokumentrot, så blir de tillgängliga.

## Alltid öppna en bestämd dokumentrot

Om du ställer in `lunascapeDocEditor.rootMode` på `fixed` öppnas alltid dokumentroten i `lunascapeDocEditor.root`, vilken Markdown-fil du än öppnar.

## Se även

- [Dokumentrötter och filkonventioner](../04-document-tools/structure.md)
- [Projektinställningar](../04-document-tools/project-configuration.md)
- [Lista över VS Code-inställningar](../08-reference/settings.md)
