# Documenten controleren

Met docs-lint controleert u de opbouw van koppen, verbroken links, ontbrekende verplichte documenten en hoofdstukken, afwijkend terminologiegebruik, de samenhang van requirement-ID's en meer. Een controle geldt altijd voor de hele documentatiehoofdmap.

## Een controle uitvoeren

1. Druk in de werkbalk op [Documenthulpmiddelen] en open het tabblad [Controle].
2. Druk op [Documentatiehoofdmap controleren].
   U kunt dit ook uitvoeren met "Lunascape Docs: Documentatiehoofdmap controleren" in het opdrachtenpalet.
3. Bekijk de lijst met bevindingen.

## De resultaten lezen

- Met [Dit document] / [Alles] boven de lijst schakelt u tussen de weergegeven bevindingen. De controle zelf geldt altijd voor de hele documentatiehoofdmap.
- Bevindingen hebben vier niveaus: fout, waarschuwing, informatie en suggestie. [Documenthulpmiddelen] in de werkbalk toont het aantal fouten en waarschuwingen.
- Druk op een bevinding om de bijbehorende plek in de Markdown-bron te openen in de editor van VS Code.
- Bevindingen die de hele documentatiehoofdmap betreffen (zoals een ontbrekend testdocument) verschijnen als item "Volledige documentatiehoofdmap" en hebben geen positie.
- Dezelfde bevindingen verschijnen ook in het paneel Problemen van VS Code.

## Wat er wordt gecontroleerd

Druk op [Regels bekijken en wijzigen] om de lijst met actieve controles en het doel van elke controle te zien. De belangrijkste zijn:

| Item | Betekenis |
|---|---|
| Kopstructuur | Er is één H1 en de kopniveaus slaan geen niveau over |
| Interne links | De gelinkte documenten bestaan en blijven binnen de documentatiehoofdmap |
| Taal van codeblokken | Bij codeblokken is een taalnaam opgegeven |
| Vereiste mappen en documenten | De mappen en documenten die het profiel van de Standard Pack vraagt, zijn aanwezig |
| Vereiste hoofdstukken in een document | Elk documenttype heeft de hoofdstukken die het nodig heeft |
| Eenduidige terminologie | Af te raden formuleringen worden gemeld en de aanbevolen term wordt voorgesteld |
| Naamgeving en duplicaten van requirement-ID's | Requirement-ID's volgen de naamgevingsregel en zijn niet dubbel gedefinieerd |
| Verwijzingen naar requirement-ID's | De requirement-ID's waarnaar ontwerp, tests en statustabellen verwijzen, bestaan |
| Koppeling tussen requirements en tests | Requirement-ID's worden vanuit testdocumenten aangehaald |

Welke items actief zijn, hangt af van de Standard Pack en het profiel die in `lunascape-docs.json` zijn gekozen, en van `docs-lint.config.json`.

> **Let op**
>
> - Als u een document of een instelling wijzigt, krijgt het vorige resultaat de status "hercontrole nodig". Niets wordt automatisch als geslaagd beschouwd; druk opnieuw op [Documentatiehoofdmap controleren].
> - Niet-opgeslagen wijzigingen worden niet in de controle meegenomen. Sla eerst op.
> - Controles worden lokaal op uw apparaat en deterministisch uitgevoerd. Beoordelingen door AI en vertaalresultaten komen nooit in de controleresultaten terecht.

## Verwante onderwerpen

- [Controleregels wijzigen](rules.md)
- [Projectinstellingen](project-configuration.md)
- [Controle, aanmaken of vertalen lukt niet](../07-troubleshooting/tools.md)
