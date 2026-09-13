# Použití z AI agentů

Rozšíření registruje ve VS Code nástroj Language Model Tool `lunascape_getDocsSpecification` určený pouze ke čtení. Když se kompatibilního agenta VS Code zeptáte na funkce Lunascape Docs, nastavení nebo konvence dokumentů, může prostřednictvím tohoto nástroje získat obsah této nápovědy (obecnou specifikaci).

## Jak jej používat

V chatu VS Code se zeptejte s `#lunascapeDocs`, nebo se jednoduše zeptejte na nastavení Lunascape Docs či na strukturu dokumentů.

```text
#lunascapeDocs How do I enable English translations in lunascape-docs.json?
```

## Argumenty nástroje

| Argument | Význam |
|---|---|
| `topic` | Kapitola, kterou chcete získat: `all`, `usage` (základní operace), `structure` (kořeny dokumentace a konvence souborů), `editing` (úprava dokumentu), `configuration` (nastavení projektu), `security` (zabezpečení a hranice zápisu) nebo `ai` (použití z AI agentů) |
| `locale` | Jazyk nápovědy (jazykový tag přibalené nápovědy, například `ja` nebo `en`). Když jej vynecháte, použije se jazyk zobrazení VS Code, a pokud není k dispozici, vrátí se japonská nápověda |

> **Poznámka**
>
> - Nástroj nikdy neodesílá obsah dokumentů nikam ven.
> - Nástroj nikdy nevrací názvy pracovních prostorů ani lokální cesty.
> - Nástroj nikdy neupravuje soubory.
> - Funguje z kompatibilních agentů VS Code i bez souboru `AGENTS.md`. Jiným AI klientům, kteří nepoužívají rozhraní API nástrojů rozšíření, se nesdílí automaticky.

## Související témata

- [Zobrazení této nápovědy](../02-reading/help.md)
- [Zabezpečení a hranice zápisu](security.md)
