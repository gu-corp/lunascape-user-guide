# Modifier l'ordre des documents

L'ordre affiché dans l'INDEX peut être modifié par glisser-déposer ou au clavier. Le nouvel ordre est enregistré dans le front matter du document, sous la forme `navigation.order`.

## Réorganiser par glisser-déposer

1. Faites glisser un document ou un dossier dans l'INDEX.
2. Déposez-le avant ou après un élément du même niveau, ou sur un dossier.
   Au sein d'un même niveau, l'ordre change. Si vous le déposez sur un autre dossier, l'élément est déplacé dans ce dossier.

## Réorganiser au clavier ou par le menu

- Placez le focus sur un élément de l'INDEX, puis appuyez sur `Alt`+`Shift`+`↑` / `Alt`+`Shift`+`↓`.
- Choisissez [Déplacer vers le haut] / [Déplacer vers le bas] dans le menu de l'élément.

## Ce qui est enregistré

- Lors d'une réorganisation au sein d'un même niveau, la valeur `navigation.order` du front matter du document de référence est mise à jour. Pour un dossier, elle est écrite dans le `README.md` de ce dossier. Si le dossier n'en possède pas, un `README.md` contenant uniquement le front matter est créé.
- Lors d'un déplacement vers un autre dossier, le document de référence et ses traductions correspondantes sont déplacés ensemble. Avant le déplacement, une confirmation s'affiche au sujet des conséquences sur les liens relatifs.
- Aucune opération Git d'indexation ni de validation n'est effectuée.

> **Remarque**
>
> - La réorganisation n'est pas possible pendant un filtrage, pendant l'édition d'un document, ni dans un espace de travail non approuvé.
> - Le message « L'INDEX a été mis à jour » signifie qu'une autre modification vient d'être appliquée. Recommencez l'opération.
> - La page de démarrage ne peut pas être déplacée vers un autre dossier.

> **Conseil**
>
> Attribuer à `navigation.order` des valeurs par pas de 100, par exemple 100, 200, 300, facilite l'insertion de documents intermédiaires par la suite. Pour en savoir plus, reportez-vous à [Définir les informations de navigation](../04-document-tools/navigation-metadata.md).

## Voir aussi

- [Créer et organiser des documents et des dossiers](organize.md)
- [Définir les informations de navigation](../04-document-tools/navigation-metadata.md)
