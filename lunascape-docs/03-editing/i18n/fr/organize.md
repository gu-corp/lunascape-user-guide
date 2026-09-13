# Créer et organiser des documents et des dossiers

Le menu d'élément de l'INDEX permet de créer, dupliquer, renommer et supprimer des documents et des dossiers. La saisie se fait dans une petite boîte de dialogue à l'intérieur de la visionneuse, sans interrompre la lecture.

> **Remarque**
>
> Ces opérations ne sont disponibles que si l'espace de travail est approuvé dans VS Code. Elles ne peuvent pas s'exécuter pendant la modification d'un document, pendant le traitement d'une autre opération, ni lorsque l'élément visé comporte des modifications non enregistrées.

## Créer un document ou un dossier

1. Ouvrez le menu d'élément ([⋯] ou clic droit) du dossier de destination.
   Pour créer directement sous la racine de documentation, utilisez le [⋯] situé à l'extrémité droite du titre de l'INDEX, ou faites un clic droit sur une zone vide de l'INDEX.
2. Choisissez [Nouveau document] ou [Nouveau dossier].
3. Saisissez un nom, puis appuyez sur [Créer].
   Un nom de document doit comporter une extension Markdown (`.md`, `.markdown`, `.mdx`, etc.).

Les nouveaux documents sont créés comme documents de la langue par défaut (documents de référence).

## Dupliquer un document

1. Ouvrez le menu d'élément du document, puis choisissez [Dupliquer].
2. Saisissez un nouveau nom, puis appuyez sur [Créer].

Seul le document de référence est dupliqué. Ses traductions ne le sont pas.

## Modifier le titre

Modifie le titre (H1) du document. Le nom de fichier ne change pas.

1. Ouvrez le menu d'élément d'un document ou d'un dossier, puis choisissez [Modifier le titre].
2. Saisissez le nouveau titre sur une seule ligne, puis appuyez sur [Modifier].

Pour un dossier, c'est le titre du `README.md` de ce dossier qui est modifié. Lorsque la langue affichée est une traduction, c'est le titre du document de cette langue qui change.

## Modifier le nom du document

Modifie le nom du document affiché dans la barre d'outils (le nom de la racine de documentation).

1. Faites un clic droit sur le nom du document dans la barre d'outils. Le [⋯] situé à droite du titre de l'INDEX ouvre le même menu.
2. Choisissez [Renommer le document], puis saisissez un nouveau nom.

Tant que rien n'est configuré, le nom du dossier est affiché tel quel.

Le nom modifié est écrit **à l'endroit qui fournit actuellement le nom du document**. Il n'est pas écrit à un endroit non utilisé pour l'affichage, ce qui laisserait ignorer un titre visible.

| État actuel | Destination de l'écriture |
|---|---|
| `lunascape-docs.json` contient un nom | `lunascape-docs.json` est mis à jour |
| Aucun nom, mais la racine de documentation contient un README | Le titre (H1) du README est réécrit |
| Ni l'un ni l'autre | `lunascape-docs.json` est créé et le nom y est enregistré |

Le message affiché après la modification indique à quel endroit l'écriture a eu lieu.

> **Conseil**
>
> Le nom du document est déterminé dans cet ordre : le nom dans `lunascape-docs.json`, puis le titre du README de la racine de documentation, puis le nom du dossier.

## Renommer un fichier ou un dossier

1. Ouvrez le menu d'élément, puis choisissez [Renommer le fichier] ou [Renommer le dossier].
2. Saisissez le nouveau nom, puis appuyez sur [Modifier].

Les traductions correspondantes (le même chemin sous `i18n/<langue>/`) sont renommées en même temps.

## Supprimer

1. Ouvrez le menu d'élément, puis choisissez [Déplacer vers la corbeille].
2. Vérifiez le contenu du message de confirmation, puis approuvez le déplacement.

L'élément est déplacé vers la corbeille du système d'exploitation ; il peut donc être restauré si nécessaire. Les traductions ne sont pas supprimées et restent en place.

## Noms qui ne peuvent pas être utilisés

- Les noms commençant par `.` (ils n'apparaîtraient pas dans l'INDEX)
- `i18n` (réservé aux fichiers de traduction)
- Les noms réservés par Windows (`CON`, `PRN`, etc.)
- Les noms se terminant par un point ou une espace
- Les noms contenant des caractères de contrôle ou des caractères interdits dans les noms de fichiers
- Les noms déjà présents dans le même dossier (y compris ceux qui ne diffèrent que par la casse)

> **Remarque**
>
> La page de démarrage (normalement le `README.md` de la racine) ne peut être ni renommée ni déplacée. Modifiez d'abord `startPage` dans `lunascape-docs.json`.

## Rubriques associées

- [Modifier l'ordre des documents](reorder.md)
- [Utiliser l'INDEX](../02-reading/index-panel.md)
