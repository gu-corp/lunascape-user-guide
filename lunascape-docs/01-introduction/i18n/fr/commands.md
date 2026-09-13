# Liste des commandes

Dans la palette de commandes (`⇧⌘P` / `Ctrl+Shift+P`), saisissez « Lunascape Docs » pour exécuter les commandes suivantes.

| Commande | Rôle |
|---|---|
| Lunascape Docs : Ouvrir la visionneuse de spécifications | Ouvre la racine de documentation la plus proche dans la visionneuse. La lecture, la modification, la vérification et la traduction se font dans cet écran |
| Lunascape Docs : Ouvrir dans la visionneuse de spécifications | Affiche dans la visionneuse le fichier Markdown ouvert dans l'éditeur |
| Lunascape Docs : Créer un document à partir d'un modèle | Crée un premier ensemble de documents dans un projet dépourvu de dossier de documentation |
| Lunascape Docs : Vérifier la racine de documentation | Vérifie l'ensemble de la racine de documentation avec docs-lint et affiche les résultats dans les Outils de document et dans le panneau « Problèmes » |
| Lunascape Docs : Ouvrir l'aide | Ouvre ce guide d'aide |

## Opérations depuis l'explorateur

Dans l'explorateur, faites un clic droit sur un fichier `.md`, `.markdown` ou `.mdx` : vous pouvez alors choisir [Lunascape Docs : Ouvrir dans la visionneuse de spécifications].

> **Conseil**
>
> Pour afficher également les fichiers Markdown dans Lunascape Docs lorsque vous les ouvrez normalement, ajoutez une association d'éditeur aux paramètres de l'espace de travail.
>
> ```json
> {
>   "workbench.editorAssociations": {
>     "*.md": "lunascapeDocEditor.markdownPortal"
>   }
> }
> ```

## Visite guidée

La visite guidée « Démarrer avec Lunascape Docs », accessible depuis le menu [Aide] → « Bienvenue » de VS Code, vous permet d'essayer les premières opérations dans l'ordre.

## Voir aussi

- [Opérations de base](../02-reading/README.md)
- [Liste des raccourcis clavier](../08-reference/keyboard.md)
