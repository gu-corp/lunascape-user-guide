# Salvar rascunhos

Quando você edita um documento na versão Web, as alterações não são gravadas no repositório: elas ficam guardadas no navegador como um “rascunho”.

## Criar um rascunho

1. Abra um documento e pressione [Editar], no canto inferior direito.
2. Faça a edição e pressione [Salvar].
   Aparece “Salvo como rascunho” e a alteração fica guardada no navegador.

- Os documentos com rascunho recebem um selo no INDEX. Acima do texto, aparece “Este documento é um rascunho neste dispositivo (não publicado)”.
- [Rascunhos], na barra de ferramentas, mostra a quantidade; ao pressionar, a lista de rascunhos é aberta.

## Descartar um rascunho

- Para descartar o rascunho de um documento, pressione [Descartar o rascunho], acima do texto.
- Para descartar todos, use a lista de rascunhos.

## Aplicar ao repositório

A “solicitação de publicação”, que envia os rascunhos como Pull Request, está implementada, mas não está ativa no visualizador público. Para aplicar as alterações ao repositório, edite pela versão VS Code ou em um clone local.

> **Nota**
>
> - Os rascunhos ficam guardados no navegador (IndexedDB). Eles não passam para outro navegador nem para outro dispositivo, e são apagados quando você limpa os dados do site no navegador.
> - Se o documento no repositório for atualizado depois que você criou o rascunho, aparece “O documento de origem foi atualizado”. Confira o conteúdo e decida se descarta o rascunho ou se continua com ele.
> - Ao editar uma pasta local aberta por [Abrir documentos], as alterações são salvas diretamente no arquivo, se o navegador tiver suporte a isso. Em navegadores sem suporte, elas são mantidas apenas durante a sessão.

## Tópicos relacionados

- [O que você pode fazer na versão Web](README.md)
- [Editar um documento](../03-editing/README.md)
