# Nelze upravovat, ukládat ani měnit pořadí

## Chybí tlačítko [Upravit]

- V [Nastavení zobrazení] je vypnuto [Tlačítko úprav]. Zapněte je, nebo použijte [⋯] → [Upravit] vpravo nahoře nad textem, případně nabídku položky v INDEX → [Upravit].
- Totéž platí, když je `editor.showEditButton` v souboru `lunascape-docs.json` nastaveno na `false`.
- Během zobrazení nápovědy nelze upravovat. Zavřete nápovědu.

## Nelze přepnout do vizuálního zobrazení

„Tento dokument obsahuje syntaxi MDX, proto jej nelze přepnout do běžného editačního zobrazení“: dokumenty se syntaxí specifickou pro MDX (komponenty, `import` a podobně) se upravují pouze v zobrazení Markdown, aby tato syntaxe zůstala zachována.

## Nelze přímo upravit vzorce ani diagramy

Vizuální zobrazení ukazuje výsledek vykreslení. V editačním zobrazení stiskněte [Markdown] a upravte zdrojový text.

## Nelze měnit pořadí ani přetahovat

- Pořadí nelze měnit během filtrování, během úprav dokumentu a během zpracování jiné operace v INDEX.
- Pokud pracovní prostor není důvěryhodný, nejsou dostupné akce vytváření, uspořádání ani odstranění. Označte pracovní prostor ve VS Code jako důvěryhodný.
- „INDEX byl aktualizován. Přetáhněte položku znovu.“: právě se projevila jiná změna. Proveďte operaci znovu.
- Úvodní stránku (kořenový soubor `README.md`) nelze přesunout.

## Zobrazí se „Máte neuložené změny“

Cílový soubor se právě upravuje v editoru VS Code. Nejprve změny uložte nebo zahoďte a akci zopakujte.

## Nelze změnit název

Následující názvy nelze použít.

- Názvy začínající na `.`, název `i18n` a vyhrazené názvy systému Windows (například `CON`)
- Názvy končící tečkou nebo mezerou a názvy obsahující řídicí znaky či znaky nepovolené v názvech souborů
- Názvy, které už ve stejné složce existují (včetně názvů lišících se pouze velikostí písmen)
- Názvy dokumentů bez přípony Markdown

## Změny jsem uložil, ale v Gitu se neobjeví nebo se nezapíšou

Lunascape Docs pouze zapisuje do souboru; neprovádí v Gitu přípravu ke commitu ani commit. Zkontrolujte zobrazení správy zdrojového kódu ve VS Code a podle potřeby změny commitněte.

## Související témata

- [Úprava dokumentu](../03-editing/README.md)
- [Vytváření a uspořádání dokumentů a složek](../03-editing/organize.md)
- [Změna pořadí dokumentů](../03-editing/reorder.md)
