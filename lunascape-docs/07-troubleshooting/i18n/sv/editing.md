# Det går inte att redigera, spara eller ändra ordning

## Knappen [Redigera] saknas

- [Redigeringsknappen] i [Visningsinställningar] är avstängd. Slå på den, eller använd [⋯] → [Redigera] uppe till höger i dokumentet, eller INDEX-postens meny → [Redigera].
- Detsamma gäller när `editor.showEditButton` i `lunascape-docs.json` är `false`.
- Det går inte att redigera medan hjälpen visas. Stäng hjälpen.

## Det går inte att växla till visuell visning

”Det här dokumentet innehåller MDX-syntax och kan därför inte öppnas i den vanliga redigeringsvyn”: dokument med MDX-specifik syntax (komponenter, `import` med mera) redigeras endast i Markdown-vyn, för att syntaxen ska bevaras.

## Det går inte att redigera matematik eller diagram direkt

Den visuella visningen visar det renderade resultatet. Tryck på [Markdown] i redigeringsvyn och redigera källtexten.

## Det går inte att ändra ordning eller dra

- Det går inte att ändra ordning under filtrering, medan ett dokument redigeras eller medan en annan INDEX-åtgärd pågår.
- När arbetsytan inte är betrodd går det inte att skapa, organisera eller ta bort. Ange arbetsytan som betrodd i VS Code.
- ”INDEX har uppdaterats. Dra en gång till”: en annan ändring har just tillämpats. Utför åtgärden en gång till.
- Startsidan (rotens `README.md`) kan inte flyttas.

## ”Det finns osparade ändringar” visas

Filen i fråga redigeras i VS Code-redigeraren. Spara eller kasta ändringarna först och försök sedan igen.

## Det går inte att byta namn

Följande namn kan inte användas.

- Namn som börjar med `.`, `i18n` och Windows reserverade namn (`CON` med flera)
- Namn som slutar med punkt eller blanksteg och namn som innehåller kontrolltecken eller tecken som inte är tillåtna i filnamn
- Namn som redan finns i samma mapp (inklusive namn som endast skiljer sig i stora och små bokstäver)
- Dokumentnamn utan filnamnstillägg för Markdown

## Sparade ändringar syns inte i Git eller checkas inte in

Lunascape Docs skriver bara till filen och utför varken staging eller incheckning i Git. Kontrollera i vyn för versionshantering i VS Code och checka in vid behov.

## Relaterade avsnitt

- [Redigera ett dokument](../03-editing/README.md)
- [Skapa och organisera dokument och mappar](../03-editing/organize.md)
- [Ändra dokumentens ordning](../03-editing/reorder.md)
