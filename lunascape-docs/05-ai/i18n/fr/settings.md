# Paramètres IA

Choisissez l'IA et le modèle auxquels confier votre travail. Cet écran utilise ses propres listes déroulantes, et non la sélection rapide de VS Code.

1. Appuyez sur [Outils de document] → l'onglet [IA] → [Paramètres IA…].
2. Choisissez un [Fournisseur].
   Les fournisseurs inutilisables sur ce poste apparaissent non sélectionnables, avec le motif.
3. Choisissez un [Modèle]. Les choix varient selon le fournisseur.
4. Fermez l'écran. Le choix est enregistré par utilisateur et réutilisé la fois suivante.

## Fournisseurs

| Fournisseur | Type | Détection |
|---|---|---|
| Claude Code | Session | Présence de la commande `claude` |
| Codex | Session | Présence de la commande `codex` |
| Modèles de langage de VS Code | API | Modèles enregistrés auprès de l'API Language Model de VS Code |
| API Anthropic | API | Clé d'API enregistrée |
| API compatible OpenAI | API | Clé d'API et point de terminaison enregistrés |

Un fournisseur de type **session** lit et écrit les fichiers lui-même et exécute lui-même la vérification du document. Ses résultats sont écrits directement dans l'arbre de travail et se consultent dans les différences Git.

Un fournisseur de type **API** renvoie le Markdown d'un seul document, et l'extension affiche les différences avant l'enregistrement.

## Enregistrer une clé d'API

L'API Anthropic et les API compatibles OpenAI deviennent utilisables une fois une clé d'API enregistrée.

1. Choisissez le [Fournisseur] à enregistrer. Le champ de la clé d'API apparaît.
2. Saisissez la [Clé d'API]. Pour une API compatible OpenAI, saisissez aussi le [Point de terminaison] (par exemple `https://api.openai.com/v1`).
3. Appuyez sur [Enregistrer]. « Clé enregistrée » s'affiche.

> **Remarque**
>
> - Les clés sont conservées dans le SecretStorage de VS Code et ne sont plus jamais affichées. Elles ne sont écrites ni dans `settings.json` ni dans un document. [Supprimer la clé] permet d'en supprimer une.
> - La liste des modèles est récupérée auprès de chaque service avec la clé enregistrée. Tant que la récupération n'aboutit pas, une liste connue est affichée.
> - Un fournisseur de type API ne peut exécuter que « Traduire cette page » et « Relire cette page ». Le parcours de plusieurs documents et la création de documents relèvent des fournisseurs de type session.

> **Astuce**
>
> Si aucun fournisseur n'est trouvé, installez Claude Code ou Codex, ou enregistrez une clé d'API. Rouvrez [Paramètres IA…] pour qu'il soit détecté.

## Voir aussi

- [Confier un travail à une IA](README.md)
- [Liste des paramètres VS Code](../08-reference/settings.md)
