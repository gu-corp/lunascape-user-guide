# Paramètres de VS Code

Recherchez « Lunascape Docs » dans les paramètres de VS Code (`⌘,` / `Ctrl+,`) pour modifier les éléments suivants. Ce sont tous des paramètres propres à l'utilisateur ; ils ne sont jamais enregistrés dans les documents du projet.

## Racine de documentation

| Paramètre | Valeurs | Par défaut | Rôle |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` choisit automatiquement la racine de documentation la plus proche du fichier Markdown ouvert et, si celui-ci n'appartient à aucune, ouvre temporairement son dossier parent. `fixed` ouvre toujours la racine indiquée dans `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Tableau de chaînes | `["docs"]` | Noms de dossiers reconnus automatiquement comme racines de documentation en mode `auto`. Un dossier contenant `lunascape-docs.json` est reconnu quel que soit son nom. Si le fichier `lunascape-docs.json` situé à la racine du dépôt contient `defaultFolder` ou `roots`, ces valeurs sont prioritaires |
| `lunascapeDocEditor.root` | Chemin | `docs` | Racine de documentation, relative à l'espace de travail, utilisée en mode `fixed` ou à l'ouverture par la commande |
| `lunascapeDocEditor.startPage` | Chemin | `README.md` | Page de départ, relative à la racine de documentation |
| `lunascapeDocEditor.title` | Chaîne | `Lunascape Docs` | Remplace le titre de l'onglet du document. Sans effet sur le nom affiché dans le sélecteur de racine de documentation |
| `lunascapeDocEditor.ignoredDirectories` | Tableau de chaînes | `["99-archive"]` | Noms de dossiers exclus de l'INDEX |

## Affichage

| Paramètre | Valeurs | Par défaut | Rôle |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` utilise un fond blanc, `auto` suit le thème de VS Code |
| `lunascapeDocEditor.locale` | Étiquette de langue | Aucune | Votre langue de document préférée, utilisée lorsqu'elle est disponible. Ne modifie pas la langue de référence du projet |
| `lunascapeDocEditor.documentMetadata.compact` | Booléen | `true` | Replie le tableau de gestion du document placé après le titre H1 en une ligne « Informations du document » |
| `lunascapeDocEditor.tree.showFileNames` | Booléen | `false` | Affiche les noms de fichiers dans l'INDEX à la place des titres de documents |
| `lunascapeDocEditor.tree.showDocumentIcons` | Booléen | `false` | Affiche les icônes de document dans l'INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Booléen | `false` | Affiche les icônes de dossier dans l'INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Booléen | `false` | Affiche dans l'INDEX le nombre d'éléments contenus directement dans chaque dossier |
| `lunascapeDocEditor.tree.showGuides` | Booléen | `true` | Affiche les lignes de guidage des niveaux dans l'INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | Interligne de l'INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Booléen | `true` | Ferme l'INDEX la première fois seulement, lorsqu'il n'y a qu'un seul document |

## Édition

| Paramètre | Valeurs | Par défaut | Rôle |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | Vue d'édition utilisée tant que vous n'en avez pas changé. La dernière vue utilisée est prioritaire |
| `lunascapeDocEditor.editor.showEditButton` | Booléen | `true` | Affiche [Modifier] en bas à droite du document |

## Figures

| Paramètre | Valeurs | Par défaut | Rôle |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | Moteur de rendu TikZ. `bundled` utilise le moteur approuvé fourni avec le produit (absent de la version distribuée actuelle), `workspace` utilise `node-tikzjax` 1.0.5 situé à la racine d'un espace de travail approuvé (développement et évaluation uniquement), `disabled` n'effectue aucun rendu |

## Paramètres déconseillés

| Paramètre | À utiliser à la place |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` dans `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` dans `lunascape-docs.json` |

Les paramètres personnels ne peuvent pas remplacer les langues du projet.

## Rubriques associées

- [Modifier les paramètres d'affichage](../02-reading/display-settings.md)
- [Configuration du projet](../04-document-tools/project-configuration.md)
