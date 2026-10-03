# Ouvrir un dépôt GitHub

Dans la version Web et dans Lunascape, vous pouvez ouvrir et lire un dépôt GitHub tel quel, sans le dupliquer. Aucune connexion n'est nécessaire pour un dépôt public.

## Ouvrir depuis l'écran

1. Appuyez sur [Ouvrir des documents] (l'icône de dossier) dans la barre d'outils. L'écran « Ouvrir des documents » s'ouvre.
2. Dans le volet de gauche, choisissez l'emplacement à ouvrir.

   | Emplacement | Contenu |
   |---|---|
   | Tout | Tout ce qui figure ci-dessous. Les éléments ouverts récemment apparaissent en tête |
   | Ouverts récemment | Les dépôts et dossiers déjà ouverts |
   | Sélection | Les manuels présentés par le site |
   | Dépôts GitHub | Une fois la connexion à GitHub établie, les dépôts que vous pouvez lire |
   | Cet ordinateur | Les dossiers de cet appareil. Dans Lunascape, les dépôts dupliqués y figurent aussi |

3. Appuyez sur [Ouvrir] sur la ligne voulue. Pour réduire la liste, saisissez du texte dans [Filtrer par nom de document ou de dépôt], en haut.

Pour un dépôt absent de la liste, indiquez-le avec [Saisir owner/repo et ouvrir] dans le volet de gauche.

> **Astuce**
>
> - Les dépôts GitHub de la liste sont ceux sur lesquels l'application GitHub « Lunascape Docs » est installée et pour lesquels vous disposez d'un droit de lecture. Si un dépôt est introuvable, demandez à son propriétaire d'ajouter l'application.

## Vérifier l'emplacement d'un document

La petite icône située à gauche de la barre d'outils (la pastille d'emplacement) indique où se trouve le document que vous lisez.

| Icône | Emplacement |
|---|---|
| Le logo GitHub | Le document est lu depuis GitHub. Il n'est pas enregistré sur cet appareil |
| Un ordinateur | Un dossier de cet appareil géré par Lunascape. Le nom de la branche Git et le nombre de fichiers modifiés s'affichent aussi |
| Un dossier | Un dossier de cet appareil |

Appuyez sur l'icône pour afficher l'emplacement, son état et les actions possibles depuis cet emplacement ([Voir sur GitHub], [Copier le lien], etc.).

## Dupliquer un dépôt dans Lunascape

Dans Lunascape, vous pouvez dupliquer un dépôt GitHub sur cet appareil, puis le modifier et faire des commits avec Git.

- Dans l'écran « Ouvrir des documents », appuyez sur [Dupliquer] sur la ligne du dépôt.
- Si vous lisez un dépôt ouvert depuis GitHub, appuyez sur la pastille d'emplacement, puis sur [Dupliquer sur cet ordinateur]. Une fois la duplication terminée, le même document s'ouvre dans sa version présente sur cet appareil.

Un dépôt dupliqué porte la mention « Sur cet ordinateur » dans la liste, et [Ouvrir sur cet ordinateur] y apparaît en premier.

## Ouvrir par URL

L'adresse indique simplement le dépôt, puis l'emplacement du document. Le chemin correspond à l'emplacement dans le dépôt : il suit donc le même ordre que l'URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Élément à indiquer | Syntaxe |
|---|---|
| Dépôt seul (branche par défaut) | `/github/owner/repo` |
| Document dans le dépôt | `/github/owner/repo/docs/01-product/vision.md` |
| Branche ou tag précis | Ajoutez `?ref=v1.2.0` à la fin |

L'adresse change lorsque vous changez de page. Appuyez sur [Partager ce document] dans la barre d'outils pour transmettre le lien de la page que vous lisez. Les boutons [Précédent] et [Suivant] du navigateur fonctionnent aussi.

L'ancienne forme `?source=` s'ouvre toujours. Une fois la page ouverte, l'adresse est réécrite sous la nouvelle forme.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Attention**
>
> - Sans connexion, l'API GitHub limite le nombre de requêtes (60 par heure). Pour un dépôt contenant de nombreux documents ou pour une lecture répétée, appuyez sur [Se connecter avec GitHub].
> - Un nom de branche contenant `/` (par exemple `feature/xxx`) peut être indiqué avec `?ref=` dans la forme d'adresse ci-dessus. La forme `?source=` ne permet pas de l'écrire.
> - Les documents sont chargés avec les droits GitHub de la personne qui les consulte. Les personnes sans droit de lecture ne les voient pas.

## Ouvrir les documents d'un dossier local

Appuyez sur [Ouvrir des documents] dans la barre d'outils, puis sur [Ouvrir les documents d'un dossier local] dans le volet de gauche, et choisissez un dossier de l'appareil. Les fichiers sont traités dans le navigateur et ne sont jamais envoyés à l'extérieur. Cette fonction est disponible dans les navigateurs qui prennent en charge la sélection de dossier (Chrome, Edge, etc.).

## Voir aussi

- [Consulter un dépôt privé](private-repository.md)
- [Impossible d'ouvrir la version Web ou de se connecter](../07-troubleshooting/web.md)
