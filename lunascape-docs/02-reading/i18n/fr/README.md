# Opérations de base

Les opérations de base, depuis l'ouverture des documents jusqu'à la page que vous souhaitez lire.

## Ouvrir les documents

1. Ouvrez le dépôt dans VS Code.
2. Dans la palette de commandes (`⇧⌘P` / `Ctrl+Shift+P`), exécutez « Lunascape Docs : Ouvrir la visionneuse de spécifications ».
   La racine de documentation la plus proche (le dossier `docs` par défaut) est trouvée et sa page de démarrage s'affiche.

> **Conseil**
>
> - Cliquez avec le bouton droit sur un fichier Markdown dans l'explorateur, puis choisissez [Lunascape Docs : Ouvrir dans la visionneuse de spécifications] pour démarrer à partir de ce fichier.
> - Si vous ouvrez un fichier Markdown qui n'appartient à aucune racine de documentation, son dossier s'affiche comme racine de documentation temporaire.

## Se déplacer entre les pages

| Opération | Méthode |
|---|---|
| Ouvrir depuis la table des matières | Appuyez sur un nom de document dans l'INDEX à gauche |
| Suivre un lien | Appuyez sur un lien dans le texte. Il s'ouvre dans la même vue |
| Parcourir l'historique | [Précédent] et [Suivant] dans la barre d'outils, ou `Alt`+`←` / `Alt`+`→` |
| Revenir à la page de démarrage | [Accueil des spécifications] dans la barre d'outils |
| Monter d'un niveau | [INDEX parent] dans la barre d'outils, ou un élément du fil d'Ariane |
| Se déplacer dans la page | Appuyez sur un titre dans « Sur cette page » à droite |

## Rechercher un document

Saisissez un mot dans [Filtrer les documents], au-dessus de l'INDEX, pour n'afficher que les documents dont le nom correspond. Effacez le champ pour tout réafficher.

## Mettre à jour le contenu

Lorsque vous enregistrez un fichier Markdown dans l'éditeur de VS Code, l'affichage se met à jour automatiquement. Après une modification effectuée avec un outil externe, appuyez sur [Recharger] dans la barre d'outils.

> **Remarque**
>
> - Les liens externes (`https://`, par exemple) s'ouvrent dans votre navigateur par défaut. Les liens vers des fichiers situés en dehors de la racine de documentation ne s'ouvrent pas.
> - Les documents consultés sont traités sur votre appareil. Aucun document n'est envoyé à l'extérieur pour être lu.

## Voir aussi

- [Utiliser l'INDEX](index-panel.md)
- [Changer de racine de documentation](roots.md)
- [Modifier un document](../03-editing/README.md)
