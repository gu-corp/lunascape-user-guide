# Udgiv dine dokumenter på nettet

Du kan udgive dokumenterne i dit eget lager som et websted på GitHub Pages eller enhver anden statisk hosting. Der er to måder. Disse trin er beregnet til udviklere, der kan clone Lunascape Docs-lageret og bruge `npm`.

## Metode 1: placer de to viewer-filer

Placer kun selve viewer'en (`index.html` og `lsdoc.js`), og lad dokumenterne blive indlæst fra GitHub. Dokumenterne selv indgår ikke i webstedet, så dette er sikkert selv for private lagre (læserne logger ind med GitHub).

1. Kør følgende kommando i Lunascape Docs-lageret.

   ```sh
   npm run build:viewer
   ```

   `index.html` og `lsdoc.js` genereres i `dist/viewer/`.
2. Læg de to filer i `docs/` i det lager, du vil udgive.
3. Aktivér GitHub Pages.

Hvilken dokumentrod der vises, afgøres i denne rækkefølge.

1. Indstillingen `source` inde i `index.html`
2. `repository` i en `lunascape-docs.json` i samme mappe
3. Udledning ud fra `*.github.io`-URL'en og forgreningsopsætningen

## Metode 2: eksporter et statisk websted, der indeholder dokumenterne

Eksporter viewer'en sammen med dokumentfilerne, og host resultatet, som det er.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Outputtet indeholder viewer'en, dokumenterne under `docs/`, oversigtsfilen `lunascape-docs-manifest.json` og `.nojekyll`. Placer det på S3 eller GitHub Pages for at udgive det. Se `examples/workflows/publish-docs-pages.yml` i lageret for et eksempel med GitHub Actions.

> **Bemærk**
>
> - **Eksporter aldrig dokumenter fra et privat lager til GitHub Pages.** GitHub Pages uden for Enterprise Cloud kan læses af alle. Hvis du har brug for begrænset udgivelse, så brug metode 1 og lad læserne logge ind med GitHub.
> - At åbne `index.html` direkte via `file://` virker ikke, fordi browsere på den måde blokerer for indlæsning af nabofiler og kørsel af ES-moduler. Brug VS Code-udgaven eller en HTTP-server, når du vil kontrollere det lokalt.
> - Tegnebibliotekerne til TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob og Penrose indlæses ved visning. På et eksporteret websted skal du også placere `vendor/`-mappen sammen med det øvrige.

## Relaterede emner

- [Hvad Web-udgaven kan](README.md)
- [Læs et privat lager](private-repository.md)
