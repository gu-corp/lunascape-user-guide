# Skapa och organisera dokument och mappar

Från objektmenyn i INDEX kan du skapa, duplicera, byta namn på och ta bort dokument och mappar. Inmatningen sker i en liten dialogruta inne i visaren, utan att läsningen avbryts.

> **Obs!**
>
> De här åtgärderna är endast tillgängliga när arbetsytan är betrodd i VS Code. De kan inte utföras medan ett dokument redigeras, medan en annan åtgärd pågår eller när objektet har osparade ändringar.

## Skapa ett dokument eller en mapp

1. Öppna objektmenyn ([⋯] eller högerklick) för mappen där objektet ska skapas.
   För att skapa direkt under dokumentroten använder du [⋯] längst till höger i INDEX-rubriken eller högerklickar på ett tomt område i INDEX.
2. Välj [Nytt dokument] eller [Ny mapp].
3. Ange ett namn och tryck på [Skapa].
   Ett dokumentnamn behöver en Markdown-filändelse (`.md`, `.markdown`, `.mdx` och så vidare).

Nya dokument skapas som dokument på standardspråket (originaldokument).

## Duplicera ett dokument

1. Öppna dokumentets objektmeny och välj [Duplicera].
2. Ange ett nytt namn och tryck på [Skapa].

Endast originaldokumentet dupliceras. Översättningarna dupliceras inte.

## Ändra titeln

Ändrar dokumentets rubrik (H1). Filnamnet ändras inte.

1. Öppna objektmenyn för ett dokument eller en mapp och välj [Ändra titel].
2. Ange den nya titeln på en rad och tryck på [Ändra].

För en mapp ändras rubriken i mappens `README.md`. När en översättning visas ändras titeln på det språkets dokument.

## Ändra dokumentnamnet

Ändrar dokumentnamnet som visas i verktygsfältet (dokumentrotens namn).

1. Högerklicka på dokumentnamnet i verktygsfältet. Samma meny öppnas också via [⋯] längst till höger i INDEX-rubriken.
2. Välj [Ändra dokumentnamn] och ange ett nytt namn.

När inget är inställt visas mappnamnet som det är.

Namnet du anger skrivs till **den plats som just nu används som dokumentnamn**. Det skrivs aldrig till en plats som inte används för visningen, så att en synlig rubrik hamnar i ett tillstånd där den ignoreras.

| Nuvarande tillstånd | Skrivs till |
|---|---|
| `lunascape-docs.json` innehåller ett namn | `lunascape-docs.json` uppdateras |
| Inget namn, men dokumentroten har en README | README-filens rubrik (H1) skrivs om |
| Ingetdera | `lunascape-docs.json` skapas och namnet sparas där |

Meddelandet som visas efter ändringen anger vilken av dem som skrevs.

> **Tips**
>
> Dokumentnamnet bestäms i följande ordning: namnet i `lunascape-docs.json`, därefter rubriken i dokumentrotens README, därefter mappnamnet.

## Byta namn på en fil eller mapp

1. Öppna objektmenyn och välj [Byt filnamn] eller [Byt mappnamn].
2. Ange det nya namnet och tryck på [Ändra].

Motsvarande översättningar (samma sökväg under `i18n/<språk>/`) byter namn samtidigt.

## Ta bort

1. Öppna objektmenyn och välj [Flytta till papperskorgen].
2. Kontrollera bekräftelsemeddelandet och godkänn flytten.

Objektet flyttas till operativsystemets papperskorg och kan vid behov återställas. Översättningarna tas inte bort utan finns kvar.

## Namn som inte kan användas

- Namn som börjar med `.` (de visas inte i INDEX)
- `i18n` (reserverat för översättningsfiler)
- Namn som är reserverade i Windows (`CON`, `PRN` och så vidare)
- Namn som slutar med punkt eller blanksteg
- Namn som innehåller kontrolltecken eller tecken som inte är tillåtna i filnamn
- Namn som redan finns i samma mapp (inklusive namn som endast skiljer sig i versaler och gemener)

> **Obs!**
>
> Startsidan (normalt `README.md` i roten) kan inte byta namn eller flyttas. Ändra `startPage` i `lunascape-docs.json` först.

## Relaterade avsnitt

- [Ändra dokumentens ordning](reorder.md)
- [Använda INDEX](../02-reading/index-panel.md)
