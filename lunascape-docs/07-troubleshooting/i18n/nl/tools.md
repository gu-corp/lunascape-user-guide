# Controle, aanmaken of vertaling lukt niet

## Controle

### "docs-lint is niet beschikbaar" wordt weergegeven

- De uitvoeringsomgeving van docs-lint ontbreekt in de extensie, of er is een probleem met de configuratie. Installeer de extensie opnieuw.
- "Vertrouw deze werkruimte in VS Code om het lokale pack en de instellingen veilig te laden": om een lokale Standard Pack te gebruiken is een vertrouwde werkruimte nodig.

### Het resultaat blijft op "opnieuw controleren vereist" staan

Als u een document of een instelling wijzigt, vervalt het vorige resultaat. Druk nog een keer op [Documentatiehoofdmap controleren]. Niet-opgeslagen wijzigingen worden niet meegenomen.

### Er gaat niets open als u op een bevinding drukt

Items voor "hele documentatiehoofdmap" zijn niet aan een bepaald document gekoppeld en hebben dus geen positie. Controleer het betreffende document aan de hand van de inhoud van de bevinding.

### Regels kunnen niet worden opgeslagen

- Er is een vertrouwde werkruimte nodig.
- "De lint-instellingen zijn door een andere bewerking gewijzigd": `docs-lint.config.json` is extern gewijzigd. Laad de meest recente staat en probeer het opnieuw.
- Configuratiebestanden die symbolische koppelingen zijn of die buiten de documentatiehoofdmap staan, kunnen niet worden bewerkt.

## Maken op basis van een sjabloon

- "Het voorbeeld van het sjabloon is verlopen" / "De invoer is gewijzigd": druk nog een keer op [Voorbeeld] en maak het document daarna aan.
- "Er bestaat al een document op de opslaglocatie": bestaande bestanden worden niet overschreven. Geef een andere opslaglocatie op.
- De opslaglocatie moet een pad ten opzichte van de documentatiehoofdmap zijn, met de extensie `.md` of `.mdx`. Onder `i18n` kunt u niets aanmaken.
- "Vertrouw de werkruimte om documenten te maken": vertrouw de werkruimte in VS Code.

<!-- ai-only:start -->
## Vertaling

### De vertaalknoppen kunnen niet worden ingedrukt

- "AI-vertaling is niet ingeschakeld voor deze documentatiehoofdmap": stel `translation.enabled` in `lunascape-docs.json` in op `true`.
- "De standaardtaal van het project is niet ingesteld": sla de standaardtaal op via [Weergave-instellingen wijzigen](../02-reading/display-settings.md).
- "Voeg de doeltaal toe aan de ondersteunde talen": voeg de doeltaal toe aan `locales`.
- "Er is geen brondocument om te vertalen": u hebt een vertaalde pagina geopend. Schakel over naar de pagina in de standaardtaal.
- Bij een tijdelijke mapweergave kunt u geen batchvertaling gebruiken. Plaats een `lunascape-docs.json` in die map om er een documentatiehoofdmap van te maken.

### Een vertaalvoorstel wordt geweigerd of moet opnieuw worden gemaakt

- "Het brondocument is gewijzigd. Maak het vertaalvoorstel opnieuw": het brondocument of de doeltaal is gewijzigd nadat het voorstel was gemaakt. Vertaal nog een keer.
- Als in het antwoord van het taalmodel beschermde identifiers of code ontbreken, wordt het antwoord niet geaccepteerd. De inhoud van het antwoord kunt u bekijken in het uitvoerpaneel onder "Lunascape Docs Vertaling".
- "Batchvertaling verwerkt maximaal 1000 documenten per keer": verdeel het bereik per map of via een expliciete selectie.
<!-- ai-only:end -->

## Verwante onderwerpen

- [Documenten controleren](../04-document-tools/check.md)
- [Een document maken op basis van een sjabloon](../04-document-tools/templates.md)
- [Werk overdragen aan een AI](../05-ai/README.md)
