# Úprava dokumentu

Dokumenty lze upravovat přímo v prohlížeči. Editor nabízí „vizuální zobrazení“, kde upravujete to, co vidíte, a „zobrazení zdroje Markdown“; mezi oběma se přepíná jedním tlačítkem.

## Zahájení úprav

Stiskněte kteroukoli z následujících možností. Všechny otevřou stejný editor.

- [Upravit] vpravo dole u textu
- [⋯] (další akce) vpravo nahoře u textu → [Upravit]
- Nabídka položky v INDEX → [Upravit]

## Úpravy

1. Upravujte text přímo.
   Na panelu nástrojů v horní části editoru máte k dispozici formát odstavce (běžný text, nadpisy 1–4, citace, kód), [Tučné], [Kurzíva], [Odrážkový seznam], [Číslovaný seznam], [Odkaz], [Vložit tabulku], [Šířka obrázku], [Zpět] a [Znovu].
2. Chcete-li upravovat zdroj Markdown přímo, stiskněte [Markdown].
   Dalším stisknutím se vrátíte do vizuálního zobrazení. Naposledy použité zobrazení se zapamatuje a obnoví se při příštím stisknutí [Upravit].
3. Stiskněte [Uložit] (uložit lze také pomocí Ctrl+S / ⌘S).
   Zapíše se do souboru Markdown a zobrazení se vrátí do režimu čtení. Chcete-li úpravy ukončit a vrátit se k naposledy uloženému obsahu, stiskněte [Zahodit úpravy].

## Vždy začínat v editoru (režim úprav)

Stiskněte na panelu nástrojů [Režim úprav] a zapněte jej: od té chvíle se každý dokument otevře v editoru, tak jako poznámkový blok. Použijte jej, když spíše píšete než čtete.

- Když je zapnutý, stisknutí [Uložit] editor nezavře. [Zahodit úpravy] se vrátí k naposledy uloženému obsahu a editor ponechá otevřený.
- Dalším stisknutím jej vypnete a vrátíte se do režimu čtení. Zapnutí/vypnutí se zapamatuje pro každého uživatele.
- U kořene dokumentace, do kterého nelze zapisovat (například úložiště GitHub jen ke čtení), se nezobrazuje.

## Neuložené úpravy

Úpravy, které jste neuložili, se v tomto zařízení automaticky uchovávají. Přechodem k jinému dokumentu ani zavřením karty či okna se neztratí.

- [Neuloženo] v editoru znamená, že se text liší od naposledy uloženého obsahu.
- Při příštím otevření stejného dokumentu se pokračuje z uchovaných úprav a upozorní vás na to. Pokud se samotný dokument mezitím změnil, upozorní i na to; pomocí [Zahodit úpravy] se vrátíte k nejnovějšímu obsahu.
- Uchované úpravy zmizí po stisknutí [Uložit] nebo [Zahodit úpravy]. Nic nebylo uloženo, takže se neobjeví v Git ani mezi koncepty.

> **Poznámka**
>
> - Uložení pouze zapíše soubor. Přidání do fáze (staging) ani odevzdání (commit) v Git se nikdy neprovádí automaticky.
> - Vzorce a diagramy jako Mermaid, TikZ a Vega-Lite se ve vizuálním zobrazení zobrazují vykreslené. Chcete-li změnit jejich obsah, přepněte na [Markdown].
> - Dokumenty obsahující syntaxi specifickou pro MDX (komponenty, `import` a podobně) se kvůli zachování této syntaxe upravují pouze v zobrazení Markdown.
> - Front matter (blok ohraničený řádky `---` na začátku) zůstane zachován, i když upravujete ve vizuálním zobrazení.

> **Tip**
>
> - [Otevřít ve VS Code] otevře soubor v běžném textovém editoru. Uložení v něm automaticky aktualizuje zobrazení v prohlížeči.
> - Chcete-li tlačítko [Upravit] skrýt, vypněte [Tlačítko úprav] v [Nastavení zobrazení]. Chcete-li je skrýt pro celý projekt, nastavte v souboru `lunascape-docs.json` hodnotu `editor.showEditButton` na `false`.
> - Výchozí počáteční zobrazení (vizuální nebo Markdown) lze změnit nastavením `lunascapeDocEditor.editor.defaultMode` nebo hodnotou `editor.defaultMode` v souboru `lunascape-docs.json`.

## Související témata

- [Vytváření a organizace dokumentů a složek](organize.md)
- [Úprava velikosti obrázků](images.md)
- [Psaní vzorců](math.md)
- [Kreslení diagramů a grafů](diagrams.md)
