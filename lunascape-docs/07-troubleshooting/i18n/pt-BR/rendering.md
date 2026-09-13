# Diagramas, fórmulas matemáticas e imagens não aparecem

## Um diagrama TikZ aparece como código recolhido

- A extensão distribuída não inclui o mecanismo de desenho do TikZ. Essa exibição é normal.
- Para fins de desenvolvimento e avaliação, instale o `node-tikzjax` 1.0.5 na raiz de um espaço de trabalho confiável e defina a configuração `lunascapeDocEditor.tikz.runtime` como `workspace`.
- Na versão para navegador web, o TikZ não é desenhado.

## As fórmulas matemáticas aparecem como texto comum

- Verifique os delimitadores. Em linha, use `$...$` ou `\(...\)`; em bloco, use `$$...$$` ou `\[...\]`.
- Um `$` dentro de código em linha ou de um bloco de código não vira fórmula matemática.
- Escritas com aparência de valores monetários, como `$5 and $10`, não são tratadas como fórmulas matemáticas.
- Fórmulas muito grandes ou com muitas expansões de macro não são desenhadas quando ultrapassam os limites (`maxSize: 50`, `maxExpand: 1000`). Divida-as.

## O diagrama exibe "não é possível desenhar"

- As mensagens de erro do Mermaid, do Vega-Lite, do WaveDrom e de outros indicam o problema de sintaxe. Verifique o código na tela de edição, em [Markdown].
- Vega-Lite: incorpore os dados em `data.values` ou `datasets`. Dados em URL externa e marcas de imagem não podem ser usados.
- WaveDrom: escreva em JSON estrito. O formato JavaScript (chaves sem aspas, por exemplo) não pode ser usado.
- Penrose: use apenas o `@preset set-theory` no início e as instruções permitidas (`Set`, `Subset`, `Disjoint`, `Intersecting`, `AutoLabel All`).
- "O SVG gerado contém referências não seguras" / "O SVG gerado ultrapassa o limite": diagramas que contêm referências a recursos externos, ou grandes demais, não são exibidos. Reduza o conteúdo ou remova as referências.

## A imagem não aparece

- Indique o caminho da imagem como um caminho relativo ao documento. Imagens fora da raiz da documentação não são exibidas.
- Em `width` de `<img>`, indique apenas o número (`width="360"`).

## Os diagramas não aparecem no site publicado

As bibliotecas de desenho do TikZ, do Vega-Lite, do Markmap, do WaveDrom, do Svgbob e do Penrose são carregadas no momento da exibição. Coloque também a pasta `vendor/` junto com o site publicado.

## Itens relacionados

- [Escrever fórmulas matemáticas](../03-editing/math.md)
- [Escrever diagramas e gráficos](../03-editing/diagrams.md)
- [Ajustar o tamanho das imagens](../03-editing/images.md)
