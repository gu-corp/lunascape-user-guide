# Evidence a záznamy

Evidence v horní části karty [AI] ukazuje stav překladu pro každý podporovaný jazyk. I bez použití AI si v ní ověříte, co chybí.

| Zobrazení | Význam |
|---|---|
| Nepřeloženo | Počet dokumentů, které zatím nemají překlad |
| Neaktuální | Počet dokumentů, jejichž překlad existuje, ale originál je novější než zaznamenaný stav |
| Přeloženo | Počet překladů, které odpovídají originálu |

Evidence se vypočítá procházením kořene dokumentace. Nepodílí se na tom AI ani jazykový model.

## Aktualizace záznamů o překladu

Aby bylo možné určit stav „Neaktuální“, je třeba mít zaznamenaný originál a překlad ve stavu, v jakém byly v okamžiku překladu. Relační (session) AI zapisuje soubory přímo, takže se záznam nevytvoří automaticky.

1. Až je překlad hotový a obsah zkontrolovaný, stiskněte [Aktualizovat záznamy o překladu].
2. Překlady bez záznamu se zaznamenají jako odpovídající aktuálnímu originálu.

Relace Claude Code a ukládání přes API zaznamenávají tento stav automaticky (relace dostane pokyn použít nástroj MCP `record_translation_freshness`). Toto tlačítko potřebujete tehdy, když jste překládali pomocí Codex nebo chatu ve VS Code.

Od té chvíle se při každé změně originálu jeho překlad zobrazí jako „Neaktuální“.

> **Poznámka**
>
> - Překlady, které již záznam mají, se nepřepisují. Nedojde tak ke smazání stavu „Neaktuální“.
> - Záznamy se ukládají do `.lunascape-docs/translation-freshness.json`. Ukládá se pouze relativní cesta, jazyk, hash obsahu a datum a čas – nikoli text dokumentu.

## Související témata

- [Práce, kterou lze předat](tasks.md)
- [Čtení v jiném jazyce](../02-reading/languages.md)
