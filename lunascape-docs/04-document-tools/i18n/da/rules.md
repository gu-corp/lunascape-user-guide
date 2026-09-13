# Ændre kontrolregler

Du kan ændre notifikationsniveauet (fejl, advarsel, info) for hver kontrol eller slå en kontrol fra. Ændringerne gemmes i `docs-lint.config.json` i dokumentroden og deles med teamet.

## Ændre et notifikationsniveau

1. Tryk på [Dokumentværktøjer] på værktøjslinjen, og åbn fanen [Kontrol].
2. Tryk på [Gennemgå og ændr reglerne].
   Listen over kontroller foldes ud i det samme kort. Hver kontrol viser sit formål og kilden til den aktuelle indstilling (Project, Profile, Pack eller Default).
3. Vælg notifikationsniveauet for den kontrol, du vil ændre.
4. Tryk på [Gem, og kontrollér igen].
   Indstillingen gemmes, og hele dokumentroden kontrolleres igen med de nye indstillinger.

| Valgmulighed | Betydning |
|---|---|
| [Standardindstilling (…)] | Fjerner tilsidesættelsen og vender tilbage til standardindstillingen, der bestemmes af profilen, Standard Pack og standardværdien i den rækkefølge |
| [Fra] | Kontrollerer ikke dette punkt |
| [Info] / [Advarsel] / [Fejl] | Rapporterer på dette notifikationsniveau |

> **Bemærk**
>
> - Det kræver en browser, du har tillid til, at gemme.
> - Det er kun notifikationsniveauet for hver kontrol, der gemmes. Indstillingerne for de enkelte punkter bevares, som de er. Standard Pack og selve profilen ændres ikke på denne skærm.
> - Hvis `docs-lint.config.json` er blevet ændret udefra lige inden, du gemmer, afbrydes lagringen. Indlæs den nyeste tilstand, og prøv igen.
> - Hvis der ikke findes en `docs-lint.config.json`, oprettes den, når du gemmer.

## Redigere indstillingsfilerne direkte

- Tryk på [Åbn de detaljerede indstillinger] for at åbne `docs-lint.config.json` i VS Code.
- Åbn [Hvor reglerne kommer fra, og dokumentindstillingerne], og tryk på [Rediger dokumentindstillingerne] for at åbne `lunascape-docs.json` i VS Code. Standard Pack og profilen vælges her.

Begge filer har fuldførelse og beskrivelser fra de JSON Schema-filer, der følger med udvidelsen.

## Standard Pack og profiler

Standard Pack er en dokumentationsstandard, der samler de nødvendige dokumenttyper, kapitelopbygninger, termer og skabeloner. Den vælges med `documentStandards` i `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Den medfølgende Pack `builtin:gu-corp-software` indeholder profilerne `base`, `web-application`, `api-service`, `regulated-financial-product` og `smart-contract`.

## Relaterede emner

- [Kontrollere dokumenter](check.md)
- [Projektindstillinger](project-configuration.md)
