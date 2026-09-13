# Dokumenty nie są wyświetlane

## Pojawia się komunikat „Nie znaleziono pliku Markdown ani folderu docs do otwarcia”

- Obszar roboczy nie zawiera folderu `docs` albo używa innej nazwy.
  - Umieść w tym folderze plik `lunascape-docs.json`, aby był rozpoznawany jako katalog główny dokumentacji niezależnie od nazwy.
  - Możesz też dodać nazwę folderu do ustawienia `lunascapeDocEditor.rootDirectoryNames`.
- Jeśli nie ma jeszcze żadnych dokumentów, utwórz je poleceniem „Lunascape Docs: Utwórz dokumentację na podstawie szablonu”.
- Można również otworzyć plik Markdown w edytorze i uruchomić polecenie „Lunascape Docs: Otwórz w przeglądarce specyfikacji”.

## Dokumentu nie ma w panelu INDEX

- Sprawdź, czy rozszerzenie pliku to `.md`, `.markdown` lub `.mdx`.
- Następujące foldery nie są wyświetlane: foldery zaczynające się od `.`, `node_modules` oraz foldery podane w `ignoredDirectories` (domyślnie `99-archive`).
- Tłumaczenia znajdujące się w `i18n/` nie są wyświetlane w panelu INDEX osobno. Przełączasz się na nie z menu języków.
- Jeśli dopiero co dodany plik nie jest widoczny, naciśnij [Załaduj ponownie].
- Możesz oglądać inny katalog główny dokumentacji. Sprawdź jego nazwę na lewym końcu paska narzędzi.

## Naciśnięcie folderu nic nie wyświetla

Plik `README.md` w tym folderze jest „deskryptorem służącym wyłącznie do konfiguracji” — zawiera tylko front matter, bez treści. Rozwiń folder w panelu INDEX i wybierz dokument z jego wnętrza.

## Otwiera się niewłaściwy katalog główny dokumentacji

- Gdy ustawienie `lunascapeDocEditor.rootMode` ma wartość `fixed`, zawsze otwierany jest katalog wskazany w `lunascapeDocEditor.root`.
- Przy wartości `auto` wybierany jest katalog główny dokumentacji położony najbliżej otwartego pliku Markdown. Możesz go zmienić listą rozwijaną na lewym końcu paska narzędzi.

## Katalog główny dokumentacji ma inną nazwę, niż oczekiwano

Nazwa jest ustalana w kolejności: `title` w pliku `lunascape-docs.json` → `navigation.title` w głównym pliku `README.md` → jego nagłówek H1 → `index.md` → nazwa folderu. Aby ją ustalić na stałe, ustaw `title`.

## Panel INDEX zniknął

- W katalogu głównym dokumentacji z tylko jednym dokumentem panel INDEX zamyka się automatycznie przy pierwszym otwarciu. Możesz go otworzyć ikoną kolumn na pasku narzędzi. Zachowanie to wyłączysz opcją [Ukryj automatycznie, gdy jest tylko jeden dokument] w [Ustawienia widoku].
- Na wąskim ekranie otwórz go przyciskiem [Otwórz INDEX] (trzy poziome linie) po lewej stronie przycisku [Wstecz].

## Naciśnięcie odsyłacza nic nie otwiera

- „Nie znaleziono celu odsyłacza”: plik docelowy nie istnieje. Odsyłacze wewnętrzne sprawdzisz przyciskiem [Sprawdzanie] w Narzędziach dokumentów.
- „Nie otwarto odsyłacza, który jest niebezpieczny lub nieobsługiwany”: odsyłacze prowadzące poza katalog główny dokumentacji oraz odsyłacze o schemacie innym niż `https://` lub `mailto:` nie są otwierane.

## Wyświetlany jest inny język, niż oczekiwano

- W menu języków sprawdź język wyświetlanej strony i podstawę jego wyboru.
- Ostatnio wybrany język interfejsu jest zapamiętywany. Wybierz ponownie język domyślny w menu języków.
- Jeśli ustawienie osobiste `lunascapeDocEditor.locale` jest ustawione, pierwszeństwo ma tłumaczenie na ten język.

## Powiązane tematy

- [Przełączanie katalogów głównych dokumentacji](../02-reading/roots.md)
- [Katalogi główne dokumentacji i konwencje plików](../04-document-tools/structure.md)
