# Nie można otworzyć wersji Web ani się zalogować

## Po zalogowaniu repozytorium nie pojawia się na liście

Na tym koncie nie zainstalowano aplikacji GitHub App „Lunascape Docs” albo repozytorium nie zostało nią objęte. Poproś właściciela repozytorium lub administratora organizacji o instalację zgodnie z opisem w [Przeglądanie prywatnego repozytorium](../06-web/private-repository.md).

## Nie można przejść dalej z ekranu logowania

- Nie masz uprawnień do odczytu tego repozytorium. Poproś właściciela repozytorium o nadanie uprawnień.
- „Logowanie przez GitHub nie jest skonfigurowane dla tej witryny”: w samodzielnie wdrożonej przeglądarce dokumentów nie skonfigurowano usługi logowania. Usługę musi skonfigurować administrator.

## Okno wyskakujące do logowania się nie otwiera

Przeglądarka blokuje okna wyskakujące. Zezwól na okna wyskakujące dla tej witryny i spróbuj ponownie.

## Pojawia się komunikat „Sesja logowania wygasła”

Ważność logowania wygasła. Naciśnij ponownie [Zaloguj się przez GitHub].

## Otwarcie publicznego repozytorium kończy się błędem 404

- Sprawdź zapis `owner/repo@ref/dir`.
- Nie można podać nazwy gałęzi zawierającej `/`.

## Po pewnym czasie strony przestają się wczytywać

Bez zalogowania obowiązuje limit korzystania z API GitHub (60 wywołań na godzinę). Gdy pojawi się komunikat „Osiągnięto limit liczby wywołań”, odczekaj chwilę albo użyj [Zaloguj się przez GitHub].

## Pojawia się komunikat „Ta witryna nie może wyświetlić tego repozytorium”

Aby otworzyć repozytorium z samodzielnie wdrożonej przeglądarki dokumentów, należy dodać adres URL tej witryny do `viewer.origins` w pliku `lunascape-docs.json` po stronie repozytorium.

## Po otwarciu `index.html` nic się nie wyświetla

Otwarcie bezpośrednio przez `file://` nie działa. Otwórz plik przez serwer HTTP albo użyj wersji dla VS Code.

## Wyeksportowana witryna zgłasza „Nie znaleziono pliku lunascape-docs-manifest.json”

Umieść na serwerze komplet plików wygenerowanych przez `npm run export:web` (wraz z manifestem) w niezmienionej postaci.

## Nie można zapisać wersji roboczej

- „Nie można otworzyć IndexedDB”, „W użyciu w innej karcie”: przyczyną jest tryb prywatny przeglądarki albo inna karta z tą samą witryną. Otwórz witrynę w zwykłym oknie i zamknij pozostałe karty.
- Wersje robocze są zapisywane osobno dla każdego urządzenia i każdej przeglądarki. Nie są przenoszone na inne urządzenie.

## Powiązane tematy

- [Otwieranie repozytorium GitHub](../06-web/open-repository.md)
- [Zapisywanie wersji roboczych](../06-web/drafts.md)
