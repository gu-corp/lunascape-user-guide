# Kan ikke redigere, gemme eller ændre rækkefølge

## [Rediger]-knappen mangler

- [Redigeringsknappen] under [Visningsindstillinger] er slået fra. Slå den til, eller brug [⋯] → [Rediger] øverst til højre i dokumentet, eller [Rediger] i INDEX-punktets menu.
- Det samme gælder, når `editor.showEditButton` i `lunascape-docs.json` er `false`.
- Redigering er ikke mulig, mens hjælpen vises. Luk hjælpen.

## Kan ikke skifte til visuel visning

»Dette dokument indeholder MDX-syntaks og kan derfor ikke skiftes til den almindelige redigeringsvisning«: dokumenter med MDX-specifik syntaks (komponenter, `import` osv.) redigeres kun i Markdown-visningen for at bevare syntaksen.

## Kan ikke redigere matematik eller diagrammer direkte

Den visuelle visning viser det gengivne resultat. Tryk på [Markdown] i redigeringsvisningen, og rediger kilden.

## Kan ikke ændre rækkefølge eller trække

- Det er ikke muligt at ændre rækkefølgen, mens du filtrerer, mens et dokument redigeres, eller mens en anden INDEX-handling er i gang.
- Når du ikke har tillid til arbejdsområdet, er handlingerne opret, organiser og slet ikke tilgængelige. Hav tillid til arbejdsområdet i VS Code.
- »INDEX er blevet opdateret. Træk igen«: en anden ændring blev netop anvendt. Gentag handlingen.
- Startsiden (rodens `README.md`) kan ikke flyttes.

## »Der er ikke-gemte ændringer« vises

Målfilen redigeres i VS Code-editoren. Gem eller kassér ændringerne først, og prøv derefter igen.

## Kan ikke omdøbe

Følgende navne kan ikke bruges.

- Navne, der begynder med `.`, `i18n` og Windows-reserverede navne (`CON` osv.)
- Navne, der slutter med et punktum eller et mellemrum, og navne, der indeholder kontroltegn eller tegn, der ikke er tilladt i filnavne
- Navne, der allerede findes i samme mappe (herunder navne, der kun adskiller sig i store og små bogstaver)
- Dokumentnavne uden en Markdown-filtype

## Gemte ændringer vises ikke i Git eller bliver ikke committet

Lunascape Docs skriver kun filen. Den stager eller committer aldrig i Git. Kontrollér visningen Kildestyring i VS Code, og commit efter behov.

## Relaterede emner

- [Rediger et dokument](../03-editing/README.md)
- [Opret og organiser dokumenter og mapper](../03-editing/organize.md)
- [Skift rækkefølgen på dokumenter](../03-editing/reorder.md)
