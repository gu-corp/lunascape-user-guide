# Verfügbare Aufgaben

Wählen Sie im Tab [AI] unter [Aufgabe]. Je nach Aufgabe ändern sich die übergebene Anweisung und die anschließende Prüfung.

| Aufgabe | Inhalt | Voraussetzung | API-Typ |
|---|---|---|---|
| Diese Seite übersetzen | Übersetzt das angezeigte Dokument in die gewählte Sprache | Das Dokument ist geöffnet, eine Zielsprache | Ja |
| Fehlende Übersetzungen sammeln | Übersetzt der Reihe nach die nicht übersetzten und veralteten Dokumente der gewählten Sprache | Eine Zielsprache | Nur Sitzungstyp |
| Diese Seite korrigieren | Prüft und korrigiert Terminologie, Stil und die vom Dokumentstandard geforderte Gliederung | Das Dokument ist geöffnet | Ja |
| Neues Dokument erstellen | Erstellt ein neues Dokument gemäß Dokumentstandard und Vorlage | Ein Thema (optional) | Nur Sitzungstyp |

## Was die Anweisung enthält

| Nr. | Inhalt |
|---|---|
| 1 | Den Ort der Dokumentwurzel, mit der Anweisung, außerhalb davon nichts zu ändern |
| 2 | Die Standardsprache (Originaldokument) und den Ablageort der Übersetzungen (`i18n/<Sprache>/` im selben Ordner wie das Dokument) |
| 3 | Dass `navigation.order` allein zum Originaldokument gehört und eine Übersetzung nur `navigation.title` überschreiben darf |
| 4 | Dass Anforderungs-IDs, Links, Code, Mermaid, TeX und die Struktur des Front Matter unverändert bleiben |
| 5 | Den Dokumentstandard und das Glossar (`terminology` in `docs-lint.config.json`) |
| 6 | Zum Schluss die Dokumentprüfung auszuführen, die geänderten Dateien zu melden und keine Git-Operationen durchzuführen |

> **Hinweis**
>
> Die Ziele von „Fehlende Übersetzungen sammeln“ stammen aus dem Verzeichnis, höchstens 200 Dokumente pro Durchlauf. Führen Sie die Aufgabe bei Bedarf mehrmals aus.

## Verwandte Themen

- [Arbeit an eine KI übergeben](README.md)
- [Verzeichnis und Aufzeichnungen](ledger.md)
