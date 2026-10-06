# Otwieranie repozytorium GitHub

W wersji internetowej możesz otworzyć repozytorium GitHub i czytać je bezpośrednio, bez klonowania. Repozytoria publiczne nie wymagają logowania.

## Otwieranie z ekranu

1. Naciśnij [Otwórz dokumenty] (ikona folderu) na pasku narzędzi. Otworzy się ekran „Otwórz dokumenty”.
2. W kolumnie po lewej wybierz miejsce, z którego chcesz otworzyć dokumenty.

   | Miejsce | Co zawiera |
   |---|---|
   | Wszystkie | Wszystko poniżej. Ostatnio otwarte elementy są na początku |
   | Ostatnio otwarte | Repozytoria i foldery, które były już otwierane |
   | Polecane | Podręczniki polecane przez witrynę |
   | Repozytoria GitHub | Po zalogowaniu do GitHub — repozytoria, które możesz czytać |
   | Ten komputer | Foldery na tym urządzeniu |

3. Naciśnij [Otwórz] w wierszu, który chcesz otworzyć. Aby zawęzić listę wierszy, wpisz tekst w polu [Filtruj według nazwy dokumentu lub repozytorium] u góry.

Repozytorium, którego nie ma na liście, wskaż za pomocą [Wpisz owner/repo i otwórz] w kolumnie po lewej.

> **Wskazówka**
>
> - Na liście pojawiają się repozytoria GitHub, w których zainstalowano aplikację GitHub App „Lunascape Docs” i do których masz uprawnienia do odczytu. Jeśli repozytorium nie widać, poproś jego właściciela o dodanie tej aplikacji.

## Sprawdzanie lokalizacji dokumentu

Mała ikona po lewej stronie paska narzędzi (etykieta lokalizacji) pokazuje, gdzie znajduje się czytany dokument.

| Ikona | Lokalizacja |
|---|---|
| Znak GitHub | Dokument jest czytany z GitHub. Nie jest zapisany na tym urządzeniu |
| Folder | Folder na tym urządzeniu |

Po naciśnięciu ikony wyświetlane są lokalizacja, jej stan oraz dostępne działania (np. [Zobacz w GitHub], [Kopiuj link]).

## Otwieranie przez adres URL

Adres składa się z repozytorium i położenia dokumentu zapisanych kolejno. Ścieżka określa położenie w repozytorium, więc kolejność jest taka sama jak w adresie URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Co wskazać | Zapis |
|---|---|
| Tylko repozytorium (gałąź domyślna) | `/github/owner/repo` |
| Dokument w repozytorium | `/github/owner/repo/docs/01-product/vision.md` |
| Gałąź lub tag | Dodaj na końcu `?ref=v1.2.0` |

Po przejściu na inną stronę zmienia się także adres. Naciśnij [Udostępnij ten dokument] na pasku narzędzi, aby przekazać link do czytanej strony. Działają też przyciski przeglądarki [Wstecz] i [Dalej].

Starsza postać z `?source=` nadal się otwiera. Po otwarciu adres zostaje zmieniony na nową postać.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Uwaga**
>
> - Bez zalogowania obowiązuje limit GitHub API (60 żądań na godzinę). W przypadku repozytoriów z wieloma dokumentami lub częstego przeglądania naciśnij [Zaloguj się przez GitHub].
> - Nazwy gałęzi zawierające `/` (np. `feature/xxx`) można podać za pomocą `?ref=` w powyższej postaci adresu. W postaci `?source=` nie da się ich zapisać.
> - Dokumenty są wczytywane z uprawnieniami GitHub osoby czytającej. Osoby bez uprawnień do odczytu ich nie zobaczą.

## Otwieranie dokumentów z folderu lokalnego

Naciśnij [Otwórz dokumenty] na pasku narzędzi, następnie w kolumnie po lewej naciśnij [Otwórz dokumenty z folderu lokalnego] i wybierz folder na urządzeniu. Pliki są przetwarzane w przeglądarce i nigdzie nie są wysyłane. Funkcja działa w przeglądarkach obsługujących wybór folderu (Chrome, Edge i in.).

## Powiązane tematy

- [Przeglądanie repozytorium prywatnego](private-repository.md)
- [Wersja internetowa się nie otwiera lub nie można się zalogować](../07-troubleshooting/web.md)
