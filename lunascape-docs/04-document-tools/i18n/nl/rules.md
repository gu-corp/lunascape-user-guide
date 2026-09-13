# Controleregels wijzigen

U kunt het meldingsniveau (fout, waarschuwing, info) van elke controle wijzigen of een controle uitschakelen. Wijzigingen worden opgeslagen in `docs-lint.config.json` in de documentatiehoofdmap en met het team gedeeld.

## Een meldingsniveau wijzigen

1. Druk op [Documenthulpmiddelen] in de werkbalk en open het tabblad [Controle].
2. Druk op [Regels bekijken en wijzigen].
   De lijst met controles wordt binnen dezelfde kaart uitgeklapt. Bij elke controle staan het doel en de herkomst van de huidige instelling (Project, Profile, Pack of Default).
3. Kies het meldingsniveau van de controle die u wilt wijzigen.
4. Druk op [Opslaan en opnieuw controleren].
   De instelling wordt opgeslagen en de hele documentatiehoofdmap wordt opnieuw gecontroleerd met de nieuwe instellingen.

| Optie | Betekenis |
|---|---|
| [Standaardinstelling (…)] | Verwijdert de overschrijving en keert terug naar de standaardinstelling, bepaald door achtereenvolgens het profiel, de Standard Pack en de standaardwaarde |
| [Uit] | Voert deze controle niet uit |
| [Info] / [Waarschuwing] / [Fout] | Meldt op dit niveau |

> **Opmerking**
>
> - Voor het opslaan is een vertrouwde werkruimte vereist.
> - Alleen het meldingsniveau van elke controle wordt opgeslagen. De opties per controle blijven ongewijzigd. De Standard Pack en het profiel zelf wijzigt u niet in dit scherm.
> - Als `docs-lint.config.json` vlak voor het opslaan extern is gewijzigd, wordt het opslaan afgebroken. Laad de nieuwste versie opnieuw en probeer het nogmaals.
> - Als `docs-lint.config.json` niet bestaat, wordt het bij het opslaan aangemaakt.

## De instellingenbestanden rechtstreeks bewerken

- Met [Geavanceerde instellingen openen] opent u `docs-lint.config.json` in VS Code.
- Open [Herkomst van de regels en documentinstellingen] en druk op [Documentinstellingen bewerken] om `lunascape-docs.json` in VS Code te openen. Hier kiest u de Standard Pack en het profiel.

Voor beide bestanden zijn aanvulling en beschrijvingen beschikbaar via de JSON Schema's die bij de extensie zijn geleverd.

## Standard Pack en profielen

Een Standard Pack is een documentatiestandaard die de vereiste documenttypen, hoofdstukindeling, terminologie en sjablonen bundelt. U kiest er een met `documentStandards` in `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

De meegeleverde pack `builtin:gu-corp-software` bevat de profielen `base`, `web-application`, `api-service`, `regulated-financial-product` en `smart-contract`.

## Verwante onderwerpen

- [Documenten controleren](check.md)
- [Projectinstellingen](project-configuration.md)
