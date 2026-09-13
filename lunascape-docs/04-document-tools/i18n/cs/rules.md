# Změna pravidel kontroly

U každé kontroly můžete změnit úroveň upozornění (chyba, varování, informace) nebo ji vypnout. Změny se ukládají do souboru `docs-lint.config.json` v kořeni dokumentace a sdílejí se s týmem.

## Změna úrovně upozornění

1. Na panelu nástrojů stiskněte [Nástroje dokumentů] a otevřete kartu [Kontrola].
2. Stiskněte [Zkontrolovat a změnit pravidla].
   Ve stejné kartě se rozbalí seznam kontrol. U každé položky se zobrazí její účel a zdroj aktuálního nastavení (Project, Profile, Pack nebo Default).
3. Zvolte úroveň upozornění u položky, kterou chcete změnit.
4. Stiskněte [Uložit a zkontrolovat znovu].
   Nastavení se uloží a celý kořen dokumentace se znovu zkontroluje s novým nastavením.

| Možnost | Význam |
|---|---|
| [Standardní nastavení (…)] | Odstraní přepsání a vrátí se ke standardnímu nastavení, které se určí v pořadí profil, Standard Pack a výchozí hodnota |
| [Nepoužívat] | Tuto položku nekontroluje |
| [Informace] / [Varování] / [Chyba] | Hlásí na této úrovni upozornění |

> **Poznámka**
>
> - Uložení vyžaduje důvěryhodný pracovní prostor.
> - Ukládá se pouze úroveň upozornění jednotlivých položek. Možnosti jednotlivých položek zůstávají beze změny. Standard Pack ani samotný profil se na této obrazovce nemění.
> - Pokud byl soubor `docs-lint.config.json` těsně před uložením změněn zvenčí, uložení se přeruší. Načtěte nejnovější stav a zkuste to znovu.
> - Pokud soubor `docs-lint.config.json` neexistuje, vytvoří se při uložení.

## Přímá úprava konfiguračních souborů

- Stisknutím [Otevřít podrobná nastavení] otevřete soubor `docs-lint.config.json` ve VS Code.
- Otevřete [Zdroj pravidel a nastavení dokumentů] a stiskněte [Upravit nastavení dokumentů]; tím otevřete soubor `lunascape-docs.json` ve VS Code. Standard Pack a profil se volí zde.

U obou souborů je k dispozici doplňování a popisy podle schémat JSON Schema dodávaných s rozšířením.

## Standard Pack a profily

Standard Pack je standard dokumentace, který shrnuje požadované typy dokumentů, členění kapitol, terminologii a šablony. Volí se pomocí `documentStandards` v souboru `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Dodávaný pack `builtin:gu-corp-software` obsahuje profily `base`, `web-application`, `api-service`, `regulated-financial-product` a `smart-contract`.

## Související témata

- [Kontrola dokumentů](check.md)
- [Nastavení projektu](project-configuration.md)
