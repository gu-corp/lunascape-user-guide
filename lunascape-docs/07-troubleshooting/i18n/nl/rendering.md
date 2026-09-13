# Diagrammen, formules of afbeeldingen worden niet weergegeven

## Een TikZ-figuur wordt als ingevouwen bron getoond

- De gedistribueerde extensie bevat geen TikZ-rendering-engine. Dit is de normale weergave.
- Voor ontwikkeling en evaluatie installeert u `node-tikzjax` 1.0.5 direct in de hoofdmap van een vertrouwde werkruimte en stelt u de instelling `lunascapeDocEditor.tikz.runtime` in op `workspace`.
- In de webbrowserversie wordt TikZ niet weergegeven.

## Formules worden als gewone tekst weergegeven

- Controleer de scheidingstekens. Binnen de tekst zijn dat `$...$` of `\(...\)`, voor losstaande formules `$$...$$` of `\[...\]`.
- Een `$` binnen inline code of een codeblok wordt nooit een formule.
- Bedragachtige schrijfwijzen zoals `$5 and $10` worden niet als formule behandeld.
- Zeer grote formules of formules met veel macro-expansie worden niet weergegeven wanneer ze de limieten (`maxSize: 50`, `maxExpand: 1000`) overschrijden. Splits ze op.

## Een diagram meldt dat het niet kan worden weergegeven

- De foutmelding van Mermaid, Vega-Lite, WaveDrom en andere geeft het syntaxisprobleem aan. Controleer de bron in het bewerkingsscherm met [Markdown].
- Vega-Lite: neem gegevens op in `data.values` of `datasets`. Gegevens via een externe URL en afbeeldingsmarkeringen kunnen niet worden gebruikt.
- WaveDrom: schrijf strikte JSON. De JavaScript-vorm (sleutels zonder aanhalingstekens en dergelijke) kan niet worden gebruikt.
- Penrose: gebruik alleen `@preset set-theory` aan het begin en de toegestane instructies (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- "De gegenereerde SVG bevat onveilige verwijzingen" / "De gegenereerde SVG overschrijdt de limiet": diagrammen die naar externe bronnen verwijzen of die te groot zijn, worden niet weergegeven. Beperk de inhoud of verwijder de verwijzingen.

## Een afbeelding wordt niet weergegeven

- Geef het pad van een afbeelding op als pad relatief ten opzichte van het document. Afbeeldingen buiten de documentatiehoofdmap worden niet weergegeven.
- De `width` van een `<img>` bevat alleen een getal (`width="360"`).

## Diagrammen ontbreken op een geëxporteerde website

De rendering-bibliotheken voor TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob en Penrose worden bij de weergave geladen. Plaats de map `vendor/` samen met de geëxporteerde site.

## Verwante onderwerpen

- [Formules schrijven](../03-editing/math.md)
- [Diagrammen en grafieken schrijven](../03-editing/diagrams.md)
- [De grootte van afbeeldingen aanpassen](../03-editing/images.md)
