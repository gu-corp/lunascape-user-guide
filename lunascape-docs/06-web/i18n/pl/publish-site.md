# Publikowanie własnych dokumentów w sieci

Dokumenty z własnego repozytorium można opublikować jako witrynę w GitHub Pages lub na dowolnym hostingu statycznym. Są na to dwa sposoby. Ta procedura jest przeznaczona dla programistów, którzy mogą sklonować repozytorium Lunascape Docs i korzystać z `npm`.

## Sposób 1: umieszczenie dwóch plików przeglądarki

Wdrażasz tylko samą przeglądarkę (`index.html` i `lsdoc.js`), a dokumenty są wczytywane z GitHub. Same dokumenty nie stanowią części witryny, więc jest to bezpieczne również w przypadku repozytoriów prywatnych (czytelnicy logują się w GitHub).

1. W repozytorium Lunascape Docs wykonaj następujące polecenie.

   ```sh
   npm run build:viewer
   ```

   W katalogu `dist/viewer/` zostaną wygenerowane pliki `index.html` i `lsdoc.js`.
2. Umieść te dwa pliki w folderze `docs/` repozytorium, które chcesz opublikować.
3. Włącz GitHub Pages.

Wyświetlany katalog główny dokumentacji jest ustalany w następującej kolejności.

1. Ustawienie `source` w pliku `index.html`
2. Wartość `repository` zapisana w pliku `lunascape-docs.json` w tym samym folderze
3. Wnioskowanie na podstawie adresu URL `*.github.io` i układu gałęzi

## Sposób 2: wyeksportowanie witryny statycznej wraz z dokumentami

Eksportujesz przeglądarkę razem z plikami dokumentów i hostujesz wynik bez zmian.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

Na wyjściu powstaje komplet plików przeglądarki, dokumenty z folderu `docs/`, plik listy `lunascape-docs-manifest.json` oraz `.nojekyll`. Aby opublikować witrynę, umieść katalog wyjściowy w S3 lub w GitHub Pages. Przykład automatycznej publikacji za pomocą GitHub Actions znajdziesz w pliku `examples/workflows/publish-docs-pages.yml` w repozytorium.

> **Uwaga**
>
> - **Nie eksportuj dokumentów z prywatnego repozytorium do GitHub Pages.** Poza Enterprise Cloud strony GitHub Pages może przeglądać każdy. Jeśli potrzebujesz publikacji o ograniczonym dostępie, skorzystaj ze sposobu 1 i pozwól czytelnikom zalogować się w GitHub.
> - Otwarcie pliku `index.html` bezpośrednio przez `file://` nie zadziała, ponieważ przeglądarki blokują wczytywanie sąsiednich plików i uruchamianie modułów ES w ten sposób. Aby sprawdzić wynik lokalnie, użyj wersji dla VS Code lub serwera HTTP.
> - Biblioteki renderujące dla TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob i Penrose są wczytywane w chwili wyświetlania. W wyeksportowanej witrynie umieść również folder `vendor/`.

## Tematy pokrewne

- [Możliwości wersji internetowej](README.md)
- [Przeglądanie prywatnego repozytorium](private-repository.md)
