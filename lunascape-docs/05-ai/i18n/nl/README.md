# Werk aan een AI overdragen

Lunascape Docs roept zelf geen taalmodel aan. Het product levert **context, hulpmiddelen en controles**, en laat het vertalen, proeflezen en schrijven over aan de AI die u gebruikt.

## Het idee

| Wat het product levert | Inhoud |
|---|---|
| Context | De afspraken over de documenten (waar vertalingen staan, front matter, de documentstandaard, de woordenlijst) en de plaats van het betreffende document |
| Werkhulpmiddelen | Het overzicht van niet-vertaalde en verouderde documenten, het lezen en schrijven van documenten, het aanmaken vanuit een sjabloon |
| Controle achteraf | Verificatie met docs-lint, en het verschil in dekking en actualiteit |

De opdracht bevat geen tekst uit het document: de AI leest de bestanden zelf, schrijft ze zelf en controleert ze zelf.

## Werk overdragen

1. Druk op [Documenthulpmiddelen] in de werkbalk en open het tabblad [AI].
2. Kies onder [Taak] het werk dat u wilt overdragen.
3. Vul de benodigde gegevens in (doeltaal, onderwerp).
4. Druk op [Deze taak overdragen].
   Er wordt een terminal van VS Code geopend; de gekozen AI ontvangt de opdracht en begint met het werk.

> **Tip**
>
> Bij een sessie van Claude Code horen de werkhulpmiddelen (de MCP-server `lunascape-docs`). De sessie kan zelf de lijst met niet-vertaalde en verouderde documenten ophalen, docs-lint uitvoeren en na het vertalen de actualiteit vastleggen.

## Het resultaat controleren

| Soort provider | Waar het resultaat terechtkomt |
|---|---|
| Sessie (Claude Code, Codex) | Schrijft rechtstreeks in de werkmap. **Controleer het in het Git-verschil** |
| API (taalmodellen van VS Code, Anthropic, OpenAI-compatibel) | Geeft per document een voorstel terug. Controleer het met [Verschil openen] en schrijf het weg met [Opslaan] |

### Een voorstel van een API-provider controleren

Bij uitvoering via een API-provider komt het voorstel binnen op het tabblad [AI].

1. Druk op [Verschil openen] en vergelijk het met de huidige inhoud.
2. Druk op [Opslaan] als het goed is. Bij een vertaling wordt ook de actualiteit vastgelegd. Druk op [Verwerpen] als u ervan afziet.
   Druk op [Stoppen] om een lopende generatie af te breken.

> **Let op**
>
> - Lunascape Docs zet nooit iets klaar in Git en maakt nooit een commit. Controleer wijzigingen altijd in het verschil.
> - In een werkruimte die u niet vertrouwt, en bij het tijdelijk weergeven van een map buiten de documentatiehoofdmap, kunt u geen werk overdragen.

## Verwante onderwerpen

- [Werk dat u kunt overdragen](tasks.md)
- [AI-instellingen](settings.md)
- [Het overzicht en de registratie](ledger.md)
