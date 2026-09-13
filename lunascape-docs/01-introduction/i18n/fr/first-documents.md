# Créer vos premiers documents

Dans un projet qui ne possède pas encore de dossier de documentation, vous pouvez créer un premier ensemble de documents depuis la palette de commandes.

1. Ouvrez le dossier du projet dans VS Code et approuvez l’espace de travail.
2. Dans la palette de commandes (`⇧⌘P` / `Ctrl+Shift+P`), exécutez « Lunascape Docs : Créer une documentation à partir d’un modèle ».
   Si l’espace de travail contient plusieurs dossiers, choisissez celui dans lequel créer les documents.
3. Choisissez la structure à créer.
   - [Document d’une page] : uniquement un `README.md`. Convient à une spécification courte, à des notes ou à un document explicatif isolé.
   - [Ensemble de documents] : une page d’accueil, ainsi que les pages d’entrée de `specification/` (spécifications), `manual/` (manuel) et `help/` (aide).
4. Saisissez le titre de la documentation. Il est utilisé pour le README et pour les titres de chaque document.
5. Saisissez le dossier de documentation à créer, en chemin relatif à l’espace de travail. La valeur par défaut est `docs`.
6. Vérifiez la liste des fichiers à créer, puis appuyez sur [Créer].
   Une fois la création terminée, le nouveau `README.md` s’ouvre dans la visionneuse.

> **Remarque**
>
> - Les fichiers existants ne sont jamais remplacés. Si ne serait-ce qu’un des fichiers à créer existe déjà, rien n’est créé et l’opération est interrompue.
> - La création n’est pas possible dans un espace de travail non approuvé.

> **Conseil**
>
> - Si vous disposez déjà d’un dossier de documentation, cette procédure est inutile : passez à [Opérations de base](../02-reading/README.md).
> - Lorsque la documentation s’étoffe, vous pouvez ajouter les documents un par un depuis l’onglet [Créer] des Outils de document, en choisissant un modèle.

## Rubriques connexes

- [Créer un document à partir d’un modèle](../04-document-tools/templates.md)
- [Racines de documentation et conventions de fichiers](../04-document-tools/structure.md)
