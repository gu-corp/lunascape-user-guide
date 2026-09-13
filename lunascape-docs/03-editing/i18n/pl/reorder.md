# Zmiana kolejności dokumentów

Kolejność wyświetlaną w panelu INDEX można zmienić metodą przeciągnij i upuść lub za pomocą klawiatury. Zmieniona kolejność jest zapisywana we front matter dokumentu jako `navigation.order`.

## Zmiana kolejności metodą przeciągnij i upuść

1. Przeciągnij dokument lub folder w panelu INDEX.
2. Upuść go przed innym elementem tego samego poziomu, za nim albo na folderze.
   W obrębie tego samego poziomu zmienia się kolejność. Upuszczenie na innym folderze przenosi element do tego folderu.

## Zmiana kolejności za pomocą klawiatury lub menu

- Ustaw fokus na elemencie w panelu INDEX i naciśnij `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Wybierz [Przenieś w górę] / [Przenieś w dół] w menu elementu.

## Co jest zapisywane

- Przy zmianie kolejności w obrębie tego samego poziomu aktualizowana jest wartość `navigation.order` we front matter dokumentu źródłowego. W przypadku folderu zapis następuje w pliku `README.md` tego folderu. Jeśli folder nie ma pliku `README.md`, tworzony jest plik `README.md` zawierający wyłącznie front matter.
- Przy przeniesieniu do innego folderu dokument źródłowy i odpowiadające mu tłumaczenia są przenoszone razem. Przed przeniesieniem wyświetlane jest potwierdzenie dotyczące wpływu na linki względne.
- Operacje Git (dodanie do przechowalni ani zatwierdzenie) nie są wykonywane.

> **Uwaga**
>
> - Zmiana kolejności nie jest możliwa podczas filtrowania, podczas edycji dokumentu ani w niezaufanym obszarze roboczym.
> - Komunikat „INDEX został zaktualizowany” oznacza, że przed chwilą została zastosowana inna zmiana. Wykonaj operację ponownie.
> - Strony początkowej nie można przenieść do innego folderu.

> **Wskazówka**
>
> Nadawanie wartości `navigation.order` co 100, na przykład 100, 200, 300, ułatwia późniejsze wstawianie dokumentów pomiędzy nimi. Szczegółowe informacje znajdziesz w temacie [Ustawianie metadanych nawigacji](../04-document-tools/navigation-metadata.md).

## Tematy pokrewne

- [Tworzenie i porządkowanie dokumentów oraz folderów](organize.md)
- [Ustawianie metadanych nawigacji](../04-document-tools/navigation-metadata.md)
