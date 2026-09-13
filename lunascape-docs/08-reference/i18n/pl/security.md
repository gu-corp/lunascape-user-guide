# Bezpieczeństwo i granice zapisu

Granice, które Lunascape Docs utrzymuje, aby chronić dokumenty i urządzenie.

## Wyświetlanie

- Kod HTML wygenerowany z Markdown oraz SVG wygenerowany z diagramów są przed wyświetleniem oczyszczane przez DOMPurify 3.4.14.
- Dowolne skrypty zawarte w MDX nie są wykonywane.
- KaTeX działa z ustawieniami `trust: false`, `maxSize: 50` i `maxExpand: 1000` i nie ufa ani zewnętrznemu kodowi HTML, ani dowolnym poleceniom.
- Biblioteki renderujące Markmap, WaveDrom, Svgbob, Vega-Lite i Penrose są wczytywane lokalnie, w ustalonych wersjach, tylko wtedy, gdy w dokumencie występuje odpowiedni blok. Odwołania do zasobów zewnętrznych, surowy kod HTML i zapisy wykonywalne nie są dozwolone, a z wygenerowanego SVG usuwane są skrypty, obrazy zewnętrzne oraz elementy `link`, `style` i `foreignObject`.
- Renderowanie TikZ nie uruchamia programu LaTeX zainstalowanego na urządzeniu. Odbywa się sekwencyjnie w procesie roboczym TeX opartym na WebAssembly, z systemem plików w pamięci, z ograniczeniami danych wejściowych, kolejki, pamięci, czasu wykonania (15 sekund) i wyjściowego SVG; instrukcje wejścia/wyjścia na plikach są odrzucane.

## Dostęp do dokumentów i plików

- Odnośniki w dokumentach i operacje na plikach nie mogą wyjść poza katalog główny dokumentacji.
- Tworzenie, zmiana nazwy, przenoszenie i usuwanie z poziomu INDEX są przed zastosowaniem ponownie weryfikowane po stronie rozszerzenia: katalog główny dokumentacji, wersja INDEX, ścieżka dokumentu źródłowego, typ obiektu, granice dowiązań symbolicznych oraz niezapisane dokumenty. Żądania pochodzące z nieaktualnego menu lub z innego katalogu głównego dokumentacji nie są wykonywane.
- Podczas edycji dokumentu oraz w trakcie wykonywania innej operacji na INDEX zmiany w INDEX są wyłączone.
- Tworzenie z szablonu ponownie weryfikuje po podglądzie zaufanie do obszaru roboczego, tożsamość katalogu głównego dokumentacji, wersję INDEX, Standard Pack i generowaną treść, miejsce zapisu oraz granice dowiązań symbolicznych. Nie nadpisuje istniejących plików i nie tworzy treści innej niż w podglądzie ani wyniku rozwinięcia przekraczającego 4 MiB.
- Zapis pliku konfiguracyjnego sprawdza jego wersję bezpośrednio przed zapisem i zostaje przerwany po wykryciu zmiany zewnętrznej.

## Wysyłanie na zewnątrz

- Dokumenty nie są wysyłane na zewnątrz w celu przeglądania, edycji ani sprawdzania. Sprawdzanie dokumentów przebiega lokalnie i deterministycznie.
- Tylko tłumaczenie (tłumaczenie tej strony oraz tłumaczenie zbiorcze) wysyła dokumenty do modelu językowego — po wcześniejszym pokazaniu miejsca docelowego i zakresu wysyłki i wyłącznie po wyraźnym zatwierdzeniu. <!-- ai-only -->
- Propozycje tłumaczenia są przedstawiane jako różnice; wersje dokumentu źródłowego i dokumentu docelowego są ponownie weryfikowane, a propozycja jest stosowana tylko wtedy, gdy człowiek wyraźnie ją zapisze. <!-- ai-only -->
- Narzędzie specyfikacji dla agentów AI nie zwraca treści dokumentów, nazw obszarów roboczych ani ścieżek lokalnych. <!-- ai-only -->

## Git

- Zapis wykonuje wyłącznie zapis do pliku. Żadna funkcja nie dodaje zmian do poczekalni Git ani nie tworzy commitów automatycznie.
- Istniejące pliki, takie jak `_meta.json`, nie są po cichu usuwane ani zmieniane. Osierocone wersje tłumaczeń również nie są automatycznie usuwane ani przenoszone.

## Zobacz też

- [Główne specyfikacje](README.md)
- [Korzystanie z poziomu AI](ai-agents.md)
