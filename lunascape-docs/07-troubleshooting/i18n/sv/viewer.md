# Dokument visas inte

## "Ingen Markdown- eller docs-mapp som kan öppnas hittades" visas

- Arbetsytan saknar en `docs`-mapp, eller så används ett annat namn än `docs`.
  - Lägg en `lunascape-docs.json` i mappen, så känns den igen som dokumentrot oavsett namn.
  - Eller lägg till mappnamnet i inställningen `lunascapeDocEditor.rootDirectoryNames`.
- Om det ännu inte finns några dokument skapar du dem med "Lunascape Docs: Skapa dokument från mall".
- Du kan också öppna en Markdown-fil i redigeraren och sedan köra "Lunascape Docs: Öppna i specifikationsvisaren".

## Ett dokument visas inte i INDEX

- Kontrollera att filändelsen är `.md`, `.markdown` eller `.mdx`.
- Följande mappar visas inte: mappar som börjar med `.`, `node_modules` och mappar som anges i `ignoredDirectories` (standard är `99-archive`).
- Översättningar under `i18n/` visas inte separat i INDEX. Växla till dem från språkmenyn.
- Om en fil du nyss lagt till inte visas trycker du på [Läs in på nytt].
- Du kanske tittar på en annan dokumentrot. Kontrollera dokumentrotens namn längst till vänster i verktygsfältet.

## Inget visas när du trycker på en mapp

Mappens `README.md` är en "beskrivning enbart för inställningar" som bara har front matter och ingen brödtext. Öppna mappen i INDEX och välj ett dokument i den.

## Fel dokumentrot öppnas

- Om inställningen `lunascapeDocEditor.rootMode` är `fixed` öppnas alltid `lunascapeDocEditor.root`.
- Med `auto` väljs den dokumentrot som ligger närmast den öppnade Markdown-filen. Du kan växla med listrutan längst till vänster i verktygsfältet.

## Dokumentroten har ett annat namn än väntat

Namnet bestäms i ordningen `title` i `lunascape-docs.json` → `navigation.title` i rotens `README.md` → dess H1 → `index.md` → mappnamnet. Ange `title` om du vill låsa namnet.

## INDEX har försvunnit

- I en dokumentrot med bara ett dokument stängs INDEX automatiskt första gången. Du kan öppna det med kolumnikonen i verktygsfältet. Du kan stänga av beteendet med [Dölj när det bara finns ett dokument] under [Visningsinställningar].
- När skärmen är smal öppnar du det med [Öppna INDEX] (tre streck) till vänster om [Tillbaka].

## En länk öppnas inte när du trycker på den

- "Länkmålet hittades inte": filen som länken pekar på finns inte. Du kan kontrollera interna länkar med [Kontroll] i Dokumentverktyg.
- "En osäker länk eller en länk som inte stöds öppnades inte": länkar utanför dokumentroten, eller till andra scheman än `https://` och `mailto:`, öppnas inte.

## Fel språk visas

- Kontrollera i språkmenyn vilket språk den visade sidan har och på vilken grund.
- Det visningsspråk du valde senast sparas. Välj standardspråket på nytt i språkmenyn.
- Om den personliga inställningen `lunascapeDocEditor.locale` är angiven prioriteras översättningen på det språket.

## Relaterade avsnitt

- [Växla dokumentrot](../02-reading/roots.md)
- [Dokumentrot och filkonventioner](../04-document-tools/structure.md)
