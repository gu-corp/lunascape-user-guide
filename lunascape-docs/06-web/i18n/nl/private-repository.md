# Een privérepository lezen

Nadat u zich met GitHub hebt aangemeld, kunt u de documenten van privérepository's lezen, beperkt tot de repository's waarvoor u leestoegang hebt. Lunascape Docs heeft nooit eigen accounts of machtigingen.

## Aanmelden en openen

1. Open <https://docs.lunascape.org/>.
   Wanneer u een privédocument opgeeft of nog niet bent aangemeld, verschijnt het aanmeldscherm.
2. Druk op [Aanmelden met GitHub].
   Het autorisatiescherm van GitHub wordt geopend in een pop-up.
3. Druk na het aanmelden op [Documenten openen] in de werkbalk en kies de gewenste repository via [Kiezen uit leesbare repository's].

> **Tip**
>
> - De naam van het aangemelde account wordt in de werkbalk weergegeven. Ook [Afmelden] en [Aanmelden met een ander account] kunt u hier uitvoeren.
> - In de lijst verschijnen de repository's van de accounts (organisaties of personen) waarop de GitHub App "Lunascape Docs" is geïnstalleerd, beperkt tot de repository's waarvoor u leestoegang hebt.

## Instellingen door de eigenaar van de repository

Als de betreffende repository niet in de lijst verschijnt, moet de eigenaar van de repository of de beheerder van de organisatie de GitHub App "Lunascape Docs" installeren.

- De gevraagde machtigingen zijn Contents (lezen en schrijven) en Pull requests (lezen en schrijven). Lezen is voor het bekijken, schrijven is voor het publicatieverzoek (Pull Request) vanaf het web. Lunascape Docs slaat de inhoud van de documenten nooit op.
- De installatie gebeurt per account (organisatie of persoon). U stelt in of het doel "All repositories" is (waaronder ook later aangemaakte repository's automatisch vallen) of alleen de geselecteerde repository's.

| Situatie | Stappen |
|---|---|
| Nieuw introduceren op een organisatie- of persoonlijk account | Voer dit uit via de [installatiepagina](https://github.com/apps/lunascape-docs/installations/new) |
| Doelrepository's toevoegen in een organisatie waar het al is geïnstalleerd | Stel dit in via Settings van de organisatie → GitHub Apps → Lunascape Docs → Configure → Repository access |

Ook wanneer de app voor een hele organisatie is geïnstalleerd, kan elk lid alleen de repository's bekijken waarvoor het zelf leestoegang heeft. Een publicatieverzoek kan het ook alleen sturen naar repository's waarvoor het zelf schrijftoegang heeft.

> **Tip**
> - Bij een nieuwe installatie worden de gevraagde machtigingen in een lijst op het installatiescherm getoond, en met het drukken op "Install" hebt u ze goedgekeurd. Er zijn geen extra handelingen nodig.
> - Een organisatie die de app al had geïnstalleerd voordat een machtiging werd toegevoegd, ontvangt een bevestigingsmail bij de beheerders, en boven aan Settings van de organisatie → GitHub Apps → Lunascape Docs → Configure verschijnt een goedkeuringsknop. Totdat er is goedgekeurd, kan die organisatie alleen bekijken, en bij het sturen van een publicatieverzoek verschijnt "Schrijftoegang moet worden verleend".
> - Met welke machtigingen de app nu is geïnstalleerd, kunt u op datzelfde Configure-scherm controleren. Voor een persoonlijk account is dat Settings → Applications → Installed GitHub Apps.
> - Als u de doelrepository's per ongeluk hebt verwijderd of de app hebt gedeïnstalleerd, kunt u ze herstellen door opnieuw te installeren via de [installatiepagina](https://github.com/apps/lunascape-docs/installations/new). Het afwijzingsbericht van een publicatieverzoek bevat een link naar het scherm waar u dit herstelt.
> - Als u aan de kant van de repository geen publicatieverzoeken wilt ontvangen, schrijft u `"publish": { "enabled": false }` in `lunascape-docs.json`. Het lezen blijft gewoon werken.

## Verwante onderwerpen

- [Een GitHub-repository openen](open-repository.md)
- [De webversie kan niet openen of aanmelden](../07-troubleshooting/web.md)
