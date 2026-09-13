# Använda INDEX

INDEX till vänster är trädet med mappar och dokument i dokumentroten.

## Filtrera

1. Skriv ett ord i [Filtrera dokument] ovanför INDEX.
2. Endast de poster vars dokumentnamn matchar visas. Radera texten för att återgå.

> **Obs!**
>
> Under filtrering går det inte att ändra ordningen med dra och släpp.

## Öppna och stänga mappar

- Tryck på pilen till vänster om mappnamnet, eller på namnet på en mapp utan omslagssida, för att öppna eller stänga den.
- En mapp med omslagssida (en `README.md` eller `index.md` med brödtext) öppnar den sidan när du trycker på namnet. Använd [Öppna mapp] / [Stäng mapp] i postmenyn för att bara öppna eller stänga mappen.
- Mapparnas öppna och stängda läge sparas per användare och skrivs aldrig till filer som Git hanterar.

## README och mappens omslagssida

`README.md` är filen som beskriver vad mappen innehåller.

- I en mapp med en README visas den filen när du trycker på mappnamnet.
- I en mapp utan README visas det översta dokumentet i mappen.
- README-filens rubrik (H1) blir mappens namn i INDEX.

En README är inte obligatorisk. Lägg till en i efterhand genom att välja [Skapa README] i mappens postmeny (visas bara för mappar som saknar README).

## Visa eller dölja INDEX

- Den vänstra ikonen bland verktygsfältets kolumnkontroller visar eller döljer INDEX. Den högra ikonen visar eller döljer ”På den här sidan”.
- På smala skärmar börjar INDEX i stängt läge. Tryck på [Öppna INDEX] (tre streck) till vänster om [Tillbaka] för att öppna INDEX ovanpå brödtexten. Stäng det med [×] inuti INDEX, ett klick på bakgrunden, `Esc` eller genom att gå till ett annat dokument. Detta tillfälliga läge ändrar inte inställningen för breda skärmar.
- I en dokumentrot med bara ett dokument stängs INDEX automatiskt första gången. Öppna det igen med kolumnikonen. Stäng av beteendet med [Dölj när det bara finns ett dokument] under [Visningsinställningar].

## Använda postmenyn

Håll pekaren över en post i INDEX och tryck på [⋯] som visas, eller högerklicka på posten, för att öppna dess meny. Posterna står i följande ordning.

| Grupp | Poster |
|---|---|
| Vanliga åtgärder | [Öppna mapp] / [Stäng mapp], [Öppna INDEX] (öppnar mappens omslagssida), [Redigera], [Ändra titel], [Öppna i VS Code], [Kopiera sökväg] |
| Skapa och ordna | [Skapa README] (endast mappar utan README), [Nytt dokument], [Ny mapp], [Duplicera], [Ändra filnamn] / [Ändra mappnamn], [Flytta upp ett steg], [Flytta ned ett steg] |
| Ta bort | [Flytta till papperskorgen] |

- För att skapa direkt under dokumentroten trycker du på [⋯] längst till höger i INDEX-rubriken, eller högerklickar på en tom yta i INDEX, och väljer [Nytt dokument] eller [Ny mapp]. I samma meny finns [Ändra dokumentnamn] och, om dokumentroten saknar README, [Skapa README]. Samma meny öppnas om du högerklickar på dokumentnamnet i verktygsfältet.
- Inuti menyn flyttar du dig med `↑` `↓` och går till första och sista posten med `Home` `End`. Stänger du med `Esc` återgår fokus till den plats det hade innan menyn öppnades.

> **Obs!**
>
> Posterna för att skapa, ordna och ta bort visas bara när arbetsytan är betrodd i VS Code. De är inte heller tillgängliga medan ett dokument redigeras eller medan en annan INDEX-åtgärd pågår.

## Ändra utseendet

Under [Visningsinställningar] kan du ändra visningen av filnamn, ikoner för dokument och mappar, antalet poster i mappar, hjälplinjer för nivåer och visningstätheten. Mer information finns i [Ändra visningsinställningar](display-settings.md).

## Se även

- [Skapa och ordna dokument och mappar](../03-editing/organize.md)
- [Ändra dokumentens ordning](../03-editing/reorder.md)
