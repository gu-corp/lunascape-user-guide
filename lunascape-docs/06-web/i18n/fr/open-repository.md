# Ouvrir un dépôt GitHub

Dans la version Web, vous ouvrez les documents en indiquant un dépôt GitHub. Pour un dépôt public, la connexion n'est pas nécessaire.

## Ouvrir depuis l'écran

1. Ouvrez <https://docs.lunascape.org/>.
2. Appuyez sur [Ouvrir des documents] (l'icône de dossier) dans la barre d'outils.
3. Saisissez le dépôt sous [Indiquer un dépôt], puis appuyez sur [Ouvrir].
   Lorsque vous êtes connecté à GitHub, vous pouvez aussi choisir dans une liste sous [Choisir parmi les dépôts lisibles].

> **Astuce**
>
> - L'icône GitHub voisine ouvre sur github.com le document que vous êtes en train de lire. Il ne s'agit pas d'une commande d'ouverture de documents.

## Ouvrir par URL

L'adresse reprend telles quelles la position du dépôt et celle du document. Le chemin correspond à l'emplacement dans le dépôt : l'ordre est donc le même que dans l'URL GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| Ce que vous indiquez | Forme |
|---|---|
| Dépôt seul (branche par défaut) | `/github/owner/repo` |
| Un document dans le dépôt | `/github/owner/repo/docs/01-product/vision.md` |
| Une branche ou une étiquette | ajoutez `?ref=v1.2.0` à la fin |

L'adresse change à mesure que vous changez de page. Appuyez sur [Partager ce document] dans la barre d'outils pour transmettre un lien vers la page que vous lisez. Les boutons [Précédent] et [Suivant] du navigateur fonctionnent également.

L'ancienne forme `?source=` s'ouvre toujours comme auparavant. Une fois ouverte, elle est réécrite dans la nouvelle forme.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Remarque**
>
> - Sans connexion, la limite d'utilisation de l'API GitHub (60 appels par heure) s'applique. Pour les dépôts comportant beaucoup de documents ou pour une consultation répétée, utilisez [Se connecter avec GitHub].
> - Les noms de branche contenant `/` (comme `feature/xxx`) s'indiquent avec `?ref=` dans la forme d'adresse ci-dessus. La forme `?source=` ne permet pas de les écrire.
> - Les documents sont chargés avec les droits GitHub du lecteur. Les personnes sans droit de lecture ne les voient pas.

## Ouvrir les documents d'un dossier local

Appuyez sur [Ouvrir des documents] dans la barre d'outils, puis, sous la liste, sur [Ouvrir les documents d'un dossier local], et choisissez un dossier de votre appareil. Les fichiers sont traités dans le navigateur et ne sont jamais envoyés à l'extérieur. Cela fonctionne dans les navigateurs qui prennent en charge la sélection de dossier (Chrome, Edge, etc.).

## Voir aussi

- [Consulter un dépôt privé](private-repository.md)
- [Impossible d'ouvrir la version Web ou de se connecter](../07-troubleshooting/web.md)
