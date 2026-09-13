# Les documents ne s'affichent pas

## Le message « Aucun dossier Markdown ou docs à ouvrir » s'affiche

- L'espace de travail ne contient pas de dossier `docs`, ou celui-ci porte un autre nom.
  - Placez un fichier `lunascape-docs.json` dans ce dossier pour qu'il soit reconnu comme racine de documentation, quel que soit son nom.
  - Vous pouvez aussi ajouter le nom du dossier au paramètre `lunascapeDocEditor.rootDirectoryNames`.
- S'il n'existe encore aucun document, créez-en un avec « Lunascape Docs : créer une documentation à partir d'un modèle ».
- Vous pouvez également ouvrir un fichier Markdown dans l'éditeur, puis exécuter « Lunascape Docs : ouvrir dans la visionneuse de spécifications ».

## Un document n'apparaît pas dans l'INDEX

- Vérifiez que l'extension est `.md`, `.markdown` ou `.mdx`.
- Les dossiers suivants ne s'affichent pas : les dossiers commençant par `.`, `node_modules` et les dossiers indiqués dans `ignoredDirectories` (par défaut `99-archive`).
- Les versions traduites situées sous `i18n/` n'apparaissent pas séparément dans l'INDEX. Passez de l'une à l'autre depuis le menu des langues.
- Si un fichier que vous venez d'ajouter n'apparaît pas, appuyez sur [Recharger].
- Vous consultez peut-être une autre racine de documentation. Vérifiez le nom de la racine à l'extrémité gauche de la barre d'outils.

## Rien ne s'affiche lorsque j'appuie sur un dossier

Le fichier `README.md` de ce dossier est un « descripteur de configuration » : il ne contient que le front matter, sans corps de texte. Ouvrez le dossier dans l'INDEX et choisissez un document à l'intérieur.

## Ce n'est pas la racine de documentation attendue qui s'ouvre

- Lorsque le paramètre `lunascapeDocEditor.rootMode` vaut `fixed`, c'est toujours `lunascapeDocEditor.root` qui s'ouvre.
- Avec `auto`, la racine de documentation la plus proche du fichier Markdown ouvert est retenue. Vous pouvez en changer avec la liste déroulante à l'extrémité gauche de la barre d'outils.

## Le nom de la racine de documentation n'est pas celui attendu

Le nom est déterminé dans cet ordre : `title` dans `lunascape-docs.json` → `navigation.title` du `README.md` racine → son H1 → `index.md` → le nom du dossier. Pour le fixer, définissez `title`.

## L'INDEX a disparu

- Dans une racine de documentation ne comptant qu'un seul document, l'INDEX se ferme automatiquement la première fois. Vous pouvez le rouvrir avec l'icône d'affichage en colonnes de la barre d'outils, et désactiver ce comportement avec [Masquer s'il n'y a qu'un seul document] dans les [Paramètres d'affichage].
- Lorsque l'écran est étroit, ouvrez-le avec [Ouvrir l'INDEX] (les trois traits), à gauche de [Précédent].

## Un lien ne s'ouvre pas

- « Cible du lien introuvable » : le fichier cible n'existe pas. Vous pouvez vérifier les liens internes avec la [Vérification] des Outils de document.
- « Lien non sécurisé ou non pris en charge : ouverture annulée » : les liens pointant hors de la racine de documentation, ou utilisant un schéma autre que `https://` et `mailto:`, ne s'ouvrent pas.

## La langue affichée n'est pas celle attendue

- Dans le menu des langues, vérifiez la langue de la page affichée et sur quoi elle repose.
- La dernière langue d'affichage choisie est mémorisée. Sélectionnez de nouveau la langue par défaut dans le menu des langues.
- Si le paramètre personnel `lunascapeDocEditor.locale` est défini, la version traduite dans cette langue est prioritaire.

## Voir aussi

- [Changer de racine de documentation](../02-reading/roots.md)
- [Racines de documentation et conventions de fichiers](../04-document-tools/structure.md)
