# Die Web-Version lässt sich nicht öffnen oder die Anmeldung schlägt fehl

## Angemeldet, aber das Repository erscheint nicht in der Liste

Die GitHub App „Lunascape Docs“ ist für dieses Konto nicht installiert, oder das Repository ist nicht einbezogen. Bitten Sie den Besitzer des Repositorys oder eine Administratorin bzw. einen Administrator der Organisation, sie nach der Anleitung unter [Ein privates Repository lesen](../06-web/private-repository.md) zu installieren.

## Der Anmeldebildschirm lässt sich nicht verlassen

- Sie haben keine Leseberechtigung für das Repository. Bitten Sie den Besitzer des Repositorys, Ihnen die Berechtigung zu erteilen.
- „Für diese Website ist keine GitHub-Anmeldung eingerichtet“: Für einen selbst bereitgestellten Viewer ist kein Anmeldedienst eingerichtet. Eine Administratorin bzw. ein Administrator muss den Anmeldedienst einrichten.

## Das Pop-up-Fenster für die Anmeldung öffnet sich nicht

Der Browser blockiert das Pop-up. Lassen Sie Pop-ups für diese Website zu und versuchen Sie es erneut.

## „Ihre Anmeldung ist abgelaufen“ wird angezeigt

Die Anmeldung ist abgelaufen. Drücken Sie erneut auf [Mit GitHub anmelden].

## Ein öffentliches Repository liefert 404

- Prüfen Sie die Schreibweise `owner/repo@ref/dir`.
- Branch-Namen, die `/` enthalten, können nicht angegeben werden.

## Nach einer Weile wird nichts mehr geladen

Ohne Anmeldung gilt die Nutzungsgrenze der GitHub API (60 Aufrufe pro Stunde). Wenn „Nutzungsgrenze erreicht“ angezeigt wird, warten Sie eine Weile oder melden Sie sich über [Mit GitHub anmelden] an.

## „Dieses Repository kann von dieser Website nicht angezeigt werden“ wird angezeigt

Um das Repository aus einem selbst bereitgestellten Viewer zu öffnen, muss die URL dieser Website auf der Seite des Repositorys unter `viewer.origins` in `lunascape-docs.json` eingetragen werden.

## Beim Öffnen von `index.html` wird nichts angezeigt

Direkt über `file://` geöffnet funktioniert es nicht. Öffnen Sie die Datei über einen HTTP-Server oder verwenden Sie die VS Code-Version.

## Auf der exportierten Website erscheint „lunascape-docs-manifest.json wurde nicht gefunden“

Stellen Sie den vollständigen Satz der mit `npm run export:web` erzeugten Dateien (einschließlich des Manifests) unverändert bereit.

## Entwürfe lassen sich nicht speichern

- „IndexedDB kann nicht geöffnet werden“ / „Wird in einem anderen Tab verwendet“: Ursache ist der private Modus des Browsers oder ein anderer Tab, in dem dieselbe Website geöffnet ist. Öffnen Sie die Website in einem normalen Fenster und schließen Sie die anderen Tabs.
- Entwürfe werden pro Gerät und Browser gespeichert. Sie werden nicht auf ein anderes Gerät übertragen.

## Verwandte Themen

- [Ein GitHub-Repository öffnen](../06-web/open-repository.md)
- [Entwürfe speichern](../06-web/drafts.md)
