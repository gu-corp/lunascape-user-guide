# Zmiana ustawień widoku

Za pomocą przycisku [Ustawienia widoku] (koło zębate) na pasku narzędzi każdy użytkownik może zmienić wygląd panelu INDEX oraz widoczność przycisku edycji.

1. Naciśnij [Ustawienia widoku] na pasku narzędzi.
2. Przełącz pozycje, które chcesz zmienić. Zmiany są stosowane natychmiast.
3. Naciśnij ponownie [Ustawienia widoku] albo kliknij poza panelem, aby go zamknąć.

## Dostępne ustawienia

| Sekcja | Pozycja | Działanie |
|---|---|---|
| Język dokumentu | (stan bieżący) | Pokazuje język domyślny projektu i aktualnie wyświetlany język. Pozycja [Ustaw języki projektu…] otwiera ustawienia języków projektu |
| Zawartość | [Nazwy plików] | Pokazuje nazwy plików zamiast tytułów dokumentów |
| | [Ikony dokumentów] | Pokazuje ikonę przy każdym dokumencie |
| | [Ikony folderów] | Pokazuje ikonę przy każdym folderze |
| | [Liczba elementów w folderze] | Pokazuje liczbę dokumentów w folderze |
| | [Prowadnice wcięć] | Pokazuje linie wskazujące poziom zagnieżdżenia |
| | [Ukryj automatycznie, gdy jest tylko jeden dokument] | W katalogu głównym dokumentacji z jednym dokumentem zamyka panel INDEX automatycznie, tylko przy pierwszym otwarciu |
| | [Zwiń informacje o dokumencie] | Zwija tabelę zarządzania na początku dokumentu do wiersza „Informacje o dokumencie”. Po wyłączeniu tabela jest pokazywana w całości |
| | [Gęstość widoku] | Odstęp między wierszami panelu INDEX: [Standardowy] / [Kompaktowa] |
| | [Przycisk edycji] | Pokazuje przycisk [Edytuj] w prawym dolnym rogu treści |
| Operacje | [Przywróć ustawienia domyślne projektu] | Usuwa wszystkie zmiany użytkownika i przywraca ustawienia projektu |
| | [Otwórz ustawienia rozszerzenia] | Otwiera ustawienia Lunascape Docs w oknie ustawień VS Code |

> **Wskazówka**
>
> - Ustawienia widoku są zapisywane osobno dla każdego użytkownika i każdego katalogu głównego dokumentacji; nie są zapisywane w plikach śledzonych przez Git.
> - Ustawienia mają następujący priorytet: „ustawienia widoku użytkownika → ustawienia VS Code → `lunascape-docs.json` → ustawienia domyślne produktu”. Wspólne wartości domyślne zespołu określa się w sekcjach `tree` i `editor` pliku `lunascape-docs.json`.

## Przełączanie kolorystyki

Naciśnięcie przełącznika motywu (słońce/księżyc) na pasku narzędzi przełącza między białym tłem a kolorystyką VS Code. Kolorystykę przy otwarciu określa ustawienie `lunascapeDocEditor.appearance` (`light` lub `auto`).

## Zobacz też

- [Korzystanie z panelu INDEX](index-panel.md)
- [Ustawienia projektu](../04-document-tools/project-configuration.md)
- [Lista ustawień VS Code](../08-reference/settings.md)
