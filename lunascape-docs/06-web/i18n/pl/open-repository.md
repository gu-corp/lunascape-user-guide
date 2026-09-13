# Otwieranie repozytorium GitHub

W wersji webowej dokumenty otwiera się, wskazując repozytorium GitHub. W przypadku repozytoriów publicznych logowanie nie jest potrzebne.

## Otwieranie z ekranu

1. Otwórz <https://docs.lunascape.org/>.
2. Naciśnij [Otwórz dokumenty] (ikona folderu) na pasku narzędzi.
3. Wpisz repozytorium w polu [Podaj repozytorium] i naciśnij [Otwórz].
   Gdy jesteś zalogowany w GitHub, możesz też wybrać pozycję z listy w [Wybierz z dostępnych repozytoriów].

> **Wskazówka**
>
> - Sąsiednia ikona GitHub otwiera czytany właśnie dokument w serwisie github.com. Nie służy do otwierania dokumentów.

## Otwieranie przez adres URL

Adres zawiera po kolei repozytorium i położenie dokumentu. Ścieżka jest położeniem wewnątrz repozytorium, więc kolejność jest taka sama jak w adresie GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Co wskazujesz | Zapis |
|---|---|
| Samo repozytorium (gałąź domyślna) | `/github/owner/repo` |
| Dokument wewnątrz repozytorium | `/github/owner/repo/docs/01-product/vision.md` |
| Gałąź lub tag | dodaj na końcu `?ref=v1.2.0` |

Przy przechodzeniu między stronami adres się zmienia. Naciśnij [Udostępnij ten dokument] na pasku narzędzi, aby przekazać komuś odnośnik do czytanej strony. Działają też przyciski przeglądarki [Wstecz] i [Dalej].

Wcześniejszy zapis z `?source=` nadal się otwiera. Po otwarciu adres zostaje zmieniony na nowy zapis.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Uwaga**
>
> - Bez zalogowania obowiązuje limit użycia API GitHub (60 wywołań na godzinę). W przypadku repozytoriów z wieloma dokumentami lub wielokrotnego przeglądania użyj [Zaloguj się przez GitHub].
> - Nazwy gałęzi zawierające `/` (na przykład `feature/xxx`) można wskazać za pomocą `?ref=` w powyższym zapisie adresu. W zapisie z `?source=` nie da się ich zapisać.
> - Dokumenty są wczytywane z uprawnieniami GitHub osoby czytającej. Osoby bez prawa odczytu ich nie zobaczą.

## Otwieranie dokumentów z folderu lokalnego

Naciśnij [Otwórz dokumenty] na pasku narzędzi, a następnie [Otwórz dokumenty z folderu lokalnego] pod listą i wybierz folder na swoim urządzeniu. Pliki są przetwarzane wewnątrz przeglądarki i nie są nigdzie wysyłane. Działa to w przeglądarkach obsługujących wybór folderu (Chrome, Edge i inne).

## Powiązane tematy

- [Przeglądanie repozytorium prywatnego](private-repository.md)
- [Nie można otworzyć wersji webowej ani się zalogować](../07-troubleshooting/web.md)
