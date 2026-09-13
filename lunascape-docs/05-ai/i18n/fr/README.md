# Confier un travail à une IA

Lunascape Docs n'appelle aucun modèle de langage. Le produit prépare **le contexte, les outils et les vérifications**, et laisse la traduction, la relecture et la rédaction à l'IA que vous utilisez.

## Le principe

| Ce que le produit fournit | Contenu |
|---|---|
| Contexte | Les conventions de la documentation (emplacement des traductions, front matter, standard de document, glossaire) et l'emplacement du document visé |
| Outils de travail | Le registre des traductions non traduites et à mettre à jour, la lecture et l'écriture des documents, la création à partir de modèles |
| Vérifications | La validation par docs-lint, l'écart de couverture et de fraîcheur |

L'instruction ne contient pas le texte du document : l'IA lit elle-même les fichiers, les écrit et les vérifie.

## Confier un travail

1. Dans la barre d'outils, appuyez sur [Outils de document], puis ouvrez l'onglet [IA].
2. Sous [Travail], choisissez le travail à confier.
3. Renseignez les éléments nécessaires (langue cible, sujet).
4. Appuyez sur [Confier ce travail].
   Un terminal VS Code s'ouvre et l'IA choisie reçoit l'instruction et commence le travail.

> **Conseil**
>
> Une session Claude Code est accompagnée des outils de travail (le serveur MCP `lunascape-docs`) : elle peut récupérer elle-même la liste des documents non traduits ou à mettre à jour, exécuter docs-lint et enregistrer la fraîcheur après traduction.

## Vérifier le résultat

| Forme du fournisseur | Où arrive le résultat |
|---|---|
| Session (Claude Code, Codex) | Écrit directement dans l'arbre de travail. **Vérifiez dans le différentiel Git** |
| API (modèles de langage de VS Code, Anthropic, compatibles OpenAI) | Renvoie une proposition document par document. Vérifiez avec [Ouvrir le différentiel], puis écrivez avec [Enregistrer] |

### Vérifier une proposition en mode API

Avec un fournisseur de type API, la proposition arrive dans l'onglet [IA].

1. Appuyez sur [Ouvrir le différentiel] et comparez avec le contenu actuel.
2. Si cela vous convient, appuyez sur [Enregistrer]. Dans le cas d'une traduction, la fraîcheur est également enregistrée. Pour renoncer, appuyez sur [Abandonner].
   Pour interrompre une génération en cours, appuyez sur [Arrêter].

> **Remarque**
>
> - Lunascape Docs n'effectue jamais d'indexation ni de commit Git. Vérifiez toujours les modifications dans le différentiel.
> - Vous ne pouvez pas confier de travail dans un espace de travail non approuvé, ni pendant l'affichage temporaire d'un dossier situé hors d'une racine de documentation.

## Voir aussi

- [Travaux disponibles](tasks.md)
- [Paramètres de l'IA](settings.md)
- [Le registre et ses enregistrements](ledger.md)
