# Korzystanie z INDEX

INDEX po lewej stronie ekranu to drzewo folderów i dokumentów znajdujących się w katalogu głównym dokumentacji.

## Filtrowanie

1. Wpisz słowo w polu [Filtruj dokumenty] nad INDEX.
2. Wyświetlane są tylko pozycje, których nazwy pasują do wpisanego tekstu. Po wyczyszczeniu pola widok wraca do poprzedniego stanu.

> **Uwaga**
>
> Podczas filtrowania nie można zmieniać kolejności metodą przeciągnij i upuść.

## Rozwijanie i zwijanie folderów

- Naciśnij strzałkę po lewej stronie nazwy folderu albo nazwę folderu bez strony tytułowej, aby go rozwinąć lub zwinąć.
- Folder ze stroną tytułową (plikiem `README.md` lub `index.md` z treścią) otwiera tę stronę po naciśnięciu jego nazwy. Aby tylko rozwinąć lub zwinąć folder, użyj poleceń [Rozwiń folder] / [Zwiń folder] w menu pozycji.
- Stan rozwinięcia folderów jest zapamiętywany dla każdego użytkownika osobno i nie jest zapisywany w plikach śledzonych przez Git.

## README i strona tytułowa folderu

`README.md` to plik opisujący zawartość danego folderu.

- Naciśnięcie nazwy folderu z plikiem README powoduje wyświetlenie tego pliku README.
- W folderze bez pliku README wyświetlany jest pierwszy dokument w środku.
- Nagłówek (H1) pliku README staje się nazwą folderu widoczną w INDEX.

Plik README nie jest wymagany. Aby dodać go później, wybierz polecenie [Utwórz README] w menu pozycji folderu (jest ono widoczne tylko dla folderów bez pliku README).

## Pokazywanie i ukrywanie INDEX

- Lewa ikona w elementach sterujących kolumnami na pasku narzędzi pokazuje lub ukrywa INDEX. Prawa ikona pokazuje lub ukrywa panel „Na tej stronie”.
- Na wąskich ekranach INDEX jest początkowo zamknięty. Naciśnij [Otwórz INDEX] (trzy poziome linie) po lewej stronie przycisku [Wstecz], aby otworzyć INDEX nad treścią dokumentu. Zamkniesz go przyciskiem [×] w INDEX, kliknięciem tła, klawiszem `Esc` lub przejściem do innego dokumentu. To tymczasowe otwarcie nie zmienia ustawienia dla szerokich ekranów.
- W katalogu głównym dokumentacji z tylko jednym dokumentem do wyświetlenia INDEX zamyka się automatycznie przy pierwszym otwarciu. Możesz otworzyć go ponownie ikoną kolumn. Zachowanie to można wyłączyć opcją [Ukryj automatycznie, gdy jest tylko jeden dokument] w [Ustawienia widoku].

## Korzystanie z menu pozycji

Menu pozycji otworzysz przyciskiem [⋯], który pojawia się po najechaniu wskaźnikiem myszy na pozycję w INDEX, albo klikając pozycję prawym przyciskiem myszy. Pozycje są uporządkowane w następującej kolejności.

| Grupa | Pozycje |
|---|---|
| Często używane operacje | [Rozwiń folder] / [Zwiń folder], [Otwórz INDEX] (otwiera stronę tytułową folderu), [Edytuj], [Zmień tytuł], [Otwórz w VS Code], [Kopiuj ścieżkę] |
| Tworzenie i porządkowanie | [Utwórz README] (tylko foldery bez pliku README), [Nowy dokument], [Nowy folder], [Duplikuj], [Zmień nazwę pliku] / [Zmień nazwę folderu], [Przenieś w górę], [Przenieś w dół] |
| Usuwanie | [Przenieś do kosza] |

- Aby utworzyć element bezpośrednio w katalogu głównym dokumentacji, naciśnij [⋯] przy prawej krawędzi nagłówka INDEX albo kliknij prawym przyciskiem myszy puste miejsce w INDEX, a następnie wybierz [Nowy dokument] lub [Nowy folder]. W tym samym menu znajdują się polecenie [Zmień nazwę dokumentu] oraz — jeśli katalog główny dokumentacji nie ma pliku README — polecenie [Utwórz README]. To samo menu otworzysz, klikając prawym przyciskiem myszy nazwę dokumentu widoczną na pasku narzędzi.
- Wewnątrz menu klawisze `↑` `↓` przenoszą między pozycjami, a `Home` `End` — na początek i koniec listy. Zamknięcie menu klawiszem `Esc` przywraca fokus w miejsce, z którego menu zostało otwarte.

> **Uwaga**
>
> Pozycje służące do tworzenia, porządkowania i usuwania są widoczne tylko wtedy, gdy obszar roboczy jest zaufany w VS Code. Nie są one dostępne również podczas edytowania dokumentu ani w trakcie przetwarzania innej operacji INDEX.

## Zmiana wyglądu

W [Ustawienia widoku] możesz zmienić wyświetlanie nazw plików, ikony dokumentów i folderów, liczbę elementów w folderach, linie prowadzące poziomów oraz gęstość widoku. Szczegóły znajdziesz w rozdziale [Zmiana ustawień widoku](display-settings.md).

## Powiązane tematy

- [Tworzenie i porządkowanie dokumentów oraz folderów](../03-editing/organize.md)
- [Zmiana kolejności dokumentów](../03-editing/reorder.md)
