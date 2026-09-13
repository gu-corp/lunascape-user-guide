# Changer de racine de documentation

Une racine de documentation est le dossier le plus haut d'un ensemble de documents. L'INDEX, le filtrage, les vérifications et la traduction fonctionnent tous par racine de documentation.

## Comment une racine de documentation est trouvée

Lunascape Docs remonte les dossiers parents à partir du fichier Markdown ouvert et retient comme racine de documentation le dossier le plus proche qui correspond à l'un des cas suivants.

- Un dossier contenant `lunascape-docs.json` (quel que soit son nom)
- Un dossier nommé `docs` (le paramètre `lunascapeDocEditor.rootDirectoryNames` permet d'ajouter d'autres noms)

Lorsque vous exécutez « Lunascape Docs : Ouvrir la visionneuse de spécification », c'est la racine de documentation du paramètre `lunascapeDocEditor.root` (par défaut `docs`) qui s'ouvre.

## Passer à une autre racine de documentation

Lorsque l'espace de travail comporte plusieurs racines de documentation, le nom de la racine, à l'extrême gauche de la barre d'outils, devient une liste déroulante.

1. Appuyez sur le nom de la racine de documentation, à l'extrême gauche de la barre d'outils.
2. Choisissez une racine de documentation dans la liste.
   Sa page de départ s'affiche et l'INDEX change.

> **Conseil**
>
> Les noms affichés dans la liste sont déterminés dans cet ordre. Ils ne changent pas lorsque vous changez de langue d'affichage.
>
> 1. `title` dans `lunascape-docs.json`
> 2. `navigation.title` du `README.md` de la racine, sinon son H1
> 3. `navigation.title` de l'`index.md` de la racine, sinon son H1
> 4. Le nom du dossier (pour un dossier `docs` standard, le nom de son dossier parent)

## Ouvrir un fichier Markdown hors de toute racine de documentation

Lorsque vous ouvrez un fichier Markdown qui ne se trouve pas dans une racine de documentation, son dossier s'affiche comme racine de documentation temporaire. L'INDEX présente les fichiers Markdown de ce dossier et des dossiers situés en dessous.

- Appuyez sur [Dossier parent] dans la barre d'outils pour étendre l'affichage au dossier parent, à l'intérieur de l'espace de travail.
- Dans cet affichage, les paramètres de langue du projet et la traduction par lot ne sont pas disponibles. Placez un `lunascape-docs.json` dans le dossier pour en faire une racine de documentation et les rendre disponibles.

## Toujours ouvrir la même racine de documentation

Réglez le paramètre `lunascapeDocEditor.rootMode` sur `fixed` pour toujours ouvrir la racine de documentation indiquée dans `lunascapeDocEditor.root`, quel que soit le fichier Markdown que vous ouvrez.

## Rubriques associées

- [Racines de documentation et conventions de fichiers](../04-document-tools/structure.md)
- [Configuration du projet](../04-document-tools/project-configuration.md)
- [Liste des paramètres VS Code](../08-reference/settings.md)
