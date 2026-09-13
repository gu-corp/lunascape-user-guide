# Les figures, formules ou images ne s'affichent pas

## Une figure TikZ s'affiche sous forme de source repliée

- L'extension distribuée n'intègre pas de moteur de rendu TikZ. Cet affichage est normal.
- À des fins de développement ou d'évaluation, installez `node-tikzjax` 1.0.5 à la racine d'un espace de travail approuvé et réglez le paramètre `lunascapeDocEditor.tikz.runtime` sur `workspace` pour obtenir le rendu.
- La version navigateur Web n'effectue pas le rendu de TikZ.

## Les formules s'affichent en texte brut

- Vérifiez les délimiteurs : `$...$` ou `\(...\)` en ligne, `$$...$$` ou `\[...\]` pour une formule isolée.
- Un `$` placé dans du code en ligne ou dans un bloc de code ne devient jamais une formule.
- Une écriture qui ressemble à un montant, comme `$5 and $10`, n'est pas traitée comme une formule.
- Les formules très volumineuses ou comportant de nombreuses expansions de macros ne sont pas rendues au-delà des limites (`maxSize: 50`, `maxExpand: 1000`). Découpez-les.

## Une figure indique qu'elle ne peut pas être rendue

- Les messages d'erreur de Mermaid, Vega-Lite, WaveDrom et autres signalent le problème de syntaxe. Vérifiez la source dans l'écran d'édition avec [Markdown].
- Vega-Lite : intégrez les données dans `data.values` ou `datasets`. Les données provenant d'une URL externe et les marques d'image ne peuvent pas être utilisées.
- WaveDrom : écrivez du JSON strict. La forme JavaScript (clés sans guillemets, etc.) ne peut pas être utilisée.
- Penrose : n'utilisez que `@preset set-theory` en tête et les instructions autorisées (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- « Le SVG généré contient des références non sécurisées » / « Le SVG généré dépasse la limite » : les figures qui référencent des ressources externes, ou qui sont trop volumineuses, ne sont pas affichées. Réduisez leur contenu ou supprimez les références.

## Une image ne s'affiche pas

- Le chemin d'une image est relatif au document. Les images situées hors de la racine de documentation ne s'affichent pas.
- L'attribut `width` d'une balise `<img>` n'accepte qu'un nombre (`width="360"`).

## Les figures manquent sur le site Web exporté

Les bibliothèques de rendu de TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob et Penrose sont chargées au moment de l'affichage. Déployez également le dossier `vendor/` avec le site exporté.

## Voir aussi

- [Écrire des formules](../03-editing/math.md)
- [Écrire des figures et des graphiques](../03-editing/diagrams.md)
- [Ajuster la taille des images](../03-editing/images.md)
