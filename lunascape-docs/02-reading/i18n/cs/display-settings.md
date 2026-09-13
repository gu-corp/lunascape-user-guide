# Změna nastavení zobrazení

Pomocí [Nastavení zobrazení] (ozubené kolo) na panelu nástrojů může každý uživatel změnit vzhled panelu INDEX a zobrazení tlačítka úprav.

1. Na panelu nástrojů stiskněte [Nastavení zobrazení].
2. Přepněte položky, které chcete změnit. Změny se projeví okamžitě.
3. Panel zavřete opětovným stisknutím [Nastavení zobrazení] nebo klepnutím mimo něj.

## Položky, které lze nastavit

| Oddíl | Položka | Funkce |
|---|---|---|
| Jazyk dokumentu | (aktuální stav) | Zobrazuje výchozí jazyk projektu a právě zobrazený jazyk. Volba [Nastavit jazyky projektu…] otevře nastavení jazyků projektu |
| Obsah | [Názvy souborů] | Místo názvů dokumentů zobrazuje názvy souborů |
| | [Ikony dokumentů] | Zobrazuje ikonu u položek dokumentů |
| | [Ikony složek] | Zobrazuje ikonu u položek složek |
| | [Počty položek] | Zobrazuje počet dokumentů obsažených ve složce |
| | [Vodítka odsazení] | Zobrazuje vodicí čáry znázorňující úrovně |
| | [Skrýt, když je dokument jen jeden] | V kořeni dokumentace s jediným dokumentem zavře INDEX automaticky, ale jen při prvním otevření |
| | [Sbalit údaje o dokumentu] | Sbalí správní tabulku v záhlaví dokumentu do řádku „Údaje o dokumentu“. Když je vypnuto, tabulka se zobrazuje tak, jak je |
| | [Hustota zobrazení] | Řádkování panelu INDEX vyberete z možností [Standardní] / [Kompaktní] |
| | [Tlačítko úprav] | Zobrazuje tlačítko [Upravit] vpravo dole u textu dokumentu |
| Akce | [Obnovit výchozí nastavení projektu] | Odstraní všechny uživatelské změny a vrátí nastavení projektu |
| | [Otevřít nastavení rozšíření] | Otevře nastavení Lunascape Docs v okně nastavení VS Code |

> **Tip**
>
> - Nastavení zobrazení se ukládá zvlášť pro každého uživatele a každý kořen dokumentace a nezapisuje se do souborů spravovaných v Gitu.
> - Nastavení se uplatňuje v pořadí „nastavení zobrazení uživatele → nastavení VS Code → `lunascape-docs.json` → výchozí nastavení produktu“. Výchozí hodnoty společné pro celý tým se určují v položkách `tree` a `editor` v souboru `lunascape-docs.json`.

## Přepnutí barevného schématu

Stisknutím přepínače motivu (slunce/měsíc) na panelu nástrojů přepnete mezi bílým pozadím a barevným schématem VS Code. Schéma použité po otevření určuje nastavení `lunascapeDocEditor.appearance` (`light` nebo `auto`).

## Související témata

- [Používání panelu INDEX](index-panel.md)
- [Nastavení projektu](../04-document-tools/project-configuration.md)
- [Přehled nastavení VS Code](../08-reference/settings.md)
