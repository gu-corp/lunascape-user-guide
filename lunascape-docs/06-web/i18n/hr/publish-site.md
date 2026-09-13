# Objavljivanje vlastitih dokumenata na webu

Dokumente iz vlastitog repozitorija možete objaviti kao web-mjesto na platformi GitHub Pages ili na bilo kojem statičkom hostingu. Postoje dva načina. Ovi koraci namijenjeni su razvojnim programerima koji mogu klonirati repozitorij Lunascape Docs i koristiti `npm`.

## Način 1: postavljanje dviju datoteka preglednika

Postavlja se samo preglednik (`index.html` i `lsdoc.js`), a dokumenti se učitavaju s GitHuba. Sami dokumenti nisu dio web-mjesta, pa je ovo sigurno i za privatne repozitorije (čitatelji se prijavljuju putem GitHuba).

1. U repozitoriju Lunascape Docs pokrenite sljedeću naredbu.

   ```sh
   npm run build:viewer
   ```

   U mapi `dist/viewer/` stvaraju se datoteke `index.html` i `lsdoc.js`.
2. Obje datoteke stavite u mapu `docs/` repozitorija koji želite objaviti.
3. Omogućite GitHub Pages.

Korijen dokumentacije koji će se prikazati određuje se ovim redoslijedom.

1. Postavka `source` unutar datoteke `index.html`
2. Vrijednost `repository` u datoteci `lunascape-docs.json` u istoj mapi
3. Zaključivanje na temelju URL-a `*.github.io` i rasporeda grana

## Način 2: izvoz statičkog web-mjesta s dokumentima

Preglednik i datoteke dokumenata izvoze se zajedno i takvi se postavljaju na hosting.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Izlaz sadrži preglednik, dokumente iz mape `docs/`, datoteku popisa `lunascape-docs-manifest.json` i `.nojekyll`. Postavite ga na S3 ili GitHub Pages da biste ga objavili. Primjer automatske objave putem GitHub Actions potražite u datoteci `examples/workflows/publish-docs-pages.yml` u repozitoriju.

> **Napomena**
>
> - **Nemojte izvoziti dokumente iz privatnog repozitorija i postavljati ih na GitHub Pages.** GitHub Pages izvan platforme Enterprise Cloud može čitati svatko. Ako je potrebna ograničena objava, upotrijebite način 1 i neka se čitatelji prijave putem GitHuba.
> - Otvaranje datoteke `index.html` izravno putem `file://` ne funkcionira jer preglednici na taj način onemogućuju učitavanje susjednih datoteka i izvođenje ES modula. Za provjeru na vlastitom računalu upotrijebite verziju za VS Code ili HTTP poslužitelj.
> - Biblioteke za iscrtavanje za TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob i Penrose učitavaju se pri prikazu. Uz izvezeno web-mjesto postavite i mapu `vendor/`.

## Povezane teme

- [Što možete raditi u web-verziji](README.md)
- [Pregledavanje privatnog repozitorija](private-repository.md)
