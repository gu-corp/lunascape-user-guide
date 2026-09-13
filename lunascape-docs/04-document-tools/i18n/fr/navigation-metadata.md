# Configurer les informations de navigation

Le nom et l'ordre affichés dans l'INDEX s'écrivent dans le YAML front matter de chaque document. Les documents s'affichent même sans cela, en utilisant le titre (H1) et l'ordre des noms de fichiers.

## Nom et ordre d'un document

Écrivez ce qui suit au début du document.

```yaml
---
navigation:
  title: Prise en main
  order: 200
---
```

| Champ | Signification |
|---|---|
| `navigation.title` | Le nom affiché dans l'INDEX. S'il est omis, le H1 est utilisé, puis le nom du fichier |
| `navigation.order` | Un entier qui détermine l'ordre, croissant. S'il est omis, un ordre par défaut stable (par nom de fichier) s'applique |

> **Astuce**
>
> - Attribuez les valeurs d'`order` par pas de 100, comme 100, 200, 300, afin de pouvoir insérer 150 entre elles plus tard.
> - Un `order` manquant, incorrect ou en double ne masque jamais un document.
> - Réordonner dans l'INDEX écrit `navigation.order` à votre place ; il n'est pas nécessaire de l'écrire à la main.

## Nom et ordre d'un dossier

Le nom et l'ordre d'un dossier appartiennent au front matter de son `README.md` (ou `index.md` en l'absence de README). La page de couverture n'a pas besoin de contenu.

```yaml
---
navigation:
  title: Planification produit
  order: 100
---
```

Un dossier sans page de couverture utilise son nom de dossier et l'ordre par défaut. Lorsqu'un changement de titre ou un réordonnancement dans l'INDEX le nécessite, un `README.md` contenant uniquement le front matter est créé. La simple consultation ne crée jamais de fichier.

## Traitement dans les versions traduites

- L'ordre et le rôle d'un dossier (page de couverture ou configuration uniquement) sont décidés par le seul document en Langue par défaut.
- Une traduction peut uniquement remplacer `navigation.title`. Lorsque le document de référence possède du contenu, le H1 de la traduction est également utilisé comme nom.
- Une traduction seule n'ajoute jamais de page.

## Tri et repli des éléments enfants

`navigation.children.sort` et `navigation.children.defaultCollapsed`, dans la page de couverture d'un dossier, sont définis pour contrôler la façon dont ses enfants directs sont triés et s'ils commencent repliés. Leur lecture et leur édition dans VS Code sont prévues prochainement.

## Voir aussi

- [Modifier l'ordre des documents](../03-editing/reorder.md)
- [Racines documentaires et conventions de fichiers](structure.md)
