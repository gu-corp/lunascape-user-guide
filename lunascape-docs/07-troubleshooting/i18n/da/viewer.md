# Dokumenter vises ikke

## »Der blev ikke fundet nogen Markdown- eller docs-mappe, der kan åbnes« vises

- Arbejdsområdet har ingen `docs`-mappe, eller det bruger et andet navn end `docs`.
  - Læg en `lunascape-docs.json` i mappen, så genkendes den som dokumentrod uanset navnet.
  - Eller tilføj mappenavnet til indstillingen `lunascapeDocEditor.rootDirectoryNames`.
- Hvis der endnu ikke er nogen dokumenter, kan du oprette dem med »Lunascape Docs: Opret dokumentation fra skabelon«.
- Du kan også åbne en Markdown-fil i editoren og derefter køre »Lunascape Docs: Åbn i specifikationsfremviser«.

## Et dokument mangler i INDEX

- Kontrollér, at filtypen er `.md`, `.markdown` eller `.mdx`.
- Følgende mapper vises ikke: mapper, der begynder med `.`, `node_modules` og mapper, der er angivet i `ignoredDirectories` (standard er `99-archive`).
- Oversættelser under `i18n/` vises ikke enkeltvis i INDEX. Skift til dem fra sprogmenuen.
- Hvis en fil, du netop har tilføjet, ikke vises, skal du trykke på [Genindlæs].
- Du ser måske en anden dokumentrod. Kontrollér dokumentrodens navn yderst til venstre på værktøjslinjen.

## Der vises intet, når du trykker på en mappe

Mappens `README.md` er en »ren konfigurationsdeskriptor« med kun front matter og ingen brødtekst. Åbn mappen i INDEX, og vælg et dokument inde i den.

## Den forkerte dokumentrod åbnes

- Når indstillingen `lunascapeDocEditor.rootMode` er sat til `fixed`, åbnes altid `lunascapeDocEditor.root`.
- Med `auto` vælges den dokumentrod, der er tættest på den åbnede Markdown-fil. Du kan skifte med rullelisten yderst til venstre på værktøjslinjen.

## Dokumentroden har et uventet navn

Navnet bestemmes i rækkefølgen `title` i `lunascape-docs.json` → `navigation.title` i rod-`README.md` → dens H1 → `index.md` → mappenavnet. Sæt `title` for at fastsætte det.

## INDEX forsvandt

- I en dokumentrod med kun ét dokument lukker INDEX sig selv første gang. Du kan åbne det igen med kolonneikonet på værktøjslinjen. Du kan slå det fra med [Skjul automatisk, hvis der kun er ét dokument] under [Visningsindstillinger].
- På en smal skærm kan du åbne det med [Åbn INDEX] (tre linjer) til venstre for [Tilbage].

## Et link åbnes ikke

- »Linkmålet blev ikke fundet«: målfilen findes ikke. Du kan kontrollere interne links med [Kontrol] i Dokumentværktøjer.
- »Et usikkert eller ikke-understøttet link blev ikke åbnet«: links uden for dokumentroden eller til et andet skema end `https://` og `mailto:` åbnes ikke.

## Det forkerte sprog vises

- Kontrollér den viste sides sprog og begrundelsen i sprogmenuen.
- Det visningssprog, du valgte sidst, huskes. Vælg standardsproget igen i sprogmenuen.
- Hvis den personlige indstilling `lunascapeDocEditor.locale` er sat, foretrækkes oversættelsen på det sprog.

## Relaterede emner

- [Skift dokumentrod](../02-reading/roots.md)
- [Dokumentrødder og filkonventioner](../04-document-tools/structure.md)
