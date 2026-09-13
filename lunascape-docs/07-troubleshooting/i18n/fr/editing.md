# Impossible de modifier, d'enregistrer ou de réordonner

## Le bouton [Modifier] est absent

- L'option [Bouton de modification] des [Paramètres d'affichage] est désactivée. Activez-la, ou utilisez [⋯] → [Modifier] en haut à droite du document, ou encore le menu de l'élément dans l'INDEX → [Modifier].
- Il en va de même lorsque `editor.showEditButton` dans `lunascape-docs.json` vaut `false`.
- La modification est impossible pendant l'affichage de l'aide. Fermez l'aide.

## Impossible de passer à l'affichage visuel

« Ce document contient une syntaxe MDX ; le passage à l'écran de modification habituel est impossible » : les documents comportant une syntaxe propre à MDX (composants, `import`, etc.) se modifient uniquement dans l'affichage Markdown, afin de préserver cette syntaxe.

## Impossible de modifier directement les formules ou les figures

L'affichage visuel montre le résultat du rendu. Dans l'écran de modification, appuyez sur [Markdown] et modifiez la source.

## Impossible de réordonner ou de faire glisser

- Le changement d'ordre est impossible pendant un filtrage, pendant la modification d'un document et pendant le traitement d'une autre opération de l'INDEX.
- Lorsque l'espace de travail n'est pas approuvé, les opérations de création, d'organisation et de suppression sont indisponibles. Approuvez l'espace de travail dans VS Code.
- « L'INDEX a été mis à jour. Faites glisser à nouveau. » : une autre modification vient d'être appliquée. Recommencez l'opération.
- La page de démarrage (le `README.md` de la racine) ne peut pas être déplacée.

## Le message « Des modifications non enregistrées sont présentes » s'affiche

Le fichier concerné est en cours de modification dans l'éditeur de VS Code. Enregistrez-le ou abandonnez les modifications, puis réessayez.

## Impossible de renommer

Les noms suivants ne sont pas utilisables.

- Les noms commençant par `.`, `i18n`, les noms réservés de Windows (`CON`, etc.)
- Les noms se terminant par un point ou une espace, et les noms contenant des caractères de contrôle ou des caractères interdits dans les noms de fichiers
- Les noms déjà présents dans le même dossier (y compris ceux qui ne diffèrent que par la casse)
- Les noms de document sans extension Markdown

## L'enregistrement n'apparaît pas dans Git ou n'est pas validé

Lunascape Docs se contente d'écrire dans le fichier ; il n'effectue ni indexation ni commit dans Git. Vérifiez dans la vue Gestion de code source de VS Code et validez si nécessaire.

## Voir aussi

- [Modifier un document](../03-editing/README.md)
- [Créer et organiser des documents et des dossiers](../03-editing/organize.md)
- [Modifier l'ordre des documents](../03-editing/reorder.md)
