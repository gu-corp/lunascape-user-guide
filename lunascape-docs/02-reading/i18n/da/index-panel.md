# Sådan bruger du INDEX

INDEX i venstre side er træet over mapper og dokumenter i dokumentroden.

## Filtrér

1. Skriv et ord i [Filtrér dokumenter] over INDEX.
2. Kun de emner, hvis dokumentnavn passer, vises. Ryd feltet for at vende tilbage.

> **Bemærk**
>
> Mens filtreringen er aktiv, kan du ikke ændre rækkefølgen ved at trække og slippe.

## Åbn og luk mapper

- Tryk på pilen til venstre for et mappenavn, eller på navnet på en mappe uden forside, for at åbne eller lukke den.
- En mappe med en forside (en `README.md` eller `index.md` med brødtekst) åbner forsiden, når du trykker på navnet. Brug [Åbn mappe] / [Luk mappe] i emnemenuen, hvis du kun vil åbne eller lukke.
- Mappernes åbne- og lukkestatus huskes for hver bruger og skrives aldrig til filer under Git.

## README og mappens forside

`README.md` er den fil, der beskriver indholdet af mappen.

- Trykker du på navnet på en mappe med en README, vises den README.
- En mappe uden README viser i stedet det øverste dokument i mappen.
- README'ens overskrift (H1) bliver mappens navn i INDEX.

En README er ikke påkrævet. Vil du tilføje en senere, skal du vælge [Opret README] i mappens emnemenu (den vises kun for mapper uden README).

## Vis eller skjul INDEX

- Med det venstre ikon i værktøjslinjens kolonnevisning viser eller skjuler du INDEX. Det højre ikon viser eller skjuler "På denne side".
- På smalle skærme starter INDEX i lukket tilstand. Tryk på [Åbn INDEX] (de tre streger) til venstre for [Tilbage], hvorefter INDEX åbner oven på brødteksten. Luk med [×] inde i INDEX, med et klik på baggrunden, med `Esc` eller ved at skifte dokument. Denne midlertidige tilstand ændrer ikke indstillingen på brede skærme.
- I en dokumentrod med kun ét dokument at vise lukker INDEX automatisk første gang. Du kan åbne den igen med kolonneikonet. Slå det fra med [Skjul automatisk, hvis der kun er ét dokument] under [Visningsindstillinger].

## Brug emnemenuen

Før musen hen over et emne i INDEX for at få vist [⋯], eller højreklik på emnet, for at åbne dets menu. Emnerne står i denne rækkefølge.

| Gruppe | Emner |
|---|---|
| Hyppige handlinger | [Åbn mappe] / [Luk mappe], [Åbn INDEX] (åbner mappens forside), [Rediger], [Skift titel], [Åbn i VS Code], [Kopiér stien] |
| Opret og organisér | [Opret README] (kun mapper uden README), [Nyt dokument], [Ny mappe], [Dupliker], [Skift filnavn] / [Skift mappenavn], [Flyt en op], [Flyt en ned] |
| Slet | [Flyt til papirkurv] |

- Vil du oprette noget direkte under dokumentroden, skal du bruge [⋯] yderst til højre i INDEX-overskriften eller højreklikke på et tomt område i INDEX og derefter vælge [Nyt dokument] eller [Ny mappe]. I samme menu står [Skift dokumentnavn] og, hvis dokumentroden ikke har en README, [Opret README]. Højreklikker du på dokumentnavnet i værktøjslinjen, åbnes den samme menu.
- I menuen flytter du dig med `↑` `↓`, og med `Home` `End` springer du til første og sidste emne. Lukker du med `Esc`, vender fokus tilbage til det sted, menuen blev åbnet fra.

> **Bemærk**
>
> Emnerne til at oprette, organisere og slette vises kun, når du har tillid til arbejdsområdet i VS Code. De er heller ikke tilgængelige, mens et dokument redigeres, eller mens en anden INDEX-handling behandles.

## Skift udseendet

Under [Visningsindstillinger] kan du ændre visningen af filnavne, ikoner for dokumenter og mapper, antallet af emner i mapperne, hjælpelinjerne for niveauerne og visningstætheden. Se [Sådan ændrer du visningsindstillinger](display-settings.md) for detaljer.

## Relaterede emner

- [Sådan opretter og organiserer du dokumenter og mapper](../03-editing/organize.md)
- [Sådan ændrer du dokumenternes rækkefølge](../03-editing/reorder.md)
