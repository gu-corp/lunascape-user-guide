# Entwürfe speichern

Wenn Sie ein Dokument im Web-Viewer bearbeiten, werden die Änderungen nicht in das Repository geschrieben, sondern als „Entwurf" im Browser gespeichert.

## Einen Entwurf anlegen

1. Öffnen Sie ein Dokument und drücken Sie unten rechts [Bearbeiten].
2. Bearbeiten Sie das Dokument und drücken Sie [Speichern].
   „Als Entwurf gespeichert" wird angezeigt, und die Änderung wird im Browser gespeichert.

- Dokumente mit einem Entwurf erhalten im INDEX eine Markierung. Über dem Text erscheint „Dieses Dokument ist ein Entwurf auf diesem Gerät (nicht veröffentlicht)".
- [Entwürfe] in der Symbolleiste zeigt die Anzahl an; ein Druck darauf öffnet die Liste der Entwürfe.

## Einen Entwurf verwerfen

- Um den Entwurf eines einzelnen Dokuments zu verwerfen, drücken Sie über dem Text [Entwurf verwerfen].
- Um alle Entwürfe zu verwerfen, verwenden Sie die Liste der Entwürfe.

## Entwürfe in das Repository übernehmen

Die „Veröffentlichungsanfrage", die Entwürfe als Pull Request sendet, ist zwar umgesetzt, im öffentlichen Viewer aber nicht aktiviert. Um das Repository zu ändern, bearbeiten Sie die Dokumente mit der VS Code-Erweiterung oder in einem lokalen Klon.

> **Hinweis**
>
> - Entwürfe werden im Browser (IndexedDB) gespeichert. Sie werden nicht auf einen anderen Browser oder ein anderes Gerät übertragen. Wenn Sie die Websitedaten des Browsers löschen, werden auch die Entwürfe gelöscht.
> - Wird das Dokument im Repository geändert, nachdem Sie einen Entwurf angelegt haben, erscheint „Die Quelle wurde aktualisiert". Prüfen Sie den Inhalt und entscheiden Sie dann, ob Sie den Entwurf verwerfen oder weiterverwenden.
> - Wenn Sie über [Dokumente öffnen] einen lokalen Ordner öffnen und bearbeiten, werden die Änderungen direkt in die Datei geschrieben, sofern der Browser dies unterstützt. Bei Browsern ohne diese Unterstützung bleiben sie nur für die aktuelle Sitzung erhalten.

## Verwandte Themen

- [Was der Web-Viewer kann](README.md)
- [Ein Dokument bearbeiten](../03-editing/README.md)
