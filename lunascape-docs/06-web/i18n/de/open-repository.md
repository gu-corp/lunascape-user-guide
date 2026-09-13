# Ein GitHub-Repository öffnen

In der Web-Version öffnen Sie Dokumente, indem Sie ein GitHub-Repository angeben. Für öffentliche Repositorys ist keine Anmeldung nötig.

## Über den Bildschirm öffnen

1. Öffnen Sie <https://docs.lunascape.org/>.
2. Drücken Sie in der Symbolleiste auf [Dokumente öffnen] (das Ordnersymbol).
3. Geben Sie das Repository unter [Repository direkt angeben] ein und drücken Sie auf [Öffnen].
   Wenn Sie bei GitHub angemeldet sind, können Sie unter [Aus lesbaren Repositorys wählen] auch aus einer Liste auswählen.

> **Hinweis**
>
> - Das GitHub-Symbol daneben öffnet das Dokument, das Sie gerade lesen, auf github.com. Es dient nicht dazu, Dokumente zu öffnen.

## Über eine URL öffnen

Die Adresse reiht Repository und Position des Dokuments einfach aneinander. Der Pfad ist die Position innerhalb des Repositorys, also dieselbe Reihenfolge wie in der GitHub-URL.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Angabe | Schreibweise |
|---|---|
| Nur Repository (Standardbranch) | `/github/owner/repo` |
| Ein Dokument im Repository | `/github/owner/repo/docs/01-product/vision.md` |
| Branch oder Tag angeben | am Ende `?ref=v1.2.0` anhängen |

Beim Wechsel der Seite ändert sich auch die Adresse. Wenn Sie in der Symbolleiste auf [Dieses Dokument teilen] drücken, können Sie einen Link auf die gerade gelesene Seite weitergeben. Auch [Zurück] und [Vor] des Browsers funktionieren.

Die frühere Form mit `?source=` lässt sich weiterhin öffnen. Nach dem Öffnen wird sie in die neue Form umgeschrieben.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Achtung**
>
> - Ohne Anmeldung gilt das Nutzungslimit der GitHub-API (60 Anfragen pro Stunde). Melden Sie sich bei Repositorys mit vielen Dokumenten oder bei wiederholtem Lesen über [Mit GitHub anmelden] an.
> - Branchnamen mit `/` (etwa `feature/xxx`) können Sie im oben gezeigten Adressformat mit `?ref=` angeben. In der Form mit `?source=` lassen sie sich nicht schreiben.
> - Dokumente werden mit den GitHub-Rechten der lesenden Person geladen. Wer keine Leseberechtigung hat, sieht sie nicht.

## Dokumente aus einem lokalen Ordner öffnen

Drücken Sie in der Symbolleiste auf [Dokumente öffnen] und wählen Sie unterhalb der Liste über [Dokumente aus einem lokalen Ordner öffnen] einen Ordner auf Ihrem Gerät aus. Die Dateien werden im Browser verarbeitet und nicht nach außen übertragen. Das funktioniert in Browsern, die die Ordnerauswahl unterstützen (Chrome, Edge und andere).

## Verwandte Themen

- [Ein nicht öffentliches Repository lesen](private-repository.md)
- [Die Web-Version lässt sich nicht öffnen oder die Anmeldung schlägt fehl](../07-troubleshooting/web.md)
