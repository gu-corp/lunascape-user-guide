# Utilisation depuis une IA

L'extension enregistre auprès de VS Code l'outil Language Model Tool en lecture seule `lunascape_getDocsSpecification`. Lorsqu'un agent VS Code compatible est interrogé sur les fonctionnalités, la configuration ou les conventions documentaires de Lunascape Docs, il peut récupérer le contenu de cette aide (la spécification générale) au moyen de cet outil.

## Utilisation

Dans le chat de VS Code, posez votre question en ajoutant `#lunascapeDocs`, ou interrogez simplement l'outil sur la configuration ou la structure documentaire de Lunascape Docs.

```text
#lunascapeDocs lunascape-docs.json で英語の翻訳を有効にするには？
```

## Arguments de l'outil

| Argument | Contenu |
|---|---|
| `topic` | Le chapitre à récupérer : `all`, `usage` (opérations de base), `structure` (racines documentaires et conventions de fichiers), `editing` (modifier un document), `configuration` (configuration du projet), `security` (sécurité et limites d'enregistrement) ou `ai` (utilisation depuis une IA) |
| `locale` | La langue de l'aide (un tag de langue de l'aide fournie, tel que `ja` ou `en`). En cas d'omission, la langue d'affichage de VS Code est utilisée, à défaut l'aide en japonais est renvoyée |

> **Remarque**
>
> - L'outil n'envoie jamais le contenu des documents vers l'extérieur.
> - L'outil ne renvoie jamais les noms d'espace de travail ni les chemins locaux.
> - L'outil ne modifie aucun fichier.
> - Il est utilisable depuis un agent VS Code compatible même en l'absence d'un fichier `AGENTS.md`. Il n'est pas partagé automatiquement avec les autres clients d'IA qui n'utilisent pas l'API d'outils de l'extension.

## Voir aussi

- [Afficher l'aide](../02-reading/help.md)
- [Sécurité et limites d'enregistrement](security.md)
