# Não é possível editar, salvar ou reordenar

## Não há o botão [Editar]

- O [Botão de edição] em [Configurações de exibição] está desativado. Ative-o ou use [⋯] → [Editar] no canto superior direito do documento, ou o menu do item no INDEX → [Editar].
- O mesmo vale quando `editor.showEditButton` em `lunascape-docs.json` está definido como `false`.
- Não é possível editar enquanto a Ajuda está aberta. Feche a Ajuda.

## Não é possível alternar para a exibição visual

«Este documento contém sintaxe MDX e não pode ser aberto na tela de edição normal»: documentos que contêm sintaxe específica do MDX (componentes, `import` e afins) são editados somente na exibição Markdown, para preservar essa sintaxe.

## Não é possível editar diretamente fórmulas matemáticas ou diagramas

A exibição visual mostra o resultado renderizado. Na tela de edição, pressione [Markdown] e edite o código-fonte.

## Não é possível reordenar ou arrastar

- Não é possível reordenar durante a filtragem, durante a edição de um documento nem enquanto outra operação do INDEX está em andamento.
- Quando o espaço de trabalho não é confiável, as ações de criar, organizar e excluir ficam indisponíveis. Torne o espaço de trabalho confiável no VS Code.
- «O INDEX foi atualizado. Arraste novamente»: outra alteração acabou de ser aplicada. Repita a operação.
- A página inicial (o `README.md` da raiz) não pode ser movida.

## Aparece a mensagem «Há alterações não salvas»

O arquivo em questão está sendo editado no editor do VS Code. Salve ou descarte as alterações primeiro e tente novamente.

## Não é possível renomear

Os nomes a seguir não podem ser usados.

- Nomes que começam com `.`, `i18n` e nomes reservados do Windows (`CON` e afins)
- Nomes terminados em ponto ou espaço e nomes que contêm caracteres de controle ou caracteres não permitidos em nomes de arquivo
- Nomes que já existem na mesma pasta (incluindo nomes que diferem apenas por maiúsculas e minúsculas)
- Nomes de documento sem uma extensão Markdown

## Salvei, mas as alterações não aparecem no Git ou não são confirmadas

O Lunascape Docs apenas grava o arquivo; ele não faz o preparo (staging) nem o commit no Git. Verifique na exibição de Controle do Código-Fonte do VS Code e faça o commit conforme necessário.

## Tópicos relacionados

- [Editar um documento](../03-editing/README.md)
- [Criar e organizar documentos e pastas](../03-editing/organize.md)
- [Alterar a ordem dos documentos](../03-editing/reorder.md)
