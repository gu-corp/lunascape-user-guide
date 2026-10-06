# Co je Lunascape Docs

Lunascape Docs je nástroj, který s dokumenty Markdown uloženými v úložišti Git pracuje přímo jako s „webem specifikací“. Není potřeba předchozí sestavení, server dokumentace ani vyhrazená databáze.

## Co můžete dělat

| Účel | Hlavní funkce |
|---|---|
| Číst | INDEX (obsah), odkazy v textu, popis cesty, zpět a vpřed, obsah stránky, vyhledávání s filtrem |
| Prohlížet | Tabulky, bloky kódu, automatické přizpůsobení obrázků, vzorce KaTeX, diagramy Mermaid, Vega-Lite, Markmap, WaveDrom a Svgbob, sbalené zobrazení tabulek správy dokumentů |
| Psát | Přepínání mezi vizuálními úpravami a úpravami zdroje Markdown; vytváření, duplikování, přejmenování a změna pořadí v panelu INDEX |
| Ověřovat | Kontrola dokumentů pomocí docs-lint, ověření povinných dokumentů, kapitol a termínů podle Standard Pack, vytváření ze šablon |
| Překládat | Generování návrhů překladu po jednotlivých stránkách nebo hromadně. Uložení až po kontrole <!-- ai-only --> |
| Používat s AI | Nástroj pro specifikace jen pro čtení, který mohou využívat agenti ve VS Code <!-- ai-only --> |

## Kde lze Lunascape Docs používat

| Prostředí | Použití |
|---|---|
| Rozšíření pro VS Code | Prohlížení, úpravy, kontrola a překlad úložiště ve vašem počítači. Tato nápověda se zaměřuje hlavně na něj |
| Verze pro webový prohlížeč | Prohlížení dokumentů na GitHubu (veřejných i soukromých), koncepty ve vašem zařízení, prohlížení místní složky |
| Rozšíření pro Chromium | Otevře verzi pro webový prohlížeč na kartě prohlížeče |

## Základní principy

- **Originálem je Markdown.** Dokumenty zůstávají soubory Markdown spravovanými v Gitu. Lunascape Docs je nepřevádí do jiného formátu ani je v jiném formátu neuchovává.
- **Ukládáte vy.** Upravený obsah se zapíše do souboru, jen když stisknete [Uložit]. Stage ani commit v Gitu se neprovádějí automaticky.
- **Dokumenty se zpracovávají ve vašem zařízení.** Kvůli prohlížení ani úpravám se dokumenty nikam neodesílají. Pouze při překladu se předem zobrazí cíl a obsah odesílaných dat a odešlou se až po vašem schválení.
- **Překlady se ukládají do `i18n/<locale>/`.** Dokumenty ve výchozím jazyce zůstávají na svém místě, překlady se ukládají se stejnou relativní cestou například do `i18n/en/`.
- **AI pouze navrhuje.** Návrhy překladu se ukládají až po kontrole rozdílů. Dokumenty se nikdy nepřepisují bez vašeho vědomí. <!-- ai-only -->

## Související témata

- [Názvy a funkce částí obrazovky](screen.md)
- [Instalace rozšíření](install.md)
- [Základní ovládání](../02-reading/README.md)
