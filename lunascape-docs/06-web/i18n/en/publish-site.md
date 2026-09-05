# Publishing your documents on the Web

You can publish the documents of your own repository as a website on GitHub Pages or any static hosting. There are two ways. These steps are for developers who can clone the Lunascape Docs repository and use `npm`.

## Option 1: place the two viewer files

Deploy only the viewer (`index.html` and `lsdoc.js`) and let it load the documents from GitHub. The documents themselves are not part of the site, so this is safe for private repositories (readers sign in with GitHub).

1. Run the following in the Lunascape Docs repository.

   ```sh
   npm run build:viewer
   ```

   `index.html` and `lsdoc.js` are generated in `dist/viewer/`.
2. Put the two files into `docs/` of the repository you want to publish.
3. Enable GitHub Pages.

The documentation root to show is resolved in this order.

1. The `source` setting inside `index.html`
2. `repository` in a `lunascape-docs.json` in the same folder
3. Inference from the `*.github.io` URL and the branch layout

## Option 2: export a static site including the documents

Export the viewer together with the document files and host the result as is.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

The output contains the viewer, the documents under `docs/`, the manifest `lunascape-docs-manifest.json` and `.nojekyll`. Put it on S3 or GitHub Pages to publish. See `examples/workflows/publish-docs-pages.yml` in the repository for a GitHub Actions example.

> **Note**
>
> - **Never export the documents of a private repository to GitHub Pages.** GitHub Pages outside Enterprise Cloud is readable by everyone. For restricted publishing, use option 1 and let readers sign in with GitHub.
> - Opening `index.html` directly via `file://` does not work, because browsers block loading neighboring files and running ES modules that way. To check locally, use the VS Code extension or an HTTP server.
> - The rendering libraries for TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob and Penrose are loaded on demand. Deploy the `vendor/` folder together with an exported site.

## Related topics

- [What the Web viewer does](README.md)
- [Reading a private repository](private-repository.md)
