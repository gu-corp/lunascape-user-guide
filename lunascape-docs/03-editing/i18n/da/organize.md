# Oprette og organisere dokumenter og mapper

Fra INDEX-punktmenuen kan du oprette, duplikere, omdøbe og slette dokumenter og mapper. Indtastningen sker i en lille dialog inde i fremviseren, så læsningen ikke afbrydes.

> **Bemærk**
>
> Disse handlinger er kun mulige, når du har tillid til arbejdsområdet i VS Code. De kan ikke udføres, mens et dokument redigeres, mens en anden handling er i gang, eller når målet har ugemte ændringer.

## Oprette et dokument eller en mappe

1. Åbn punktmenuen ([⋯] eller højreklik) for den mappe, der skal indeholde det nye element.
   Hvis du vil oprette direkte under dokumentroden, skal du bruge [⋯] yderst til højre i INDEX-overskriften eller højreklikke på et tomt område i INDEX.
2. Vælg [Nyt dokument] eller [Ny mappe].
3. Indtast et navn, og tryk på [Opret].
   Et dokumentnavn skal have en Markdown-filtype (`.md`, `.markdown`, `.mdx` og lignende).

Nye dokumenter oprettes som dokumenter på standardsproget (originaldokumenter).

## Duplikere et dokument

1. Åbn dokumentets punktmenu, og vælg [Dupliker].
2. Indtast et nyt navn, og tryk på [Opret].

Det er kun originaldokumentet, der duplikeres. Oversættelserne duplikeres ikke.

## Skifte titel

Ændrer dokumentets overskrift (H1). Filnavnet ændres ikke.

1. Åbn punktmenuen for et dokument eller en mappe, og vælg [Skift titel].
2. Indtast den nye titel på én linje, og tryk på [Skift].

For en mappe ændres overskriften i mappens `README.md`. Når det viste sprog er en oversættelse, ændres titlen på dokumentet på dette sprog.

## Skifte dokumentnavn

Ændrer det dokumentnavn, der vises på værktøjslinjen (navnet på dokumentroden).

1. Højreklik på dokumentnavnet på værktøjslinjen. Menuen kan også åbnes fra [⋯] yderst til højre i INDEX-overskriften.
2. Vælg [Skift dokumentnavn], og indtast et nyt navn.

Hvis intet er angivet, vises mappenavnet som det er.

Det navn, du ændrer, skrives til **det sted, der lige nu bruges som dokumentnavn**. Der skrives ikke til et sted, som ikke bruges til visningen, så en overskrift, du kan se, ender aldrig med at blive ignoreret.

| Nuværende tilstand | Skrives til |
|---|---|
| `lunascape-docs.json` indeholder et navn | `lunascape-docs.json` opdateres |
| Der er intet navn, men dokumentroden har en README | README-overskriften (H1) omskrives |
| Ingen af delene | `lunascape-docs.json` oprettes, og navnet gemmes |

Meddelelsen efter ændringen viser, hvilket af stederne der blev skrevet til.

> **Tip**
>
> Dokumentnavnet bestemmes i denne rækkefølge: navnet i `lunascape-docs.json`, derefter overskriften i dokumentrodens README og til sidst mappenavnet.

## Ændre et fil- eller mappenavn

1. Åbn punktmenuen, og vælg [Skift filnavn] eller [Skift mappenavn].
2. Indtast det nye navn, og tryk på [Skift].

De tilsvarende oversættelser (den samme sti under `i18n/<sprog>/`) omdøbes samtidig.

## Slette

1. Åbn punktmenuen, og vælg [Flyt til papirkurv].
2. Kontrollér indholdet af bekræftelsesmeddelelsen, og godkend flytningen.

Elementet flyttes til styresystemets papirkurv, så det kan gendannes, hvis det er nødvendigt. Oversættelserne slettes ikke, men bliver stående.

## Navne, der ikke kan bruges

- Navne, der begynder med `.` (de vises ikke i INDEX)
- `i18n` (reserveret til oversættelsesfiler)
- Navne, der er reserveret i Windows (`CON`, `PRN` og lignende)
- Navne, der slutter med et punktum eller et mellemrum
- Navne med kontroltegn eller tegn, der ikke kan bruges i filnavne
- Navne, der allerede findes i den samme mappe (herunder navne, der kun adskiller sig ved store og små bogstaver)

> **Bemærk**
>
> Startsiden (normalt `README.md` i roden) kan ikke omdøbes eller flyttes. Ændr først `startPage` i `lunascape-docs.json`.

## Relaterede emner

- [Ændre dokumenternes rækkefølge](reorder.md)
- [Bruge INDEX](../02-reading/index-panel.md)
