# Práce, které lze předat

Vyberte je v kartě [AI] pod položkou [Práce]. Pro každou práci se liší předávané pokyny i následná kontrola.

| Práce | Obsah | Co je potřeba | Typ API |
|---|---|---|---|
| Přeložit tuto stránku | Přeloží zobrazený dokument do zvoleného jazyka | Otevřený cílový dokument, cílový jazyk | ○ |
| Přeložit vše nepřeložené | Postupně přeloží nepřeložené a neaktuální dokumenty zvoleného jazyka | Cílový jazyk | Pouze typ relace |
| Zkorigovat tuto stránku | Zkontroluje a opraví terminologii, styl a členění kapitol, které vyžaduje standard dokumentu | Otevřený cílový dokument | ○ |
| Vytvořit nový dokument | Vytvoří nový dokument podle standardu dokumentu a šablon | Téma (nepovinné) | Pouze typ relace |

## Co pokyny obsahují

| Č. | Obsah |
|---|---|
| 1 | Umístění kořene dokumentace. S pokynem nic mimo něj neměnit |
| 2 | Výchozí jazyk (originál) a umístění překladů (složka `i18n/<jazyk>/` vedle dokumentu) |
| 3 | Že `navigation.order` patří pouze originálu a že překlad smí přepsat jedině `navigation.title` |
| 4 | Že se nesmí měnit ID požadavků, odkazy, kód, Mermaid, TeX ani struktura front matter |
| 5 | Standard dokumentu a slovník (`terminology` v souboru `docs-lint.config.json`) |
| 6 | Že se po dokončení má spustit kontrola dokumentu, nahlásit změněné soubory a neprovádět žádné operace Git |

> **Tip**
>
> Cíle pro „Přeložit vše nepřeložené“ vznikají z evidence a na jedno spuštění jich je nejvýše 200. Pokud je jich více, spusťte práci opakovaně.

## Související témata

- [Předání práce AI](README.md)
- [Evidence a záznamy](ledger.md)
