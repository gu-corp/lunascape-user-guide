# Configuration du projet

Le fichier `lunascape-docs.json` placé directement sous la racine documentaire contient les paramètres de cette racine, partagés par l'équipe. Il est géré dans Git.

## Créer ou modifier le fichier de configuration

- Dans la barre d'outils, appuyez sur [Outils de document] → onglet [Vérification] → [Origine des règles et paramètres du document] → [Modifier les paramètres du document] pour l'ouvrir dans VS Code. Si le fichier n'existe pas, un fichier initial est créé à ce moment-là.
- Le nom de fichier `lunascape-docs.json` est automatiquement associé au JSON Schema fourni, qui offre l'auto-complétion et une description de chaque champ. Aucune entrée `$schema` n'est nécessaire.

## Exemple de configuration

```json
{
  "id": "product-docs",
  "title": "Documentation produit",
  "indexTitle": "INDEX",
  "startPage": "README.md",
  "appearance": "light",
  "defaultLocale": "ja",
  "fallbackLocale": "en",
  "locales": ["ja", "en"],
  "ignoredDirectories": ["99-archive"],
  "tree": {
    "autoHideSingleItem": true,
    "showFileNames": false,
    "showDocumentIcons": false,
    "showFolderIcons": false,
    "showItemCounts": false,
    "showGuides": true,
    "density": "comfortable"
  },
  "editor": {
    "defaultMode": "visual",
    "showEditButton": true
  },
  "documentStandards": {
    "pack": "builtin:gu-corp-software",
    "profile": "web-application"
  },
  "translation": {
    "enabled": true,
    "contextFiles": ["README.md", "glossary/TERMS.md"],
    "maxContextCharacters": 49152
  }
}
```

## Description des champs

