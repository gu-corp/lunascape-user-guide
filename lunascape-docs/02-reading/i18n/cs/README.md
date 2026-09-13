# Základní operace

Základní operace od otevření dokumentů až po přechod na stránku, kterou si chcete přečíst.

## Otevření dokumentů

1. Otevřete úložiště ve VS Code.
2. V paletě příkazů (`⇧⌘P` / `Ctrl+Shift+P`) spusťte příkaz „Lunascape Docs: Otevřít prohlížeč specifikace“.
   Vyhledá se nejbližší kořen dokumentace (ve výchozím nastavení složka `docs`) a zobrazí se jeho úvodní stránka.

> **Tip**
>
> - Klepněte pravým tlačítkem na soubor Markdown v Průzkumníku a zvolte [Lunascape Docs: Otevřít v prohlížeči specifikace] – dokumenty se otevřou od tohoto souboru.
> - Když otevřete soubor Markdown, který nepatří do žádného kořene dokumentace, zobrazí se jeho složka jako dočasný kořen dokumentace.

## Přechod mezi stránkami

| Operace | Postup |
|---|---|
| Otevření z obsahu | Stiskněte název dokumentu v panelu INDEX vlevo |
| Přechod po odkazu | Stiskněte odkaz v textu. Otevře se ve stejném zobrazení |
| Procházení historie | [Zpět] a [Vpřed] na panelu nástrojů nebo `Alt`+`←` / `Alt`+`→` |
| Návrat na úvodní stránku | [Úvodní stránka specifikace] na panelu nástrojů |
| Přechod o úroveň výš | [Nadřazený INDEX] na panelu nástrojů nebo položka v popisu cesty |
| Přechod v rámci stránky | Stiskněte nadpis v panelu „Na této stránce“ vpravo |

## Vyhledání dokumentu

Zadejte slovo do pole [Filtrovat dokumenty] nad panelem INDEX a zobrazí se pouze dokumenty, jejichž název odpovídá. Po vymazání pole se zobrazí zase všechny.

## Aktualizace na nejnovější obsah

Když uložíte soubor Markdown v editoru VS Code, zobrazení se aktualizuje automaticky. Pokud jste soubory změnili externím nástrojem, stiskněte [Znovu načíst] na panelu nástrojů.

> **Poznámka**
>
> - Externí odkazy v textu (`https://` a podobně) se otevírají ve výchozím prohlížeči. Odkazy na soubory mimo kořen dokumentace se neotevřou.
> - Prohlížené dokumenty se zpracovávají ve vašem zařízení. Pro čtení dokumentu se nikam nic neodesílá.

## Související témata

- [Používání panelu INDEX](index-panel.md)
- [Přepínání kořenů dokumentace](roots.md)
- [Úprava dokumentu](../03-editing/README.md)
