# Documentatiehoofdmappen en bestandsconventies

Dit zijn de regels waarmee Lunascape Docs documenten vindt en de INDEX opbouwt. Het bestandssysteem zelf is het brondocument, dus een register of een buildconfiguratie is niet nodig.

## Documentatiehoofdmap

- De dichtstbijzijnde map `docs`, of de map waarin `lunascape-docs.json` staat, wordt de documentatiehoofdmap.
- Met een `lunascape-docs.json` hoeft de map niet `docs` te heten.
- Opent u een Markdown-bestand dat niet bij een documentatiehoofdmap hoort, dan wordt de map ervan als tijdelijke documentatiehoofdmap weergegeven.

## Bestanden die in de INDEX verschijnen

- Bestanden met `.md`, `.markdown` en `.mdx` worden weergegeven. Nieuwe bestanden verschijnen altijd, ook zonder front matter of navigatiegegevens.
- Mappen die met `.` beginnen, `node_modules` en de mappen die u opgeeft in `ignoredDirectories` (standaard `99-archive`) worden niet weergegeven.
- Alles onder `i18n/` geldt als vertaling en wordt niet afzonderlijk in de INDEX vermeld.

## Openingspagina van een map

- Een `README.md` met inhoud (of `index.md` als die er niet is) is de openingspagina van die map. Drukt u in de INDEX op de mapnaam, dan wordt de openingspagina geopend.
- Een `README.md` die alleen uit front matter bestaat, zonder inhoud, geldt als "descriptor uitsluitend voor instellingen" en wordt niet als pagina weergegeven. Gebruik dit wanneer een map alleen een titel of een volgorde nodig heeft.
- Zijn zowel `README.md` als `index.md` aanwezig, dan heeft `README.md` voorrang.

## Standaardtaal en vertalingen

- Documenten in de standaardtaal (het brondocument) blijven op hun plaats staan.
- Een vertaling plaatst u in `i18n/<taal>/` in dezelfde map als het brondocument, onder dezelfde bestandsnaam. De mapstructuur opnieuw opbouwen onder `i18n/` wordt niet herkend.
- Dat is de enige plaats waar een vertaling wordt gevonden. Hetzelfde bestand elders geplaatst is een losstaand bestand dat bij geen enkel document als vertaling geldt.

```text
docs/
  lunascape-docs.json
  README.md                  ← openingspagina van de hoofdmap (startpagina)
  i18n/en/README.md          ← de Engelse versie daarvan
  01-product/
    README.md                ← openingspagina van de map
    requirements.md
    i18n/en/README.md        ← de Engelse versies van de twee documenten hierboven
    i18n/en/requirements.md
  99-archive/                ← standaard uitgesloten van de INDEX
```

## Over `_meta.json`

De `_meta.json` van Nextra wordt niet voor navigatie gebruikt. Bestaande bestanden worden niet gewijzigd en niet verwijderd. In de toekomst worden ze alleen behandeld door een uitdrukkelijke functie voor importeren en exporteren.

## Verwante onderwerpen

- [Navigatiegegevens instellen](navigation-metadata.md)
- [Projectinstellingen](project-configuration.md)
- [Van documentatiehoofdmap wisselen](../02-reading/roots.md)
