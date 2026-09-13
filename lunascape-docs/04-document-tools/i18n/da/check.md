# Kontrollér dokumenter

Med docs-lint kan du kontrollere overskrifternes opbygning, døde links, manglende påkrævede dokumenter og kapitler, uensartet terminologi, sammenhængen mellem krav-id'er med mere. En kontrol omfatter altid hele dokumentroden.

## Kør en kontrol

1. Tryk på [Dokumentværktøjer] på værktøjslinjen, og åbn fanen [Kontrol].
2. Tryk på [Kontrollér dokumentroden].
   Du kan også køre "Lunascape Docs: Kontrollér dokumentroden" fra kommandopaletten.
3. Gennemgå listen med resultater.

## Læs resultaterne

- Med [Dette dokument] / [Alle] over listen skifter du mellem det viste omfang. Selve kontrollens omfang er altid hele dokumentroden.
- Bemærkningerne har fire niveauer: "fejl", "advarsel", "information" og "forslag". [Dokumentværktøjer] på værktøjslinjen viser antallet af fejl og advarsler.
- Tryk på en bemærkning for at åbne det tilsvarende sted i Markdown-kilden i VS Code-editoren.
- Bemærkninger, der vedrører hele dokumentroden (f.eks. et manglende testdokument), vises som punkter under "Hele dokumentroden" og har ingen placering.
- De samme bemærkninger vises også i panelet "Problemer" i VS Code.

## Det, der kontrolleres

Tryk på [Gennemgå og ændr reglerne] for at se listen over aktive kontroller og formålet med hver enkelt. De vigtigste punkter er:

| Punkt | Indhold |
|---|---|
| Overskrifternes opbygning | Om der er præcis én H1, og om overskriftsniveauerne springer over et trin |
| Interne links | Om de dokumenter, der linkes til, findes og bliver inden for dokumentroden |
| Kodeblokkenes sprog | Om kodeblokkene angiver et sprognavn |
| Påkrævede mapper og dokumenter | Om de mapper og dokumenter, profilen i Standard Pack kræver, findes |
| Påkrævede kapitler i dokumentet | Om hver dokumenttype har de kapitler, den kræver |
| Ensartet terminologi | Finder udtryk, der bør undgås, og foreslår de anbefalede termer |
| Navngivning og gentagelse af krav-id'er | Om krav-id'erne følger navngivningsreglen og ikke er defineret to gange |
| Sammenhæng i henvisninger til krav-id'er | Om de krav-id'er, som design, test og statusoversigter henviser til, findes |
| Sammenhæng mellem krav og test | Om krav-id'erne er nævnt i testdokumenterne |

Hvilke punkter der er aktive, afgøres af den Standard Pack og den profil, du har valgt i `lunascape-docs.json`, samt af `docs-lint.config.json`.

> **Bemærk**
>
> - Når du ændrer et dokument eller en indstilling, bliver det forrige resultat til "kræver ny kontrol". Intet godkendes automatisk. Tryk på [Kontrollér dokumentroden] igen.
> - Ikke-gemte ændringer indgår ikke i kontrollen. Gem først.
> - Kontrollen køres lokalt på maskinen og giver altid samme resultat. Vurderinger fra AI og resultater af oversættelser blandes aldrig ind i kontrollens resultater.

## Relaterede emner

- [Ændr kontrolreglerne](rules.md)
- [Projektindstillinger](project-configuration.md)
- [Kontrol, oprettelse eller oversættelse virker ikke](../07-troubleshooting/tools.md)
