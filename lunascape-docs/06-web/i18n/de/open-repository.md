# Ein GitHub-Repository öffnen

In der Web-Version können Sie ein GitHub-Repository direkt öffnen und lesen, ohne es zu klonen. Für öffentliche Repositorys ist keine Anmeldung nötig.

## Über die Oberfläche öffnen

1. Klicken Sie in der Symbolleiste auf [Dokumente öffnen] (das Ordnersymbol). Der Bildschirm „Dokumente öffnen“ wird angezeigt.
2. Wählen Sie in der linken Spalte aus, wo gesucht werden soll.

   | Ort | Angezeigte Einträge |
   |---|---|
   | Alle | Alle unten genannten Einträge. Zuletzt geöffnete Einträge stehen oben |
   | Zuletzt geöffnet | Bisher geöffnete Repositorys und Ordner |
   | Empfohlen | Von der Website vorgestellte Handbücher |
   | GitHub-Repositorys | Bei Anmeldung mit GitHub die Repositorys, die Sie lesen dürfen |
   | Dieser Computer | Ordner auf diesem Gerät |

3. Klicken Sie in der gewünschten Zeile auf [Öffnen]. Wenn Sie oben in [Nach Dokument- oder Repository-Namen filtern] etwas eingeben, werden die Zeilen eingegrenzt.

Ein Repository, das nicht in der Liste steht, geben Sie in der linken Spalte über [owner/repo eingeben und öffnen] an.

> **Tipp**
>
> - In der Liste erscheinen die GitHub-Repositorys, in denen die GitHub App „Lunascape Docs“ installiert ist und für die Sie eine Leseberechtigung haben. Fehlt ein Repository, bitten Sie den Eigentümer des Repositorys, die App hinzuzufügen.

## Den Ort eines Dokuments prüfen

Das kleine Symbol im linken Bereich der Symbolleiste (der Orts-Chip) zeigt, wo sich das Dokument befindet, das Sie gerade lesen.

| Symbol | Ort |
|---|---|
| GitHub-Logo | Wird von GitHub gelesen. Auf diesem Gerät ist nichts gespeichert |
| Ordner | Ein Ordner auf diesem Gerät |

Wenn Sie auf das Symbol klicken, werden der Ort, sein Status und die dort möglichen Aktionen angezeigt (etwa [Auf GitHub ansehen] und [Link kopieren]).

## Über eine URL öffnen

Die Adresse besteht aus dem Repository und der Position des Dokuments. Der Pfad ist die Position innerhalb des Repositorys und entspricht damit dem Aufbau der GitHub-URL.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Angabe | Schreibweise |
|---|---|
| Nur das Repository (Standard-Branch) | `/github/owner/repo` |
| Ein Dokument im Repository | `/github/owner/repo/docs/01-product/vision.md` |
| Branch oder Tag angeben | `?ref=v1.2.0` am Ende anhängen |

Wenn Sie die Seite wechseln, ändert sich auch die Adresse. Mit [Dieses Dokument teilen] in der Symbolleiste können Sie einen Link auf die gerade gelesene Seite weitergeben. Auch [Zurück] und [Vor] des Browsers funktionieren.

Die frühere Form mit `?source=` lässt sich weiterhin öffnen. Nach dem Öffnen wird die Adresse in die neue Form umgeschrieben.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Hinweis**
>
> - Ohne Anmeldung gilt das Nutzungslimit der GitHub-API (60 Anfragen pro Stunde). Bei Repositorys mit vielen Dokumenten oder bei wiederholtem Lesen melden Sie sich über [Mit GitHub anmelden] an.
> - Branchnamen mit `/` (etwa `feature/xxx`) lassen sich in der oben gezeigten Adressform mit `?ref=` angeben. In der Form mit `?source=` ist das nicht möglich.
> - Dokumente werden mit den GitHub-Berechtigungen der lesenden Person geladen. Wer keine Leseberechtigung hat, sieht sie nicht.

## Dokumente aus einem lokalen Ordner öffnen

Klicken Sie in der Symbolleiste auf [Dokumente öffnen], und wählen Sie in der linken Spalte über [Dokumente aus einem lokalen Ordner öffnen] einen Ordner auf Ihrem Gerät aus. Die Dateien werden im Browser verarbeitet und nicht nach außen gesendet. Diese Funktion steht in Browsern zur Verfügung, die die Ordnerauswahl unterstützen (z. B. Chrome, Edge).

## Verwandte Themen

- [Ein privates Repository lesen](private-repository.md)
- [Die Web-Version lässt sich nicht öffnen oder die Anmeldung schlägt fehl](../07-troubleshooting/web.md)
