# Spara utkast

När du redigerar ett dokument i webbversionen skrivs ändringarna inte till lagringsplatsen, utan sparas som ett "utkast" i webbläsaren.

## Skapa ett utkast

1. Öppna ett dokument och tryck på [Redigera] längst ned till höger.
2. Redigera och tryck på [Spara].
   "Sparat som utkast" visas och ändringen sparas i webbläsaren.

- Dokument med ett utkast får en markering i INDEX. Ovanför texten visas "Det här dokumentet är ett utkast på den här enheten (ej publicerat)".
- [Utkast] i verktygsfältet visar antalet, och när du trycker på knappen öppnas listan med utkast.

## Förkasta ett utkast

- Tryck på [Förkasta utkastet] ovanför texten för att förkasta utkastet för ett enskilt dokument.
- Använd listan med utkast för att förkasta alla.

## Överföra till lagringsplatsen

"Publiceringsbegäran", som skickar utkast som en pull request, är implementerad men inte aktiverad i den publika visningen. Redigera med VS Code-versionen eller i en lokal klon för att ändra lagringsplatsen.

> **Obs!**
>
> - Utkast sparas i webbläsaren (IndexedDB). De följer inte med till en annan webbläsare eller en annan enhet, och om du rensar webbplatsdata i webbläsaren försvinner även utkasten.
> - Om dokumentet i lagringsplatsen uppdateras efter att du skapat ett utkast visas "Uppströms har uppdaterats". Kontrollera innehållet och avgör sedan om du vill förkasta utkastet eller använda det som det är.
> - Om du öppnar en lokal mapp från [Öppna dokument] och redigerar där sparas ändringarna direkt i filen, förutsatt att webbläsaren har stöd för det. I webbläsare utan stöd bevaras de bara under den aktuella sessionen.

## Relaterade avsnitt

- [Vad webbversionen kan göra](README.md)
- [Redigera ett dokument](../03-editing/README.md)
