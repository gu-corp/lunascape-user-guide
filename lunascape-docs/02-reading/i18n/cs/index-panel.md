# Používání INDEXu

INDEX vlevo je strom složek a dokumentů v kořeni dokumentace.

## Filtrování

1. Do pole [Filtrovat dokumenty] nad INDEXem zadejte slovo.
2. Zobrazí se jen položky, jejichž název odpovídá. Po smazání zadaného textu se zobrazení vrátí do původního stavu.

> **Poznámka**
>
> Během filtrování nelze měnit pořadí přetažením myší.

## Rozbalování a sbalování složek

- Stisknutím šipky vlevo od názvu složky nebo názvu složky bez titulní stránky složku rozbalíte či sbalíte.
- Složka s titulní stránkou (soubor `README.md` nebo `index.md` s obsahem) se po stisknutí názvu otevře na této stránce. Chcete-li ji pouze rozbalit či sbalit, použijte v nabídce položky [Rozbalit složku] / [Sbalit složku].
- Stav rozbalení se pamatuje pro každého uživatele zvlášť a nezapisuje se do souborů sledovaných v Gitu.

## README a titulní stránka složky

`README.md` je soubor, který popisuje obsah dané složky.

- U složky, která má README, se po stisknutí názvu složky zobrazí toto README.
- U složky bez README se zobrazí první dokument uvnitř.
- Nadpis (H1) souboru README se stane názvem složky v INDEXu.

README není povinné. Chcete-li je doplnit později, zvolte v nabídce položky složky [Vytvořit README] (zobrazuje se jen u složek, které je nemají).

## Zobrazení a skrytí INDEXu

- Levou ikonou v ovládání sloupců na panelu nástrojů INDEX zobrazíte či skryjete. Pravá ikona zobrazuje či skrývá „Na této stránce“.
- Na úzké obrazovce začíná INDEX zavřený. Stisknutím [Otevřít INDEX] (tři čáry) vlevo od [Zpět] se INDEX otevře jako překryv nad textem dokumentu. Zavřete jej pomocí [×] uvnitř INDEXu, kliknutím na pozadí, klávesou `Esc` nebo přechodem na jiný dokument. Toto dočasné otevření nemění nastavení pro širokou obrazovku.
- V kořeni dokumentace s jediným zobrazovaným dokumentem se INDEX při prvním otevření automaticky zavře. Znovu jej otevřete ikonou sloupců. Toto chování lze vypnout volbou [Skrýt, když je dokument jen jeden] v [Nastavení zobrazení].

## Používání nabídky položky

Nabídku položky otevřete pomocí [⋯], které se zobrazí po najetí myší na položku v INDEXu, nebo klepnutím pravým tlačítkem na položku. Položky jsou seřazeny takto.

| Skupina | Položky |
|---|---|
| Časté akce | [Rozbalit složku] / [Sbalit složku], [Otevřít INDEX] (otevře titulní stránku složky), [Upravit], [Změnit název], [Otevřít ve VS Code], [Kopírovat cestu] |
| Vytváření a uspořádání | [Vytvořit README] (jen u složek bez něj), [Nový dokument], [Nová složka], [Duplikovat], [Přejmenovat soubor] / [Přejmenovat složku], [Posunout nahoru], [Posunout dolů] |
| Odstranění | [Přesunout do koše] |

- Chcete-li vytvořit položku přímo v kořeni dokumentace, stiskněte [⋯] na pravém konci nadpisu INDEXu nebo klepněte pravým tlačítkem na prázdnou část INDEXu a zvolte [Nový dokument] nebo [Nová složka]. Ve stejné nabídce je [Přejmenovat dokument] a, pokud kořen dokumentace nemá README, také [Vytvořit README]. Stejná nabídka se otevře i po klepnutí pravým tlačítkem na název dokumentu na panelu nástrojů.
- V nabídce se pohybujete klávesami `↑` `↓`, klávesami `Home` `End` přejdete na první a poslední položku. Po zavření klávesou `Esc` se zaměření vrátí tam, kde bylo před otevřením.

> **Poznámka**
>
> Položky pro vytváření, uspořádání a odstranění se zobrazují jen tehdy, je-li pracovní prostor ve VS Code důvěryhodný. Nejsou dostupné ani během úprav dokumentu nebo při zpracování jiné operace v INDEXu.

## Změna vzhledu

V [Nastavení zobrazení] můžete změnit zobrazení názvů souborů, ikon dokumentů a složek, počtu položek ve složce, vodicích čar úrovní a hustoty zobrazení. Podrobnosti najdete v tématu [Změna nastavení zobrazení](display-settings.md).

## Související témata

- [Vytváření a uspořádání dokumentů a složek](../03-editing/organize.md)
- [Změna pořadí dokumentů](../03-editing/reorder.md)
