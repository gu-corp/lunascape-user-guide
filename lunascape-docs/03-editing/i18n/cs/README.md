# Úprava dokumentu

Dokumenty lze upravovat přímo v prohlížeči. Editor nabízí vizuální zobrazení, kde upravujete to, co vidíte, a zobrazení zdroje Markdown; mezi oběma se přepíná jedním tlačítkem.

## Zahájení úprav

Stiskněte kteroukoli z následujících možností. Všechny otevřou stejný editor.

- [Upravit] vpravo dole pod textem
- [⋯] (další akce) vpravo nahoře nad textem → [Upravit]
- Nabídka položky v panelu INDEX → [Upravit]

## Úpravy

1. Upravte text přímo.
   Na panelu nástrojů v horní části editoru máte k dispozici formát odstavce (text, nadpisy 1–4, citace, kód), [Tučné], [Kurzíva], [Odrážkový seznam], [Číslovaný seznam], [Odkaz], [Vložit tabulku], [Šířka obrázku], [Zpět] a [Znovu].
2. Chcete-li upravit přímo zdroj Markdown, stiskněte [Markdown].
   Dalším stisknutím se vrátíte do vizuálního zobrazení. Naposledy použité zobrazení se uloží a obnoví se při příštím stisknutí tlačítka [Upravit].
3. Stiskněte [Uložit].
   Změny se zapíší do souboru Markdown a prohlížeč se vrátí do režimu čtení. Chcete-li úpravy zahodit, stiskněte [Zrušit].

> **Poznámka**
>
> - Uložení pouze zapíše soubor. Přidání do oblasti připravených změn (staging) ani revize (commit) v Gitu neprobíhají automaticky.
> - Vzorce a diagramy, jako jsou Mermaid, TikZ nebo Vega-Lite, se ve vizuálním zobrazení ukazují vykreslené. Chcete-li změnit jejich obsah, přepněte na [Markdown].
> - Dokumenty obsahující syntaxi specifickou pro MDX (komponenty, `import` a podobně) lze upravovat pouze v zobrazení Markdown, aby tato syntaxe zůstala zachována.
> - Front matter (blok mezi řádky `---` na začátku souboru) zůstává zachován i při úpravách ve vizuálním zobrazení.

> **Tip**
>
> - Stisknutím [Otevřít ve VS Code] otevřete soubor v běžném textovém editoru. Po uložení v textovém editoru se zobrazení v prohlížeči automaticky aktualizuje.
> - Pokud nechcete tlačítko [Upravit] zobrazovat, vypněte [Tlačítko úprav] v [Nastavení zobrazení]. Chcete-li je skrýt v celém projektu, nastavte v souboru `lunascape-docs.json` hodnotu `editor.showEditButton` na `false`.
> - Výchozí zobrazení při otevření (vizuální, nebo Markdown) změníte nastavením `lunascapeDocEditor.editor.defaultMode` nebo hodnotou `editor.defaultMode` v souboru `lunascape-docs.json`.

## Související témata

- [Vytváření a uspořádání dokumentů a složek](organize.md)
- [Úprava velikosti obrázků](images.md)
- [Psaní vzorců](math.md)
- [Kreslení diagramů a grafů](diagrams.md)
