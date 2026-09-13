# Impossible d'ouvrir la version Web ou de se connecter

## Le dépôt n'apparaît pas dans la liste après connexion

L'application GitHub « Lunascape Docs » n'est pas installée sur ce compte, ou le dépôt concerné n'y est pas inclus. Demandez au propriétaire du dépôt ou à l'administrateur de l'organisation de l'installer en suivant la procédure décrite dans [Consulter un dépôt privé](../06-web/private-repository.md).

## Impossible d'aller au-delà de l'écran de connexion

- Vous n'avez pas l'autorisation de lecture sur le dépôt concerné. Demandez au propriétaire du dépôt de vous l'accorder.
- « Aucune connexion GitHub n'est configurée pour ce site » : la visionneuse que vous avez déployée vous-même n'a pas de service de connexion configuré. Un administrateur doit en configurer un.

## La fenêtre contextuelle de connexion ne s'ouvre pas

Le navigateur bloque les fenêtres contextuelles. Autorisez-les pour ce site, puis réessayez.

## Le message « Votre connexion a expiré » s'affiche

La connexion a expiré. Appuyez de nouveau sur [Se connecter avec GitHub].

## L'ouverture d'un dépôt public renvoie une erreur 404

- Vérifiez la notation `owner/repo@ref/dir`.
- Les noms de branche contenant `/` ne peuvent pas être indiqués.

## Le chargement cesse de fonctionner au bout d'un moment

Sans connexion, la limite d'utilisation de l'API GitHub (60 appels par heure) s'applique. Si le message « Limite d'appels atteinte » s'affiche, patientez un moment ou utilisez [Se connecter avec GitHub].

## Le message « Ce site ne peut pas afficher ce dépôt » s'affiche

Pour ouvrir un dépôt depuis une visionneuse que vous avez déployée vous-même, l'URL de ce site doit être ajoutée à `viewer.origins` dans le fichier `lunascape-docs.json` du dépôt.

## Rien ne s'affiche à l'ouverture de `index.html`

L'ouverture directe via `file://` ne fonctionne pas. Ouvrez le fichier via un serveur HTTP ou utilisez la version VS Code.

## Le site exporté affiche « lunascape-docs-manifest.json est introuvable »

Déployez tel quel l'ensemble des fichiers produits par `npm run export:web`, manifeste compris.

## Impossible d'enregistrer un brouillon

- « Impossible d'ouvrir IndexedDB », « Utilisé par un autre onglet » : la cause est le mode de navigation privée du navigateur ou un autre onglet affichant le même site. Ouvrez le site dans une fenêtre normale et fermez les autres onglets.
- Les brouillons sont enregistrés par appareil et par navigateur. Ils ne sont pas transmis à un autre appareil.

## Rubriques connexes

- [Ouvrir un dépôt GitHub](../06-web/open-repository.md)
- [Enregistrer un brouillon](../06-web/drafts.md)
