# Zapisywanie wersji roboczych

Gdy edytujesz dokument w wersji Web, zmiany nie są zapisywane w repozytorium, lecz przechowywane w przeglądarce jako „wersja robocza".

## Tworzenie wersji roboczej

1. Otwórz dokument i naciśnij [Edytuj] w prawym dolnym rogu.
2. Wprowadź zmiany i naciśnij [Zapisz].
   Pojawi się komunikat „Zapisano jako wersję roboczą", a zmiana zostanie zachowana w przeglądarce.

- Dokumenty z wersją roboczą są oznaczone plakietką w panelu INDEX. Nad treścią widoczna jest informacja „Ten dokument to wersja robocza na tym urządzeniu (nieopublikowana)".
- Przycisk [Wersje robocze] na pasku narzędzi pokazuje ich liczbę, a po naciśnięciu otwiera listę wersji roboczych.

## Odrzucanie wersji roboczej

- Aby odrzucić wersję roboczą jednego dokumentu, naciśnij [Odrzuć wersję roboczą] nad treścią.
- Aby odrzucić wszystkie, użyj listy wersji roboczych.

## Przenoszenie zmian do repozytorium

Prośba o publikację, która wysyła wersje robocze jako Pull Request, jest zaimplementowana, ale nie jest włączona w publicznie dostępnej wersji Web. Aby wprowadzić zmiany w repozytorium, edytuj dokument w wersji VS Code lub w lokalnej kopii repozytorium.

> **Uwaga**
>
> - Wersje robocze są zapisywane w przeglądarce (IndexedDB). Nie są przenoszone do innej przeglądarki ani na inne urządzenie, a usunięcie danych witryny w przeglądarce powoduje ich utratę.
> - Jeżeli po utworzeniu wersji roboczej dokument w repozytorium zostanie zmieniony, pojawi się informacja „Źródło nadrzędne zostało zaktualizowane". Sprawdź treść i zdecyduj, czy odrzucić wersję roboczą, czy pozostawić ją bez zmian.
> - Jeżeli edytujesz lokalny folder otwarty za pomocą [Otwórz dokumenty], zmiany są zapisywane bezpośrednio w pliku, o ile przeglądarka to obsługuje. W przeglądarkach bez tej obsługi są zachowywane tylko na czas bieżącej sesji.

## Tematy pokrewne

- [Możliwości wersji Web](README.md)
- [Edytowanie dokumentu](../03-editing/README.md)
