# Ein privates Repository lesen

Nach der Anmeldung bei GitHub können Sie die Dokumente privater Repositorys lesen – beschränkt auf jene, für die Sie Leseberechtigung haben. Lunascape Docs besitzt niemals eigene Konten oder Berechtigungen.

## Anmelden und öffnen

1. Öffnen Sie <https://docs.lunascape.org/>.
   Wenn Sie ein privates Dokument angeben oder noch nicht angemeldet sind, erscheint der Anmeldebildschirm.
2. Drücken Sie [Mit GitHub anmelden].
   Der Autorisierungsbildschirm von GitHub öffnet sich in einem Pop-up.
3. Drücken Sie nach der Anmeldung in der Symbolleiste [Dokumente öffnen] und wählen Sie unter [Aus lesbaren Repositorys wählen] das Repository aus, das Sie öffnen möchten.

> **Hinweis**
>
> - Der Name des angemeldeten Kontos wird in der Symbolleiste angezeigt. [Abmelden] und [Mit anderem Konto anmelden] sind ebenfalls von hier aus möglich.
> - In der Liste erscheinen die Repositorys der Konten (Organisationen oder Einzelpersonen), in denen die GitHub App „Lunascape Docs“ installiert ist, beschränkt auf jene, für die Sie Leseberechtigung haben.

## Einstellungen durch den Repository-Eigentümer

Wenn das gewünschte Repository nicht in der Liste erscheint, muss der Eigentümer des Repositorys oder ein Administrator der Organisation die GitHub App „Lunascape Docs“ installieren.

- Die angeforderten Berechtigungen sind Contents (Lesen und Schreiben) und Pull requests (Lesen und Schreiben). Das Lesen dient der Ansicht, das Schreiben der Veröffentlichungsanfrage (Pull Request) aus dem Web. Lunascape Docs speichert die Inhalte der Dokumente niemals.
- Die Installation erfolgt pro Konto (Organisation oder Einzelperson). Legen Sie fest, ob das Ziel „All repositories“ ist (womit auch künftig erstellte Repositorys automatisch eingeschlossen werden) oder nur ausgewählte Repositorys.

| Situation | Vorgehen |
|---|---|
| Neu in einer Organisation oder einem persönlichen Konto einführen | Über die [Installationsseite](https://github.com/apps/lunascape-docs/installations/new) durchführen |
| In einer Organisation mit bestehender Installation Repositorys hinzufügen | Unter Settings → GitHub Apps → Lunascape Docs → Configure → Repository access der Organisation einstellen |

Auch wenn die App für eine ganze Organisation installiert ist, kann jedes Mitglied nur die Repositorys lesen, für die es Leseberechtigung besitzt. Und Veröffentlichungsanfragen kann es nur für die Repositorys senden, für die es Schreibberechtigung besitzt.

> **Hinweis**
> - Bei einer Neuinstallation werden die angeforderten Berechtigungen auf dem Installationsbildschirm aufgelistet, und mit dem Drücken von „Install“ gelten sie als genehmigt. Weitere Schritte sind nicht nötig.
> - Eine Organisation, die die App schon vor der Erweiterung einer Berechtigung installiert hatte, erhält eine Bestätigungs-E-Mail an ihre Administratoren, und oben unter Settings → GitHub Apps → Lunascape Docs → Configure der Organisation erscheint eine Genehmigungsschaltfläche. Bis zur Genehmigung kann in dieser Organisation nur gelesen werden; beim Senden einer Veröffentlichungsanfrage erscheint „Die Erteilung einer Schreibberechtigung ist erforderlich“.
> - Mit welchen Berechtigungen die App derzeit eingebunden ist, sehen Sie auf demselben Configure-Bildschirm. Bei einem persönlichen Konto ist es Settings → Applications → Installed GitHub Apps.
> - Wenn ein Ziel-Repository versehentlich entfernt oder die App deinstalliert wurde, lässt sich der ursprüngliche Zustand wiederherstellen, indem Sie es über die [Installationsseite](https://github.com/apps/lunascape-docs/installations/new) erneut einrichten. Die Ablehnungsmeldung einer Veröffentlichungsanfrage enthält einen Link zum Bildschirm, auf dem sich dies beheben lässt.
> - Wenn ein Repository keine Veröffentlichungsanfragen annehmen soll, schreiben Sie `"publish": { "enabled": false }` in die `lunascape-docs.json`. Das Lesen bleibt weiterhin nutzbar.

## Verwandte Themen

- [Ein GitHub-Repository öffnen](open-repository.md)
- [Die Web-Version lässt sich nicht öffnen oder es ist keine Anmeldung möglich](../07-troubleshooting/web.md)
