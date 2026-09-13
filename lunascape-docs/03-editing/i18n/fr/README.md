# Modifier un document

Les documents se modifient directement dans la visionneuse. L'éditeur propose un affichage visuel, où vous modifiez ce que vous voyez, et un affichage de la source Markdown ; un seul bouton permet de passer de l'un à l'autre.

## Commencer la modification

Appuyez sur l'un des éléments suivants. Ils ouvrent tous le même éditeur.

- [Modifier], en bas à droite du document
- [⋯] (autres actions), en haut à droite du document → [Modifier]
- Le menu de l'élément dans INDEX → [Modifier]

## Modifier

1. Modifiez le texte directement.
   La barre d'outils en haut de l'éditeur propose le format de paragraphe (corps de texte, titres 1 à 4, citation, code), [Gras], [Italique], [Liste à puces], [Liste numérotée], [Lien], [Insérer un tableau], [Taille de l'image], [Annuler] et [Rétablir].
2. Pour modifier directement la source Markdown, appuyez sur [Markdown].
   Appuyez de nouveau pour revenir à l'affichage visuel. Le dernier affichage utilisé est mémorisé et restauré la prochaine fois que vous appuyez sur [Modifier].
3. Appuyez sur [Enregistrer].
   Le fichier Markdown est écrit et la visionneuse revient en mode lecture. Pour abandonner, appuyez sur [Annuler].

> **Remarque**
>
> - L'enregistrement se limite à écrire le fichier. L'indexation et la validation Git ne sont jamais automatiques.
> - Les formules et les figures telles que Mermaid, TikZ et Vega-Lite s'affichent sous leur forme rendue dans l'affichage visuel. Passez à [Markdown] pour en modifier le contenu.
> - Les documents contenant une syntaxe propre à MDX (composants, `import`, etc.) se modifient uniquement dans l'affichage Markdown, afin de préserver cette syntaxe.
> - Le front matter (le bloc délimité par `---` en début de fichier) est conservé lorsque vous modifiez le document dans l'affichage visuel.

> **Astuce**
>
> - [Ouvrir dans VS Code] ouvre le fichier dans l'éditeur de texte habituel. L'enregistrement depuis cet éditeur met à jour automatiquement l'affichage de la visionneuse.
> - Pour masquer le bouton [Modifier], désactivez [Bouton de modification] dans [Paramètres d'affichage]. Pour le masquer dans tout le projet, définissez `editor.showEditButton` sur `false` dans `lunascape-docs.json`.
> - L'affichage initial par défaut (visuel ou Markdown) se règle avec le paramètre `lunascapeDocEditor.editor.defaultMode` ou avec `editor.defaultMode` dans `lunascape-docs.json`.

## Voir aussi

- [Créer et organiser des documents et des dossiers](organize.md)
- [Ajuster la taille des images](images.md)
- [Écrire des formules](math.md)
- [Créer des figures et des graphiques](diagrams.md)
