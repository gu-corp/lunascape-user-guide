# Korištenje iz AI agenata

Proširenje registrira alat Language Model Tool `lunascape_getDocsSpecification` samo za čitanje u VS Code. Kada se kompatibilnog agenta u VS Codeu pita o značajkama, postavkama ili dokumentacijskim konvencijama Lunascape Docsa, tim alatom može dohvatiti sadržaj ove pomoći (opću specifikaciju).

## Kako se koristi

U razgovoru u VS Codeu postavite pitanje uz `#lunascapeDocs` ili jednostavno pitajte o postavkama ili strukturi dokumenata u Lunascape Docsu.

```text
#lunascapeDocs Kako u lunascape-docs.json omogućiti prijevod na engleski?
```

## Argumenti alata

| Argument | Značenje |
|---|---|
| `topic` | Poglavlje koje se dohvaća: `all`, `usage` (Osnovne radnje), `structure` (Korijeni dokumentacije i konvencije datoteka), `editing` (Uređivanje dokumenta), `configuration` (Postavke projekta), `security` (Sigurnost i granice zapisivanja) ili `ai` (Korištenje iz AI agenata) |
| `locale` | Jezik pomoći (oznaka jezika priložene pomoći, primjerice `ja` ili `en`). Ako se izostavi, upotrebljava se jezik prikaza VS Codea, a inače se vraća pomoć na japanskom |

> **Napomena**
>
> - Alat nikamo ne šalje sadržaj dokumenata.
> - Alat ne vraća nazive radnih prostora ni lokalne putanje.
> - Alat ne mijenja datoteke.
> - Radi iz kompatibilnih agenata u VS Codeu i bez datoteke `AGENTS.md`. Ne dijeli se automatski s drugim AI klijentima koji ne upotrebljavaju API alata ovog proširenja.

## Povezane teme

- [Prikaz ove pomoći](../02-reading/help.md)
- [Sigurnost i granice zapisivanja](security.md)
