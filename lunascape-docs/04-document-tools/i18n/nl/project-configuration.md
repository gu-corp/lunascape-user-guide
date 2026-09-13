# Projectinstellingen

`lunascape-docs.json` direct onder de documentatiehoofdmap bevat de instellingen van die hoofdmap, die het team deelt. Het bestand wordt beheerd in Git.

## Het instellingenbestand maken of bewerken

- Druk in de werkbalk op [Documenthulpmiddelen] → tabblad [Controle] → [Herkomst van de regels en documentinstellingen] → [Documentinstellingen bewerken] om het bestand in VS Code te openen. Bestaat het bestand nog niet, dan wordt op dat moment een beginbestand aangemaakt.
- Aan de bestandsnaam `lunascape-docs.json` wordt automatisch het meegeleverde JSON Schema gekoppeld, met aanvulling en een beschrijving bij elk veld. Een `$schema`-vermelding is niet nodig.

## Voorbeeld

```json
{
  "id": "product-docs",
  "title": "Productdocumentatie",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Beschrijving van de velden

| Veld | Inhoud | Standaard |
|---|---|---|
| `id` | De sleutel waaronder de weergave-instellingen per gebruiker worden bewaard. Geef een vaste waarde op als de instellingen behouden moeten blijven wanneer de map verplaatst wordt | Het pad van de map |
| `title` | De naam die links in de werkbalk en in de lijst met documentatiehoofdmappen verschijnt. Deze verandert niet met de weergavetaal | De kop van de README/index van de hoofdmap, anders de mapnaam |
| `indexTitle` | De kop van de INDEX | `INDEX` |
| `startPage` | Het document dat als eerste wordt geopend (pad ten opzichte van de documentatiehoofdmap) | `README.md` |
| `appearance` | Het kleurenschema: `light` (altijd licht) of `auto` (volgt het thema van VS Code) | `light` |
| `defaultLocale` | De standaardtaal (de taal van de brondocumenten), opgegeven als BCP 47-taalcode (`ja`, `en`, `zh-Hant` enzovoort). Dit is de brontaal voor vertalingen | Niet ingesteld (voor de weergave afgeleid uit de tekst) |
| `fallbackLocale` | De taal die het eerst wordt getoond aan lezers van wie de omgevingstaal met geen van de ondersteunde talen overeenkomt. Noem een taal die in `locales` staat | Niet ingesteld (`defaultLocale` wordt gebruikt) |
| `locales` | De lijst met ondersteunde talen, inclusief `defaultLocale`. Ze vormen het taalmenu en de mogelijke doeltalen voor vertaling | Alleen `defaultLocale` |
| `ignoredDirectories` | Mapnamen die uit de INDEX, het zoeken en de controles worden weggelaten. Wie dit opgeeft, vervangt de standaardwaarde | `["99-archive"]` |
| `tree` | De standaardwaarden voor de weergave van de INDEX. Gebruikers kunnen ze bij de weergave-instellingen overschrijven | Zoals in het voorbeeld hierboven |
| `editor.defaultMode` | De bewerkingsweergave zolang de gebruiker nog niet heeft gewisseld: `visual` of `source` | `visual` |
| `editor.showEditButton` | Of [Bewerken] rechtsonder in het document wordt getoond | `true` |
| `documentStandards.pack` | De Standard Pack voor de documentcontrole en de sjablonen: `builtin:<naam>` of een pad ten opzichte van de documentatiehoofdmap | Geen |
| `documentStandards.profile` | De naam van een profiel dat de pack definieert | Geen |
| `translation.enabled` | Schakelt vertaalvoorstellen en vertaling in bulk in | `true` |
| `translation.contextFiles` | Markdown-bestanden van het brondocument (pad ten opzichte van de documentatiehoofdmap) die bij het vertalen als naslag voor terminologie en stijl worden meegegeven | `[]` |
| `translation.maxContextCharacters` | De bovengrens voor het totale aantal tekens van de naslagdocumenten (maximaal 1048576) | `49152` |
| `description` | Een regel over de documentenverzameling, getoond op de kaarten van de startpagina van een repository. Net als bij `title` een tekst of een object per taal | Geen |

## Aangeven waar de documenten in de repository staan

Een `lunascape-docs.json` direct onder de repository kan in plaats van de instellingen van die map een **kaart van de repository** bevatten. Wie een van de volgende drie velden invult, maakt er een kaart van; de map zelf is dan geen documentatiehoofdmap.

| Veld | Inhoud | Standaard |
|---|---|---|
| `defaultFolder` | In welke map de documenten staan (pad ten opzichte van deze map). De map waarnaar het verwijst heeft zelf geen instellingenbestand nodig | Geen (`docs` wordt gebruikt) |
| `roots` | De lijst met documentenverzamelingen, als er meerdere zijn (paden ten opzichte van deze map, in weergavevolgorde). Deze map wordt dan de startpagina | Geen |
| `excludes` | Mappen die bij het zoeken naar documentatiehoofdmappen worden overgeslagen (paden ten opzichte van deze map). Komen bovenop de standaarduitsluitingen zoals `node_modules` | `[]` |
| `home.cards` | Of de startpagina onder zijn README de kaarten van de documentenverzamelingen toont. Zet dit op `false` als u de links zelf in de README schrijft | `true` |

De documentatiehoofdmap wordt in deze volgorde bepaald. De eerste die wordt gevonden, wordt gebruikt.

1. De map die u via een instelling of een opdracht hebt opgegeven
2. Waar `defaultFolder` of `roots` in de `lunascape-docs.json` direct onder de repository naar verwijst
3. Een map met een `lunascape-docs.json` (zijn er twee of meer onder een gemeenschappelijke bovenliggende map, dan wordt die de startpagina)
4. De map `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. De repository zelf

> **Tip**
>
> Als u niets invult, geldt stap 4, en dus blijft een gewone repository met één `docs/` werken zoals voorheen. Vul `defaultFolder` alleen in wanneer de map anders heet, bijvoorbeeld `manual`.

### Voorbeeld van een kaart

```json
{
  "title": "Lunascape Help",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Voorrang van de instellingen

Voor de velden die met de weergave te maken hebben, geldt deze volgorde.

1. De weergave-instellingen van de gebruiker (paneel [Weergave-instellingen])
2. De instellingen van VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. De standaardwaarden van het product

Alleen de talen (`defaultLocale`, `fallbackLocale`, `locales`) vormen een uitzondering: daarvoor is `lunascape-docs.json` bepalend. Persoonlijke instellingen in VS Code kunnen de talen van het project niet overschrijven.

> **Opmerking**
>
> Een Standard Pack kan ook in `docs-lint.config.json` worden opgegeven als `standard`. Staat de pack in beide bestanden, dan heeft `docs-lint.config.json` voorrang.

## Verwante onderwerpen

- [Controleregels wijzigen](rules.md)
- [Weergave-instellingen wijzigen](../02-reading/display-settings.md)
- [Overzicht van de VS Code-instellingen](../08-reference/settings.md)
