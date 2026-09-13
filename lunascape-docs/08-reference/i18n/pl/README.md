# Główne specyfikacje

## Wymagania

| Środowisko | Wymagania |
|---|---|
| Rozszerzenie VS Code | VS Code 1.90 lub nowszy. Funkcje zapisujące pliki działają w zaufanym obszarze roboczym |
| Przeglądarka internetowa | Nowsze wersje Chrome, Edge, Safari i Firefox. Przeglądanie folderu lokalnego wymaga przeglądarki obsługującej wybór folderu (File System Access API) |
| Rozszerzenie Chromium | Manifest V3. Uprawnienia do hostów nie są wymagane |

## Obsługiwane dokumenty

| Pozycja | Szczegóły |
|---|---|
| Pliki | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabele, listy zadań, bloki kodu, przekreślenie), obrazy lokalne, YAML front matter |
| MDX | Wyświetlane są wyłącznie dozwolone komponenty. Dowolne skrypty nie są wykonywane |
| HTML | Wyświetlany po oczyszczeniu przez DOMPurify 3.4.14 |

## Diagramy i wzory matematyczne

| Rodzaj | Nazwa języka | Uwagi |
|---|---|---|
| Wzory matematyczne | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Tylko dane osadzone. Zewnętrzne adresy URL i znaczniki obrazów są niedozwolone |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Tylko ścisły JSON |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | W wersji dystrybucyjnej źródło jest wyświetlane w formie zwiniętej. Limity: 64 KiB danych wejściowych, 15 sekund, 2 MiB SVG |
| Penrose (eksperymentalnie) | `penrose` | Tylko ustawienie wstępne `set-theory` |

## Limity

| Pozycja | Wartość |
|---|---|
| Wynik rozwinięcia szablonu | 4 MiB |
| Kontekst odniesienia tłumaczenia | Domyślnie 49 152 znaki, maksymalnie 1 048 576 znaków |
| Liczba dokumentów w jednym tłumaczeniu zbiorczym | 1000 dokumentów |
| Dowolna szerokość obrazu | 16–4096 px |

## Pliki

| Plik | Rola | W Git |
|---|---|---|
| `lunascape-docs.json` | Ustawienia katalogu głównego dokumentacji | Tak |
| `docs-lint.config.json` | Ustawienia reguł sprawdzania | Tak |
| `.lunascape-docs/translation-freshness.json` | Zapis aktualności tłumaczeń (wyłącznie ścieżki, języki, skróty i znaczniki czasu) | Tak |
| Ustawienia VS Code i stan obszaru roboczego | Osobiste ustawienia widoku, wybór dostawcy, stan rozwinięcia panelu INDEX | Nie |

## Dołączony Standard Pack

`builtin:gu-corp-software` — profile: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Powiązane tematy

- [Lista ustawień VS Code](settings.md)
- [Bezpieczeństwo i granice zapisu](security.md)
