# Grundläggande användning

Den grundläggande användningen, från att öppna dokumenten till att komma fram till den sida du vill läsa.

## Öppna dokumenten

1. Öppna lagringsplatsen i VS Code.
2. Kör ”Lunascape Docs: Öppna specifikationsvisaren” i kommandopaletten (`⇧⌘P` / `Ctrl+Shift+P`).
   Närmaste dokumentrot (som standard mappen `docs`) hittas och dess startsida visas.

> **Tips**
>
> - Högerklicka på en Markdown-fil i Utforskaren och välj [Lunascape Docs: Öppna i specifikationsvisaren] för att börja från den filen.
> - Om du öppnar en Markdown-fil som inte hör till någon dokumentrot visas dess mapp som en tillfällig dokumentrot.

## Flytta mellan sidor

| Åtgärd | Så gör du |
|---|---|
| Öppna från innehållsförteckningen | Tryck på ett dokumentnamn i INDEX till vänster |
| Följa en länk | Tryck på en länk i texten. Den öppnas i samma vy |
| Gå genom historiken | [Tillbaka] och [Framåt] i verktygsfältet, eller `Alt`+`←` / `Alt`+`→` |
| Återvända till startsidan | [Specifikationens startsida] i verktygsfältet |
| Gå upp en nivå | [Överordnat INDEX] i verktygsfältet, eller ett objekt i sökvägen |
| Flytta inom sidan | Tryck på en rubrik i ”På den här sidan” till höger |

## Hitta ett dokument

Skriv ett ord i [Filtrera dokument] ovanför INDEX, så visas bara de dokument vars namn stämmer. Töm fältet för att visa allt igen.

## Uppdatera innehållet

När du sparar en Markdown-fil i VS Code-redigeraren uppdateras vyn automatiskt. Om du har ändrat filerna med ett externt verktyg trycker du på [Läs in på nytt] i verktygsfältet.

> **Obs!**
>
> - Externa länkar (`https://` och liknande) öppnas i din standardwebbläsare. Länkar till filer utanför dokumentroten öppnas inte.
> - Dokumenten behandlas på din enhet. Inget skickas någonstans för att du ska kunna läsa ett dokument.

## Relaterade ämnen

- [Använda INDEX](index-panel.md)
- [Byta dokumentrot](roots.md)
- [Redigera ett dokument](../03-editing/README.md)
