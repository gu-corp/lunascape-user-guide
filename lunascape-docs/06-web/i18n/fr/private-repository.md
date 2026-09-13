# Consulter un dépôt privé

Les documents des dépôts privés sont consultables après connexion avec GitHub, uniquement pour les dépôts auxquels vous avez un accès en lecture. Lunascape Docs ne possède jamais de compte ni de droits propres.

## Se connecter et ouvrir

1. Ouvrez <https://docs.lunascape.org/>.
   Lorsque vous indiquez un document privé ou que vous n'êtes pas encore connecté, l'écran de connexion s'affiche.
2. Appuyez sur [Se connecter avec GitHub].
   L'écran d'autorisation de GitHub s'ouvre dans une fenêtre contextuelle.
3. Une fois connecté, appuyez sur [Ouvrir des documents] dans la barre d'outils, puis choisissez le dépôt à ouvrir dans [Choisir parmi les dépôts lisibles].

> **Astuce**
>
> - Le nom du compte connecté s'affiche dans la barre d'outils. Vous pouvez aussi vous [Se déconnecter] ou vous [Se connecter avec un autre compte] à cet endroit.
> - La liste présente les dépôts des comptes (organisations ou particuliers) sur lesquels la GitHub App « Lunascape Docs » est installée, limités à ceux auxquels vous avez un accès en lecture.

## Réglages effectués par le propriétaire du dépôt

Si le dépôt visé n'apparaît pas dans la liste, le propriétaire du dépôt ou l'administrateur de l'organisation doit installer la GitHub App « Lunascape Docs ».

- Les droits demandés sont Contents (lecture et écriture) et Pull requests (lecture et écriture). La lecture sert à la consultation, l'écriture aux demandes de publication (Pull Request) depuis le Web. Lunascape Docs ne conserve jamais le contenu des documents.
- L'installation se fait par compte (organisation ou particulier). Vous choisissez de viser « All repositories » (qui inclut automatiquement les dépôts créés par la suite) ou seulement les dépôts sélectionnés.

| Situation | Procédure |
|---|---|
| Installer pour la première fois sur une organisation ou un compte particulier | Depuis la [page d'installation](https://github.com/apps/lunascape-docs/installations/new) |
| Ajouter des dépôts visés dans une organisation où l'app est déjà installée | Settings de l'organisation → GitHub Apps → Lunascape Docs → Configure → Repository access |

Même lorsque l'app est installée pour toute une organisation, chaque membre ne peut consulter que les dépôts auxquels il a un accès en lecture. Il ne peut envoyer une demande de publication que vers les dépôts auxquels il a un accès en écriture.

> **Astuce**
> - Lors d'une nouvelle installation, les droits demandés sont énumérés sur l'écran d'installation, et le fait d'appuyer sur « Install » vaut approbation. Aucune autre opération n'est nécessaire.
> - Une organisation qui avait installé l'app avant l'ajout d'un droit reçoit un e-mail à ses administrateurs, et un bouton d'approbation s'affiche en haut de Settings de l'organisation → GitHub Apps → Lunascape Docs → Configure. Jusqu'à l'approbation, cette organisation peut seulement consulter, et l'envoi d'une demande de publication affiche « L'octroi d'un droit d'écriture est nécessaire ».
> - Vous pouvez vérifier avec quels droits l'app est actuellement installée sur ce même écran Configure. Pour un compte particulier, c'est Settings → Applications → Installed GitHub Apps.
> - Si les dépôts visés ont été retirés par erreur ou si l'app a été désinstallée, il suffit de la réinstaller depuis la [page d'installation](https://github.com/apps/lunascape-docs/installations/new) pour revenir à l'état initial. Le message de refus d'une demande de publication comporte un lien vers l'écran de correction.
> - Si vous ne souhaitez pas que le dépôt accepte de demandes de publication, écrivez `"publish": { "enabled": false }` dans `lunascape-docs.json`. La consultation reste utilisable telle quelle.

## Voir aussi

- [Ouvrir un dépôt GitHub](open-repository.md)
- [Impossible d'ouvrir ou de se connecter dans la version Web](../07-troubleshooting/web.md)
