# Ein GitHub-Repository öffnen

In der Web-Version und in Lunascape können Sie ein GitHub-Repository direkt öffnen und lesen, ohne es zu duplizieren. Für öffentliche Repositorys ist keine Anmeldung erforderlich.

## Über den Bildschirm öffnen

1. Klicken Sie in der Symbolleiste auf [Dokumente öffnen] (das Ordnersymbol). Der Bildschirm „Dokumente öffnen“ wird geöffnet.
2. Wählen Sie in der linken Spalte aus, wo geöffnet werden soll.

   | Ort | Angezeigte Einträge |
   |---|---|
   | Alle | Alle unten genannten Einträge. Zuletzt geöffnete Einträge stehen oben |
   | Zuletzt geöffnet | Bisher geöffnete Repositorys und Ordner |
   | Empfohlen | Von der Website vorgestellte Handbücher |
   | GitHub-Repositorys | Wenn Sie mit GitHub angemeldet sind: die Repositorys, die Sie lesen dürfen |
   | Dieser Computer | Ordner auf diesem Gerät. In Lunascape stehen hier auch duplizierte Repositorys |

3. Klicken Sie in der gewünschten Zeile auf [Öffnen]. Wenn Sie oben in [Nach Dokument- oder Repository-Namen filtern] etwas eingeben, werden die Zeilen eingegrenzt.

Ein Repository, das nicht in der Liste steht, geben Sie in der linken Spalte über [owner/repo eingeben und öffnen] an.

> **Tipp**
>
> - In der Liste erscheinen die GitHub-Repositorys, in denen die GitHub App „Lunascape Docs“ installiert ist und für die Sie Leserechte haben. Fehlt ein Repository, bitten Sie dessen Eigentümer, die App hinzuzufügen.

## Speicherort eines Dokuments prüfen

Das kleine Symbol links in der Symbolleiste (die Ortsanzeige) zeigt, wo sich das Dokument befindet, das Sie gerade lesen.

| Symbol | Ort |
|---|---|
| GitHub-Logo | Sie lesen das Dokument direkt von GitHub. Auf diesem Gerät ist nichts gespeichert |
| Computer | Ein Ordner auf diesem Gerät, den Lunascape verwaltet. Der Name des Git-Branchs und die Anzahl der geänderten Dateien werden ebenfalls angezeigt |
| Ordner | Ein Ordner auf diesem Gerät |

Wenn Sie auf das Symbol klicken, werden der Ort, sein Zustand und die von dort aus möglichen Aktionen angezeigt (etwa [Auf GitHub ansehen] und [Link kopieren]).

## Ein Repository in Lunascape duplizieren

In Lunascape können Sie ein GitHub-Repository auf dieses Gerät duplizieren und es dann mit Git bearbeiten und committen.

- Klicken Sie im Bildschirm „Dokumente öffnen“ in der Zeile des Repositorys auf [Duplizieren].
- Wenn Sie ein Repository lesen, das Sie von GitHub geöffnet haben, klicken Sie auf die Ortsanzeige und dann auf [Auf diesen Computer duplizieren]. Sobald das Duplizieren abgeschlossen ist, wird dasselbe Dokument in der Fassung auf diesem Gerät geöffnet.

Duplizierte Repositorys sind in der Liste mit „Auf diesem Computer vorhanden“ gekennzeichnet, und [Auf diesem Computer öffnen] steht an erster Stelle.

## Über eine URL öffnen

Die Adresse nennt das Repository und den Ort des Dokuments direkt hintereinander. Der Pfad gibt den Ort innerhalb des Repositorys an und folgt daher derselben Reihenfolge wie die GitHub-URL.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Angabe | Schreibweise |
|---|---|
| Nur das Repository (Standard-Branch) | `/github/owner/repo` |
| Ein Dokument im Repository | `/github/owner/repo/docs/01-product/vision.md` |
| Einen Branch oder Tag angeben | `?ref=v1.2.0` am Ende anhängen |

Wenn Sie die Seite wechseln, ändert sich auch die Adresse. Mit [Dieses Dokument teilen] in der Symbolleiste können Sie einen Link zu der Seite weitergeben, die Sie gerade lesen. Auch [Zurück] und [Vor] des Browsers funktionieren.

Die frühere Form mit `?source=` lässt sich weiterhin öffnen. Nach dem Öffnen wird sie in die neue Form umgeschrieben.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Hinweis**
>
> - Ohne Anmeldung gilt die Nutzungsbegrenzung der GitHub-API (60 Anfragen pro Stunde). Bei Repositorys mit vielen Dokumenten oder bei wiederholtem Lesen melden Sie sich mit [Mit GitHub anmelden] an.
> - Branch-Namen mit `/` (etwa `feature/xxx`) lassen sich in der obigen Adressform mit `?ref=` angeben. In der Form mit `?source=` ist das nicht möglich.
> - Dokumente werden mit den GitHub-Berechtigungen der lesenden Person geladen. Wer keine Leserechte hat, sieht sie nicht.

## Dokumente aus einem lokalen Ordner öffnen

Klicken Sie in der Symbolleiste auf [Dokumente öffnen] und dann in der linken Spalte auf [Dokumente aus einem lokalen Ordner öffnen]. Wählen Sie anschließend einen Ordner auf Ihrem Gerät aus. Die Dateien werden im Browser verarbeitet und nicht nach außen gesendet. Diese Funktion steht in Browsern zur Verfügung, die die Ordnerauswahl unterstützen (z. B. Chrome und Edge).

## Verwandte Themen

- [Ein privates Repository lesen](private-repository.md)
- [Web-Version: Öffnen oder Anmelden nicht möglich](../07-troubleshooting/web.md)
