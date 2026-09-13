# Navigationsinformationen festlegen

Der im INDEX angezeigte Name und die Reihenfolge werden im YAML front matter jedes Dokuments festgelegt. Dokumente werden auch ohne diese Angaben angezeigt; dann werden die Überschrift (H1) und die Reihenfolge nach Dateiname verwendet.

## Name und Reihenfolge eines Dokuments

Schreiben Sie am Anfang des Dokuments Folgendes.

```yaml
---
navigation:
  title: Erste Schritte
  order: 200
---
```

| Feld | Bedeutung |
|---|---|
| `navigation.title` | Der im INDEX angezeigte Name. Wird er weggelassen, wird die H1 verwendet, andernfalls der Dateiname |
| `navigation.order` | Eine ganze Zahl, die die Reihenfolge bestimmt; aufsteigend sortiert. Wird sie weggelassen, gilt eine stabile Standardreihenfolge (nach Dateiname) |

> **Tipp**
>
> - Vergeben Sie `order`-Werte in Hunderterschritten, etwa 100, 200, 300, damit Sie später einen Wert wie 150 dazwischen einfügen können.
> - Fehlende, ungültige oder doppelte `order`-Werte blenden ein Dokument nie aus.
> - Wenn Sie die Reihenfolge im INDEX ändern, wird `navigation.order` automatisch geschrieben. Sie müssen es nicht von Hand eintragen.

## Name und Reihenfolge eines Ordners

Der Name und die Reihenfolge eines Ordners stehen im front matter seiner `README.md` (oder `index.md`, wenn keine README vorhanden ist). Die Titelseite braucht keinen eigenen Textinhalt.

```yaml
---
navigation:
  title: Produktplanung
  order: 100
---
```

Ein Ordner ohne Titelseite wird mit seinem Ordnernamen und der Standardreihenfolge angezeigt. Wenn eine Titeländerung oder eine Umsortierung im INDEX es erfordert, wird eine `README.md` erstellt, die nur aus front matter besteht. Durch bloßes Lesen wird nie eine Datei angelegt.

## Umgang bei Übersetzungen

- Die Reihenfolge und die Rolle eines Ordners (Titelseite oder nur zur Konfiguration) werden allein vom Dokument in der Standardsprache bestimmt.
- Eine Übersetzung darf nur `navigation.title` überschreiben. Wenn das Originaldokument Textinhalt hat, wird auch die H1 der Übersetzung als Name verwendet.
- Eine Übersetzung allein fügt keine Seite hinzu.

## Reihenfolge und Einklappen von Unterelementen

Für die Titelseite eines Ordners sind `navigation.children.sort` und `navigation.children.defaultCollapsed` definiert, mit denen sich festlegen lässt, wie die direkt untergeordneten Elemente sortiert werden und ob sie zunächst eingeklappt sind. Das Lesen und Bearbeiten in VS Code ist geplant.

## Verwandte Themen

- [Die Reihenfolge von Dokumenten ändern](../03-editing/reorder.md)
- [Dokumentwurzeln und Dateikonventionen](structure.md)
