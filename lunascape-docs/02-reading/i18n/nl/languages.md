# Lezen in een andere taal

Als een document vertalingen heeft, kunt u de taal wisselen via het taalmenu (wereldbol) op de werkbalk.

## De taal wisselen

1. Druk op het taalmenu op de werkbalk.
   De taal van de huidige pagina wordt getoond, samen met de reden daarvoor (het pad van de vertaling, automatische detectie of de standaardtaal van het project).
2. Kies de taal waarin u wilt lezen.
   De vertaling van hetzelfde document wordt geopend. De gekozen taal wordt onthouden; het volgende document dat u opent, wordt in die taal getoond als er een vertaling is.

In de lijst met talen ziet u of dit document in die taal vertaald is.

| Weergave | Betekenis |
|---|---|
| Vertaald | Er is een vertaling en die kan worden geopend |
| Niet vertaald | Het project ondersteunt deze taal, maar van dit document is er nog geen vertaling |
| Verouderd | Er is een vertaling, maar het oorspronkelijke document is na de vertaling gewijzigd |

> **Let op**
>
> - Het kiezen van een taal opent alleen een bestaande vertaling. Er wordt geen vertaling gemaakt en er wordt geen bestand aangemaakt. Gebruik [Vertalingen maken en beheren…] in hetzelfde menu om een vertaling te maken.
> - Als wordt vastgesteld dat de taal van de huidige pagina afwijkt van de standaardtaal van het project, verschijnt er een waarschuwing. De instellingen worden niet gewijzigd.

## De taal waarin een document opent

Als u een document opent, wordt de eerste weergavetaal in deze volgorde bepaald.

1. De taal die u eerder in deze documentatiehoofdmap zelf hebt gekozen. Uw keuze wordt bewaard (ook de keuze voor de standaardtaal wordt als keuze bewaard).
2. De weergavetaal van VS Code (in de webbrowserversie: de taalinstellingen van de browser). Een overeenkomende ondersteunde taal wordt automatisch gekozen. Een taal met regio (zoals `en-US`) komt ook overeen met de basistaal (`en`).
3. De terugvaltaal van het project (`fallbackLocale` in `lunascape-docs.json`).
4. De standaardtaal van het project.

> **Tip**
>
> - Als de taal automatisch is gekozen, staat bij de huidige taal in het taalmenu de vermelding "Automatisch gekozen". Beweeg de aanwijzer over de badge om de reden te zien.
> - `fallbackLocale` is de taal die u toont aan lezers wier omgevingstaal met geen van de ondersteunde talen overeenkomt. Stelt u in een project met Japans als brontaal en een Engelse versie `"en"` in, dan opent voor een lezer met bijvoorbeeld een Spaanstalige omgeving de Engelse versie. Zonder instelling wordt de standaardtaal gebruikt.

## Waar vertalingen staan

Documenten in de standaardtaal blijven op hun plaats staan; vertalingen zet u onder dezelfde bestandsnaam in **`i18n/<taal>/` in dezelfde map**.

```text
docs/
  README.md                  ← standaardtaal (bijvoorbeeld Japans)
  i18n/en/README.md          ← de Engelse versie daarvan
  guide/
    setup.md
    i18n/en/setup.md         ← de Engelse versie daarvan
```

> **Let op**
>
> - De mapstructuur opnieuw opbouwen onder `i18n/` (`i18n/en/guide/setup.md`) wordt niet herkend. `i18n/` staat altijd in dezelfde map als het document zelf.
> - Vertalingen worden uitsluitend op die ene plaats gezocht. Zet u de vertaling van hetzelfde document ook in de `i18n/` van een bovenliggende map, dan ontstaat er geen conflict over "welke voorrang heeft": dat bestand wordt een verweesd bestand dat noch in het taalmenu, noch in het overzicht verschijnt (en het wordt niet automatisch verwijderd). Zet dezelfde vertaling niet op twee plaatsen.

## Lezen in de webbrowserversie

Ook in de webbrowserversie wisselt u op dezelfde manier van taal wanneer er een vertaling is. Wilt u lezen in een taal waarvoor geen vertaling bestaat, dan kunt u de paginavertaling van uw browser gebruiken. Code, formules en diagrammen worden daarbij niet vertaald.

## Verwante onderwerpen

- [Werk aan een AI overdragen](../05-ai/README.md)
- [Werk dat u kunt overdragen](../05-ai/tasks.md)
- [Weergave-instellingen wijzigen](../02-reading/display-settings.md)
