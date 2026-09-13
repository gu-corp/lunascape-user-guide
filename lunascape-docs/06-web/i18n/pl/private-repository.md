# Przeglądanie prywatnego repozytorium

Dokumenty w prywatnych repozytoriach możesz przeglądać po zalogowaniu się przez GitHub — ograniczone do tych repozytoriów, do których masz uprawnienia odczytu. Lunascape Docs nigdy nie ma własnych kont ani uprawnień.

## Zaloguj się i otwórz

1. Otwórz <https://docs.lunascape.org/>.
   Jeśli wskażesz prywatny dokument lub nie jesteś jeszcze zalogowany, pojawi się ekran logowania.
2. Naciśnij [Zaloguj się przez GitHub].
   Ekran uwierzytelniania GitHub otworzy się w wyskakującym okienku.
3. Po zalogowaniu naciśnij [Otwórz dokumenty] na pasku narzędzi i w [Wybierz z dostępnych repozytoriów] wskaż repozytorium, które chcesz otworzyć.

> **Wskazówka**
>
> - Nazwa zalogowanego konta jest widoczna na pasku narzędzi. Stąd możesz też [Wyloguj się] lub [Zaloguj się na inne konto].
> - Na liście pojawiają się repozytoria kont (organizacji lub osób), na których zainstalowano aplikację GitHub „Lunascape Docs”, ograniczone do tych, do których masz uprawnienia odczytu.

## Ustawienia po stronie właściciela repozytorium

Jeśli dane repozytorium nie pojawia się na liście, właściciel repozytorium lub administrator organizacji musi zainstalować aplikację GitHub „Lunascape Docs”.

- Wymagane uprawnienia to Contents (odczyt i zapis) oraz Pull requests (odczyt i zapis). Odczyt służy do przeglądania, a zapis do prośby o publikację (Pull Request) z sieci Web. Lunascape Docs nigdy nie przechowuje treści dokumentów.
- Aplikacja jest instalowana na poziomie konta (organizacji lub osoby). Ustawiasz, czy ma obejmować „All repositories” (wraz z repozytoriami utworzonymi później), czy tylko wybrane repozytoria.

| Sytuacja | Kroki |
|---|---|
| Wdrożenie w nowej organizacji lub na koncie osobistym | Przeprowadź je ze [strony instalacji](https://github.com/apps/lunascape-docs/installations/new) |
| Dodanie repozytoriów w organizacji, która już ją ma | Ustaw w Settings organizacji → GitHub Apps → Lunascape Docs → Configure → Repository access |

Nawet po zainstalowaniu aplikacji w całej organizacji każdy członek może przeglądać tylko te repozytoria, do których sam ma uprawnienia odczytu. Prośbę o publikację może wysłać tylko do tych repozytoriów, do których sam ma uprawnienia zapisu.

> **Wskazówka**
> - Przy nowej instalacji wymagane uprawnienia są wyświetlane w formie listy na ekranie instalacji, a naciśnięcie „Install” oznacza ich zatwierdzenie. Nie są potrzebne żadne dodatkowe czynności.
> - Organizacja, która zainstalowała aplikację przed dodaniem nowego uprawnienia, otrzymuje wiadomość e-mail do administratorów, a na górze Settings organizacji → GitHub Apps → Lunascape Docs → Configure pojawia się przycisk zatwierdzenia. Dopóki nie zostanie zatwierdzone, w tej organizacji działa tylko przeglądanie, a przy wysłaniu prośby o publikację wyświetla się komunikat „Wymagane jest nadanie uprawnień zapisu”.
> - To, z jakimi uprawnieniami aplikacja jest obecnie zainstalowana, możesz sprawdzić na tym samym ekranie Configure. W przypadku konta osobistego jest to Settings → Applications → Installed GitHub Apps.
> - Jeśli przez pomyłkę usuniesz dane repozytorium z listy lub odinstalujesz aplikację, możesz przywrócić stan pierwotny, instalując ją ponownie ze [strony instalacji](https://github.com/apps/lunascape-docs/installations/new). Komunikat o odrzuceniu prośby o publikację zawiera link do ekranu naprawy.
> - Jeśli po stronie repozytorium nie chcesz przyjmować próśb o publikację, wpisz w `lunascape-docs.json` `"publish": { "enabled": false }`. Przeglądanie nadal działa bez zmian.

## Powiązane tematy

- [Otwieranie repozytorium GitHub](open-repository.md)
- [Nie można otworzyć w wersji Web ani się zalogować](../07-troubleshooting/web.md)
