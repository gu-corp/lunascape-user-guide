# Kontrola dokumentů

Nástroj docs-lint umožňuje zkontrolovat strukturu nadpisů, nefunkční odkazy, chybějící povinné dokumenty a kapitoly, nejednotnou terminologii, soulad identifikátorů požadavků a další. Kontrola se vždy provádí nad celým kořenem dokumentace.

## Spuštění kontroly

1. Na panelu nástrojů stiskněte [Nástroje dokumentů] a otevřete kartu [Kontrola].
2. Stiskněte [Zkontrolovat kořen dokumentace].
   Kontrolu lze spustit také příkazem „Lunascape Docs: Zkontrolovat kořen dokumentace“ z palety příkazů.
3. Projděte si seznam výsledků.

## Čtení výsledků

- Přepínačem [Tento dokument] / [Vše] nad seznamem zvolíte, co se zobrazí. Samotný rozsah kontroly je vždy celý kořen dokumentace.
- Nálezy mají čtyři úrovně: „chyba“, „varování“, „informace“ a „návrh“. Na panelu nástrojů se u položky [Nástroje dokumentů] zobrazuje počet chyb a varování.
- Po stisknutí nálezu se v editoru VS Code otevře odpovídající místo ve zdrojovém souboru Markdown.
- Nálezy, které se týkají celého kořene dokumentace (například chybějící testovací dokument), se zobrazují jako položky „celý kořen dokumentace“ a nemají určené místo.
- Tytéž nálezy se zobrazují také v panelu „Problémy“ ve VS Code.

## Kontrolované položky

Po stisknutí [Zkontrolovat a změnit pravidla] se zobrazí seznam aktivních kontrol a účel každé z nich. Hlavní položky jsou tyto.

| Položka | Obsah |
|---|---|
| Struktura nadpisů | Zda je právě jeden nadpis H1 a zda úrovně nadpisů nepřeskakují |
| Vnitřní odkazy | Zda cílové dokumenty existují a nevedou mimo kořen dokumentace |
| Jazyk bloků kódu | Zda je u bloků kódu uveden název jazyka |
| Povinné složky a dokumenty | Zda jsou k dispozici složky a dokumenty vyžadované profilem Standard Pack |
| Povinné kapitoly dokumentu | Zda má každý typ dokumentu své povinné kapitoly |
| Jednotnost terminologie | Označí nevhodné výrazy a vede ke sjednocení na doporučené termíny |
| Pojmenování a duplicita ID požadavků | Zda identifikátory požadavků odpovídají pravidlu pojmenování a nejsou definovány dvakrát |
| Soulad odkazů na ID požadavků | Zda identifikátory požadavků, na které odkazuje návrh, testy či přehledové tabulky, skutečně existují |
| Vazba požadavků a testů | Zda jsou identifikátory požadavků odkazovány z testovacích dokumentů |

Které položky jsou aktivní, určuje Standard Pack a profil zvolený v souboru `lunascape-docs.json` a dále soubor `docs-lint.config.json`.

> **Poznámka**
>
> - Po změně dokumentu nebo nastavení se předchozí výsledek označí jako „vyžaduje novou kontrolu“. Nic není automaticky považováno za vyhovující. Stiskněte znovu [Zkontrolovat kořen dokumentace].
> - Neuložené změny se do kontroly nepromítnou. Nejprve je uložte.
> - Kontrola probíhá v zařízení a je deterministická. Výsledky hodnocení nebo překladu pomocí AI se do výsledků kontroly nikdy nemísí.

## Související témata

- [Změna pravidel kontroly](rules.md)
- [Nastavení projektu](project-configuration.md)
- [Kontrola, vytváření nebo překlad se nedaří](../07-troubleshooting/tools.md)
