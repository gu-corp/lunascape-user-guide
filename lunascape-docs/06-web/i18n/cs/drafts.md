# Uložení konceptu

Když upravíte dokument ve webové verzi, změny se nezapíší do úložiště, ale uloží se v prohlížeči jako „koncept“.

## Vytvoření konceptu

1. Otevřete dokument a vpravo dole stiskněte [Upravit].
2. Proveďte úpravy a stiskněte [Uložit].
   Zobrazí se „Uloženo jako koncept“ a změna se uloží v prohlížeči.

- Dokumenty s konceptem mají v INDEX odznak. Nad textem se zobrazí „Tento dokument je koncept v tomto zařízení (nepublikováno)“.
- Položka [Koncepty] na panelu nástrojů zobrazuje počet a po stisknutí otevře seznam konceptů.

## Zahození konceptu

- Koncept jednoho dokumentu zahodíte stisknutím [Zahodit koncept] nad textem.
- Všechny koncepty zahodíte ze seznamu konceptů.

## Promítnutí do úložiště

„Žádost o publikování“, která odešle koncepty jako pull request, je sice implementovaná, ale ve veřejném prohlížeči není povolená. Chcete-li změnit úložiště, upravte dokument ve verzi pro VS Code nebo v místním klonu.

> **Poznámka**
>
> - Koncepty se ukládají v prohlížeči (IndexedDB). Nepřenášejí se do jiného prohlížeče ani do jiného zařízení. Vymazáním dat webu v prohlížeči se koncepty smažou.
> - Pokud se dokument v úložišti změní poté, co jste vytvořili koncept, zobrazí se „Zdroj byl aktualizován“. Zkontrolujte obsah a rozhodněte, zda koncept zahodíte, nebo jej ponecháte.
> - Pokud upravujete místní složku otevřenou přes [Otevřít dokumenty], změny se zapisují přímo do souboru, jestliže to prohlížeč podporuje. V prohlížečích bez této podpory se uchovají jen po dobu dané relace.

## Související témata

- [Co umí webová verze](README.md)
- [Úprava dokumentu](../03-editing/README.md)
