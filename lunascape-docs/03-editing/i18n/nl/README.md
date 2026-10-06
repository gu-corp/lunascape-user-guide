# Een document bewerken

Documenten kunt u direct in de viewer bewerken. Het bewerkscherm heeft een "visuele weergave", waarin u bewerkt wat u ziet, en een "Markdown-bronweergave"; met één knop schakelt u ertussen.

## Beginnen met bewerken

Druk op een van de volgende. Ze openen allemaal hetzelfde bewerkscherm.

- [Bewerken] rechtsonder in de tekst
- [⋯] (Meer acties) rechtsboven in de tekst → [Bewerken]
- Het itemmenu in de INDEX → [Bewerken]

## Bewerken

1. Bewerk de tekst rechtstreeks.
   In de werkbalk boven aan het bewerkscherm kunt u de alinea-opmaak (hoofdtekst, koppen 1–4, citaat, code), [Vet], [Cursief], [Opsomming], [Genummerde lijst], [Koppeling], [Tabel invoegen], [Afbeeldingsbreedte], [Ongedaan maken] en [Opnieuw uitvoeren] gebruiken.
2. Wilt u de Markdown-bron rechtstreeks bewerken, druk dan op [Markdown].
   Druk er nogmaals op om terug te keren naar de visuele weergave. De laatst gebruikte weergave wordt onthouden en hersteld wanneer u de volgende keer op [Bewerken] drukt.
3. Druk op [Opslaan] (opslaan kan ook met Ctrl+S / ⌘S).
   De tekst wordt naar het Markdown-bestand geschreven en de viewer keert terug naar de leesweergave. Wilt u stoppen met bewerken en terug naar wat het laatst is opgeslagen, druk dan op [Bewerkingen verwerpen].

## Altijd in het bewerkscherm beginnen (bewerkmodus)

Druk in de werkbalk op [Bewerkmodus] om die in te schakelen: vanaf dan begint elk document dat u opent in het bewerkscherm. Gebruik dit wanneer u zoals in een kladblok blijft doorschrijven.

- Zolang die aan staat, sluit [Opslaan] het bewerkscherm niet. [Bewerkingen verwerpen] keert terug naar wat het laatst is opgeslagen en laat het bewerkscherm openstaan.
- Druk er nogmaals op om die uit te schakelen en terug te keren naar de leesweergave. Aan/uit wordt per gebruiker onthouden.
- Bij een documentatiehoofdmap waarnaar niet kan worden geschreven (zoals een alleen-lezen GitHub-bron) wordt die niet weergegeven.

## Niet-opgeslagen bewerkingen

Bewerkingen die u niet hebt opgeslagen, worden automatisch op dit apparaat bewaard. Ze gaan niet verloren wanneer u naar een ander document gaat of het tabblad of venster sluit.

- [Niet opgeslagen] in het bewerkscherm geeft aan dat de tekst afwijkt van wat het laatst is opgeslagen.
- Wanneer u hetzelfde document de volgende keer opent, gaat het verder vanaf de bewaarde bewerkingen en meldt dat. Is het oorspronkelijke document intussen bijgewerkt, dan meldt het dat ook. Met [Bewerkingen verwerpen] keert u terug naar de nieuwste inhoud.
- De bewaarde bewerkingen verdwijnen met [Opslaan] of [Bewerkingen verwerpen]. Ze zijn niet opgeslagen en verschijnen dus niet in Git of tussen de concepten.

> **Let op**
>
> - Opslaan schrijft alleen naar het bestand. Stagen en committen in Git gebeuren nooit automatisch.
> - Formules en diagrammen zoals Mermaid, TikZ en Vega-Lite worden in de visuele weergave als weergegeven resultaat getoond. Schakel over naar [Markdown] om de inhoud ervan te wijzigen.
> - Documenten met MDX-specifieke syntaxis (componenten, `import` en dergelijke) worden alleen in de Markdown-weergave bewerkt, om die syntaxis te behouden.
> - Front matter (het blok tussen de `---`-regels boven aan het bestand) blijft behouden wanneer u in de visuele weergave bewerkt.

> **Tip**
>
> - Met [VS Codeで開く] (Openen in VS Code) opent u het bestand in de gewone teksteditor. Wanneer u daar opslaat, wordt de weergave in de viewer automatisch bijgewerkt.
> - Wilt u de knop [Bewerken] niet weergeven, schakel dan [Bewerkknop] uit bij [Weergave-instellingen]. Om die voor het hele project te verbergen, stelt u `editor.showEditButton` in op `false` in `lunascape-docs.json`.
> - De standaard beginweergave (visueel of Markdown) stelt u in met de instelling `lunascapeDocEditor.editor.defaultMode` of met `editor.defaultMode` in `lunascape-docs.json`.

## Zie ook

- [Documenten en mappen maken en ordenen](organize.md)
- [Afbeeldingen op grootte brengen](images.md)
- [Formules schrijven](math.md)
- [Diagrammen en grafieken tekenen](diagrams.md)
