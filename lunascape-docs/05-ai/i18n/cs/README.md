# Předání práce AI

Lunascape Docs nevolá jazykový model. Připraví **kontext, nástroje a kontrolu** a samotný překlad, korekturu a psaní přenechá AI, kterou používáte.

## Princip

| Co produkt poskytuje | Obsah |
|---|---|
| Kontext | Konvence dokumentace (kde jsou uloženy překlady, front matter, standard dokumentů, glosář) a umístění cílového dokumentu |
| Pracovní nástroje | Evidence nepřeložených a neaktuálních dokumentů, čtení a zápis dokumentů, vytváření ze šablon |
| Následná kontrola | Ověření pomocí docs-lint, rozdíl v pokrytí a aktuálnosti |

Pokyn neobsahuje text dokumentu. AI si soubory sama přečte, sama je zapíše a sama je ověří.

## Předání práce

1. Na panelu nástrojů stiskněte [Nástroje dokumentů] a otevřete kartu [AI].
2. V poli [Úloha] vyberte práci, kterou chcete předat.
3. Vyplňte potřebné položky (cílový jazyk, téma).
4. Stiskněte [Předat tuto úlohu].
   Otevře se terminál VS Code a zvolená AI převezme pokyn a začne pracovat.

> **Tip**
>
> Relaci Claude Code doprovázejí pracovní nástroje (server MCP `lunascape-docs`). Relace si sama načte seznam nepřeložených a neaktuálních dokumentů, spustí docs-lint a po překladu zaznamená aktuálnost.

## Kontrola výsledku

| Typ poskytovatele | Kam výsledek směřuje |
|---|---|
| Relace (Claude Code, Codex) | Zapisuje přímo do pracovního stromu. **Zkontrolujte jej v rozdílech Git** |
| API (jazykové modely VS Code, Anthropic, kompatibilní s OpenAI) | Vrací návrh po jednom dokumentu. Zkontrolujte jej pomocí [Otevřít rozdíly] a zapište pomocí [Uložit] |

### Kontrola návrhu od poskytovatele API

Při spuštění s poskytovatelem API dorazí návrh na kartu [AI].

1. Stiskněte [Otevřít rozdíly] a porovnejte jej s aktuálním obsahem.
2. Pokud vyhovuje, stiskněte [Uložit]. U překladu se zároveň zaznamená aktuálnost. Chcete-li jej zahodit, stiskněte [Zahodit].
   Chcete-li generování zastavit v průběhu, stiskněte [Zastavit].

> **Poznámka**
>
> - Lunascape Docs nikdy neprovádí v Gitu přípravu do indexu ani potvrzení změn. Změny vždy zkontrolujte v rozdílech.
> - V nedůvěryhodném pracovním prostoru a při dočasném zobrazení složky mimo kořen dokumentace nelze práci předat.

## Související témata

- [Úlohy, které lze předat](tasks.md)
- [Nastavení AI](settings.md)
- [Evidence a záznamy](ledger.md)
