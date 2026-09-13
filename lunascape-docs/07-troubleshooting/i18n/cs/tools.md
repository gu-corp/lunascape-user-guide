# Kontrola, vytváření nebo překlad se nedaří

## Kontrola

### Zobrazí se „docs-lint není k dispozici“

- Rozšíření neobsahuje běhové prostředí nástroje docs-lint, nebo je problém v nastavení. Přeinstalujte rozšíření.
- „Chcete-li bezpečně načíst místní Pack a nastavení, označte tento pracovní prostor ve VS Code jako důvěryhodný“: k použití místního balíčku Standard Pack je potřeba důvěryhodný pracovní prostor.

### Výsledek zůstává ve stavu „je nutná opětovná kontrola“

Změníte-li dokument nebo nastavení, předchozí výsledek pozbývá platnosti. Stiskněte znovu [Zkontrolovat kořen dokumentace]. Neuložené změny se nezohlední.

### Po stisknutí zjištění se nic neotevře

Položky typu „celý kořen dokumentace“ nejsou vázány na konkrétní dokument, a nemají tedy žádnou pozici. Podle obsahu zjištění zkontrolujte příslušný dokument.

### Pravidla nelze uložit

- Je potřeba důvěryhodný pracovní prostor.
- „Nastavení nástroje Lint bylo změněno jinou operací“: soubor `docs-lint.config.json` byl změněn zvenčí. Načtěte nejnovější stav a zkuste to znovu.
- Symbolické odkazy a soubory nastavení mimo kořen dokumentace nelze upravovat.

## Vytváření ze šablony

- „Náhled šablony vypršel“ / „Zadané údaje byly změněny“: před vytvořením stiskněte znovu [Náhled].
- „Dokument v cílovém umístění již existuje“: existující soubory se nepřepisují. Zadejte jiné cílové umístění.
- Cílové umístění vyžaduje cestu relativní ke kořeni dokumentace a příponu `.md` nebo `.mdx`. Ve složce `i18n` nelze dokumenty vytvářet.
- „Chcete-li vytvářet dokumenty, označte pracovní prostor jako důvěryhodný“: označte pracovní prostor ve VS Code jako důvěryhodný.

<!-- ai-only:start -->
## Překlad

### Tlačítka překladu nelze stisknout

- „Pro tento kořen dokumentace není povolen překlad pomocí AI“: nastavte `translation.enabled` v souboru `lunascape-docs.json` na `true`.
- „Výchozí jazyk projektu není nastaven“: uložte výchozí jazyk podle části [Změna nastavení zobrazení](../02-reading/display-settings.md).
- „Přidejte cílový jazyk mezi podporované jazyky“: přidejte cílový jazyk do `locales`.
- „Nebyl nalezen originál k překladu“: máte otevřenou přeloženou stránku. Přepněte na stránku ve výchozím jazyce.
- Při dočasném zobrazení složky nelze hromadný překlad použít. Vložte do složky soubor `lunascape-docs.json` a udělejte z ní kořen dokumentace.

### Návrh překladu je odmítnut nebo je vyžadováno jeho nové vytvoření

- „Originál byl změněn. Vytvořte návrh překladu znovu“: po vytvoření návrhu se změnil originál nebo cílový dokument. Přeložte znovu.
- Pokud v odpovědi jazykového modelu chybí chráněné identifikátory nebo kód, odpověď se nepřijme. Obsah odpovědi si můžete prohlédnout v panelu výstupu „Lunascape Docs Překlad“.
- „Hromadný překlad zpracuje najednou nejvýše 1000 dokumentů“: rozdělte rozsah po složkách nebo výslovným výběrem.
<!-- ai-only:end -->

## Související témata

- [Kontrola dokumentů](../04-document-tools/check.md)
- [Vytvoření dokumentu ze šablony](../04-document-tools/templates.md)
- [Předání práce AI](../05-ai/README.md)
