# Čtení v jiném jazyce

Dokument, který má překlad, můžete číst v jiném jazyce přepnutím jazyka v jazykové nabídce (glóbus) na panelu nástrojů.

## Přepnutí jazyka

1. Stiskněte jazykovou nabídku na panelu nástrojů.
   Zobrazí se jazyk aktuální stránky a důvod jeho určení (cesta k překladu, automatická detekce nebo výchozí jazyk projektu).
2. Vyberte jazyk, ve kterém chcete číst.
   Otevře se překlad téhož dokumentu. Zvolený jazyk se zapamatuje a další dokument, který otevřete, se zobrazí v tomto jazyce, pokud pro něj překlad existuje.

V seznamu jazyků je u každého jazyka uvedeno, zda pro tento dokument existuje překlad.

| Zobrazení | Význam |
|---|---|
| Přeloženo | Překlad existuje a lze jej otevřít |
| Nepřeloženo | Jazyk je projektem podporován, ale tento dokument zatím nemá překlad |
| Neaktuální | Překlad existuje, ale zdrojový dokument se po přeložení změnil |

> **Poznámka**
>
> - Výběrem jazyka pouze otevřete existující překlad. Nikdy se tím nevygeneruje překlad ani nevytvoří soubor. Chcete-li překlad vytvořit, použijte ve stejné nabídce [Vytvořit nebo spravovat překlady…].
> - Když se zjistí, že se jazyk aktuální stránky liší od výchozího jazyka projektu, zobrazí se upozornění. Konfigurace se nikdy nepřepíše.

## Jazyk zobrazený jako první

Když otevřete dokument, jazyk, ve kterém se zobrazí jako první, se určí v tomto pořadí.

1. Jazyk, který jste dříve sami vybrali v tomto kořeni dokumentace. Vaše volba se uloží (i výběr výchozího jazyka se uloží jako volba).
2. Jazyk zobrazení VS Code (ve webovém prohlížeči jazyková nastavení prohlížeče). Automaticky se vybere odpovídající podporovaný jazyk; jazyk s oblastí, například `en-US`, odpovídá i svému základnímu jazyku `en`.
3. Záložní jazyk projektu (`fallbackLocale` v `lunascape-docs.json`).
4. Výchozí jazyk projektu.

> **Tip**
>
> - Když byl jazyk vybrán automaticky, u aktuálního jazyka v jazykové nabídce se zobrazí odznak „Automaticky vybráno". Najeďte na něj ukazatelem a zobrazí se důvod.
> - `fallbackLocale` je jazyk zobrazený čtenářům, jejichž jazyk prostředí neodpovídá žádnému z podporovaných jazyků. V projektu, jehož originál je v japonštině a má anglický překlad, nastavení `"en"` otevře anglickou verzi například čtenáři ve španělském prostředí. Pokud není nastaven, použije se výchozí jazyk.

## Kde se ukládají překlady

Dokumenty ve výchozím jazyce zůstávají na svém místě; překlad se ukládá do **složky `i18n/<jazyk>/` ve stejné složce**, pod stejným názvem souboru.

```text
docs/
  README.md                  ← výchozí jazyk (například japonština)
  i18n/en/README.md          ← jeho anglický překlad
  guide/
    setup.md
    i18n/en/setup.md         ← jeho anglický překlad
```

> **Poznámka**
>
> - Znovuvytvoření struktury složek pod `i18n/` (`i18n/en/guide/setup.md`) není rozpoznáno. Složka `i18n/` je vždy umístěna vedle dokumentu, který překládá.
> - Toto je jediné místo, ze kterého se překlad načítá. Když překlad téhož dokumentu umístíte i do `i18n/` v nadřazené složce, nevznikne žádný konflikt o tom, „která má přednost": taková kopie se jednoduše stane osiřelým souborem, který se neobjeví ani v jazykové nabídce, ani v rejstříku (a nikdy se automaticky nesmaže). Neumisťujte stejný překlad na dvě místa.

## Čtení ve webovém prohlížeči

I ve webovém prohlížeči můžete jazyky přepínat stejným způsobem, pokud překlad existuje. Chcete-li číst v jazyce, pro který překlad není, můžete použít funkci překladu stránky ve svém prohlížeči. Kód, vzorce a diagramy jsou z překladu vyňaty.

## Související témata

- [Předání práce AI](../05-ai/README.md)
- [Práce, kterou lze předat](../05-ai/tasks.md)
- [Změna nastavení zobrazení](../02-reading/display-settings.md)
