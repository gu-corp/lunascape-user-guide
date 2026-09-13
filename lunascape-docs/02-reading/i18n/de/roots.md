# Dokumentwurzel wechseln

Eine Dokumentwurzel ist der oberste Ordner eines Satzes von Dokumenten. INDEX, Filterung, Prüfung und Übersetzung arbeiten alle je Dokumentwurzel.

## So wird eine Dokumentwurzel gefunden

Lunascape Docs geht von der geöffneten Markdown-Datei aus die übergeordneten Ordner durch und verwendet den nächstgelegenen Ordner, auf den eine der folgenden Bedingungen zutrifft, als Dokumentwurzel.

- Ein Ordner, der `lunascape-docs.json` enthält (der Ordnername spielt keine Rolle)
- Ein Ordner mit dem Namen `docs` (weitere Namen fügen Sie mit der Einstellung `lunascapeDocEditor.rootDirectoryNames` hinzu)

Wenn Sie „Lunascape Docs: Spezifikationsviewer öffnen“ ausführen, wird die Dokumentwurzel aus der Einstellung `lunascapeDocEditor.root` (Standard `docs`) geöffnet.

## Zu einer anderen Dokumentwurzel wechseln

Wenn der Arbeitsbereich mehrere Dokumentwurzeln enthält, wird der Name der Dokumentwurzel ganz links in der Symbolleiste zu einem Aufklappmenü.

1. Drücken Sie ganz links in der Symbolleiste auf den Namen der Dokumentwurzel.
2. Wählen Sie in der Liste eine Dokumentwurzel aus.
   Die Startseite der gewählten Dokumentwurzel wird angezeigt, und INDEX wechselt.

> **Hinweis**
>
> Die Namen in der Liste werden in dieser Reihenfolge bestimmt. Sie ändern sich nicht, wenn Sie die Anzeigesprache wechseln.
>
> 1. `title` in `lunascape-docs.json`
> 2. `navigation.title` der `README.md` der Wurzel, sonst deren H1
> 3. `navigation.title` der `index.md` der Wurzel, sonst deren H1
> 4. Der Ordnername (bei einem standardmäßigen `docs`-Ordner der Name des übergeordneten Ordners)

## Markdown-Dateien außerhalb einer Dokumentwurzel öffnen

Wenn Sie eine Markdown-Datei öffnen, die in keiner Dokumentwurzel liegt, wird deren Ordner als vorübergehende Dokumentwurzel angezeigt. In INDEX stehen die Markdown-Dateien dieses Ordners und der darunterliegenden Ordner.

- Drücken Sie in der Symbolleiste auf [Übergeordneter Ordner], um den Anzeigebereich auf den übergeordneten Ordner innerhalb des Arbeitsbereichs zu erweitern.
- In dieser Ansicht stehen die Spracheinstellungen des Projekts und die Sammelübersetzung nicht zur Verfügung. Legen Sie `lunascape-docs.json` in den Ordner, um ihn zu einer Dokumentwurzel zu machen; dann sind sie verfügbar.

## Immer eine feste Dokumentwurzel öffnen

Setzen Sie die Einstellung `lunascapeDocEditor.rootMode` auf `fixed`, damit immer die Dokumentwurzel aus `lunascapeDocEditor.root` geöffnet wird, gleich welche Markdown-Datei Sie öffnen.

## Verwandte Themen

- [Dokumentwurzeln und Dateikonventionen](../04-document-tools/structure.md)
- [Projektkonfiguration](../04-document-tools/project-configuration.md)
- [VS Code-Einstellungen](../08-reference/settings.md)
