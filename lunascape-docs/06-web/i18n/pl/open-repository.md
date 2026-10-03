# Otwieranie repozytorium GitHub

W wersji internetowej i w Lunascape możesz otworzyć repozytorium GitHub i czytać je bezpośrednio, bez klonowania. Repozytoria publiczne nie wymagają logowania.

## Otwieranie z ekranu

1. Naciśnij [Otwórz dokumenty] (ikona folderu) na pasku narzędzi. Otworzy się ekran „Otwórz dokumenty”.
2. W kolumnie po lewej wybierz, gdzie chcesz szukać.

   | Miejsce | Co zawiera |
   |---|---|
   | Wszystkie | Wszystkie poniższe miejsca. Ostatnio otwarte elementy są na początku |
   | Ostatnio otwarte | Repozytoria i foldery, które już otwierano |
   | Polecane | Podręczniki polecane przez witrynę |
   | Repozytoria GitHub | Repozytoria, które możesz czytać, gdy jesteś zalogowany do GitHub |
   | Ten komputer | Foldery na tym urządzeniu. W Lunascape są tu też sklonowane repozytoria |

3. Naciśnij [Otwórz] w wybranym wierszu. Aby zawęzić listę, wpisz tekst w polu [Filtruj według nazwy dokumentu lub repozytorium] u góry.

Aby otworzyć repozytorium, którego nie ma na liście, użyj [Wpisz owner/repo i otwórz] w kolumnie po lewej.

> **Wskazówka**
>
> - Na liście są repozytoria GitHub, w których zainstalowano GitHub App „Lunascape Docs” i do których masz uprawnienia do odczytu. Jeśli jakiegoś repozytorium brakuje, poproś jego właściciela o dodanie tej aplikacji.

## Sprawdzanie lokalizacji dokumentu

Mała ikona po lewej stronie paska narzędzi (wskaźnik lokalizacji) pokazuje, gdzie znajduje się czytany dokument.

| Ikona | Lokalizacja |
|---|---|
| Logo GitHub | Dokument jest czytany z GitHub. Nie jest zapisany na tym urządzeniu |
| Komputer | Folder na tym urządzeniu zarządzany przez Lunascape. Widoczne są też nazwa gałęzi Git i liczba zmienionych plików |
| Folder | Folder na tym urządzeniu |

Po naciśnięciu ikony pojawiają się lokalizacja, jej stan i czynności, które można stamtąd wykonać, np. [Zobacz w GitHub] lub [Kopiuj link].

## Klonowanie repozytorium w Lunascape

W Lunascape możesz sklonować repozytorium GitHub na to urządzenie, a potem edytować pliki i tworzyć commity w Git.

- Na ekranie „Otwórz dokumenty” naciśnij [Duplikuj] w wierszu repozytorium.
- Jeśli czytasz repozytorium otwarte z GitHub, naciśnij wskaźnik lokalizacji, a następnie [Sklonuj na ten komputer]. Po zakończeniu klonowania ten sam dokument otworzy się z kopii na tym urządzeniu.

Sklonowane repozytorium ma na liście oznaczenie „Na tym komputerze”, a jako pierwszy jest w nim przycisk [Otwórz na tym komputerze].

## Otwieranie za pomocą adresu URL

Adres zawiera nazwę repozytorium i położenie dokumentu, podane po kolei. Ścieżka to położenie wewnątrz repozytorium, więc kolejność jest taka sama jak w adresie URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Co wskazać | Zapis |
|---|---|
| Tylko repozytorium (gałąź domyślna) | `/github/owner/repo` |
| Dokument w repozytorium | `/github/owner/repo/docs/01-product/vision.md` |
| Gałąź lub tag | Dodaj na końcu `?ref=v1.2.0` |

Gdy przechodzisz na inną stronę, adres też się zmienia. Aby przekazać link do czytanej strony, naciśnij [Udostępnij ten dokument] na pasku narzędzi. Działają też przyciski przeglądarki [Wstecz] i [Dalej].

Starszy zapis `?source=` nadal działa. Po otwarciu adres jest zamieniany na nowy zapis.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Uwaga**
>
> - Bez logowania obowiązuje limit GitHub API (60 żądań na godzinę). Jeśli repozytorium ma dużo dokumentów lub często je przeglądasz, naciśnij [Zaloguj się przez GitHub].
> - Nazwy gałęzi zawierające `/` (np. `feature/xxx`) można podać za pomocą `?ref=` w opisanym wyżej formacie adresu. W zapisie `?source=` nie da się ich podać.
> - Dokumenty są wczytywane z uprawnieniami GitHub osoby, która je czyta. Osoby bez uprawnień do odczytu ich nie zobaczą.

## Otwieranie dokumentów z folderu lokalnego

Naciśnij [Otwórz dokumenty] na pasku narzędzi, potem w kolumnie po lewej naciśnij [Otwórz dokumenty z folderu lokalnego] i wybierz folder na urządzeniu. Pliki są przetwarzane w przeglądarce i nigdzie nie są wysyłane. Funkcja działa w przeglądarkach, które obsługują wybór folderu (np. Chrome, Edge).

## Powiązane tematy

- [Przeglądanie repozytorium prywatnego](private-repository.md)
- [Nie można otworzyć wersji internetowej lub się zalogować](../07-troubleshooting/web.md)
