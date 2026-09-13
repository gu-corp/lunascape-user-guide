# Skapa ett dokument från en mall

På fliken [Skapa] i Dokumentverktyg väljer du en mall, förhandsgranskar innehållet och skapar sedan ett nytt dokument.

1. Tryck på [Dokumentverktyg] i verktygsfältet och öppna fliken [Skapa].
2. Tryck på [Skapa från en mall] och välj en mall.
3. Fyll i inmatningsfälten (titel, sammanfattning och så vidare). Obligatoriska fält är märkta med ”Obligatoriskt”.
4. Ange målet som en sökväg i förhållande till dokumentroten (till exempel `03-design/api.md`).
5. Tryck på [Förhandsgranska] och granska den Markdown som genereras.
6. Tryck på [Skapa med det här innehållet].
   Dokumentet skapas och visas i visaren. Därefter kontrolleras hela dokumentroten.

## Mallar att välja mellan

| Mall | Innehåll |
|---|---|
| Ensidigt dokument | En kort specifikation, anteckningar eller ett fristående förklarande dokument i en enda fil |
| Specifikation, manual, hjälp | En fil med en allmän kapitelindelning som passar för en specifikation, en manual eller hjälp |
| Mallar i Standard Pack | När Standard Pack är valt i `lunascape-docs.json` tillkommer de dokumenttyper som profilen tillåter (kravspecifikation, designdokument och så vidare) |

> **Obs!**
>
> - Det krävs en betrodd arbetsyta för att skapa dokument.
> - Befintliga filer skrivs aldrig över. Det går inte att skapa dokumentet om det redan finns ett dokument med samma namn på målplatsen.
> - Målet måste ha filtillägget `.md` eller `.mdx`. Inget kan skapas under `i18n` (där översättningarna ligger).
> - När du har ändrat något i inmatningen trycker du på [Förhandsgranska] en gång till innan du skapar dokumentet.

> **Tips**
>
> I ett projekt som ännu inte har någon dokumentmapp kan du skapa den första uppsättningen med ”Lunascape Docs: Skapa dokument från mall” i kommandopaletten. Se [Skapa dina första dokument](../01-introduction/first-documents.md).

## Se även

- [Använda Dokumentverktyg](README.md)
- [Ändra kontrollregler](rules.md)
