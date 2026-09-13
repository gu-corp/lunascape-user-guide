# AI-instellingen

Kies de AI en het model die uw werk ontvangen. Dit scherm gebruikt zijn eigen keuzelijsten, niet de snelkeuze van VS Code.

1. Druk op [Documenthulpmiddelen] → tabblad [AI] → [AI-instellingen…].
2. Kies een provider onder [Provider].
   Providers die op deze computer niet beschikbaar zijn, worden niet-selecteerbaar weergegeven, met de reden erbij.
3. Kies een model onder [Model]. De keuzemogelijkheden verschillen per provider.
4. Sluit het scherm. De keuze wordt per gebruiker opgeslagen en de volgende keer opnieuw gebruikt.

## Providers

| Provider | Vorm | Detectie |
|---|---|---|
| Claude Code | Sessie | De opdracht `claude` |
| Codex | Sessie | De opdracht `codex` |
| Taalmodellen van VS Code | API | Modellen die zijn geregistreerd bij de VS Code Language Model API |
| Anthropic API | API | Een geregistreerde API-sleutel |
| OpenAI-compatibele API | API | Een geregistreerde API-sleutel en een eindpunt |

Een **sessie**provider leest en schrijft zelf bestanden en voert zelf de documentcontrole uit. De resultaten komen rechtstreeks in de werkmap terecht en worden in het Git-verschil bekeken.

Een **API**-provider levert de Markdown van één document terug; de extensie toont het verschil voordat er wordt opgeslagen.

## Een API-sleutel registreren

De Anthropic API en OpenAI-compatibele API's zijn bruikbaar zodra u een API-sleutel registreert.

1. Kies onder [Provider] waar u de sleutel registreert. Het invoerveld voor de sleutel verschijnt.
2. Voer de [API-sleutel] in. Bij een OpenAI-compatibele API voert u ook het [Eindpunt] in (bijvoorbeeld `https://api.openai.com/v1`).
3. Druk op [Opslaan]. Er verschijnt "Sleutel geregistreerd".

> **Let op**
>
> - Sleutels worden bewaard in de SecretStorage van VS Code en worden niet opnieuw getoond. Ze worden ook niet weggeschreven naar `settings.json` of naar een document. Met [Sleutel verwijderen] verwijdert u een sleutel.
> - De modellenlijst wordt met de geregistreerde sleutel bij elke dienst opgehaald. Zolang dat niet lukt, wordt een bekende lijst getoond.
> - Met een API-provider kunt u alleen "Deze pagina vertalen" en "Deze pagina proeflezen" uitvoeren. Meerdere documenten langslopen en documenten aanmaken doet u met een sessieprovider.

> **Tip**
>
> Wordt er geen enkele provider gevonden, installeer dan Claude Code of Codex, of registreer een API-sleutel. Open [AI-instellingen…] opnieuw en de provider wordt gedetecteerd.

## Verwante onderwerpen

- [Werk aan een AI overdragen](README.md)
- [Overzicht van VS Code-instellingen](../08-reference/settings.md)
