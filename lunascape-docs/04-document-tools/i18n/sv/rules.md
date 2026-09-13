# Ändra kontrollregler

Du kan ändra aviseringsnivån (fel, varning, information) för varje kontroll eller stänga av en kontroll. Ändringarna sparas i `docs-lint.config.json` i dokumentroten och delas med teamet.

## Ändra en aviseringsnivå

1. Tryck på [Dokumentverktyg] i verktygsfältet och öppna fliken [Kontroll].
2. Tryck på [Granska och ändra reglerna].
   Listan över kontroller fälls ut i samma kort. Varje kontroll visar sitt syfte och var den aktuella inställningen kommer ifrån (Project, Profile, Pack eller Default).
3. Välj aviseringsnivå för den kontroll du vill ändra.
4. Tryck på [Spara och kontrollera igen].
   Inställningen sparas och hela dokumentroten kontrolleras på nytt med den nya konfigurationen.

| Alternativ | Betydelse |
|---|---|
| [Standardinställning (…)] | Tar bort åsidosättningen och återgår till standardinställningen, som bestäms av profilen, Standard Pack och standardvärdet i den ordningen |
| [Av] | Kör inte den här kontrollen |
| [Information] / [Varning] / [Fel] | Rapporterar på den här nivån |

> **Obs!**
>
> - För att spara krävs en betrodd arbetsyta.
> - Endast aviseringsnivån för varje kontroll sparas. Alternativen för de enskilda kontrollerna behålls som de är. Standard Pack och profilen ändras inte från den här vyn.
> - Om `docs-lint.config.json` har ändrats externt strax före sparandet avbryts sparandet. Läs in det senaste tillståndet och försök igen.
> - Om `docs-lint.config.json` inte finns skapas filen när du sparar.

## Redigera konfigurationsfilerna direkt

- [Öppna de fullständiga inställningarna] öppnar `docs-lint.config.json` i VS Code.
- Öppna [Var reglerna kommer ifrån och dokumentinställningarna] och tryck på [Redigera dokumentinställningarna] för att öppna `lunascape-docs.json` i VS Code. Standard Pack och profilen väljer du där.

Båda filerna har komplettering och beskrivningar tack vare de JSON-scheman som medföljer tillägget.

## Standard Pack och profiler

Ett Standard Pack är en dokumentationsstandard som samlar nödvändiga dokumenttyper, kapitelindelningar, terminologi och mallar. Du väljer ett med `documentStandards` i `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Det medföljande paketet `builtin:gu-corp-software` innehåller profilerna `base`, `web-application`, `api-service`, `regulated-financial-product` och `smart-contract`.

## Relaterade avsnitt

- [Kontrollera dokument](check.md)
- [Projektinställningar](project-configuration.md)
