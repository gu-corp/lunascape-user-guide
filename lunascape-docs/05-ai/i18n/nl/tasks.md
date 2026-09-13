# Werk dat u kunt doorgeven

Kies dit in het tabblad [AI] bij [Taak]. Per taak verschillen de instructie die wordt doorgegeven en de controle achteraf.

| Werk | Inhoud | Vereist | API-type |
|---|---|---|---|
| Deze pagina vertalen | Vertaalt het geopende document naar de gekozen taal | Het betreffende document is geopend, een doeltaal | ○ |
| Niet-vertaalde documenten in bulk vertalen | Vertaalt de niet-vertaalde en verouderde documenten van de gekozen taal, op volgorde | Een doeltaal | Alleen sessietype |
| Deze pagina proeflezen | Controleert en corrigeert terminologie, stijl en de hoofdstukindeling die de documentstandaard vereist | Het betreffende document is geopend | ○ |
| Nieuw document maken | Maakt een nieuw document volgens de documentstandaard en de sjablonen | Een onderwerp (optioneel) | Alleen sessietype |

## Wat de instructie bevat

| Nr. | Inhoud |
|---|---|
| 1 | De locatie van de documentatiehoofdmap, met de instructie daarbuiten niets te wijzigen |
| 2 | De standaardtaal (het brondocument) en de plaats van de vertalingen (`i18n/<taal>/` in dezelfde map als het document) |
| 3 | Dat `navigation.order` alleen bij het brondocument hoort en dat een vertaling uitsluitend `navigation.title` mag overschrijven |
| 4 | Dat vereiste-ID's, koppelingen, code, Mermaid, TeX en de structuur van de front matter niet gewijzigd mogen worden |
| 5 | De documentstandaard en de woordenlijst (`terminology` in `docs-lint.config.json`) |
| 6 | Dat de documentcontrole na afloop wordt uitgevoerd, dat de gewijzigde bestanden worden gemeld en dat er geen Git-bewerkingen worden uitgevoerd |

> **Tip**
>
> De documenten voor "Niet-vertaalde documenten in bulk vertalen" worden uit het register samengesteld, tot 200 documenten per keer. Voer de taak bij meer documenten nogmaals uit.

## Verwante onderwerpen

- [Werk doorgeven aan een AI](README.md)
- [Het register en zijn gegevens](ledger.md)
