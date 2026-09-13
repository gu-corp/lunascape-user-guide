# Écrire des formules

Les formules s'écrivent en notation TeX et sont rendues sur l'appareil par KaTeX. Aucun accès réseau n'est utilisé.

## Notation

| Type | Délimiteurs | Exemple |
|---|---|---|
| Formule en ligne (dans une phrase) | `$...$` ou `\(...\)` | `La relation entre masse et énergie s'écrit $E = mc^2$.` |
| Formule hors ligne (sur une ligne isolée) | `$$...$$` ou `\[...\]` | Voir ci-dessous |

```markdown
$$
\frac{d}{dx}\left(\int_{a}^{x} f(t)\,dt\right) = f(x)
$$
```

- Aucune espace n'est nécessaire autour des délimiteurs. Une formule directement accolée à du texte japonais, comme `値は$V=-H$である`, est reconnue.
- Un `$` placé dans du code en ligne ou dans un bloc de code n'est pas traité comme une formule : il s'affiche tel quel.
- Une écriture ressemblant à un montant, comme `$5 and $10`, n'est pas traitée comme une formule.

## Modifier

Dans l'affichage visuel, les formules apparaissent sous leur forme rendue. Pour en modifier le contenu, appuyez sur [Markdown] dans l'écran d'édition et modifiez la source. L'enregistrement depuis l'affichage visuel conserve la source TeX et la forme d'origine des délimiteurs (`$` ou `\(`).

> **Remarque**
>
> - Par sécurité, KaTeX fonctionne avec `trust: false` et limite la taille (`maxSize: 50`) ainsi que le nombre d'expansions de macros (`maxExpand: 1000`). Les formules qui dépassent ces limites ne sont pas rendues.
> - Dans un document existant, un `tikzpicture` écrit à l'intérieur de `$$...$$` ou de `\[...\]` est reconnu comme une figure TikZ et non comme une formule.

## Rubriques associées

- [Écrire des figures et des graphiques](diagrams.md)
- [Les figures, les formules ou les images ne s'affichent pas](../07-troubleshooting/rendering.md)
