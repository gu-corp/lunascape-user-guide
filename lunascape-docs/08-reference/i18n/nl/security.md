# Beveiliging en opslaggrenzen

De grenzen die Lunascape Docs hanteert om uw documenten en uw apparaat te beschermen.

## Weergave

- HTML die uit Markdown wordt gegenereerd en SVG die uit diagrammen wordt gegenereerd, worden vóór weergave onschadelijk gemaakt met DOMPurify 3.4.14.
- Willekeurige scripts in MDX worden niet uitgevoerd.
- KaTeX draait met `trust: false`, `maxSize: 50` en `maxExpand: 1000`, en vertrouwt noch externe HTML noch willekeurige opdrachten.
- De tekenbibliotheken van Markmap, WaveDrom, Svgbob, Vega-Lite en Penrose worden alleen bij een bijbehorend blok lokaal op het apparaat geladen, in een vastgezette versie. Verwijzingen naar externe bronnen, ruwe HTML en uitvoerbare notaties zijn niet toegestaan, en scripts, externe afbeeldingen, `link`, `style` en `foreignObject` worden uit de gegenereerde SVG verwijderd.
- Het tekenen van TikZ start de LaTeX van de host niet. Het wordt na elkaar uitgevoerd in een WebAssembly-TeX-worker met een bestandssysteem in het geheugen, met grenzen aan invoer, wachtrij, geheugen, uitvoeringstijd (15 seconden) en SVG-uitvoer, en weigert opdrachten voor bestands-I/O.

## Toegang tot documenten en bestanden

- Documentkoppelingen en bestandsbewerkingen kunnen niet buiten de documentatiehoofdmap komen.
- Aanmaken, hernoemen, verplaatsen en verwijderen vanuit de INDEX worden vóór toepassing aan de kant van de extensie opnieuw gecontroleerd: documentatiehoofdmap, versie van de INDEX, pad van het brondocument, soort doel, grenzen van symbolische koppelingen en niet-opgeslagen documenten. Verzoeken vanuit een verouderd menu of vanuit een andere documentatiehoofdmap worden niet toegepast.
- Tijdens het bewerken van een document of tijdens het toepassen van een andere INDEX-bewerking zijn wijzigingen in de INDEX uitgeschakeld.
- Bij aanmaken vanuit een sjabloon worden na het voorbeeld opnieuw gecontroleerd: het vertrouwen van de werkruimte, het bestaan van de documentatiehoofdmap, de versie van de INDEX, de Standard Pack en de gegenereerde inhoud, de opslaglocatie en de grenzen van symbolische koppelingen. Bestaande bestanden worden niet overschreven, en inhoud die afwijkt van het voorbeeld of een uitgepakt resultaat groter dan 4 MiB wordt niet aangemaakt.
- Bij het opslaan van een instellingenbestand wordt vlak daarvoor de versie gecontroleerd; bij een externe wijziging wordt het opslaan afgebroken.

## Verzending naar buiten

- Documenten worden nooit naar buiten gestuurd om ze te lezen, te bewerken of te controleren. De documentcontrole wordt lokaal en deterministisch uitgevoerd.
- Alleen de vertaling (deze pagina vertalen, in bulk vertalen) stuurt documenten naar een taalmodel: de bestemming en de omvang worden vooraf getoond, en alleen na uitdrukkelijke goedkeuring. <!-- ai-only -->
- Vertaalvoorstellen worden als verschil getoond; de versies van het brondocument en van de vertaling worden opnieuw gecontroleerd, en het voorstel wordt alleen toegepast als een persoon het uitdrukkelijk opslaat. <!-- ai-only -->
- Het specificatiehulpmiddel voor AI-agents geeft geen documentinhoud, namen van werkruimten of lokale paden terug. <!-- ai-only -->

## Git

- Opslaan schrijft alleen naar het bestand. Geen enkele functie voert automatisch stagen of vastleggen in Git uit.
- Bestaande bestanden zoals `_meta.json` worden nooit stilzwijgend verwijderd of gewijzigd. Ook verweesde vertalingen worden niet automatisch verwijderd of verplaatst.

## Verwante onderwerpen

- [Belangrijkste specificaties](README.md)
- [Gebruik vanuit AI](ai-agents.md)
