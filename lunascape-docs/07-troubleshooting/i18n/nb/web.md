# Nettversjonen kan ikke åpnes eller logges på

## Du er pålogget, men repositoriet vises ikke i listen

GitHub App-en «Lunascape Docs» er ikke installert på den kontoen, eller repositoriet er ikke tatt med. Be repositorieeieren eller en organisasjonsadministrator om å installere den slik det er beskrevet i [Lese et privat repositorium](../06-web/private-repository.md).

## Kommer ikke videre fra påloggingsskjermen

- Du har ikke lesetilgang til repositoriet. Be repositorieeieren om å gi deg tilgang.
- «このサイトには GitHub ログインが設定されていません» (GitHub-pålogging er ikke konfigurert for dette nettstedet): en visning du selv har satt opp, har ingen påloggingstjeneste konfigurert. En administrator må sette opp en.

## Popup-vinduet for pålogging åpnes ikke

Nettleseren blokkerte popup-vinduet. Tillat popup-vinduer for dette nettstedet, og prøv på nytt.

## «ログインが切れています» (Påloggingen din har utløpt) vises

Påloggingen har utløpt. Trykk [Logg inn med GitHub] på nytt.

## Et offentlig repositorium gir 404

- Kontroller formatet `owner/repo@ref/dir`.
- Grennavn som inneholder `/`, kan ikke angis.

## Innlasting slutter å fungere etter en stund

Uten pålogging gjelder grensen for GitHub API-forespørsler (60 forespørsler per time). Når «回数制限に達しました» (Grensen for antall forespørsler er nådd) vises, venter du en stund eller logger på med [Logg inn med GitHub].

## «このサイトからは、このリポジトリを表示できません» (Dette nettstedet kan ikke vise dette repositoriet) vises

For å åpne et repositorium fra en visning du selv har satt opp, må nettstedets URL legges til i `viewer.origins` i repositoriets `lunascape-docs.json`.

## Ingenting vises når du åpner `index.html`

Det fungerer ikke når det åpnes direkte via `file://`. Server det over HTTP, eller bruk VS Code-versjonen.

## En eksportert side viser «lunascape-docs-manifest.json が見つかりません» (fant ikke manifestet)

Publiser hele utdataen fra `npm run export:web`, inkludert manifestet, som den er.

## Utkast kan ikke lagres

- «IndexedDB を開けません» (Kan ikke åpne IndexedDB) / «他のタブで使用中です» (Brukes i en annen fane): forårsakes av nettleserens privatmodus eller av en annen fane som viser samme nettsted. Bruk et vanlig vindu, og lukk de andre fanene.
- Utkast lagres per enhet og nettleser. De overføres ikke til en annen enhet.

## Relaterte emner

- [Åpne et GitHub-repositorium](../06-web/open-repository.md)
- [Lagre utkast](../06-web/drafts.md)
