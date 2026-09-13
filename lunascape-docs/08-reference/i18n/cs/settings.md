# Nastavení VS Code

Když v nastavení VS Code (`⌘,` / `Ctrl+,`) vyhledáte „Lunascape Docs“, můžete změnit následující položky. Všechny jsou osobním nastavením jednotlivých uživatelů a neukládají se do dokumentů projektu.

## Kořen dokumentace

| Nastavení | Hodnoty | Výchozí | Funkce |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` automaticky zvolí kořen dokumentace nejbližší otevřenému souboru Markdown; pokud soubor do žádného nepatří, dočasně otevře nadřazenou složku. `fixed` vždy otevře kořen dokumentace uvedený v `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Pole řetězců | `["docs"]` | Názvy složek, které se v režimu `auto` automaticky rozpoznávají jako kořeny dokumentace. Složka se souborem `lunascape-docs.json` se rozpozná bez ohledu na název. Pokud soubor `lunascape-docs.json` přímo v úložišti obsahuje `defaultFolder` nebo `roots`, má přednost |
| `lunascapeDocEditor.root` | Cesta | `docs` | Kořen dokumentace relativní k pracovnímu prostoru pro režim `fixed` nebo pro otevření příkazem |
| `lunascapeDocEditor.startPage` | Cesta | `README.md` | Úvodní stránka relativní ke kořeni dokumentace |
| `lunascapeDocEditor.title` | Řetězec | `Lunascape Docs` | Přepíše název karty dokumentu. Nemá vliv na název zvoleného kořene dokumentace |
| `lunascapeDocEditor.ignoredDirectories` | Pole řetězců | `["99-archive"]` | Názvy složek vyloučených z panelu INDEX |

## Zobrazení

| Nastavení | Hodnoty | Výchozí | Funkce |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` použije bílé pozadí, `auto` se řídí barevným motivem VS Code |
| `lunascapeDocEditor.locale` | Jazyková značka | Není | Váš osobní jazyk dokumentu, který se upřednostní, je-li dostupný. Nemění jazyk originálu v projektu |
| `lunascapeDocEditor.documentMetadata.compact` | Logická hodnota | `true` | Sbalí tabulku správy dokumentu pod nadpisem H1 do řádku „Informace o dokumentu“ |
| `lunascapeDocEditor.tree.showFileNames` | Logická hodnota | `false` | Zobrazí v panelu INDEX názvy souborů místo názvů dokumentů |
| `lunascapeDocEditor.tree.showDocumentIcons` | Logická hodnota | `false` | Zobrazí v panelu INDEX ikony dokumentů |
| `lunascapeDocEditor.tree.showFolderIcons` | Logická hodnota | `false` | Zobrazí v panelu INDEX ikony složek |
| `lunascapeDocEditor.tree.showItemCounts` | Logická hodnota | `false` | Zobrazí v panelu INDEX počet položek přímo ve složce |
| `lunascapeDocEditor.tree.showGuides` | Logická hodnota | `true` | Zobrazí v panelu INDEX vodicí čáry úrovní |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Řádkování panelu INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Logická hodnota | `true` | Pokud existuje jen jeden dokument, zavře panel INDEX pouze při prvním otevření |

## Úpravy

| Nastavení | Hodnoty | Výchozí | Funkce |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Zobrazení úprav, dokud je nepřepnete. Přednost má naposledy použité zobrazení |
| `lunascapeDocEditor.editor.showEditButton` | Logická hodnota | `true` | Zobrazí [Upravit] vpravo dole v textu dokumentu |

## Diagramy

| Nastavení | Hodnoty | Výchozí | Funkce |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Běhové prostředí pro vykreslování TikZ. `bundled` použije přiložené schválené běhové prostředí (v současném distribuovaném sestavení není přiloženo), `workspace` použije `node-tikzjax` 1.0.5 přímo v důvěryhodném pracovním prostoru (pouze pro vývoj a hodnocení), `disabled` nevykreslí nic |

## Zastaralá nastavení

| Nastavení | Použijte místo toho |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` v souboru `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` v souboru `lunascape-docs.json` |

Osobním nastavením nelze přepsat jazyky projektu.

## Související témata

- [Změna nastavení zobrazení](../02-reading/display-settings.md)
- [Konfigurace projektu](../04-document-tools/project-configuration.md)