| Champ | Contenu | Par défaut |
|---|---|---|
| `id` | La clé sous laquelle sont enregistrés les paramètres d'affichage de chaque utilisateur. Attribuez un ID fixe lorsque vous voulez conserver les paramètres même après avoir déplacé le dossier | Le chemin du dossier |
| `title` | Le nom affiché à l'extrême gauche de la barre d'outils et dans la liste des racines documentaires. Il ne change pas avec la langue d'affichage | Le titre du README/index de la racine, sinon le nom du dossier |
| `indexTitle` | Le titre de l'INDEX | `INDEX` |
| `startPage` | Le document ouvert en premier (chemin relatif à la racine documentaire) | `README.md` |
| `appearance` | Le jeu de couleurs : `light` (toujours clair) ou `auto` (suit le thème de VS Code) | `light` |
| `defaultLocale` | La langue par défaut (la langue du document de référence). Se spécifie avec une balise de langue BCP 47 (`ja`, `en`, `zh-Hant`, etc.). Elle sert de source de traduction | Non défini (déduit du contenu pour l'affichage) |
| `fallbackLocale` | La langue montrée en premier aux lecteurs dont la langue de l'environnement ne correspond à aucune des langues prises en charge. Indiquez une langue contenue dans `locales` | Non défini (`defaultLocale` est utilisé) |
| `locales` | La liste des langues prises en charge. Incluez-y `defaultLocale`. Elles apparaissent dans le menu des langues et deviennent les cibles de traduction | `defaultLocale` uniquement |
| `ignoredDirectories` | Les noms des dossiers exclus de l'INDEX, de la recherche et des vérifications. Le spécifier remplace la valeur par défaut | `["99-archive"]` |
| `tree` | Les valeurs par défaut de l'affichage de l'INDEX. Les utilisateurs peuvent les remplacer dans les paramètres d'affichage | Comme dans l'exemple ci-dessus |
| `editor.defaultMode` | La vue d'édition tant qu'un utilisateur n'en a pas changé : `visual` ou `source` | `visual` |
| `editor.showEditButton` | Indique si [Modifier] s'affiche en bas à droite du document | `true` |
| `documentStandards.pack` | Le Standard Pack utilisé pour la vérification des documents et les modèles : `builtin:<nom>` ou un chemin relatif à la racine documentaire | Aucun |
| `documentStandards.profile` | Un nom de profil défini par le Pack | Aucun |
| `translation.enabled` | Active la création de propositions de traduction et la traduction en lot | `true` |
| `translation.contextFiles` | Les fichiers Markdown de référence (chemin relatif à la racine documentaire) transmis lors de la traduction comme références de terminologie et de style | `[]` |
| `translation.maxContextCharacters` | La limite du nombre total de caractères des documents de référence (maximum 1048576) | `49152` |
| `description` | Une description en une ligne de l'ensemble de documents. Affichée sur la carte de la page d'accueil du dépôt. Comme `title`, s'écrit sous forme de chaîne ou d'objet par langue | Aucun |

## Indiquer où se trouvent les documents dans le dépôt

Le fichier `lunascape-docs.json` placé directement à la racine du dépôt peut contenir non pas les paramètres de ce dossier, mais une **carte du dépôt**. Renseigner l'un des trois champs suivants en fait une carte, et le dossier lui-même n'est alors pas une racine documentaire.

| Champ | Contenu | Par défaut |
|---|---|---|
| `defaultFolder` | Le dossier où se trouvent les documents (chemin relatif à la racine). Le dossier désigné n'a besoin d'aucun fichier de configuration | Aucun (`docs` est utilisé) |
| `roots` | La liste des ensembles de documents lorsqu'il y en a plusieurs (chemins relatifs à la racine, dans l'ordre d'affichage). Dans ce cas, la racine devient la page d'accueil | Aucun |
| `excludes` | Les dossiers à exclure de la découverte des racines documentaires (chemins relatifs à la racine). S'ajoutent aux exclusions par défaut comme `node_modules` | `[]` |
| `home.cards` | Indique si la page d'accueil affiche les cartes des ensembles de documents sous son README. Mettez `false` lorsque vous écrivez vous-même les liens dans le README | `true` |

La racine documentaire est déterminée dans l'ordre suivant. En partant du haut, la première trouvée est utilisée.

1. Lorsqu'un dossier est indiqué par un paramètre ou une commande, ce dossier
2. Ce que désigne `defaultFolder` ou `roots` dans le `lunascape-docs.json` situé à la racine
3. Le dossier qui contient un `lunascape-docs.json` (s'il y en a deux ou plus sous un parent commun, ce parent devient la page d'accueil)
4. Le dossier `docs` (`lunascapeDocEditor.rootDirectoryNames`)
5. La racine du dépôt elle-même

> **Astuce**
>
> Si vous n'écrivez rien, le point 4 s'applique ; un dépôt ordinaire avec un seul `docs/` fonctionne donc comme avant. Écrivez `defaultFolder` uniquement lorsque le dossier porte un autre nom, par exemple `manual`.

### Exemple de carte

```json
{
  "title": "Aide Lunascape",
  "roots": ["desktop", "mobile"],
  "excludes": ["third-party"],
  "home": { "cards": true }
}
```

## Ordre de priorité des paramètres

Les champs liés à l'affichage sont prioritaires dans l'ordre suivant.

1. Les paramètres d'affichage de l'utilisateur (panneau [Paramètres d'affichage])
2. Les paramètres de VS Code (`lunascapeDocEditor.*`)
3. `lunascape-docs.json`
4. Les valeurs par défaut du produit

Seules les langues (`defaultLocale`, `fallbackLocale`, `locales`) font exception : `lunascape-docs.json` fait foi. Les paramètres personnels de VS Code ne peuvent pas remplacer les langues du projet.

> **Remarque**
>
> Un Standard Pack peut aussi être indiqué comme `standard` dans `docs-lint.config.json`. Lorsque les deux sont présents, `docs-lint.config.json` est prioritaire.

## Voir aussi

- [Modifier les règles de vérification](rules.md)
- [Modifier les paramètres d'affichage](../02-reading/display-settings.md)
- [Liste des paramètres de VS Code](../08-reference/settings.md)
