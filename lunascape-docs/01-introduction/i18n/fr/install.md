# Installer l'extension

L'extension VS Code « Lunascape Docs Pro » est distribuée sous la forme d'un fichier VSIX. Elle est gratuite ; « Pro » désigne l'édition qui confie le travail à une IA et se met à jour toute seule.

## Configuration requise

- VS Code 1.90 ou version ultérieure
- Les fonctions qui écrivent des fichiers — créer des documents, organiser l'INDEX, enregistrer les paramètres de vérification, traduire — ne fonctionnent que dans un espace de travail que vous avez marqué comme approuvé dans VS Code.

## Installer

1. Récupérez le fichier VSIX. Ce lien pointe toujours vers la version la plus récente.

   [Télécharger lunascape-docs-pro.vsix](https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix)

2. Ouvrez la vue Extensions (`⇧⌘X` / `Ctrl+Shift+X`).
3. Choisissez [Installer à partir de VSIX...] dans le menu `…` en haut à droite, puis indiquez le fichier que vous avez récupéré.

### En ligne de commande

Une seule ligne, si vous préférez ne pas quitter le terminal. Elle récupère et installe l'extension.

macOS / Linux :

```sh
curl -L -o /tmp/lunascape-docs-pro.vsix https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix && code --install-extension /tmp/lunascape-docs-pro.vsix
```

Windows (PowerShell) :

```powershell
curl.exe -L -o "$env:TEMP\lunascape-docs-pro.vsix" https://github.com/gu-corp/lunascape-user-guide/releases/latest/download/lunascape-docs-pro.vsix; code --install-extension "$env:TEMP\lunascape-docs-pro.vsix"
```

> **Remarque**
> Si `code` est introuvable, exécutez [Shell Command : installer la commande « code » dans le PATH] depuis la palette de commandes (`⇧⌘P` / `Ctrl+Shift+P`).

## Mettre à jour

Lorsqu'une version plus récente est publiée, l'extension la récupère et l'installe. VS Code vous propose de recharger la fenêtre, et c'est à ce moment que vous commencez à l'utiliser. Vos paramètres et vos documents restent tels quels.

La vérification a lieu une fois par jour. Pour vérifier immédiatement, exécutez [Lunascape Docs : Rechercher une version plus récente] depuis la palette de commandes (`⇧⌘P` / `Ctrl+Shift+P`).

Le paramètre `lunascapeDocEditor.update.check` modifie ce comportement.

| Paramètre | Comportement |
|---|---|
| Installer une version plus récente dès qu'elle est publiée | Par défaut |
| M'avertir et me laisser décider à chaque fois | Une notification s'affiche, et rien ne change tant que vous n'avez pas appuyé sur [Mettre à jour] |
| Ne jamais vérifier | Rien ne se passe |

### Quand la mise à jour échoue

Si le message « La mise à jour n'a pas pu être récupérée : No Servers » apparaît, c'est que la version installée est la 0.22.18 ou une version antérieure. Sa fonction de mise à jour échoue systématiquement à la dernière étape après la récupération : elle ne peut donc pas se mettre à jour elle-même. Réinstallez-la une seule fois à la main, selon la procédure ci-dessus ; ensuite, elle se met à jour toute seule.

## Vérifier la version

Ouvrez « Lunascape Docs Pro » dans la vue Extensions pour voir la version installée. Vous en aurez besoin pour signaler un problème.

## Voir aussi

- [Créer vos premiers documents](first-documents.md)
- [Signaler un problème](../07-troubleshooting/report.md)
