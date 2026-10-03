# Ouvrir un dépôt GitHub

Dans la version Web, vous pouvez ouvrir et lire un dépôt GitHub directement, sans le cloner. Aucune connexion n'est nécessaire pour un dépôt public.

## Ouvrir depuis l'écran

1. Appuyez sur [Ouvrir des documents] (l'icône de dossier) dans la barre d'outils. L'écran « Ouvrir des documents » s'ouvre.
2. Dans la colonne de gauche, choisissez l'emplacement à ouvrir.

   | Emplacement | Contenu affiché |
   |---|---|
   | Tout | Tous les emplacements ci-dessous. Les éléments ouverts récemment apparaissent en premier |
   | Ouverts récemment | Les dépôts et dossiers que vous avez déjà ouverts |
   | Recommandés | Les manuels présentés par le site |
   | Dépôts GitHub | Après connexion à GitHub, les dépôts que vous pouvez lire |
   | Cet ordinateur | Les dossiers de cet appareil |

3. Appuyez sur [Ouvrir] sur la ligne souhaitée. Pour filtrer les lignes, saisissez du texte dans [Filtrer par nom de document ou de dépôt], en haut.

Pour un dépôt absent de la liste, indiquez-le avec [Saisir owner/repo et ouvrir] dans la colonne de gauche.

> **Astuce**
>
> - Les dépôts GitHub affichés dans la liste sont ceux sur lesquels l'application GitHub « Lunascape Docs » est installée et pour lesquels vous avez un droit de lecture. Si un dépôt n'apparaît pas, demandez à son propriétaire d'ajouter l'application.

## Vérifier l'emplacement du document

La petite icône située à gauche de la barre d'outils (la pastille d'emplacement) indique où se trouve le document que vous lisez.

| Icône | Emplacement |
|---|---|
| Logo GitHub | Lecture depuis GitHub. Rien n'est enregistré sur cet appareil |
| Dossier | Un dossier de cet appareil |

Appuyez sur l'icône pour afficher l'emplacement, son état et les actions possibles depuis celui-ci ([Voir sur GitHub], [Copier le lien], etc.).

## Ouvrir par URL

L'adresse reprend telle quelle le dépôt et l'emplacement du document. Le chemin correspond à l'emplacement dans le dépôt ; il suit donc le même ordre que l'URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Élément à indiquer | Syntaxe |
|---|---|
| Dépôt seul (branche par défaut) | `/github/owner/repo` |
| Document dans le dépôt | `/github/owner/repo/docs/01-product/vision.md` |
| Branche ou tag | Ajoutez `?ref=v1.2.0` à la fin |

L'adresse change lorsque vous changez de page. Appuyez sur [Partager ce document] dans la barre d'outils pour transmettre le lien de la page que vous lisez. Les boutons [Précédent] et [Suivant] du navigateur fonctionnent également.

L'ancienne forme `?source=` s'ouvre toujours. Une fois la page ouverte, l'adresse est réécrite sous la nouvelle forme.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Remarque**
>
> - Sans connexion, la limite d'utilisation de l'API GitHub s'applique (60 requêtes par heure). Pour un dépôt contenant de nombreux documents ou pour des consultations répétées, utilisez [Se connecter avec GitHub].
> - Un nom de branche contenant `/` (par exemple `feature/xxx`) peut être indiqué avec `?ref=` dans la forme d'adresse ci-dessus. La forme `?source=` ne permet pas de l'écrire.
> - Les documents sont chargés avec les droits GitHub du lecteur. Ils ne s'affichent pas pour les personnes sans droit de lecture.

## Ouvrir les documents d'un dossier local

Appuyez sur [Ouvrir des documents] dans la barre d'outils, puis sur [Ouvrir les documents d'un dossier local] dans la colonne de gauche, et choisissez un dossier de votre appareil. Les fichiers sont traités dans le navigateur et ne sont jamais envoyés à l'extérieur. Cette fonction est disponible dans les navigateurs qui prennent en charge la sélection de dossiers (Chrome, Edge, etc.).

## Voir aussi

- [Consulter un dépôt privé](private-repository.md)
- [Impossible d'ouvrir la version Web ou de se connecter](../07-troubleshooting/web.md)
