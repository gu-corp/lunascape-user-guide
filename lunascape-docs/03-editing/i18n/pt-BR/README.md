# Editar um documento

Os documentos podem ser editados diretamente no visualizador. A tela de edição tem uma exibição visual, em que você edita o que vê, e uma exibição do código-fonte Markdown; um único botão alterna entre as duas.

## Começar a editar

Pressione uma das opções a seguir. Todas abrem a mesma tela de edição.

- [Editar], no canto inferior direito do texto
- [⋯] (mais ações), no canto superior direito do texto → [Editar]
- Menu do item no INDEX → [Editar]

## Editar

1. Edite o texto diretamente.
   Na barra de ferramentas, na parte superior da tela de edição, você pode usar o formato de parágrafo (corpo do texto, títulos 1 a 4, citação, código), [Negrito], [Itálico], [Lista com marcadores], [Lista numerada], [Link], [Inserir tabela], [Tamanho da imagem], [Desfazer] e [Refazer].
2. Para editar o código-fonte Markdown diretamente, pressione [Markdown].
   Pressione novamente para voltar à exibição visual. A última exibição usada é memorizada e restaurada na próxima vez que você pressionar [Editar].
3. Pressione [Salvar].
   O conteúdo é gravado no arquivo Markdown e o visualizador volta ao modo de leitura. Para desistir, pressione [Cancelar].

> **Nota**
>
> - Salvar apenas grava o arquivo. O preparo (staging) e o commit no Git nunca são automáticos.
> - As fórmulas matemáticas e os diagramas, como Mermaid, TikZ e Vega-Lite, aparecem renderizados na exibição visual. Para alterar o conteúdo, mude para [Markdown].
> - Documentos que contenham sintaxe específica de MDX (componentes, `import` e assim por diante) são editados somente na exibição Markdown, para preservar essa sintaxe.
> - O front matter (o bloco delimitado por `---` no início) é mantido mesmo quando você edita na exibição visual.

> **Dica**
>
> - [Abrir no VS Code] abre o arquivo no editor de texto comum. Ao salvar no editor de texto, a exibição do visualizador é atualizada automaticamente.
> - Para ocultar o botão [Editar], desative [Botão de edição] em [Configurações de exibição]. Para ocultá-lo em todo o projeto, defina `editor.showEditButton` como `false` no `lunascape-docs.json`.
> - A exibição inicial padrão (visual ou Markdown) pode ser alterada na configuração `lunascapeDocEditor.editor.defaultMode` ou em `editor.defaultMode` no `lunascape-docs.json`.

## Tópicos relacionados

- [Criar e organizar documentos e pastas](organize.md)
- [Ajustar o tamanho das imagens](images.md)
- [Escrever fórmulas matemáticas](math.md)
- [Criar diagramas e gráficos](diagrams.md)
