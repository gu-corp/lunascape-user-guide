# Redigera ett dokument

Dokument kan redigeras direkt i visningsprogrammet. Redigeringsvyn har en visuell vy, där du redigerar det du ser, och en vy med Markdown-källkod. Du växlar mellan dem med en knapp.

## Börja redigera

Tryck på något av följande. Alla öppnar samma redigeringsvy.

- [Redigera] längst ned till höger i dokumentet
- [⋯] (Fler åtgärder) längst upp till höger i dokumentet → [Redigera]
- Objektmenyn i INDEX → [Redigera]

## Redigera

1. Redigera texten direkt.
   I verktygsfältet högst upp i redigeringsvyn finns styckeformat (brödtext, rubrik 1–4, citat, kod), [Fet], [Kursiv], [Punktlista], [Numrerad lista], [Länk], [Infoga tabell], [Bildstorlek], [Ångra] och [Gör om].
2. Tryck på [Markdown] när du vill redigera Markdown-källkoden direkt.
   Tryck en gång till för att återgå till den visuella vyn. Den vy du använde senast sparas och återställs nästa gång du trycker på [Redigera].
3. Tryck på [Spara].
   Ändringarna skrivs till Markdown-filen och visningsprogrammet återgår till läsläget. Tryck på [Avbryt] om du vill avbryta.

> **Obs!**
>
> - Vid sparande skrivs bara filen. Git-staging och commit sker aldrig automatiskt.
> - Matematik och diagram som Mermaid, TikZ och Vega-Lite visas som färdig grafik i den visuella vyn. Växla till [Markdown] för att ändra innehållet.
> - Dokument som innehåller MDX-specifik syntax (komponenter, `import` med mera) redigeras endast i Markdown-vyn, för att syntaxen ska bevaras.
> - Front matter (inställningarna mellan `---`-raderna högst upp) bevaras även när du redigerar i den visuella vyn.

> **Tips**
>
> - Tryck på [Öppna i VS Code] för att öppna filen i den vanliga textredigeraren. När du sparar där uppdateras visningsprogrammet automatiskt.
> - Om du inte vill visa knappen [Redigera] stänger du av [Redigeringsknappen] under [Visningsinställningar]. Ange `editor.showEditButton` till `false` i `lunascape-docs.json` om du vill dölja den i hela projektet.
> - Vilken vy som öppnas först (visuell eller Markdown) ställer du in med `lunascapeDocEditor.editor.defaultMode` eller med `editor.defaultMode` i `lunascape-docs.json`.

## Relaterade avsnitt

- [Skapa och ordna dokument och mappar](organize.md)
- [Justera bildstorleken](images.md)
- [Skriva matematik](math.md)
- [Skriva diagram och grafer](diagrams.md)
