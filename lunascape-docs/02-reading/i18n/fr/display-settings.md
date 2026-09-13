# Modifier les paramètres d'affichage

Le bouton [Paramètres d'affichage] (roue dentée) de la barre d'outils permet à chaque utilisateur de modifier l'apparence de l'INDEX et l'affichage du bouton de modification.

1. Appuyez sur [Paramètres d'affichage] dans la barre d'outils.
2. Activez ou désactivez les éléments à modifier. Les changements sont appliqués immédiatement.
3. Appuyez de nouveau sur [Paramètres d'affichage], ou cliquez en dehors du panneau, pour le fermer.

## Éléments configurables

| Catégorie | Élément | Rôle |
|---|---|---|
| Langue du document | (état actuel) | Affiche la langue par défaut du projet et la langue actuellement affichée. [Définir les langues du projet…] ouvre les paramètres de langue du projet |
| Contenu | [Noms de fichiers] | Affiche le nom de fichier à la place du titre du document |
| | [Icônes de document] | Affiche une icône sur les éléments de type document |
| | [Icônes de dossier] | Affiche une icône sur les éléments de type dossier |
| | [Nombre d'éléments] | Affiche le nombre de documents contenus dans chaque dossier |
| | [Repères de hiérarchie] | Affiche les lignes indiquant les niveaux de hiérarchie |
| | [Masquer s'il n'y a qu'un seul document] | Ferme automatiquement l'INDEX, à la première ouverture seulement, dans une racine de documentation ne contenant qu'un seul document |
| | [Replier les informations du document] | Replie le tableau de gestion situé en tête du document dans une ligne « Informations du document ». Si l'option est désactivée, le tableau est affiché tel quel |
| | [Densité d'affichage] | Choisit l'interligne de l'INDEX entre [Normale] et [Compacte] |
| | [Bouton de modification] | Affiche le bouton [Modifier] en bas à droite du document |
| Actions | [Rétablir les valeurs par défaut du projet] | Supprime toutes vos modifications et rétablit les paramètres du projet |
| | [Ouvrir les paramètres de l'extension] | Ouvre les paramètres de Lunascape Docs dans l'écran de configuration de VS Code |

> **Conseil**
>
> - Les paramètres d'affichage sont enregistrés par utilisateur et par racine de documentation ; ils ne sont jamais écrits dans les fichiers gérés par Git.
> - Les paramètres s'appliquent dans l'ordre suivant : « paramètres d'affichage de l'utilisateur → paramètres de VS Code → `lunascape-docs.json` → valeurs par défaut du produit ». Les valeurs par défaut communes à l'équipe se définissent dans `tree` et `editor` de `lunascape-docs.json`.

## Changer les couleurs

Appuyez sur le sélecteur de thème (soleil/lune) de la barre d'outils pour basculer entre un fond blanc et les couleurs de VS Code. Les couleurs appliquées à l'ouverture sont déterminées par le paramètre `lunascapeDocEditor.appearance` (`light` ou `auto`).

## Voir aussi

- [Utiliser l'INDEX](index-panel.md)
- [Paramètres du projet](../04-document-tools/project-configuration.md)
- [Liste des paramètres VS Code](../08-reference/settings.md)
