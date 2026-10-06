# Een GitHub-repository openen

In de webversie kunt u een GitHub-repository direct openen en lezen, zonder deze te klonen. Voor openbare repository's hoeft u zich niet aan te melden.

## Openen vanuit het scherm

1. Druk op [Documenten openen] (het mappictogram) in de werkbalk. Het scherm “Documenten openen” wordt geopend.
2. Kies in de linkerkolom waar u wilt openen.

   | Locatie | Wat er staat |
   |---|---|
   | Alles | Alles hieronder. Wat u onlangs hebt geopend, staat bovenaan |
   | Recent geopend | De repository's en mappen die u eerder hebt geopend |
   | Aanbevolen | De handleidingen die de site aanbeveelt |
   | GitHub-repository's | Als u bent aangemeld met GitHub: de repository's die u kunt lezen |
   | Deze computer | Mappen op dit apparaat |

3. Druk op [Openen] in de rij die u wilt openen. Typ bovenaan in [Filteren op document- of repositorynaam] om de rijen te filteren.

Een repository die niet in de lijst staat, geeft u op via [owner/repo invoeren en openen] in de linkerkolom.

> **Tip**
>
> - De GitHub-repository's in de lijst zijn de repository's waarop de GitHub App “Lunascape Docs” is geïnstalleerd en waarvoor u leesrechten hebt. Ziet u een repository niet, vraag de eigenaar dan om de App toe te voegen.

## De locatie van een document controleren

Het kleine pictogram links in de werkbalk (de locatiechip) laat zien waar het document staat dat u nu leest.

| Pictogram | Locatie |
|---|---|
| Het GitHub-logo | U leest vanaf GitHub. Er wordt niets op dit apparaat opgeslagen |
| Map | Een map op dit apparaat |

Druk op het pictogram om de locatie, de status en de beschikbare acties te zien, zoals [Bekijken op GitHub] en [Link kopiëren].

## Openen via een URL

Het adres bestaat uit de repository en de plaats van het document, achter elkaar. Het pad is de plaats binnen de repository, dus de volgorde is dezelfde als in de GitHub-URL.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Wat u opgeeft | Schrijfwijze |
|---|---|
| Alleen de repository (standaardbranch) | `/github/owner/repo` |
| Een document in de repository | `/github/owner/repo/docs/01-product/vision.md` |
| Een branch of tag | Voeg `?ref=v1.2.0` aan het eind toe |

Als u naar een andere pagina gaat, verandert ook het adres. Druk op [Dit document delen] in de werkbalk om een link naar de pagina die u leest door te geven. U kunt ook [Terug] en [Vooruit] van de browser gebruiken.

De oudere vorm met `?source=` werkt nog steeds. Na het openen wordt het adres omgezet naar de nieuwe vorm.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Let op**
>
> - Zonder aanmelding geldt de limiet van de GitHub API (60 aanvragen per uur). Meld u bij repository's met veel documenten of bij herhaald lezen aan via [Aanmelden met GitHub].
> - Branchnamen met een `/` (zoals `feature/xxx`) kunt u opgeven met `?ref=` in de adresvorm hierboven. In de vorm met `?source=` is dat niet mogelijk.
> - Documenten worden geladen met de GitHub-rechten van de lezer. Wie geen leesrechten heeft, ziet ze niet.

## Documenten uit een lokale map openen

Druk op [Documenten openen] in de werkbalk, kies [Documenten uit een lokale map openen] in de linkerkolom en selecteer een map op uw apparaat. De bestanden worden in de browser verwerkt en nergens naartoe verzonden. Dit werkt in browsers die het selecteren van mappen ondersteunen (zoals Chrome en Edge).

## Verwante onderwerpen

- [Een privérepository bekijken](private-repository.md)
- [De webversie opent niet of aanmelden lukt niet](../07-troubleshooting/web.md)
