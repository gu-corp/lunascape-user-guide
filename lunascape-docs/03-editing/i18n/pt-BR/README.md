# Editar um documento

Os documentos podem ser editados diretamente no visualizador. A tela de edição tem uma "exibição visual", em que você edita o que vê, e uma "exibição do código-fonte Markdown"; um único botão alterna entre elas.

## Começar a editar

Pressione qualquer uma das opções a seguir. Todas abrem a mesma tela de edição.

- [Editar], no canto inferior direito do documento
- [⋯] (Mais ações), no canto superior direito do documento → [Editar]
- Menu do item no INDEX → [Editar]

## Editar

1. Edite o texto diretamente.
   Na barra de ferramentas, no topo da tela de edição, você pode usar o formato de parágrafo (corpo, títulos 1 a 4, citação, código), [Negrito], [Itálico], [Lista com marcadores], [Lista numerada], [Link], [Inserir tabela], [Tamanho da imagem], [Desfazer] e [Refazer].
2. Quando quiser editar o código-fonte Markdown diretamente, pressione [Markdown].
   Pressione novamente para voltar à exibição visual. A última exibição usada é memorizada e restaurada na próxima vez que você pressionar [Editar].
3. Pressione [Salvar] (você também pode salvar com Ctrl+S / ⌘S).
   O conteúdo é gravado no arquivo Markdown e o visualizador volta ao modo de leitura. Para parar de editar e voltar ao último conteúdo salvo, pressione [Descartar edições].

## Começar sempre pela tela de edição (modo de edição)

Pressione [Modo de edição] na barra de ferramentas para ativá-lo: a partir daí, cada documento começa pela tela de edição. Use quando estiver escrevendo continuamente, como em um bloco de notas.

- Enquanto estiver ativo, pressionar [Salvar] não fecha a tela de edição. [Descartar edições] volta ao último conteúdo salvo e mantém a tela de edição aberta.
- Pressione novamente para desativá-lo e voltar ao modo de leitura. O estado ativado/desativado é memorizado para cada usuário.
- Não aparece em uma raiz da documentação que não pode ser gravada (como uma fonte somente leitura do GitHub).

## Edições não salvas

As edições que você não salvou são mantidas automaticamente neste dispositivo. Elas não se perdem ao ir para outro documento, nem ao fechar a aba ou a janela.

- [Não salvo], na tela de edição, indica que há diferenças em relação ao último conteúdo salvo.
- Na próxima vez que você abrir o mesmo documento, ele retoma a partir das edições mantidas e avisa isso. Se o documento original tiver sido atualizado desde então, também avisa. Use [Descartar edições] para voltar ao conteúdo mais recente.
- As edições mantidas desaparecem com [Salvar] ou [Descartar edições]. Como não foram salvas, elas não aparecem no Git nem entre os rascunhos.

> **Nota**
>
> - Salvar apenas grava o arquivo. O preparo (staging) e o commit no Git nunca são feitos automaticamente.
> - Fórmulas e diagramas como Mermaid, TikZ e Vega-Lite são mostrados com o resultado renderizado na exibição visual. Para alterar o conteúdo deles, alterne para [Markdown].
> - Documentos que contêm sintaxe específica de MDX (componentes, `import` e afins) são editados somente na exibição Markdown, para preservar essa sintaxe.
> - O front matter (as configurações delimitadas pelos `---` no início) é preservado mesmo quando você edita na exibição visual.

> **Dica**
>
> - Ao pressionar [Abrir no VS Code], o arquivo é aberto no editor de texto comum. Ao salvar no editor de texto, a exibição do visualizador também é atualizada automaticamente.
> - Quando não quiser exibir o botão [Editar], desative [Botão de edição] em [Configurações de exibição]. Para ocultá-lo no projeto inteiro, defina `editor.showEditButton` como `false` em `lunascape-docs.json`.
> - O padrão da exibição inicial (visual ou Markdown) pode ser alterado na configuração `lunascapeDocEditor.editor.defaultMode` ou em `editor.defaultMode` no `lunascape-docs.json`.

## Consulte também

- [Criar e organizar documentos e pastas](organize.md)
- [Ajustar o tamanho das imagens](images.md)
- [Escrever fórmulas](math.md)
- [Escrever diagramas e gráficos](diagrams.md)
