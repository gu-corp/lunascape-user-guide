# Ändra visningsinställningar

Via [Visningsinställningar] (kugghjulet) i verktygsfältet kan varje användare ändra hur INDEX visas och om redigeringsknappen visas.

1. Tryck på [Visningsinställningar] i verktygsfältet.
2. Växla de alternativ du vill ändra. Ändringarna får genomslag direkt.
3. Tryck på [Visningsinställningar] igen, eller klicka utanför panelen, för att stänga den.

## Inställningar du kan göra

| Avsnitt | Alternativ | Funktion |
|---|---|---|
| Dokumentspråk | (aktuellt läge) | Visar projektets standardspråk och språket som visas just nu. [Ange projektets språk…] öppnar projektets språkinställningar |
| Innehåll | [Filnamn] | Visar filnamn i stället för dokumentnamn |
| | [Dokumentikoner] | Visar en ikon vid varje dokument |
| | [Mappikoner] | Visar en ikon vid varje mapp |
| | [Antal i mappen] | Visar antalet dokument i mappen |
| | [Nivåhjälplinjer] | Visar hjälplinjer som markerar nivåerna |
| | [Dölj när det bara finns ett dokument] | Stänger INDEX automatiskt första gången i en dokumentrot med bara ett dokument |
| | [Fäll ihop dokumentuppgifterna] | Fäller ihop administrationstabellen högst upp i dokumentet till raden ”Dokumentuppgifter”. När alternativet är av visas tabellen som den är |
| | [Visningstäthet] | Väljer radavståndet i INDEX: [Normal] / [Kompakt] |
| | [Redigeringsknappen] | Visar [Redigera] nere till höger i dokumentet |
| Åtgärder | [Återställ till projektets standard] | Tar bort alla dina ändringar och återgår till projektets inställningar |
| | [Öppna tilläggets inställningar] | Öppnar inställningarna för Lunascape Docs i VS Code-inställningarna |

> **Tips**
>
> - Visningsinställningarna sparas per användare och per dokumentrot, och skrivs aldrig till filer som hanteras av Git.
> - Inställningarna gäller i ordningen ”användarens visningsinställningar → VS Code-inställningar → `lunascape-docs.json` → produktens standard”. Gemensamma standardvärden för teamet anges i `tree` och `editor` i `lunascape-docs.json`.

## Byta färgtema

Tryck på temaväxlaren (sol/måne) i verktygsfältet för att växla mellan vit bakgrund och VS Codes färgtema. Vilket tema som används när du öppnar bestäms av inställningen `lunascapeDocEditor.appearance` (`light` eller `auto`).

## Relaterade avsnitt

- [Använda INDEX](index-panel.md)
- [Projektinställningar](../04-document-tools/project-configuration.md)
- [Lista över VS Code-inställningar](../08-reference/settings.md)
