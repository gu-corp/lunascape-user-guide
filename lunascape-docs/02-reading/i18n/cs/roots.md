# Přepnutí kořene dokumentace

Kořen dokumentace je nejvyšší složka jedné sady dokumentů. INDEX, filtrování, kontrola i překlad pracují vždy v rámci jednoho kořene dokumentace.

## Jak se kořen dokumentace najde

Lunascape Docs postupuje od otevřeného souboru Markdown po nadřazených složkách a jako kořen dokumentace použije nejbližší složku, která odpovídá jedné z těchto podmínek.

- Složka obsahující soubor `lunascape-docs.json` (na názvu složky nezáleží)
- Složka s názvem `docs` (další názvy lze přidat nastavením `lunascapeDocEditor.rootDirectoryNames`)

Když spustíte příkaz [Lunascape Docs: Otevřít prohlížeč specifikací], otevře se kořen dokumentace podle nastavení `lunascapeDocEditor.root` (výchozí hodnota `docs`).

## Přepnutí na jiný kořen dokumentace

Pokud je v pracovním prostoru více kořenů dokumentace, změní se název kořene na levém okraji panelu nástrojů v rozevírací seznam.

1. Stiskněte název kořene dokumentace na levém okraji panelu nástrojů.
2. V seznamu vyberte kořen dokumentace.
   Zobrazí se úvodní stránka vybraného kořene dokumentace a INDEX se přepne.

> **Tip**
>
> Názvy v seznamu se určují v tomto pořadí. Při přepnutí jazyka zobrazení se nemění.
>
> 1. `title` v souboru `lunascape-docs.json`
> 2. `navigation.title` v souboru `README.md` v kořeni, jinak jeho nadpis H1
> 3. `navigation.title` v souboru `index.md` v kořeni, jinak jeho nadpis H1
> 4. Název složky (u standardní složky `docs` název její nadřazené složky)

## Otevření souboru Markdown mimo kořen dokumentace

Když otevřete soubor Markdown, který není v žádném kořeni dokumentace, zobrazí se složka s tímto souborem jako dočasný kořen dokumentace. V panelu INDEX se vypíší soubory Markdown z této složky a ze složek pod ní.

- Stisknutím tlačítka [O složku výš] na panelu nástrojů rozšíříte rozsah zobrazení až na nadřazenou složku v pracovním prostoru.
- V tomto zobrazení nelze použít jazyková nastavení projektu ani hromadný překlad. Budou dostupná, jakmile do složky umístíte soubor `lunascape-docs.json` a uděláte z ní kořen dokumentace.

## Trvalé otevírání jednoho kořene dokumentace

Když nastavení `lunascapeDocEditor.rootMode` nastavíte na `fixed`, otevře se vždy kořen dokumentace podle `lunascapeDocEditor.root` bez ohledu na to, který soubor Markdown otevřete.

## Související témata

- [Kořeny dokumentace a konvence souborů](../04-document-tools/structure.md)
- [Nastavení projektu](../04-document-tools/project-configuration.md)
- [Přehled nastavení VS Code](../08-reference/settings.md)
