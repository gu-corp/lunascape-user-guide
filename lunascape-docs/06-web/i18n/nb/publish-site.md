# Publisere dokumentene dine på Web

Du kan publisere dokumentene i ditt eget repositorium som et nettsted på GitHub Pages eller på hvilken som helst statisk hosting. Det finnes to måter. Denne fremgangsmåten er for utviklere som kan klone Lunascape Docs-repositoriet og bruke `npm`.

## Måte 1: legg ut de to visningsfilene

Du legger bare ut selve visningsprogrammet (`index.html` og `lsdoc.js`) og lar det laste dokumentene fra GitHub. Dokumentene selv inngår ikke i nettstedet, så dette er trygt også for private repositorier (leserne logger på med GitHub).

1. Kjør følgende kommando i Lunascape Docs-repositoriet.

   ```sh
   npm run build:viewer
   ```

   `index.html` og `lsdoc.js` genereres i `dist/viewer/`.
2. Legg de to filene i `docs/` i repositoriet du vil publisere.
3. Aktiver GitHub Pages.

Hvilken dokumentrot som skal vises, bestemmes i denne rekkefølgen.

1. Innstillingen `source` inne i `index.html`
2. `repository` i en `lunascape-docs.json` i samme mappe
3. Utledning fra `*.github.io`-URL-en og grenoppsettet

## Måte 2: skriv ut et statisk nettsted som inkluderer dokumentene

Du skriver ut visningsprogrammet sammen med dokumentfilene og hoster resultatet som det er.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Utdataene inneholder hele visningsprogrammet, dokumentene under `docs/`, oversiktsfilen `lunascape-docs-manifest.json` og `.nojekyll`. Legg utdataene på S3 eller GitHub Pages for å publisere. Se `examples/workflows/publish-docs-pages.yml` i repositoriet for et eksempel med GitHub Actions.

> **Merk**
>
> - **Ikke skriv ut dokumentene fra et privat repositorium og legg dem på GitHub Pages.** GitHub Pages utenfor Enterprise Cloud kan leses av hvem som helst. Hvis du trenger begrenset publisering, bruk måte 1 og la leserne logge på med GitHub.
> - Å åpne `index.html` direkte via `file://` fungerer ikke, fordi nettleseren hindrer innlasting av nabofiler og kjøring av ES-moduler på den måten. Når du vil kontrollere lokalt, bruk VS Code-versjonen eller en HTTP-server.
> - Tegnebibliotekene for TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob og Penrose lastes inn ved visning. På det utskrevne nettstedet må du også legge ut `vendor/`-mappen.

## Relaterte emner

- [Hva Web-versjonen kan gjøre](README.md)
- [Lese et privat repositorium](private-repository.md)
