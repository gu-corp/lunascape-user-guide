# Ustawienia AI

Wybierz AI i model, którym przekazujesz pracę. Nie używa się tu szybkiego wyboru VS Code — wybór następuje z list rozwijanych na tym ekranie.

1. Naciśnij [Narzędzia dokumentów] → kartę [AI] → [Ustawienia AI…].
2. Wybierz [Dostawca].
   Dostawcy niedostępni w tym środowisku są widoczni jako niemożliwi do wybrania, wraz z podaniem przyczyny.
3. Wybierz [Model]. Dostępne opcje zmieniają się zależnie od dostawcy.
4. Zamknij ekran. Wybór jest zapisywany dla każdego użytkownika i używany następnym razem.

## Dostawcy

| Dostawca | Postać | Sposób wykrywania |
|---|---|---|
| Claude Code | Sesyjna | Obecność polecenia `claude` |
| Codex | Sesyjna | Obecność polecenia `codex` |
| Modele językowe VS Code | API | Modele zarejestrowane w VS Code Language Model API |
| Anthropic API | API | Zarejestrowany klucz API |
| API zgodne z OpenAI | API | Zarejestrowany klucz API i punkt końcowy |

Dostawca **sesyjny** sam odczytuje i zapisuje pliki oraz sam uruchamia sprawdzanie dokumentów. Wyniki trafiają bezpośrednio do drzewa roboczego i sprawdza się je w różnicach Git.

Dostawca **API** zwraca Markdown jednego dokumentu, a rozszerzenie pokazuje różnice przed zapisaniem.

## Rejestrowanie klucza API

Anthropic API oraz API zgodne z OpenAI stają się dostępne po zarejestrowaniu klucza API.

1. W polu [Dostawca] wybierz miejsce rejestracji. Pojawi się pole na klucz API.
2. Wpisz [Klucz API]. W przypadku API zgodnego z OpenAI wpisz także [Punkt końcowy] (na przykład `https://api.openai.com/v1`).
3. Naciśnij [Zapisz]. Zostanie wyświetlony komunikat „Klucz zarejestrowany”.

> **Uwaga**
>
> - Klucze są przechowywane w magazynie SecretStorage programu VS Code i nie są ponownie wyświetlane. Nie są też zapisywane w pliku `settings.json` ani w dokumentach. Klucz można usunąć przyciskiem [Usuń klucz].
> - Listy modeli są pobierane z poszczególnych usług przy użyciu zarejestrowanego klucza. Dopóki pobranie się nie powiedzie, wyświetlana jest znana lista.
> - Dostawca API może wykonać tylko zadania „Przetłumacz tę stronę” i „Popraw tę stronę”. Obchodzenie wielu dokumentów i tworzenie dokumentów wykonuj u dostawcy sesyjnego.

> **Wskazówka**
>
> Jeśli nie znaleziono żadnego dostawcy, zainstaluj Claude Code lub Codex albo zarejestruj klucz API. Po ponownym otwarciu okna [Ustawienia AI…] zostaną wykryte.

## Zobacz też

- [Przekazywanie pracy do AI](README.md)
- [Lista ustawień VS Code](../08-reference/settings.md)
