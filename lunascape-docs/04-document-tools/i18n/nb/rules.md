# Endre kontrollregler

Du kan endre varslingsnivået (feil, advarsel, informasjon) for hver kontroll, eller slå en kontroll av. Endringene lagres i `docs-lint.config.json` i dokumentroten og deles med teamet.

## Endre et varslingsnivå

1. Trykk på [Dokumentverktøy] på verktøylinjen og åpne fanen [Kontroll].
2. Trykk på [Se gjennom og endre reglene].
   Listen over kontroller utvides inne i det samme kortet. Hver kontroll viser formålet sitt og hvor gjeldende innstilling kommer fra (Project, Profile, Pack eller Default).
3. Velg varslingsnivået for kontrollen du vil endre.
4. Trykk på [Lagre og kontroller på nytt].
   Innstillingen lagres, og hele dokumentroten kontrolleres på nytt med den nye konfigurasjonen.

| Valg | Betydning |
|---|---|
| [Standardinnstilling (…)] | Fjerner overstyringen og går tilbake til standardinnstillingen som bestemmes av profilen, Standard Pack og standardverdien, i den rekkefølgen |
| [Av] | Kjører ikke denne kontrollen |
| [Informasjon] / [Advarsel] / [Feil] | Rapporterer på dette nivået |

> **Merk**
>
> - Lagring krever et klarert arbeidsområde.
> - Bare varslingsnivået for hver kontroll lagres. Alternativene for hver enkelt kontroll beholdes som de er. Standard Pack og profilen selv endres ikke fra denne skjermen.
> - Hvis `docs-lint.config.json` ble endret utenfra like før lagring, avbrytes lagringen. Last inn den nyeste tilstanden og prøv på nytt.
> - Hvis `docs-lint.config.json` ikke finnes, opprettes filen når du lagrer.

## Rediger konfigurasjonsfilene direkte

- [Åpne de detaljerte innstillingene] åpner `docs-lint.config.json` i VS Code.
- Åpne [Hvor reglene kommer fra, og dokumentinnstillingene] og trykk på [Rediger dokumentinnstillingene] for å åpne `lunascape-docs.json` i VS Code. Standard Pack og profilen velges der.

Begge filene har fullføring og beskrivelser fra JSON Schema-ene som følger med utvidelsen.

## Standard Pack og profiler

En Standard Pack er en dokumentasjonsstandard som samler nødvendige dokumenttyper, kapittelinndeling, terminologi og maler. Velg en med `documentStandards` i `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Den medfølgende pakken `builtin:gu-corp-software` har profilene `base`, `web-application`, `api-service`, `regulated-financial-product` og `smart-contract`.

## Relaterte emner

- [Kontrollere dokumenter](check.md)
- [Prosjektkonfigurasjon](project-configuration.md)
