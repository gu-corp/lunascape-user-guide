# Czytanie w innym języku

Jeśli dokument ma tłumaczenia, możesz przełączać języki z menu języków (globus) na pasku narzędzi.

## Przełączanie języka

1. Naciśnij menu języków na pasku narzędzi.
   Wyświetla ono język bieżącej strony oraz sposób jego ustalenia (ścieżka tłumaczenia, automatyczne wykrywanie lub język domyślny projektu).
2. Wybierz język, w którym chcesz czytać.
   Otworzy się tłumaczenie tego samego dokumentu. Wybrany język jest zapamiętywany, a kolejny otwierany dokument zostanie wyświetlony w tym języku, jeśli istnieje jego tłumaczenie.

Lista języków pokazuje, czy dany język ma tłumaczenie tego dokumentu.

| Etykieta | Znaczenie |
|---|---|
| Przetłumaczono | Tłumaczenie istnieje i można je otworzyć |
| Brak tłumaczenia | Język jest obsługiwany przez projekt, ale ten dokument nie ma jeszcze tłumaczenia |
| Nieaktualne | Tłumaczenie istnieje, ale dokument źródłowy zmienił się po jego przetłumaczeniu |

> **Uwaga**
>
> - Wybranie języka tylko otwiera istniejące tłumaczenie. Nigdy nie generuje tłumaczenia ani nie tworzy pliku. Aby utworzyć tłumaczenie, użyj opcji [Utwórz tłumaczenia lub zarządzaj nimi…] w tym samym menu.
> - Gdy zostanie wykryte, że język bieżącej strony różni się od języka domyślnego projektu, pojawia się ostrzeżenie. Ustawienia nie są nigdy zmieniane.

## Język, w którym otwiera się dokument

Gdy otwierasz dokument, pierwszy język wyświetlania jest ustalany w następującej kolejności.

1. Język wybrany wcześniej samodzielnie w tym katalogu głównym dokumentacji. Twój wybór jest zapisywany (wybranie języka domyślnego również jest zapisywane jako wybór).
2. Język interfejsu VS Code (w wersji przeglądarkowej — ustawienia języka przeglądarki). Automatycznie wybierany jest pasujący obsługiwany język; język z oznaczeniem regionu (np. `en-US`) pasuje także do swojego języka podstawowego (`en`).
3. Język zapasowy projektu (`fallbackLocale` w pliku `lunascape-docs.json`).
4. Język domyślny projektu.

> **Wskazówka**
>
> - Gdy język został wybrany automatycznie, przy bieżącym języku w menu języków pojawia się oznaczenie „wybór automatyczny”. Najedź na nie wskaźnikiem, aby zobaczyć przyczynę.
> - `fallbackLocale` to język pokazywany czytelnikom, których język środowiska nie pasuje do żadnego z obsługiwanych języków. W projekcie, którego dokumentem źródłowym jest język japoński i który ma wersję angielską, ustawienie `"en"` sprawia, że czytelnikowi w środowisku np. hiszpańskojęzycznym otwiera się wersja angielska. Gdy nie jest ustawiony, używany jest język domyślny.

## Gdzie znajdują się tłumaczenia

Dokumenty w języku domyślnym pozostają na swoim miejscu, a tłumaczenie umieszcza się w **folderze `i18n/<język>/` obok dokumentu**, pod tą samą nazwą pliku.

```text
docs/
  README.md                  ← język domyślny (na przykład japoński)
  i18n/en/README.md          ← jego tłumaczenie angielskie
  guide/
    setup.md
    i18n/en/setup.md         ← jego tłumaczenie angielskie
```

> **Uwaga**
>
> - Odtworzenie struktury folderów pod `i18n/` (`i18n/en/guide/setup.md`) nie jest rozpoznawane. Folder `i18n/` zawsze znajduje się obok dokumentu, który tłumaczy.
> - To jedno miejsce jest jedynym, z którego rozwiązywane jest tłumaczenie. Umieszczenie tłumaczenia tego samego dokumentu także w `i18n/` folderu nadrzędnego nie powoduje konfliktu o to, „które ma pierwszeństwo”: tamta kopia staje się po prostu osieroconym plikiem, którego nie widzi ani menu języków, ani rejestr (i nie jest on nigdy usuwany automatycznie). Nie umieszczaj tego samego tłumaczenia w dwóch miejscach.

## Czytanie w wersji przeglądarkowej

W wersji przeglądarkowej także możesz przełączać języki w ten sam sposób, jeśli tłumaczenia istnieją. Aby czytać w języku, dla którego nie ma tłumaczenia, możesz skorzystać z funkcji tłumaczenia strony w przeglądarce. Kod, wzory matematyczne i diagramy są wyłączone z tłumaczenia.

## Powiązane tematy

- [Przekazywanie pracy do AI](../05-ai/README.md)
- [Praca, którą można przekazać](../05-ai/tasks.md)
- [Zmienianie ustawień widoku](../02-reading/display-settings.md)
