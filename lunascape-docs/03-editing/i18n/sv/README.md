# Redigera ett dokument

Dokument kan redigeras direkt i visaren. Redigeringsvyn har en "visuell vy", där du redigerar det du ser, och en "Markdown-källvy"; en enda knapp växlar mellan dem.

## Börja redigera

Tryck på något av följande. Alla öppnar samma redigeringsvy.

- [Redigera] längst ner till höger i dokumentet
- [⋯] (Fler åtgärder) längst upp till höger i dokumentet → [Redigera]
- INDEX-objektets meny → [Redigera]

## Redigera

1. Redigera texten direkt.
   I verktygsfältet längst upp i redigeringsvyn kan du använda styckeformat (brödtext, rubrik 1–4, citat, kod), [Fet], [Kursiv], [Punktlista], [Numrerad lista], [Länk], [Infoga tabell], [Bildstorlek], [Ångra] och [Gör om].
2. När du vill redigera Markdown-källan direkt trycker du på [Markdown].
   Tryck en gång till för att återgå till den visuella vyn. Den vy du använde senast sparas och återställs nästa gång du trycker på [Redigera].
3. Tryck på [Spara] (du kan även spara med Ctrl+S/⌘S).
   Markdown-filen skrivs och vyn återgår till läsläget. När du vill sluta redigera och återgå till det senast sparade innehållet trycker du på [Kasta redigeringar].

## Börja alltid i redigeringsvyn (redigeringsläge)

Tryck på [Redigeringsläge] i verktygsfältet för att slå på det, så börjar varje dokument i redigeringsvyn när du öppnar det. Använd det när du skriver löpande som i ett anteckningsblock.

- När det är på stängs redigeringsvyn inte när du trycker på [Spara]. [Kasta redigeringar] återgår till det senast sparade innehållet, och redigeringsvyn står kvar.
- Tryck en gång till för att slå av det och återgå till läsläget. På/av sparas per användare.
- Det visas inte för en dokumentrot som inte går att skriva till (till exempel en skrivskyddad GitHub-källa).

## Osparade redigeringar

Redigeringar som du inte har sparat behålls automatiskt på den här enheten. De går inte förlorade när du byter till ett annat dokument eller stänger fliken eller fönstret.

- [Osparat] i redigeringsvyn visar att innehållet skiljer sig från det senast sparade.
- Nästa gång du öppnar samma dokument återupptas de behållna redigeringarna, och du får ett meddelande om det. Om originaldokumentet har uppdaterats sedan dess får du även veta det. Med [Kasta redigeringar] kan du återgå till det senaste innehållet.
- De behållna redigeringarna försvinner med [Spara] eller [Kasta redigeringar]. Eftersom de inte har sparats visas de inte i Git eller bland utkasten.

> **Obs!**
>
> - Att spara skriver endast till filen. Git-stegning och commit görs aldrig automatiskt.
> - Matematik och diagram som Mermaid, TikZ och Vega-Lite visas som renderat resultat i den visuella vyn. Växla till [Markdown] för att ändra innehållet.
> - Dokument som innehåller MDX-specifik syntax (komponenter, `import` med mera) redigeras endast i Markdown-vyn för att bevara syntaxen.
> - Front matter (inställningarna som omges av `---` överst) behålls även om du redigerar i den visuella vyn.

> **Tips**
>
> - När du trycker på [Öppna i VS Code] öppnas filen i den vanliga textredigeraren. När du sparar i textredigeraren uppdateras visaren automatiskt.
> - När du inte vill visa knappen [Redigera] slår du av [Redigeringsknappen] i [Visningsinställningar]. För att dölja den för hela projektet ställer du in `editor.showEditButton` till `false` i `lunascape-docs.json`.
> - Standardvärdet för den vy som öppnas först (visuell/Markdown) kan ändras med inställningen `lunascapeDocEditor.editor.defaultMode` eller med `editor.defaultMode` i `lunascape-docs.json`.

## Se även

- [Skapa och organisera dokument och mappar](organize.md)
- [Justera bildstorlek](images.md)
- [Skriva matematik](math.md)
- [Skriva diagram och grafer](diagrams.md)
