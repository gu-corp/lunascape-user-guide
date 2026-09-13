# Publicera dina dokument på webben

Du kan publicera dokumenten i din egen lagringsplats som en webbplats på GitHub Pages eller valfri statisk webbhotellstjänst. Det finns två sätt. De här stegen riktar sig till utvecklare som kan klona lagringsplatsen för Lunascape Docs och använda `npm`.

## Sätt 1: placera visningsprogrammets två filer

Här placerar du bara själva visningsprogrammet (`index.html` och `lsdoc.js`) och låter dokumenten läsas in från GitHub. Dokumenten ingår inte i webbplatsen, så det är säkert även för privata lagringsplatser (läsarna loggar in med GitHub).

1. Kör följande kommando i lagringsplatsen för Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   `index.html` och `lsdoc.js` skapas i `dist/viewer/`.
2. Lägg de två filerna i `docs/` i den lagringsplats du vill publicera.
3. Aktivera GitHub Pages.

Vilken dokumentrot som visas avgörs i följande ordning.

1. Inställningen `source` i `index.html`
2. `repository` i filen `lunascape-docs.json` i samma mapp
3. Härledning från `*.github.io`-adressen och grenstrukturen

## Sätt 2: exportera en statisk webbplats med dokumenten

Här exporterar du visningsprogrammet tillsammans med dokumentfilerna och publicerar resultatet som det är.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Utdata innehåller hela visningsprogrammet, dokumenten under `docs/`, listfilen `lunascape-docs-manifest.json` och `.nojekyll`. Placera utdatamappen på S3 eller GitHub Pages för att publicera den. Ett exempel på automatisk publicering med GitHub Actions finns i `examples/workflows/publish-docs-pages.yml` i lagringsplatsen.

> **Obs!**
>
> - **Exportera aldrig dokument från en privat lagringsplats till GitHub Pages.** GitHub Pages utanför Enterprise Cloud kan läsas av vem som helst. Om publiceringen måste vara begränsad använder du sätt 1 och låter läsarna logga in med GitHub.
> - Att öppna `index.html` direkt med `file://` fungerar inte, eftersom webbläsaren då blockerar inläsning av intilliggande filer och körning av ES-moduler. Använd VS Code-versionen eller en HTTP-server när du vill kontrollera resultatet lokalt.
> - Ritbiblioteken för TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob och Penrose läses in vid visningen. Placera även mappen `vendor/` tillsammans med den exporterade webbplatsen.

## Relaterade avsnitt

- [Det här kan du göra i webbversionen](README.md)
- [Läsa en privat lagringsplats](private-repository.md)
