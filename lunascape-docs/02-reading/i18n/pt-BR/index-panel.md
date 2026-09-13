# Usar o INDEX

O INDEX à esquerda é a árvore de pastas e documentos da raiz da documentação.

## Filtrar

1. Digite uma palavra em [Filtrar documentos], acima do INDEX.
2. Somente os itens cujos nomes correspondem são exibidos. Apague o texto digitado para voltar ao estado anterior.

> **Nota**
>
> Durante a filtragem, não é possível reordenar por arrastar e soltar.

## Expandir e recolher pastas

- Pressione a seta à esquerda do nome da pasta, ou o nome de uma pasta sem página de abertura, para expandi-la ou recolhê-la.
- Uma pasta com página de abertura (um `README.md` ou `index.md` com conteúdo) abre essa página quando você pressiona o nome dela. Para apenas expandir ou recolher, use [Expandir pasta] / [Recolher pasta] no menu do item.
- O estado de expansão das pastas é memorizado por usuário e não é gravado em arquivos versionados no Git.

## O README e a página de abertura da pasta

`README.md` é o arquivo que descreve o conteúdo daquela pasta.

- Ao pressionar o nome de uma pasta que tem README, esse README é exibido.
- Uma pasta sem README exibe o primeiro documento que há dentro dela.
- O título (H1) do README passa a ser o nome daquela pasta no INDEX.

O README não é obrigatório. Para adicioná-lo depois, escolha [Criar um README] no menu do item da pasta (aparece somente em pastas que não têm um).

## Mostrar ou ocultar o INDEX

- O ícone da esquerda, nos controles de colunas da barra de ferramentas, mostra ou oculta o INDEX. O ícone da direita mostra ou oculta "Nesta página".
- Em telas estreitas, o INDEX começa fechado. Pressione [Abrir o INDEX] (três linhas), à esquerda de [Voltar], e o INDEX se abre sobreposto ao documento. Feche-o com o [×] dentro do INDEX, com um clique no fundo, com `Esc` ou ao navegar para outro documento. Essa abertura temporária não altera a configuração das telas largas.
- Em uma raiz da documentação com apenas um documento a exibir, o INDEX se fecha automaticamente na primeira vez. Reabra-o com o ícone de colunas. Esse comportamento pode ser desativado em [Configurações de exibição], na opção [Ocultar automaticamente se houver apenas um documento].

## Usar o menu do item

Passe o mouse sobre um item do INDEX para exibir [⋯], ou clique nele com o botão direito, para abrir o menu daquele item. Os itens aparecem nesta ordem.

| Grupo | Itens |
|---|---|
| Ações frequentes | [Expandir pasta] / [Recolher pasta], [Abrir o INDEX] (abrir a página de abertura da pasta), [Editar], [Alterar o título], [Abrir no VS Code], [Copiar o caminho] |
| Criar e organizar | [Criar um README] (somente pastas sem README), [Novo documento], [Nova pasta], [Duplicar], [Alterar o nome do arquivo] / [Alterar o nome da pasta], [Mover para cima], [Mover para baixo] |
| Excluir | [Mover para a lixeira] |

- Para criar diretamente na raiz da documentação, use o [⋯] na extremidade direita do cabeçalho do INDEX, ou clique com o botão direito em uma área vazia do INDEX, e escolha [Novo documento] ou [Nova pasta]. No mesmo menu ficam [Alterar o nome do documento] e, se a raiz da documentação não tiver README, [Criar um README]. Clicar com o botão direito no nome do documento exibido na barra de ferramentas também abre esse mesmo menu.
- Dentro do menu, `↑` `↓` movem entre os itens e `Home` `End` levam ao primeiro e ao último. Ao fechar com `Esc`, o foco volta para onde estava antes da abertura.

> **Nota**
>
> Os itens de criar, organizar e excluir só aparecem quando o espaço de trabalho é confiável no VS Code. Eles também ficam indisponíveis enquanto um documento está sendo editado ou enquanto outra operação do INDEX está em andamento.

## Alterar a aparência

Em [Configurações de exibição] é possível alterar a exibição dos nomes de arquivo, os ícones de documentos e pastas, a contagem de itens nas pastas, as linhas-guia de hierarquia e a densidade de exibição. Para saber mais, consulte [Alterar as configurações de exibição](display-settings.md).

## Tópicos relacionados

- [Criar e organizar documentos e pastas](../03-editing/organize.md)
- [Alterar a ordem dos documentos](../03-editing/reorder.md)
