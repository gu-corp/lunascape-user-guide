# Publicarea documentelor dumneavoastră pe Web

Puteți publica documentele din depozitul dumneavoastră ca site web, pe GitHub Pages sau pe orice găzduire statică. Există două metode. Acești pași se adresează dezvoltatorilor care pot clona depozitul Lunascape Docs și pot folosi `npm`.

## Metoda 1: amplasarea celor două fișiere ale vizualizatorului

Publicați numai vizualizatorul (`index.html` și `lsdoc.js`), iar documentele sunt încărcate din GitHub. Documentele nu fac parte din site, așa că metoda este sigură și pentru depozitele private (cititorii se conectează cu GitHub).

1. Rulați următoarea comandă în depozitul Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   În `dist/viewer/` sunt generate `index.html` și `lsdoc.js`.
2. Puneți cele două fișiere în folderul `docs/` al depozitului pe care vreți să îl publicați.
3. Activați GitHub Pages.

Rădăcina documentației afișată se stabilește în această ordine.

1. Setarea `source` din `index.html`
2. `repository` dintr-un fișier `lunascape-docs.json` aflat în același folder
3. Deducerea din adresa URL `*.github.io` și din structura ramurilor

## Metoda 2: exportarea unui site static care include documentele

Exportați vizualizatorul împreună cu fișierele documentelor și găzduiți rezultatul ca atare.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Rezultatul conține vizualizatorul complet, documentele din `docs/`, fișierul de listă `lunascape-docs-manifest.json` și `.nojekyll`. Amplasați rezultatul pe S3 sau pe GitHub Pages pentru a-l publica. Pentru un exemplu de publicare automată cu GitHub Actions, consultați `examples/workflows/publish-docs-pages.yml` din depozit.

> **Notă**
>
> - **Nu exportați documentele unui depozit privat pe GitHub Pages.** În afara Enterprise Cloud, GitHub Pages poate fi citit de oricine. Dacă aveți nevoie de publicare restrânsă, folosiți metoda 1 și lăsați cititorii să se conecteze cu GitHub.
> - Deschiderea directă a fișierului `index.html` prin `file://` nu funcționează, deoarece browserul interzice încărcarea fișierelor alăturate și executarea modulelor ES. Pentru verificări locale, folosiți versiunea pentru VS Code sau un server HTTP.
> - Bibliotecile de desenare pentru TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob și Penrose se încarcă la afișare. Pe site-ul exportat, amplasați și folderul `vendor/`.

## Subiecte înrudite

- [Ce puteți face în versiunea Web](README.md)
- [Consultarea unui depozit privat](private-repository.md)
