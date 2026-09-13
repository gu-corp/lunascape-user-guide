# Skapa dina första dokument

I ett projekt som ännu inte har någon dokumentmapp kan du skapa en första uppsättning dokument från kommandopaletten.

1. Öppna projektets mapp i VS Code och gör arbetsytan betrodd.
2. Kör ”Lunascape Docs: Skapa dokumentation från mall” i kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).
   Om arbetsytan innehåller flera mappar väljer du den arbetsyta som dokumenten ska skapas i.
3. Välj den struktur som ska skapas.
   - [Ensidigt dokument]: endast `README.md`. Passar för en kort specifikation, anteckningar eller ett fristående förklarande dokument.
   - [Dokumentationsuppsättning]: en startsida samt ingångssidor för `specification/` (specifikation), `manual/` (manual) och `help/` (hjälp).
4. Ange dokumentets titel. Den används för README och för rubrikerna i varje dokument.
5. Ange den dokumentmapp som ska skapas. Sökvägen anges relativt arbetsytan, och standardvärdet är `docs`.
6. Granska listan över filer som skapas och tryck på [Skapa].
   När allt har skapats öppnas den nya `README.md` i visningsprogrammet.

> **Obs!**
>
> - Befintliga filer skrivs aldrig över. Om så mycket som en av filerna som ska skapas redan finns avbryts åtgärden utan att något skapas.
> - Det går inte att skapa dokument i en arbetsyta som inte är betrodd.

> **Tips**
>
> - Om du redan har en dokumentmapp behöver du inte göra det här. Gå vidare till [Grundläggande åtgärder](../02-reading/README.md).
> - När dokumenten blir fler kan du lägga till ett dokument i taget från en mall på fliken [Skapa] i Dokumentverktyg.

## Relaterade ämnen

- [Skapa ett dokument från en mall](../04-document-tools/templates.md)
- [Dokumentrötter och filkonventioner](../04-document-tools/structure.md)
