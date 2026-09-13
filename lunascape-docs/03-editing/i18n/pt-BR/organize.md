# Criar e organizar documentos e pastas

No menu de item do INDEX é possível criar, duplicar, renomear e excluir documentos e pastas. A entrada de dados acontece em uma pequena caixa de diálogo dentro do visualizador, sem interromper a leitura.

> **Nota**
>
> Essas ações só estão disponíveis quando o espaço de trabalho é confiável no VS Code. Elas não podem ser executadas enquanto um documento está sendo editado, enquanto outra operação está em andamento ou quando o item de destino tem alterações não salvas.

## Criar um documento ou uma pasta

1. Abra o menu de item ([⋯] ou clique com o botão direito) da pasta de destino.
   Para criar diretamente na raiz da documentação, use o [⋯] na extremidade direita do título do INDEX ou clique com o botão direito em uma área vazia do INDEX.
2. Escolha [Novo documento] ou [Nova pasta].
3. Digite um nome e pressione [Criar].
   O nome do documento precisa de uma extensão Markdown (`.md`, `.markdown`, `.mdx` etc.).

Os novos documentos são criados como documentos do idioma padrão (documentos canônicos).

## Duplicar um documento

1. Abra o menu de item do documento e escolha [Duplicar].
2. Digite um novo nome e pressione [Criar].

Somente o documento canônico é duplicado; as traduções não são.

## Alterar o título

Altera o título do documento (H1). O nome do arquivo permanece o mesmo.

1. Abra o menu de item de um documento ou de uma pasta e escolha [Alterar o título].
2. Digite o novo título em uma única linha e pressione [Alterar].

No caso de uma pasta, o título do `README.md` dela é alterado. Quando uma tradução está sendo exibida, o título do documento desse idioma é alterado.

## Alterar o nome do documento

Altera o nome do documento exibido na barra de ferramentas (o nome da raiz da documentação).

1. Clique com o botão direito no nome do documento na barra de ferramentas. O [⋯] na extremidade direita do título do INDEX abre o mesmo menu.
2. Escolha [Alterar o nome do documento] e digite um novo nome.

Enquanto nada estiver configurado, o nome da pasta é exibido como está.

O nome definido é gravado **no local que atualmente fornece o nome do documento**, para que um título visível nunca acabe sendo ignorado.

| Situação atual | Gravado em |
|---|---|
| `lunascape-docs.json` contém um nome | `lunascape-docs.json` é atualizado |
| Não há nome, mas a raiz da documentação tem um README | O título (H1) do README é reescrito |
| Nenhum dos dois | `lunascape-docs.json` é criado e o nome é salvo nele |

A mensagem exibida após a alteração indica em qual deles a gravação foi feita.

> **Dica**
>
> O nome do documento é determinado nesta ordem: o nome em `lunascape-docs.json`, depois o título do README da raiz da documentação e, por fim, o nome da pasta.

## Alterar o nome de um arquivo ou de uma pasta

1. Abra o menu de item e escolha [Alterar o nome do arquivo] ou [Alterar o nome da pasta].
2. Digite o novo nome e pressione [Alterar].

As traduções correspondentes (o mesmo caminho em `i18n/<idioma>/`) são renomeadas junto.

## Excluir

1. Abra o menu de item e escolha [Mover para a lixeira].
2. Verifique o conteúdo da mensagem de confirmação e aprove a movimentação.

O item é movido para a lixeira do sistema operacional, portanto pode ser restaurado se necessário. As traduções não são excluídas e permanecem onde estão.

## Nomes que não podem ser usados

- Nomes que começam com `.` (eles não apareceriam no INDEX)
- `i18n` (reservado para arquivos de tradução)
- Nomes reservados pelo Windows (`CON`, `PRN` etc.)
- Nomes terminados em ponto ou espaço
- Nomes com caracteres de controle ou caracteres não permitidos em nomes de arquivo
- Nomes que já existem na mesma pasta (inclusive nomes que diferem apenas em maiúsculas e minúsculas)

> **Nota**
>
> A página inicial (normalmente o `README.md` da raiz) não pode ser renomeada nem movida. Altere antes o `startPage` em `lunascape-docs.json`.

## Tópicos relacionados

- [Alterar a ordem dos documentos](reorder.md)
- [Usar o INDEX](../02-reading/index-panel.md)
