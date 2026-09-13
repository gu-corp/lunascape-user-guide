# Ustawianie metadanych nawigacji

Nazwa i kolejność wyświetlane w INDEX są zapisane w YAML front matter każdego dokumentu. Dokumenty są wyświetlane nawet bez tego — używane są wtedy nagłówek (H1) oraz kolejność według nazw plików.

## Nazwa i kolejność dokumentu

Na początku dokumentu wpisz następujące dane.

```yaml
---
navigation:
  title: Wprowadzenie
  order: 200
---
```

| Pole | Znaczenie |
|---|---|
| `navigation.title` | Nazwa wyświetlana w INDEX. W przypadku pominięcia używany jest H1, a jeśli go nie ma — nazwa pliku |
| `navigation.order` | Liczba całkowita określająca kolejność, rosnąco. W przypadku pominięcia obowiązuje stabilna kolejność domyślna (według nazw plików) |

> **Wskazówka**
>
> - Nadawaj wartości `order` co 100, na przykład 100, 200, 300, aby móc później wstawić między nie wartość 150.
> - Brakujące, nieprawidłowe lub zduplikowane wartości `order` nigdy nie ukrywają dokumentu.
> - Zmiana kolejności w INDEX zapisuje `navigation.order` za Ciebie; nie trzeba wpisywać jej ręcznie.

## Nazwa i kolejność folderu

Nazwa i kolejność folderu należą do front matter jego pliku `README.md` (lub `index.md`, gdy nie ma README). Strona tytułowa nie musi mieć treści.

```yaml
---
navigation:
  title: Planowanie produktu
  order: 100
---
```

Folder bez strony tytułowej używa nazwy folderu i kolejności domyślnej. Gdy zmiana tytułu lub zmiana kolejności w INDEX tego wymaga, tworzony jest plik `README.md` zawierający wyłącznie front matter. Samo przeglądanie nigdy nie tworzy pliku.

## Obsługa w wersjach przetłumaczonych

- Kolejność oraz rolę folderu (strona tytułowa czy wyłącznie konfiguracja) ustala jedynie dokument w języku domyślnym.
- Tłumaczenie może nadpisać tylko `navigation.title`. Gdy dokument źródłowy ma treść, jako nazwa używany jest również H1 tłumaczenia.
- Samo tłumaczenie nigdy nie dodaje strony.

## Sortowanie i zwijanie elementów podrzędnych

`navigation.children.sort` oraz `navigation.children.defaultCollapsed` na stronie tytułowej folderu służą do określenia sposobu sortowania jego bezpośrednich elementów podrzędnych oraz tego, czy są one początkowo zwinięte. Ich odczyt i edycja w VS Code są planowane.

## Powiązane tematy

- [Zmiana kolejności dokumentów](../03-editing/reorder.md)
- [Katalogi główne dokumentacji i konwencje plików](structure.md)
