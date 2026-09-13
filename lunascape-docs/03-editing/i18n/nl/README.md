# Een document bewerken

Documenten kunt u rechtstreeks in de viewer bewerken. Het bewerkingsscherm heeft een visuele weergave, waarin u bewerkt wat u ziet, en een Markdown-bronweergave; met één knop schakelt u ertussen.

## Beginnen met bewerken

Druk op een van de volgende. Ze openen alle hetzelfde bewerkingsscherm.

- [Bewerken] rechtsonder in het document
- [⋯] (Meer acties) rechtsboven in het document → [Bewerken]
- Het itemmenu in INDEX → [Bewerken]

## Bewerken

1. Bewerk de tekst rechtstreeks.
   In de werkbalk boven in het bewerkingsscherm kunt u de alinea-opmaak (tekst, kop 1–4, citaat, code), [Vet], [Cursief], [Opsomming], [Genummerde lijst], [Koppeling], [Tabel invoegen], [Afbeeldingsbreedte], [Ongedaan maken] en [Opnieuw uitvoeren] gebruiken.
2. Wilt u de Markdown-bron rechtstreeks bewerken, druk dan op [Markdown].
   Druk er nogmaals op om terug te keren naar de visuele weergave. De laatst gebruikte weergave wordt onthouden en hersteld wanneer u de volgende keer op [Bewerken] drukt.
3. Druk op [Opslaan].
   Het Markdown-bestand wordt weggeschreven en de viewer keert terug naar de leesweergave. Wilt u stoppen, druk dan op [Annuleren].

> **Let op**
>
> - Bij het opslaan wordt alleen het bestand weggeschreven. Git-staging en commits gebeuren niet automatisch.
> - Formules en diagrammen zoals Mermaid, TikZ en Vega-Lite worden in de visuele weergave als eindresultaat getoond. Schakel over naar [Markdown] om de inhoud ervan te wijzigen.
> - Documenten met MDX-specifieke syntaxis (componenten, `import` en dergelijke) bewerkt u alleen in de Markdown-weergave, om die syntaxis te behouden.
> - Front matter (de instellingen tussen de `---`-regels boven aan het document) blijft behouden wanneer u in de visuele weergave bewerkt.

> **Tip**
>
> - Met [Openen in VS Code] opent u het bestand in de gewone teksteditor. Slaat u daar op, dan wordt de weergave in de viewer automatisch bijgewerkt.
> - Wilt u de knop [Bewerken] niet tonen, schakel dan [Bewerkknop] uit bij [Weergave-instellingen]. Om de knop voor het hele project te verbergen, stelt u `editor.showEditButton` in `lunascape-docs.json` in op `false`.
> - De standaardweergave bij het openen (visueel of Markdown) wijzigt u met de instelling `lunascapeDocEditor.editor.defaultMode` of met `editor.defaultMode` in `lunascape-docs.json`.

## Gerelateerde onderwerpen

- [Documenten en mappen maken en ordenen](organize.md)
- [De grootte van afbeeldingen aanpassen](images.md)
- [Formules schrijven](math.md)
- [Diagrammen en grafieken maken](diagrams.md)
