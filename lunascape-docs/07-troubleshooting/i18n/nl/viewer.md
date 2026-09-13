# Documenten verschijnen niet

## "Geen Markdown- of docs-map gevonden om te openen" wordt weergegeven

- De werkruimte heeft geen `docs`-map, of gebruikt een andere naam.
  - Zet een `lunascape-docs.json` in die map, dan wordt zij ongeacht haar naam als documentatiehoofdmap herkend.
  - Of voeg de mapnaam toe aan de instelling `lunascapeDocEditor.rootDirectoryNames`.
- Als er nog geen documenten zijn, maakt u ze met "Lunascape Docs: Documentatie maken op basis van een sjabloon".
- U kunt ook een Markdown-bestand in de editor openen en "Lunascape Docs: Openen in specificatieviewer" uitvoeren.

## Een document staat niet in de INDEX

- Controleer of de extensie `.md`, `.markdown` of `.mdx` is.
- De volgende mappen worden niet getoond: mappen die met `.` beginnen, `node_modules` en mappen die in `ignoredDirectories` zijn opgegeven (standaard `99-archive`).
- Vertalingen onder `i18n/` verschijnen niet afzonderlijk in de INDEX. U schakelt ernaartoe via het taalmenu.
- Als een zojuist toegevoegd bestand niet verschijnt, drukt u op [Opnieuw laden].
- Mogelijk kijkt u naar een andere documentatiehoofdmap. Controleer de naam van de documentatiehoofdmap uiterst links op de werkbalk.

## Op een map drukken toont niets

De `README.md` van die map is een "descriptor die alleen instellingen bevat": met front matter maar zonder tekst. Open de map in de INDEX en kies een document daarbinnen.

## Er wordt een onbedoelde documentatiehoofdmap geopend

- Als de instelling `lunascapeDocEditor.rootMode` op `fixed` staat, wordt altijd `lunascapeDocEditor.root` geopend.
- Bij `auto` wordt de documentatiehoofdmap gekozen die het dichtst bij het geopende Markdown-bestand ligt. U schakelt via de keuzelijst uiterst links op de werkbalk.

## De naam van de documentatiehoofdmap is anders dan verwacht

De naam wordt bepaald in deze volgorde: `title` in `lunascape-docs.json` → `navigation.title` van de `README.md` in de hoofdmap → de H1 daarvan → `index.md` → de mapnaam. Stel `title` in als u hem wilt vastleggen.

## De INDEX is verdwenen

- In een documentatiehoofdmap met maar één document sluit de INDEX zichzelf de eerste keer. U opent hem met het kolompictogram op de werkbalk. Via [Verbergen als er maar één document is] in [Weergave-instellingen] schakelt u dit uit.
- Op een smal scherm opent u hem met [INDEX openen] (drie streepjes) links van [Terug].

## Een koppeling gaat niet open

- "Doel van de koppeling niet gevonden": het bestand waarnaar wordt verwezen bestaat niet. Met [Controle] in Documenthulpmiddelen controleert u de interne koppelingen.
- "Onveilige of niet-ondersteunde koppeling niet geopend": koppelingen buiten de documentatiehoofdmap, of naar een ander schema dan `https://` of `mailto:`, worden niet geopend.

## De getoonde taal is anders dan bedoeld

- Controleer in het taalmenu de taal van de weergegeven pagina en de reden daarvoor.
- De laatst gekozen weergavetaal wordt onthouden. Kies de standaardtaal opnieuw in het taalmenu.
- Als de persoonlijke instelling `lunascapeDocEditor.locale` is ingesteld, krijgt de vertaling in die taal voorrang.

## Verwante onderwerpen

- [Van documentatiehoofdmap wisselen](../02-reading/roots.md)
- [Documentatiehoofdmappen en bestandsconventies](../04-document-tools/structure.md)
