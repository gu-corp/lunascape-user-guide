# Een GitHub-repository openen

In de webversie en in Lunascape kunt u een GitHub-repository direct openen en lezen, zonder deze te dupliceren. Voor openbare repository's hoeft u zich niet aan te melden.

## Openen vanuit het scherm

1. Klik in de werkbalk op [Documenten openen] (het mappictogram). Het scherm “Documenten openen” wordt geopend.
2. Kies in de linkerkolom waar u wilt openen.

   | Locatie | Wat er staat |
   |---|---|
   | Alles | Alles hieronder. Wat u onlangs hebt geopend, staat bovenaan |
   | Recent geopend | De repository's en mappen die u eerder hebt geopend |
   | Aanbevolen | De handleidingen die de site aanbeveelt |
   | GitHub-repository's | De repository's die u kunt lezen, als u bent aangemeld bij GitHub |
   | Deze computer | Mappen op dit apparaat. In Lunascape staan hier ook de repository's die u hebt gedupliceerd |

3. Klik op [Openen] in de rij die u wilt openen. Typ bovenaan in [Filteren op document- of repositorynaam] om het aantal rijen te beperken.

Staat een repository niet in de lijst, geef deze dan op via [owner/repo invoeren en openen] in de linkerkolom.

> **Tip**
>
> - In de lijst staan de GitHub-repository's waarop de GitHub App “Lunascape Docs” is geïnstalleerd en waarvoor u leesrechten hebt. Ziet u een repository niet, vraag de eigenaar dan om de App toe te voegen.

## De locatie van een document controleren

Het kleine pictogram links in de werkbalk (de locatiechip) laat zien waar het document staat dat u nu leest.

| Pictogram | Locatie |
|---|---|
| Het GitHub-logo | Wordt gelezen vanaf GitHub. Niet opgeslagen op dit apparaat |
| Een computer | Een map op dit apparaat die door Lunascape wordt beheerd. De Git-branch en het aantal gewijzigde bestanden worden ook weergegeven |
| Een map | Een map op dit apparaat |

Klik op het pictogram om de locatie, de status en de beschikbare acties te zien, zoals [Bekijken op GitHub] en [Link kopiëren].

## Een repository dupliceren in Lunascape

In Lunascape kunt u een GitHub-repository naar dit apparaat dupliceren en daarna met Git bewerken en committen.

- Klik in het scherm “Documenten openen” op [Dupliceren] in de rij van de repository.
- Leest u een repository die vanaf GitHub is geopend, klik dan op de locatiechip en daarna op [Dupliceren naar deze computer]. Als het dupliceren klaar is, wordt hetzelfde document geopend vanaf de kopie op dit apparaat.

Een gedupliceerde repository staat in de lijst met de vermelding “Op deze computer”, en [Openen op deze computer] staat vooraan.

## Openen via een URL

Het adres bestaat uit de repository gevolgd door de locatie van het document. Het pad is de locatie binnen de repository, dus de volgorde is dezelfde als in de GitHub-URL.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Wat u opgeeft | Notatie |
|---|---|
| Alleen de repository (standaardbranch) | `/github/owner/repo` |
| Een document in de repository | `/github/owner/repo/docs/01-product/vision.md` |
| Een branch of tag | Voeg `?ref=v1.2.0` toe aan het einde |

Als u naar een andere pagina gaat, verandert het adres mee. Klik in de werkbalk op [Dit document delen] om een link naar de pagina die u leest door te geven. De knoppen [Terug] en [Vooruit] van de browser werken ook.

De oudere vorm met `?source=` werkt nog steeds. Na het openen wordt het adres omgezet naar de nieuwe vorm.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Let op**
>
> - Zonder aanmelding geldt de limiet van de GitHub API (60 verzoeken per uur). Meld u aan met [Aanmelden met GitHub] bij repository's met veel documenten of als u vaak leest.
> - Branchnamen met een `/` (zoals `feature/xxx`) kunt u opgeven met `?ref=` in de bovenstaande adresvorm. In de vorm met `?source=` is dat niet mogelijk.
> - Documenten worden geladen met de GitHub-rechten van de lezer. Wie geen leesrechten heeft, ziet ze niet.

## Documenten uit een lokale map openen

Klik in de werkbalk op [Documenten openen], klik in de linkerkolom op [Documenten uit een lokale map openen] en kies een map op uw apparaat. De bestanden worden in de browser verwerkt en nergens naartoe verzonden. Dit werkt in browsers die het kiezen van mappen ondersteunen (zoals Chrome en Edge).

## Verwante onderwerpen

- [Een privérepository lezen](private-repository.md)
- [De webversie opent niet of aanmelden lukt niet](../07-troubleshooting/web.md)
