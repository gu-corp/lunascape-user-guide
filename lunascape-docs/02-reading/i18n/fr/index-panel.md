# Utiliser l'INDEX

L'INDEX, à gauche de l'écran, est l'arborescence des dossiers et des documents de la racine de documentation.

## Filtrer

1. Saisissez un mot dans [Filtrer les documents], au-dessus de l'INDEX.
2. Seuls les éléments dont le nom correspond s'affichent. Effacez la saisie pour tout réafficher.

> **Remarque**
>
> Pendant le filtrage, le réordonnancement par glisser-déposer est impossible.

## Ouvrir et fermer les dossiers

- Appuyez sur la flèche à gauche du nom d'un dossier, ou sur le nom d'un dossier sans page de couverture, pour l'ouvrir ou le fermer.
- Un dossier qui possède une page de couverture (un `README.md` ou un `index.md` avec du contenu) ouvre cette page quand vous appuyez sur son nom. Pour seulement l'ouvrir ou le fermer, utilisez [Ouvrir le dossier] / [Fermer le dossier] dans le menu de l'élément.
- L'état d'ouverture des dossiers est mémorisé pour chaque utilisateur et n'est jamais écrit dans les fichiers suivis par Git.

## Le README et la page de couverture du dossier

`README.md` est le fichier qui décrit le contenu du dossier.

- Pour un dossier qui possède un README, appuyer sur le nom du dossier affiche ce README.
- Pour un dossier sans README, c'est le premier document qu'il contient qui s'affiche.
- Le titre (H1) du README devient le nom du dossier dans l'INDEX.

Le README n'est pas obligatoire. Pour en ajouter un plus tard, choisissez [Créer un README] dans le menu de l'élément du dossier (cette entrée n'apparaît que pour les dossiers qui n'en ont pas).

## Afficher ou masquer l'INDEX

- Dans les commandes de colonnes de la barre d'outils, l'icône de gauche affiche ou masque l'INDEX. L'icône de droite affiche ou masque « Sur cette page ».
- Sur un écran étroit, l'INDEX est fermé au départ. Appuyez sur [Ouvrir l'INDEX] (les trois traits), à gauche de [Précédent] : l'INDEX s'ouvre par-dessus le document. Fermez-le avec le [×] de l'INDEX, un clic sur l'arrière-plan, `Esc`, ou en passant à un autre document. Cette ouverture temporaire ne modifie pas le réglage des écrans larges.
- Dans une racine de documentation qui n'affiche qu'un seul document, l'INDEX se ferme automatiquement la première fois. Vous pouvez le rouvrir avec l'icône de colonne. Vous pouvez désactiver ce comportement avec [Masquer s'il n'y a qu'un seul document], dans [Paramètres d'affichage].

## Utiliser le menu de l'élément

Pour ouvrir le menu d'un élément de l'INDEX, appuyez sur le [⋯] qui apparaît au survol, ou faites un clic droit sur l'élément. Les entrées se présentent dans cet ordre.

| Groupe | Entrées |
|---|---|
| Actions courantes | [Ouvrir le dossier] / [Fermer le dossier], [Ouvrir l'INDEX] (ouvre la page de couverture du dossier), [Modifier], [Modifier le titre], [Ouvrir dans VS Code], [Copier le chemin] |
| Créer et organiser | [Créer un README] (dossiers sans README uniquement), [Nouveau document], [Nouveau dossier], [Dupliquer], [Renommer le fichier] / [Renommer le dossier], [Déplacer vers le haut], [Déplacer vers le bas] |
| Supprimer | [Déplacer vers la corbeille] |

- Pour créer un élément directement sous la racine de documentation, appuyez sur le [⋯] à l'extrémité droite du titre de l'INDEX, ou faites un clic droit sur une zone vide de l'INDEX, puis choisissez [Nouveau document] ou [Nouveau dossier]. Le même menu comporte [Renommer le document] et, si la racine de documentation n'a pas de README, [Créer un README]. Un clic droit sur le nom du document affiché dans la barre d'outils ouvre le même menu.
- Dans un menu, `↑` `↓` déplacent la sélection et `Home` `End` vont à la première et à la dernière entrée. `Esc` ferme le menu et rend le focus à l'endroit d'où il a été ouvert.

> **Remarque**
>
> Les entrées de création, d'organisation et de suppression n'apparaissent que si l'espace de travail est approuvé dans VS Code. Elles sont également indisponibles pendant la modification d'un document ou le traitement d'une autre opération de l'INDEX.

## Modifier la présentation

Depuis [Paramètres d'affichage], vous pouvez modifier l'affichage des noms de fichiers, les icônes des documents et des dossiers, le nombre d'éléments par dossier, les lignes de guidage des niveaux et la densité d'affichage. Pour en savoir plus, voir [Modifier les paramètres d'affichage](display-settings.md).

## Voir aussi

- [Créer et organiser des documents et des dossiers](../03-editing/organize.md)
- [Modifier l'ordre des documents](../03-editing/reorder.md)
