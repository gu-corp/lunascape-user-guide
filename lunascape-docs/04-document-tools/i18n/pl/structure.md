# Katalogi główne dokumentacji i konwencje plików

Reguły, według których Lunascape Docs odnajduje dokumenty i buduje INDEX. Źródłem prawdy jest sam system plików, więc żaden rejestr ani konfiguracja kompilacji nie są potrzebne.

## Katalog główny dokumentacji

- Najbliższy folder `docs` lub folder zawierający plik `lunascape-docs.json` staje się katalogiem głównym dokumentacji.
- Jeśli umieścisz plik `lunascape-docs.json`, folder nie musi nazywać się `docs`.
- Otwarcie pliku Markdown spoza któregokolwiek katalogu głównego dokumentacji powoduje wyświetlenie jego folderu jako tymczasowego katalogu głównego dokumentacji.

## Pliki wyświetlane w INDEX

- Wyświetlane są pliki `.md`, `.markdown` i `.mdx`. Nowe pliki pojawiają się zawsze, nawet bez front matter czy informacji nawigacyjnych.
- Foldery zaczynające się od `.`, `node_modules` oraz foldery wskazane w `ignoredDirectories` (domyślnie `99-archive`) nie są wyświetlane.
- Wszystko, co znajduje się w `i18n/`, jest traktowane jako tłumaczenia i nie jest wymieniane osobno w INDEX.

## Strony tytułowe folderów

- Plik `README.md` (lub `index.md`, gdy nie ma README) z treścią jest stroną tytułową swojego folderu. Naciśnięcie nazwy folderu w INDEX otwiera ją.
- Plik `README.md` złożony wyłącznie z front matter, bez treści, jest „deskryptorem służącym tylko do konfiguracji” i nie jest wyświetlany jako strona. Używaj go, gdy folder potrzebuje jedynie tytułu lub kolejności.
- Gdy istnieją zarówno `README.md`, jak i `index.md`, pierwszeństwo ma `README.md`.

## Język domyślny i tłumaczenia

- Dokumenty w języku domyślnym (dokumenty źródłowe) pozostają na swoim miejscu.
- Tłumaczenie umieszcza się w folderze `i18n/<język>/` obok dokumentu, pod tą samą nazwą pliku. Odtworzenie struktury folderów w `i18n/` nie jest rozpoznawane.
- To jedyne miejsce, z którego tłumaczenie jest rozwiązywane. Ten sam plik umieszczony gdziekolwiek indziej jest plikiem osieroconym, którego żaden dokument nie uznaje za swoje tłumaczenie.

```text
docs/
  lunascape-docs.json
  README.md                  ← strona tytułowa katalogu głównego (strona początkowa)
  i18n/en/README.md          ← jego wersja angielska
  01-product/
    README.md                ← strona tytułowa folderu
    requirements.md
    i18n/en/README.md        ← wersje angielskie dwóch powyższych dokumentów
    i18n/en/requirements.md
  99-archive/                ← domyślnie wykluczone z INDEX
```

## O pliku `_meta.json`

Plik `_meta.json` z Nextry nie jest używany do nawigacji. Istniejące pliki nie są ani modyfikowane, ani usuwane. W przyszłości będzie je obsługiwać wyłącznie jawna funkcja importu/eksportu.

## Powiązane tematy

- [Ustawianie informacji nawigacyjnych](navigation-metadata.md)
- [Konfiguracja projektu](project-configuration.md)
- [Przełączanie katalogów głównych dokumentacji](../02-reading/roots.md)
