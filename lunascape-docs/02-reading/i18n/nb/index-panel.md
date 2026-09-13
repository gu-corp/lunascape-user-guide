# Bruke INDEX

INDEX til venstre på skjermen er treet med mapper og dokumenter i dokumentroten.

## Filtrere

1. Skriv inn et ord i [Filtrer dokumenter] over INDEX.
2. Bare oppføringer med dokumentnavn som stemmer, vises. Tøm feltet for å vise alt igjen.

> **Merk**
>
> Under filtrering kan du ikke endre rekkefølgen ved å dra og slippe.

## Åpne og lukke mapper

- Trykk på pilen til venstre for et mappenavn, eller på navnet til en mappe uten forside, for å åpne eller lukke den.
- En mappe med en forside (en `README.md` eller `index.md` med brødtekst) åpner forsiden når du trykker på navnet. For bare å åpne eller lukke bruker du [Åpne mappen] / [Lukk mappen] i oppføringsmenyen.
- Åpne/lukke-tilstanden huskes per bruker og skrives aldri til Git-sporede filer.

## README og mappens forside

`README.md` er filen som beskriver hva mappen inneholder.

- Trykker du på navnet til en mappe som har en README, vises den README-en.
- En mappe uten README viser i stedet det øverste dokumentet inni den.
- README-ens overskrift (H1) blir mappens navn i INDEX.

En README er ikke påkrevd. For å legge til en senere velger du [Opprett en README] i mappens oppføringsmeny (den vises bare for mapper som ikke har noen).

## Vise eller skjule INDEX

- Ikonet til venstre i verktøylinjens kolonnekontroller viser eller skjuler INDEX. Ikonet til høyre viser eller skjuler «På denne siden».
- På smale skjermer starter INDEX lukket. Trykk på [Åpne INDEX] (tre streker) til venstre for [Tilbake] for å åpne den som et overlegg over dokumentet. Lukk den med [×] inne i INDEX, et klikk på bakgrunnen, `Esc`, eller ved å navigere til et annet dokument. Denne midlertidige tilstanden endrer ikke innstillingen for brede skjermer.
- I en dokumentrot med bare ett dokument lukker INDEX seg selv én gang ved første åpning. Åpne den igjen med kolonneikonet. Du kan slå av dette med [Skjul når det bare finnes ett dokument] i [Visningsinnstillinger].

## Bruke oppføringsmenyen

Hold musepekeren over en INDEX-oppføring for å vise [⋯], eller høyreklikk oppføringen, for å åpne menyen. Oppføringene vises i denne rekkefølgen.

| Gruppe | Oppføringer |
|---|---|
| Vanlige handlinger | [Åpne mappen] / [Lukk mappen], [Åpne INDEX] (åpner mappens forside), [Rediger], [Endre tittelen], [Åpne i VS Code], [Kopier banen] |
| Opprette og organisere | [Opprett en README] (bare mapper uten en), [Nytt dokument], [Ny mappe], [Dupliser], [Endre filnavnet] / [Endre mappenavnet], [Flytt opp], [Flytt ned] |
| Slette | [Flytt til papirkurven] |

- For å opprette noe direkte under dokumentroten trykker du på [⋯] ytterst til høyre i INDEX-overskriften, eller høyreklikker et tomt område i INDEX, og velger [Nytt dokument] eller [Ny mappe]. I samme meny finner du [Endre dokumentnavnet], og hvis dokumentroten ikke har en README, [Opprett en README]. Du kan også høyreklikke dokumentnavnet som vises i verktøylinjen for å åpne den samme menyen.
- Inne i en meny flytter `↑` `↓` mellom oppføringer, og `Home` `End` hopper til første og siste. Lukker du med `Esc`, går fokus tilbake dit menyen ble åpnet.

> **Merk**
>
> Oppføringene for å opprette, organisere og slette vises bare når arbeidsområdet er klarert i VS Code. De er også utilgjengelige mens et dokument redigeres eller en annen INDEX-operasjon behandles.

## Endre utseendet

Fra [Visningsinnstillinger] kan du endre visning av filnavn, ikoner for dokumenter og mapper, antall i mapper, hierarkiets veiledningslinjer og visningstettheten. Se [Endre visningsinnstillinger](display-settings.md) for mer.

## Se også

- [Opprette og organisere dokumenter og mapper](../03-editing/organize.md)
- [Endre rekkefølgen på dokumentene](../03-editing/reorder.md)
