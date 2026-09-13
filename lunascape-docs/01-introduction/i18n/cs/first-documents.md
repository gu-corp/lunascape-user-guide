# Vytvoření prvních dokumentů

V projektu, který ještě nemá složku s dokumentací, můžete vytvořit počáteční sadu dokumentů z palety příkazů.

1. Otevřete složku projektu ve VS Code a označte pracovní prostor jako důvěryhodný.
2. V paletě příkazů (`⇧⌘P` / `Ctrl+Shift+P`) spusťte příkaz „Lunascape Docs: Vytvořit dokumentaci ze šablony".
   Pokud pracovní prostor obsahuje více složek, vyberte tu, ve které se mají dokumenty vytvořit.
3. Vyberte strukturu, která se má vytvořit.
   - [Jednostránkový dokument]: pouze `README.md`. Vhodné pro krátkou specifikaci, poznámky nebo samostatný výkladový dokument.
   - [Sada dokumentace]: úvodní stránka a vstupní stránky pro `specification/` (specifikace), `manual/` (příručka) a `help/` (nápověda).
4. Zadejte název dokumentace. Použije se pro README a pro nadpisy jednotlivých dokumentů.
5. Zadejte složku dokumentace, která se má vytvořit. Cesta je relativní vůči pracovnímu prostoru, výchozí hodnota je `docs`.
6. Zkontrolujte seznam souborů, které se vytvoří, a stiskněte [Vytvořit].
   Po dokončení se nový soubor `README.md` otevře v prohlížeči.

> **Poznámka**
>
> - Existující soubory se nikdy nepřepisují. Pokud již existuje byť jen jeden ze souborů, které se mají vytvořit, nevytvoří se nic a operace se zastaví.
> - V nedůvěryhodném pracovním prostoru vytvoření není možné.

> **Tip**
>
> - Pokud už složku s dokumentací máte, tento postup přeskočte a přejděte na [Základní ovládání](../02-reading/README.md).
> - Jak bude dokumentace růst, můžete přidávat dokumenty po jednom ze šablon na kartě [Vytvořit] v Nástrojích dokumentu.

## Související témata

- [Vytvoření dokumentu ze šablony](../04-document-tools/templates.md)
- [Kořeny dokumentace a konvence souborů](../04-document-tools/structure.md)
