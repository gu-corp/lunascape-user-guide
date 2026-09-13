# Uw eigen documenten publiceren op het web

U kunt de documenten van uw eigen repository publiceren als website op GitHub Pages of op een willekeurige statische hosting. Dat kan op twee manieren. Deze stappen zijn bedoeld voor ontwikkelaars die de repository van Lunascape Docs kunnen clonen en `npm` kunnen gebruiken.

## Manier 1: de twee viewerbestanden plaatsen

Hierbij plaatst u alleen de viewer zelf (`index.html` en `lsdoc.js`) en laadt deze de documenten vanaf GitHub. De documenten maken geen deel uit van de site, dus dit is ook veilig voor niet-openbare repository's (lezers melden zich aan bij GitHub).

1. Voer in de repository van Lunascape Docs de volgende opdracht uit.

   ```sh
   npm run build:viewer
   ```

   In `dist/viewer/` worden `index.html` en `lsdoc.js` aangemaakt.
2. Plaats de twee bestanden in `docs/` van de repository die u wilt publiceren.
3. Schakel GitHub Pages in.

De documentatiehoofdmap die wordt getoond, wordt in deze volgorde bepaald.

1. De instelling `source` in `index.html`
2. `repository` in een `lunascape-docs.json` in dezelfde map
3. Afleiding uit de `*.github.io`-URL en de indeling van de branches

## Manier 2: een statische site met de documenten exporteren

Hierbij exporteert u de viewer samen met de documentbestanden en host u het resultaat ongewijzigd.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

De uitvoer bevat de viewer, de documenten onder `docs/`, het overzichtsbestand `lunascape-docs-manifest.json` en `.nojekyll`. Plaats de uitvoer op S3 of GitHub Pages om te publiceren. Zie `examples/workflows/publish-docs-pages.yml` in de repository voor een voorbeeld van automatisch publiceren met GitHub Actions.

> **Let op**
>
> - **Exporteer de documenten van een niet-openbare repository nooit naar GitHub Pages.** GitHub Pages is buiten Enterprise Cloud voor iedereen leesbaar. Gebruik manier 1 als u beperkt wilt publiceren, en laat lezers zich aanmelden bij GitHub.
> - `index.html` rechtstreeks openen via `file://` werkt niet, omdat browsers het laden van bestanden ernaast en het uitvoeren van ES-modules op die manier blokkeren. Gebruik de VS Code-versie of een HTTP-server om het lokaal te controleren.
> - De tekenbibliotheken voor TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob en Penrose worden tijdens het weergeven geladen. Plaats bij een geëxporteerde site ook de map `vendor/`.

## Verwante onderwerpen

- [Wat de webversie kan](README.md)
- [Een niet-openbare repository lezen](private-repository.md)
