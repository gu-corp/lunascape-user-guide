# Läsa på ett annat språk

Dokument som har översättningar kan du läsa på ett annat språk genom att byta språk i språkmenyn (jordgloben) i verktygsfältet.

## Byta språk

1. Tryck på språkmenyn i verktygsfältet.
   Språket för den sida som visas anges, tillsammans med grunden för det (sökvägen till översättningen, automatisk identifiering eller projektets standardspråk).
2. Välj det språk du vill läsa på.
   Översättningen av samma dokument öppnas. Det valda språket sparas, och nästa dokument du öppnar visas på det språket om det finns en översättning.

I språklistan anges om dokumentet har en översättning eller inte.

| Visning | Betydelse |
|---|---|
| Översättning finns | Det finns en översättning och den går att öppna |
| Ingen översättning | Språket stöds av projektet, men det här dokumentet har ännu ingen översättning |
| Inaktuell | Det finns en översättning, men originaldokumentet har ändrats efter att den gjordes |

> **Obs!**
>
> - Att välja ett språk öppnar bara en översättning som redan finns. Ingen översättning skapas och ingen fil läggs till. Använd [Skapa och hantera översättningar…] i samma meny för att skapa en översättning.
> - Om språket på den sida som visas bedöms skilja sig från projektets standardspråk visas en varning. Inställningarna skrivs aldrig om.

## Språket som visas först

När du öppnar ett dokument bestäms det första visningsspråket i den här ordningen.

1. Det språk du själv har valt tidigare i den här dokumentroten. Valet sparas (även ett val av standardspråket sparas som ett val).
2. Visningsspråket i VS Code (i webbläsarversionen språkinställningen i webbläsaren). Ett språk som stöds och stämmer överens väljs automatiskt. Ett språk med region (till exempel `en-US`) stämmer även överens med grundspråket (`en`).
3. Projektets reservspråk (`fallbackLocale` i `lunascape-docs.json`).
4. Projektets standardspråk.

> **Tips**
>
> - När språket har valts automatiskt står det ”Automatiskt vald” vid det aktuella språket i språkmenyn. Håll pekaren över märket för att se orsaken.
> - `fallbackLocale` är det språk som visas för läsare vars miljöspråk inte stämmer överens med något av de språk som stöds. I ett projekt där japanska är originalspråk och det finns en engelsk version öppnas den engelska versionen för en läsare med till exempel spanskspråkig miljö om du anger `"en"`. Om inget anges används standardspråket.

## Var översättningarna ligger

Dokument på standardspråket ligger kvar där de är, och översättningen läggs i **`i18n/<språk>/` i samma mapp**, under samma filnamn.

```text
docs/
  README.md                  ← standardspråk (till exempel japanska)
  i18n/en/README.md          ← dess engelska översättning
  guide/
    setup.md
    i18n/en/setup.md         ← dess engelska översättning
```

> **Obs!**
>
> - En mappstruktur som byggs upp på nytt under `i18n/` (`i18n/en/guide/setup.md`) känns inte igen. Mappen `i18n/` ska alltid ligga i samma mapp som dokumentet.
> - Översättningen slås upp på den här enda platsen. Om du även lägger en översättning av samma dokument i en `i18n/`-mapp högre upp uppstår ingen konflikt om vilken som gäller: den filen blir i stället en föräldralös fil som varken visas i språkmenyn eller i förteckningen (och den tas inte bort automatiskt). Lägg inte samma översättning på två ställen.

## Om du läser i webbläsarversionen

I webbläsarversionen byter du språk på samma sätt när det finns en översättning. Om du vill läsa på ett språk som saknar översättning kan du använda webbläsarens sidöversättning. Kod, matematik och diagram är undantagna från översättningen.

## Relaterade avsnitt

- [Lämna över arbete till en AI](../05-ai/README.md)
- [Arbete du kan lämna över](../05-ai/tasks.md)
- [Ändra visningsinställningar](../02-reading/display-settings.md)
