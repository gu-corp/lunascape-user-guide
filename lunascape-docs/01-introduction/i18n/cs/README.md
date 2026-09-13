# Co je Lunascape Docs

Lunascape Docs umožňuje pracovat s dokumenty ve formátu Markdown uloženými v úložišti Git přímo jako se „stránkami se specifikací“. Není potřeba žádné předchozí sestavení, dokumentační server ani zvláštní databáze.

## Co umí

| Účel | Hlavní funkce |
|---|---|
| Čtení | INDEX (obsah), odkazy v textu, popis cesty, zpět a vpřed, obsah stránky, filtrované hledání |
| Zobrazení | Tabulky, bloky kódu, automatické přizpůsobení obrázků, vzorce KaTeX, diagramy Mermaid, Vega-Lite, Markmap, WaveDrom a Svgbob, sbalené zobrazení tabulek pro správu dokumentu |
| Psaní | Přepínání mezi vizuální úpravou a úpravou zdroje Markdown, vytváření, kopírování, přejmenování a změna pořadí z panelu INDEX |
| Kontrola | Kontrola dokumentu nástrojem docs-lint, ověření povinných dokumentů, kapitol a termínů podle Standard Pack, vytváření ze šablony |
| Překlad | Vytvoření návrhu překladu pro jednu stránku nebo pro všechny najednou. Uložení až po kontrole <!-- ai-only --> |
| Použití z AI | Nástroj pro specifikace jen pro čtení, na který se může odkazovat agent ve VS Code <!-- ai-only --> |

## Dostupná prostředí

| Prostředí | Použití |
|---|---|
| Rozšíření pro VS Code | Prohlížení, úpravy, kontrola a překlad úložiště ve vašem počítači. Tato nápověda se věnuje především jemu |
| Verze pro webový prohlížeč | Prohlížení dokumentů na GitHubu (veřejných i neveřejných), koncepty v zařízení, prohlížení místní složky |
| Rozšíření pro Chromium | Otevře verzi pro webový prohlížeč na kartě prohlížeče |
| Prohlížeč Lunascape | Chystá se v něm použít stejný model dokumentu |

## Základní principy

- **Originálem je Markdown.** Dokumenty zůstávají soubory Markdown spravovanými v Gitu. Lunascape Docs je nepřevádí do jiného formátu a takovou kopii si neuchovává.
- **O uložení rozhoduje uživatel.** Upravený obsah se zapíše do souboru pouze při stisknutí tlačítka [Uložit]. Přidání do fronty ani potvrzení změn v Gitu neproběhne automaticky.
- **Dokumenty se zpracovávají v zařízení.** Kvůli prohlížení ani úpravám se dokumenty nikam neodesílají. Pouze při překladu se předem zobrazí cíl odeslání a obsah a odeslání proběhne až po vašem schválení.
- **Překlady se ukládají do `i18n/<jazyk>/`.** Dokumenty ve výchozím jazyce zůstávají na svém místě, překlady se ukládají se stejnou relativní cestou například do `i18n/en/`.
- **AI pouze navrhuje.** Návrh překladu se ukládá až po kontrole rozdílů. Dokument se nikdy nepřepíše bez upozornění. <!-- ai-only -->

## Související témata

- [Názvy a funkce částí obrazovky](screen.md)
- [Instalace rozšíření](install.md)
- [Základní操作](../02-reading/README.md)
