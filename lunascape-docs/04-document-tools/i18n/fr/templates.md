# Créer un document à partir d'un modèle

Dans l'onglet [Créer] des Outils de document, vous choisissez un modèle, vous prévisualisez le contenu, puis vous créez un nouveau document.

1. Dans la barre d'outils, appuyez sur [Outils de document], puis ouvrez l'onglet [Créer].
2. Appuyez sur [Créer à partir d'un modèle], puis choisissez un modèle.
3. Renseignez les champs de saisie (titre, résumé, etc.). Les champs obligatoires portent la mention « Obligatoire ».
4. Saisissez l'emplacement d'enregistrement sous forme de chemin relatif à la racine de documentation (par exemple `03-design/api.md`).
5. Appuyez sur [Aperçu], puis vérifiez le Markdown généré.
6. Appuyez sur [Créer avec ce contenu].
   Le document est créé et s'affiche dans la visionneuse. La vérification de l'ensemble de la racine de documentation est ensuite exécutée.

## Modèles disponibles

| Modèle | Contenu |
|---|---|
| Document d'une page | Une spécification courte, des notes ou un document explicatif autonome, dans un seul fichier |
| Spécification, manuel, aide | Un seul fichier avec une structure de chapitres générale, utilisable pour une spécification, un manuel ou une aide |
| Modèles du Standard Pack | Lorsque le Standard Pack est sélectionné dans `lunascape-docs.json`, les types de documents autorisés par son profil (cahier des charges, document de conception, etc.) s'ajoutent |

> **Remarque**
>
> - La création nécessite un espace de travail approuvé.
> - Les fichiers existants ne sont jamais remplacés. La création échoue si un document du même nom se trouve déjà à l'emplacement d'enregistrement.
> - L'emplacement d'enregistrement doit porter l'extension `.md` ou `.mdx`. Aucune création n'est possible sous `i18n` (l'emplacement des traductions).
> - Après avoir modifié la saisie, appuyez de nouveau sur [Aperçu] avant de créer le document.

> **Conseil**
>
> Dans un projet qui ne possède pas encore de dossier de documents, vous pouvez créer le premier ensemble avec « Lunascape Docs: テンプレートからドキュメントを作成 » (Créer un document à partir d'un modèle) dans la palette de commandes. Reportez-vous à [Créer ses premiers documents](../01-introduction/first-documents.md).

## Rubriques associées

- [Utiliser les Outils de document](README.md)
- [Modifier les règles de vérification](rules.md)
