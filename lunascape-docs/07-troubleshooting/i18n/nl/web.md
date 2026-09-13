# De webversie opent niet of aanmelden lukt niet

## Aangemeld, maar de repository staat niet in de lijst

Op dat account is de GitHub App "Lunascape Docs" niet geïnstalleerd, of de betreffende repository valt er niet onder. Vraag de eigenaar van de repository of een beheerder van de organisatie om de app te installeren volgens de stappen in [Een niet-openbare repository bekijken](../06-web/private-repository.md).

## U komt niet voorbij het aanmeldscherm

- U hebt geen leesrechten voor de betreffende repository. Vraag de eigenaar van de repository om u rechten te geven.
- "Voor deze site is aanmelden met GitHub niet ingesteld": voor een zelf geplaatste viewer is geen aanmeldservice ingesteld. De beheerder moet een aanmeldservice instellen.

## De pop-up voor aanmelden opent niet

De browser blokkeert de pop-up. Sta pop-ups voor deze site toe en probeer het opnieuw.

## De melding "Uw aanmelding is verlopen" verschijnt

De geldigheidsduur van de aanmelding is verstreken. Druk opnieuw op [Aanmelden met GitHub].

## Een openbare repository geeft 404

- Controleer de notatie `owner/repo@ref/dir`.
- Branchnamen met `/` kunnen niet worden opgegeven.

## Na een tijdje lukt het laden niet meer

Zonder aanmelding geldt een gebruikslimiet voor de GitHub API (60 keer per uur). Verschijnt de melding "De limiet is bereikt", wacht dan even of meld u aan met [Aanmelden met GitHub].

## De melding "Deze site kan deze repository niet tonen" verschijnt

Om de repository vanuit een zelf geplaatste viewer te openen, moet de URL van die site worden toegevoegd aan `viewer.origins` in de `lunascape-docs.json` van de repository.

## Er verschijnt niets als u `index.html` opent

Rechtstreeks openen via `file://` werkt niet. Open de site via een HTTP-server of gebruik de VS Code-versie.

## Op de geëxporteerde site verschijnt "lunascape-docs-manifest.json is niet gevonden"

Plaats de volledige set bestanden die `npm run export:web` uitvoert, inclusief het manifest, ongewijzigd.

## Het concept kan niet worden opgeslagen

- "IndexedDB kan niet worden geopend" / "In gebruik door een ander tabblad": dit komt door de privémodus van de browser of door een ander tabblad waarin dezelfde site openstaat. Open de site in een gewoon venster en sluit de andere tabbladen.
- Concepten worden per apparaat en per browser opgeslagen. Ze gaan niet mee naar een ander apparaat.

## Verwante onderwerpen

- [Een GitHub-repository openen](../06-web/open-repository.md)
- [Een concept opslaan](../06-web/drafts.md)
