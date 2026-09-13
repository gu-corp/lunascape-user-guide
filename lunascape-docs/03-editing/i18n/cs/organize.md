# Vytváření a organizace dokumentů a složek

V nabídce položky v panelu INDEX můžete vytvářet, duplikovat, přejmenovávat a mazat dokumenty a složky. Zadávání probíhá v malém dialogu uvnitř prohlížeče, aniž by se přerušilo čtení.

> **Poznámka**
>
> Tyto operace jsou dostupné pouze tehdy, když je pracovní prostor ve VS Code důvěryhodný. Nelze je provést během úprav dokumentu, během zpracování jiné operace ani tehdy, když má cíl neuložené změny.

## Vytvoření dokumentu nebo složky

1. Otevřete nabídku položky ([⋯] nebo pravé tlačítko myši) u cílové složky.
   Chcete-li vytvořit položku přímo v kořeni dokumentace, použijte [⋯] na pravém okraji záhlaví panelu INDEX nebo klikněte pravým tlačítkem na prázdné místo v panelu INDEX.
2. Zvolte [Nový dokument] nebo [Nová složka].
3. Zadejte název a stiskněte [Vytvořit].
   Název dokumentu musí mít příponu formátu Markdown (`.md`, `.markdown`, `.mdx` a podobně).

Nové dokumenty se vytvářejí jako dokumenty ve výchozím jazyce (originály).

## Duplikování dokumentu

1. Otevřete nabídku položky u dokumentu a zvolte [Duplikovat].
2. Zadejte nový název a stiskněte [Vytvořit].

Duplikuje se pouze originál. Jeho překlady se neduplikují.

## Změna názvu

Změní nadpis dokumentu (H1). Název souboru zůstane stejný.

1. Otevřete nabídku položky u dokumentu nebo složky a zvolte [Změnit název].
2. Zadejte nový název na jeden řádek a stiskněte [Změnit].

U složky se změní nadpis jejího souboru `README.md`. Pokud je zobrazen překlad, změní se název dokumentu v daném jazyce.

## Změna názvu dokumentace

Změní název dokumentace zobrazený na panelu nástrojů (název kořene dokumentace).

1. Klikněte pravým tlačítkem na název dokumentace na panelu nástrojů. Stejnou nabídku otevřete také pomocí [⋯] na pravém okraji záhlaví panelu INDEX.
2. Zvolte [Přejmenovat dokument] a zadejte nový název.

Dokud není nastaven, zobrazuje se název složky tak, jak je.

Zadaný název se zapíše **tam, odkud se název dokumentace právě bere**, takže nadpis, který vidíte, nikdy nezůstane ignorovaný.

| Současný stav | Zapíše se do |
|---|---|
| `lunascape-docs.json` obsahuje název | Aktualizuje se `lunascape-docs.json` |
| Název chybí, ale kořen dokumentace má README | Přepíše se nadpis (H1) v souboru README |
| Ani jedno | Vytvoří se `lunascape-docs.json` a název se uloží do něj |

Zpráva zobrazená po změně uvádí, kam se zápis provedl.

> **Tip**
>
> Název dokumentace se určuje v tomto pořadí: název v souboru `lunascape-docs.json`, poté nadpis souboru README v kořeni dokumentace, poté název složky.

## Přejmenování souboru nebo složky

1. Otevřete nabídku položky a zvolte [Přejmenovat soubor] nebo [Přejmenovat složku].
2. Zadejte nový název a stiskněte [Změnit].

Odpovídající překlady (stejná cesta pod `i18n/<jazyk>/`) se přejmenují společně s ním.

## Smazání

1. Otevřete nabídku položky a zvolte [Přesunout do koše].
2. Zkontrolujte obsah potvrzovací zprávy a přesun potvrďte.

Cíl se přesune do koše operačního systému, takže jej lze v případě potřeby obnovit. Překlady se nemažou a zůstávají na svém místě.

## Názvy, které nelze použít

- Názvy začínající tečkou `.` (nezobrazily by se v panelu INDEX)
- `i18n` (vyhrazeno pro soubory překladů)
- Názvy vyhrazené systémem Windows (`CON`, `PRN` a podobně)
- Názvy končící tečkou nebo mezerou
- Názvy obsahující řídicí znaky nebo znaky nepovolené v názvech souborů
- Názvy, které se ve stejné složce již vyskytují (včetně názvů lišících se pouze velikostí písmen)

> **Poznámka**
>
> Úvodní stránku (obvykle `README.md` v kořeni) nelze přejmenovat ani přesunout. Nejprve změňte `startPage` v souboru `lunascape-docs.json`.

## Související témata

- [Změna pořadí dokumentů](reorder.md)
- [Používání panelu INDEX](../02-reading/index-panel.md)
