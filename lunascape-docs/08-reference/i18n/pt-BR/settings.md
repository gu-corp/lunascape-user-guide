# Configurações do VS Code

Pesquise "Lunascape Docs" nas configurações do VS Code (`⌘,` / `Ctrl+,`) para alterar os itens a seguir. Todos são configurações de cada usuário e não são salvos nos documentos do projeto.

## Raiz da documentação

| Configuração | Valores | Padrão | Função |
|---|---|---|---|
| `lunascapeDocEditor.rootMode` | `auto` / `fixed` | `auto` | `auto` escolhe automaticamente a raiz da documentação mais próxima do Markdown aberto e, se ele não pertencer a nenhuma, abre temporariamente a pasta superior. `fixed` abre sempre a raiz da documentação indicada em `root` |
| `lunascapeDocEditor.rootDirectoryNames` | Matriz de textos | `["docs"]` | Nomes de pasta descobertos automaticamente como raiz da documentação no modo `auto`. Uma pasta com `lunascape-docs.json` é descoberta independentemente do nome. Quando o `lunascape-docs.json` na raiz do repositório tem `defaultFolder` ou `roots`, esses valores têm prioridade |
| `lunascapeDocEditor.root` | Caminho | `docs` | A raiz da documentação relativa ao espaço de trabalho, usada no modo `fixed` ou ao abrir pelo comando |
| `lunascapeDocEditor.startPage` | Caminho | `README.md` | A página inicial relativa à raiz da documentação |
| `lunascapeDocEditor.title` | Texto | `Lunascape Docs` | Substitui o título da guia do documento. Não afeta o nome exibido na seleção da raiz da documentação |
| `lunascapeDocEditor.ignoredDirectories` | Matriz de textos | `["99-archive"]` | Nomes de pasta excluídos do INDEX |

## Exibição

| Configuração | Valores | Padrão | Função |
|---|---|---|---|
| `lunascapeDocEditor.appearance` | `light` / `auto` | `light` | `light` usa fundo branco; `auto` acompanha o tema de cores do VS Code |
| `lunascapeDocEditor.locale` | Marca de idioma | Nenhum | O idioma do documento que você prefere, usado quando estiver disponível. Não altera o idioma canônico do projeto |
| `lunascapeDocEditor.documentMetadata.compact` | Booleano | `true` | Recolhe a tabela de controle do documento logo após o H1 na linha "Informações do documento" |
| `lunascapeDocEditor.tree.showFileNames` | Booleano | `false` | Mostra os nomes de arquivo no INDEX em vez dos nomes dos documentos |
| `lunascapeDocEditor.tree.showDocumentIcons` | Booleano | `false` | Mostra os ícones de documento no INDEX |
| `lunascapeDocEditor.tree.showFolderIcons` | Booleano | `false` | Mostra os ícones de pasta no INDEX |
| `lunascapeDocEditor.tree.showItemCounts` | Booleano | `false` | Mostra no INDEX o número de itens diretamente dentro de cada pasta |
| `lunascapeDocEditor.tree.showGuides` | Booleano | `true` | Mostra as linhas-guia dos níveis no INDEX |
| `lunascapeDocEditor.tree.density` | `comfortable` / `compact` | `comfortable` | O espaçamento entre as linhas do INDEX |
| `lunascapeDocEditor.tree.autoHideSingleItem` | Booleano | `true` | Fecha o INDEX apenas na primeira vez, quando há um só documento |

## Edição

| Configuração | Valores | Padrão | Função |
|---|---|---|---|
| `lunascapeDocEditor.editor.defaultMode` | `visual` / `source` | `visual` | A exibição de edição usada enquanto você ainda não alternou. A última exibição usada tem prioridade |
| `lunascapeDocEditor.editor.showEditButton` | Booleano | `true` | Mostra [Editar] no canto inferior direito do texto |

## Diagramas

| Configuração | Valores | Padrão | Função |
|---|---|---|---|
| `lunascapeDocEditor.tikz.runtime` | `bundled` / `workspace` / `disabled` | `bundled` | O runtime de desenho do TikZ. `bundled` usa o runtime aprovado que acompanha o produto (não incluído na versão distribuída atual), `workspace` usa o `node-tikzjax` 1.0.5 na raiz de um espaço de trabalho confiável (apenas para desenvolvimento e avaliação) e `disabled` não desenha nada |

## Configurações obsoletas

| Configuração | Use em vez dela |
|---|---|
| `lunascapeDocEditor.defaultLocale` | `defaultLocale` do `lunascape-docs.json` |
| `lunascapeDocEditor.locales` | `locales` do `lunascape-docs.json` |

Não é possível substituir os idiomas do projeto pelas suas configurações pessoais.

## Tópicos relacionados

- [Alterar as configurações de exibição](../02-reading/display-settings.md)
- [Configuração do projeto](../04-document-tools/project-configuration.md)
