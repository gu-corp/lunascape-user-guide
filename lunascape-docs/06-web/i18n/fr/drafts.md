# Enregistrer un brouillon

Lorsque vous modifiez un document dans la visionneuse Web, les modifications ne sont pas écrites dans le dépôt : elles sont enregistrées dans le navigateur sous forme de « brouillon ».

## Créer un brouillon

1. Ouvrez un document, puis appuyez sur [Modifier] en bas à droite.
2. Modifiez le texte, puis appuyez sur [Enregistrer].
   Le message « Enregistré comme brouillon » s'affiche et la modification est conservée dans le navigateur.

- Les documents comportant un brouillon sont signalés par un badge dans l'INDEX. Au-dessus du texte s'affiche « Ce document est un brouillon local (non publié) ».
- Le bouton [Brouillons] de la barre d'outils indique le nombre de brouillons ; appuyez dessus pour ouvrir la liste.

## Supprimer un brouillon

- Pour supprimer le brouillon d'un document, appuyez sur [Supprimer le brouillon] au-dessus du texte.
- Pour tout supprimer, utilisez la liste des brouillons.

## Reporter les modifications dans le dépôt

La « demande de publication », qui envoie les brouillons sous forme de Pull Request, est implémentée mais n'est pas activée dans la visionneuse publique. Pour modifier le dépôt, utilisez l'extension VS Code ou un clone local.

> **Remarque**
>
> - Les brouillons sont enregistrés dans le navigateur (IndexedDB). Ils ne sont pas transférés vers un autre navigateur ni vers un autre appareil. Si vous effacez les données de site du navigateur, les brouillons sont également supprimés.
> - Si le document est mis à jour dans le dépôt après la création de votre brouillon, le message « La source a été mise à jour » s'affiche. Vérifiez le contenu, puis décidez de supprimer le brouillon ou de le conserver tel quel.
> - Si vous ouvrez un dossier local avec [Ouvrir des documents] pour le modifier, les modifications sont écrites directement dans le fichier lorsque le navigateur le prend en charge. Dans le cas contraire, elles ne sont conservées que pendant la session.

## Rubriques associées

- [Ce que permet la visionneuse Web](README.md)
- [Modifier un document](../03-editing/README.md)
