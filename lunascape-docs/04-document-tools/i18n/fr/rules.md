# Modifier les règles de vérification

Vous pouvez modifier le niveau de notification (erreur, avertissement, information) de chaque point de vérification, ou désactiver celui-ci. Les modifications sont enregistrées dans le fichier `docs-lint.config.json` de la racine de documentation et partagées avec l'équipe.

## Modifier un niveau de notification

1. Dans la barre d'outils, appuyez sur [Outils de document], puis ouvrez l'onglet [Vérification].
2. Appuyez sur [Consulter et modifier les règles].
   La liste des points de vérification se déplie dans la même carte. Chaque point indique son objectif et l'origine de son réglage actuel (Project, Profile, Pack ou Default).
3. Choisissez le niveau de notification du point à modifier.
4. Appuyez sur [Enregistrer et vérifier à nouveau].
   Le réglage est enregistré et l'ensemble de la racine de documentation est vérifié de nouveau avec la nouvelle configuration.

| Option | Signification |
|---|---|
| [Réglage standard (…)] | Supprime la valeur personnalisée et rétablit le réglage standard déterminé par le profil, le Standard Pack, puis la valeur par défaut, dans cet ordre |
| [Ne pas utiliser] | N'effectue pas cette vérification |
| [Information] / [Avertissement] / [Erreur] | Signale à ce niveau de notification |

> **Remarque**
>
> - L'enregistrement nécessite un espace de travail approuvé.
> - Seul le niveau de notification de chaque point est enregistré. Les options propres à chaque point sont conservées telles quelles. Le Standard Pack et le profil eux-mêmes ne se modifient pas depuis cet écran.
> - Si le fichier `docs-lint.config.json` a été modifié depuis l'extérieur juste avant l'enregistrement, celui-ci est interrompu. Chargez l'état le plus récent, puis recommencez.
> - Si le fichier `docs-lint.config.json` n'existe pas, il est créé lors de l'enregistrement.

## Modifier directement les fichiers de configuration

- Appuyez sur [Ouvrir les paramètres détaillés] pour ouvrir `docs-lint.config.json` dans VS Code.
- Ouvrez [Origine des règles et paramètres du document], puis appuyez sur [Modifier les paramètres du document] pour ouvrir `lunascape-docs.json` dans VS Code. C'est là que vous choisissez le Standard Pack et le profil.

Pour ces deux fichiers, la saisie semi-automatique et les descriptions fournies par les JSON Schema livrés avec l'extension sont actives.

## Standard Pack et profils

Un Standard Pack est un standard documentaire qui réunit les types de documents requis, la structure des chapitres, la terminologie et les modèles. Vous le choisissez avec `documentStandards` dans `lunascape-docs.json`.

```json
{
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  }
}
```

Le Pack livré `builtin:gu-corp-software` propose les profils `base`, `web-application`, `api-service`, `regulated-financial-product` et `smart-contract`.

## Voir aussi

- [Vérifier les documents](check.md)
- [Paramètres du projet](project-configuration.md)
