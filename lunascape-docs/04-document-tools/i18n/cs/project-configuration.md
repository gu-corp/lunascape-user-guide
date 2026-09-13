# Nastavení projektu

Soubor `lunascape-docs.json` přímo v kořeni dokumentace uchovává nastavení daného kořene sdílené v týmu. Spravuje se v Gitu.

## Vytvoření nebo úprava konfiguračního souboru

- Stiskněte [Nástroje dokumentů] na panelu nástrojů → kartu [Kontrola] → [Zdroj pravidel a nastavení dokumentů] → [Upravit nastavení dokumentů] a soubor se otevře ve VS Code. Pokud soubor neexistuje, v tuto chvíli se vytvoří výchozí soubor.
- K názvu souboru `lunascape-docs.json` se automaticky přiřadí přiložené JSON Schema, které nabízí doplňování a popis každé položky. Zápis `$schema` není potřeba.

## Příklad nastavení

```json
{
  "id": "product-docs",
  "title": "Produktová dokumentace",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Popis položek

| Položka | Obsah | Výchozí |
|---|---|---|
| `id` | Klíč, pod kterým se ukládá nastavení zobrazení jednotlivých uživatelů. Přiřaďte pevné ID, chcete-li nastavení zachovat i po přesunu složky | Cesta ke složce |
| `title` | Název zobrazený na levém okraji panelu nástrojů a v seznamu kořenů dokumentace. Nemění se ani při přepnutí jazyka zobrazení | Nadpis README/index kořene, jinak název složky |
| `indexTitle` | Nadpis INDEX | `INDEX` |
| `startPage` | Dokument, který se otevře jako první (relativně ke kořeni dokumentace) | `README.md` |
| `appearance` | Barevné schéma: `light` (vždy světlé) nebo `auto` (řídí se motivem VS Code) | `light` |
| `defaultLocale` | Výchozí jazyk (jazyk originálu). Zadává se jako jazyková značka BCP 47 (`ja`, `en`, `zh-Hant` a podobně). Slouží jako zdroj překladu | Nenastaveno (odhadne se z textu pro zobrazení) |
| `fallbackLocale` | Jazyk, který se jako první zobrazí čtenáři, jehož jazyk prostředí neodpovídá žádnému z podporovaných jazyků. Uveďte jazyk obsažený v `locales` | Nenastaveno (použije se `defaultLocale`) |
| `locales` | Seznam podporovaných jazyků. Zahrňte `defaultLocale`. Objeví se v nabídce jazyků a jsou to cílové jazyky překladu | Pouze `defaultLocale` |
| `ignoredDirectories` | Názvy složek vyloučených z INDEX, vyhledávání a kontrol. Zadáním nahradíte výchozí hodnotu | `["99-archive"]` |
| `tree` | Výchozí hodnoty zobrazení INDEX. Uživatelé je mohou přepsat v nastavení zobrazení | Jako v příkladu výše |
| `editor.defaultMode` | Zobrazení úprav, dokud jej uživatel nepřepne: `visual` nebo `source` | `visual` |
| `editor.showEditButton` | Zda se vpravo dole v dokumentu zobrazí [Upravit] | `true` |
| `documentStandards.pack` | Standard Pack použitý pro kontrolu dokumentů a šablony: `builtin:<název>` nebo cesta relativní ke kořeni dokumentace | Žádný |
| `documentStandards.profile` | Název profilu definovaného balíčkem Pack | Žádný |
| `translation.enabled` | Povolí tvorbu návrhů překladu a hromadný překlad | `true` |
| `translation.contextFiles` | Soubory Markdown originálu (relativně ke kořeni dokumentace) předávané při překladu jako reference k terminologii a stylu | `[]` |
| `translation.maxContextCharacters` | Horní limit celkového počtu znaků referenčních dokumentů (maximálně 1048576) | `49152` |
| `description` | Jednořádkový popis sady dokumentů. Zobrazí se na kartách domovské stránky úložiště. Stejně jako `title` jej lze zapsat jako řetězec nebo jako objekt s jednotlivými jazyky | Žádný |

## Sdělte, kde v úložišti dokumenty jsou

Soubor `lunascape-docs.json` umístěný přímo v kořeni úložiště může místo nastavení dané složky obsahovat **mapu úložiště**. Zapsáním kterékoli ze tří následujících položek se z něj stane mapa a samotná složka pak není kořenem dokumentace.

| Položka | Obsah | Výchozí |
|---|---|---|
| `defaultFolder` | Ve které složce dokumenty jsou (cesta relativní k této složce). Cíl, na který ukazuje, žádné nastavení nepotřebuje | Žádný (použije se `docs`) |
| `roots` | Seznam sad dokumentů, pokud jich máte více (cesty relativní k této složce, v pořadí zobrazení). V tomto případě se z této složky stane domovská stránka | Žádný |
| `excludes` | Složky vyloučené z hledání kořene dokumentace (cesty relativní k této složce). Přičítá se k výchozím vyloučením, jako je `node_modules` | `[]` |
| `home.cards` | Zda se na domovské stránce pod souborem README zobrazí karty sad dokumentů. Pokud si odkazy do README zapíšete sami, nastavte `false` | `true` |

Kořen dokumentace se určuje v následujícím pořadí. Postupuje se shora dolů a použije se první nalezený.

1. Složka, kterou určíte nastavením nebo příkazem
2. Cíl, na který ukazuje `defaultFolder` nebo `roots` v souboru `lunascape-docs.json` přímo v kořeni
3. Složka, ve které je `lunascape-docs.json` (jsou-li pod společným rodičem dvě nebo více, stane se tento rodič domovskou stránkou)
4. Složka `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. Samotný kořen úložiště

> **Tip**
>
> Pokud nic nezapíšete, uplatní se bod 4, takže běžné úložiště s jednou složkou `docs/` funguje jako dosud. Zápis `defaultFolder` použijte jen tehdy, chcete-li složku pojmenovat jinak, například `manual`.

### Příklad mapy

```json
{
  "title": "Nápověda Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Priorita nastavení

Položky týkající se zobrazení mají prioritu v tomto pořadí.

1. Nastavení zobrazení uživatele (panel [Nastavení zobrazení])
2. Nastavení VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Výchozí hodnoty produktu

Výjimkou jsou pouze jazyky (`defaultLocale`, `fallbackLocale`, `locales`): rozhodující je `lunascape-docs.json`. Jazyky projektu nelze přepsat osobním nastavením VS Code.

> **Poznámka**
>
> Standard Pack lze zadat také jako `standard` v souboru `docs-lint.config.json`. Jsou-li přítomny oba, má přednost `docs-lint.config.json`.

## Související témata

- [Změna pravidel kontroly](rules.md)
- [Změna nastavení zobrazení](../02-reading/display-settings.md)
- [Přehled nastavení VS Code](../08-reference/settings.md)
