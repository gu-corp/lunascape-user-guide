# Sécurité et limites d'écriture

Les limites que Lunascape Docs maintient pour protéger vos documents et votre appareil.

## Affichage

- Le HTML généré à partir du Markdown et le SVG généré à partir des figures sont assainis avec DOMPurify 3.4.14 avant d'être affichés.
- Les scripts arbitraires contenus dans le MDX ne sont jamais exécutés.
- KaTeX s'exécute avec `trust: false`, `maxSize: 50` et `maxExpand: 1000`, et ne fait confiance ni au HTML externe ni aux commandes arbitraires.
- Les bibliothèques de rendu Markmap, WaveDrom, Svgbob, Vega-Lite et Penrose sont chargées localement, dans des versions figées, uniquement lorsque le bloc correspondant est présent. Les références à des ressources externes, le HTML brut et les notations exécutables ne sont pas autorisés ; les scripts, les images externes, `link`, `style` et `foreignObject` sont retirés du SVG généré.
- Le rendu TikZ ne lance jamais le LaTeX de l'hôte : il s'exécute séquentiellement dans un processus de travail TeX en WebAssembly doté d'un système de fichiers en mémoire, avec des limites d'entrée, de file d'attente, de mémoire, de temps d'exécution (15 secondes) et de sortie SVG, et rejette les instructions d'entrée-sortie sur fichier.

## Accès aux documents et aux fichiers

- Les liens des documents et les opérations sur les fichiers ne peuvent pas sortir de la racine de documentation.
- La création, le renommage, le déplacement et la suppression depuis l'INDEX sont revérifiés côté extension — racine de documentation, version de l'INDEX, chemin du document de référence, type de la cible, limites des liens symboliques et documents non enregistrés — avant d'être appliqués. Les demandes provenant d'un menu obsolète ou d'une autre racine de documentation ne sont pas appliquées.
- Les opérations de modification de l'INDEX sont désactivées pendant l'édition d'un document ou pendant l'application d'une autre opération sur l'INDEX.
- La création à partir d'un modèle revérifie, après l'aperçu, l'approbation de l'espace de travail, l'identité de la racine de documentation, la version de l'INDEX, le Standard Pack et le contenu généré, la destination et les limites des liens symboliques. Elle n'écrase jamais un fichier existant et ne crée jamais un contenu différent de l'aperçu ni un résultat dépassant 4 Mio.
- L'enregistrement d'un fichier de configuration vérifie sa version juste avant l'écriture et s'interrompt si une modification externe est détectée.

## Envoi vers l'extérieur

- Les documents ne sont jamais envoyés à l'extérieur pour la consultation, l'édition ou la vérification. La vérification des documents s'exécute localement et de façon déterministe.
- Seule la traduction (traduction de cette page, traduction groupée) envoie des documents à un modèle de langage, après avoir indiqué la destination et l'étendue de l'envoi, et uniquement avec une approbation explicite. <!-- ai-only -->
- Les propositions de traduction sont présentées sous forme de différences ; les versions du document de référence et de la cible sont revérifiées, et une proposition n'est appliquée que si une personne l'enregistre explicitement. <!-- ai-only -->
- L'outil de spécification destiné aux agents IA ne renvoie ni le contenu des documents, ni les noms d'espace de travail, ni les chemins locaux. <!-- ai-only -->

## Git

- L'enregistrement se limite à l'écriture du fichier. Aucune fonction n'effectue automatiquement d'indexation ni de commit dans Git.
- Les fichiers existants tels que `_meta.json` ne sont jamais supprimés ni modifiés en silence. Les traductions orphelines ne sont jamais supprimées ni déplacées automatiquement.

## Voir aussi

- [Principales spécifications](README.md)
- [Utilisation depuis une IA](ai-agents.md)
