# Het overzicht en de registraties

Het overzicht boven aan het tabblad [AI] toont de vertaalstatus per ondersteunde taal. Ook zonder AI kunt u zien wat er ontbreekt.

| Weergave | Betekenis |
|---|---|
| Niet vertaald | Aantal documenten zonder vertaling |
| Verouderd | Aantal documenten waarvan de vertaling bestaat, maar waarvan het brondocument nieuwer is dan de registratie |
| Vertaald | Aantal vertalingen die het brondocument volgen |

Het overzicht wordt berekend door de documentatiehoofdmap te doorlopen. Er komt geen AI en geen taalmodel aan te pas.

## De vertaalregistratie bijwerken

Om "Verouderd" te kunnen bepalen, moeten het brondocument en de vertaling worden vastgelegd zoals ze waren op het moment van vertalen. Een AI met sessies schrijft de bestanden rechtstreeks, dus wordt er niet automatisch een registratie aangemaakt.

1. Als de vertaling klaar is en u de inhoud hebt gecontroleerd, drukt u op [Vertaalregistratie bijwerken].
2. Vertalingen zonder registratie worden vastgelegd als passend bij het huidige brondocument.

Sessies van Claude Code en het opslaan via een API leggen dit automatisch vast (een sessie krijgt de instructie de MCP-tool `record_translation_freshness` te gebruiken). U hebt deze knop nodig wanneer u met Codex of met de chat van VS Code hebt vertaald.

Vanaf dat moment wordt de vertaling als "Verouderd" weergegeven zodra u het brondocument wijzigt.

> **Let op**
>
> - Vertalingen die al een registratie hebben, worden niet overschreven. Zo gaat de status "Verouderd" niet verloren.
> - De registraties worden opgeslagen in `.lunascape-docs/translation-freshness.json`. Daarin staan alleen relatieve paden, talen, hashes van de inhoud en het tijdstip — nooit de tekst zelf.

## Verwante onderwerpen

- [Werk dat u kunt overdragen](tasks.md)
- [In een andere taal lezen](../02-reading/languages.md)
