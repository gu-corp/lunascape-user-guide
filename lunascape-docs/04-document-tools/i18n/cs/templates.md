# Vytvoření dokumentu ze šablony

Na kartě [Vytvořit] v Nástrojích dokumentů vyberete šablonu, zobrazíte si náhled obsahu a poté vytvoříte nový dokument.

1. Na panelu nástrojů stiskněte [Nástroje dokumentů] a otevřete kartu [Vytvořit].
2. Stiskněte [Vytvořit ze šablony] a vyberte šablonu.
3. Vyplňte vstupní pole (název, shrnutí a podobně). U povinných polí je uvedeno „Povinné“.
4. Zadejte umístění jako cestu relativní ke kořeni dokumentace (například `03-design/api.md`).
5. Stiskněte [Náhled] a zkontrolujte vygenerovaný Markdown.
6. Stiskněte [Vytvořit s tímto obsahem].
   Dokument se vytvoří a zobrazí v prohlížeči. Následně proběhne kontrola celého kořene dokumentace.

## Dostupné šablony

| Šablona | Obsah |
|---|---|
| Jednostránkový dokument | Krátká specifikace, poznámky nebo samostatný vysvětlující dokument v jednom souboru |
| Specifikace, příručka, nápověda | Jeden soubor s obecným členěním na kapitoly, které se hodí pro specifikaci, příručku nebo nápovědu |
| Šablony Standard Pack | Pokud je v souboru `lunascape-docs.json` vybrán Standard Pack, přibudou typy dokumentů dostupné v jeho profilu (specifikace požadavků, návrh a podobně) |

> **Poznámka**
>
> - Vytváření vyžaduje důvěryhodný pracovní prostor.
> - Existující soubory se nikdy nepřepisují. Pokud v cílovém umístění existuje dokument se stejným názvem, vytvoření se nezdaří.
> - Cílové umístění musí mít příponu `.md` nebo `.mdx`. Pod složkou `i18n` (kde jsou uloženy překlady) nelze vytvářet nic.
> - Po změně zadaných údajů stiskněte před vytvořením znovu [Náhled].

> **Tip**
>
> V projektu, který zatím nemá složku s dokumenty, vytvoříte první sadu příkazem „Lunascape Docs: Vytvořit dokumentaci ze šablony“ v paletě příkazů. Viz [Vytvoření prvních dokumentů](../01-introduction/first-documents.md).

## Související témata

- [Používání Nástrojů dokumentů](README.md)
- [Změna pravidel kontroly](rules.md)
