# Korzystanie z poziomu AI

Rozszerzenie rejestruje w VS Code narzędzie Language Model Tool `lunascape_getDocsSpecification` działające tylko do odczytu. Gdy zgodny agent VS Code zostanie zapytany o funkcje, ustawienia lub konwencje dokumentów Lunascape Docs, może za pomocą tego narzędzia pobrać treść tej pomocy (ogólną specyfikację).

## Jak z tego korzystać

W czacie VS Code zadaj pytanie z dopiskiem `#lunascapeDocs` albo po prostu zapytaj o ustawienia lub strukturę dokumentów Lunascape Docs.

```text
#lunascapeDocs lunascape-docs.json で英語の翻訳を有効にするには？
```

## Argumenty narzędzia

| Argument | Znaczenie |
|---|---|
| `topic` | Rozdział do pobrania: `all`, `usage` (podstawowa obsługa), `structure` (katalogi główne dokumentacji i konwencje plików), `editing` (edytowanie dokumentu), `configuration` (ustawienia projektu), `security` (bezpieczeństwo i granice zapisu), `ai` (korzystanie z poziomu AI) |
| `locale` | Język pomocy (tag języka dołączonej pomocy, np. `ja`, `en`). Po pominięciu używany jest język interfejsu VS Code, a w razie jego braku zwracana jest pomoc w języku japońskim |

> **Uwaga**
>
> - Narzędzie nie wysyła treści dokumentów na zewnątrz.
> - Narzędzie nie zwraca nazw obszarów roboczych ani ścieżek lokalnych.
> - Narzędzie nie modyfikuje plików.
> - Działa z poziomu zgodnych agentów VS Code nawet bez pliku `AGENTS.md`. Nie jest udostępniane automatycznie innym klientom AI, które nie korzystają z API narzędzi rozszerzenia.

## Powiązane tematy

- [Wyświetlanie pomocy](../02-reading/help.md)
- [Bezpieczeństwo i granice zapisu](security.md)
