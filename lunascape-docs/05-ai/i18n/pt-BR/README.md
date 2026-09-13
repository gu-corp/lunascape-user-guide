# Entregar tarefas a uma IA

O Lunascape Docs não chama modelos de linguagem. Ele prepara **contexto, ferramentas e verificação**, e deixa a execução da tradução, da revisão e da criação para a IA que você usa.

## A ideia

| O que o produto fornece | Conteúdo |
|---|---|
| Contexto | As convenções da documentação (onde ficam as traduções, o front matter, o padrão de documentos, o glossário) e a localização do documento de destino |
| Ferramentas de trabalho | O registro de documentos sem tradução e desatualizados, a leitura e a escrita de documentos, a criação a partir de modelos |
| Verificação posterior | A verificação pelo docs-lint, a diferença de cobertura e de atualidade |

A instrução não inclui o texto do documento. A própria IA lê os arquivos, escreve e verifica por conta própria.

## Entregar uma tarefa

1. Pressione [Ferramentas de documento] na barra de ferramentas e abra a aba [AI].
2. Em [Tarefa], escolha a tarefa que deseja entregar.
3. Preencha os itens necessários (idioma de destino, assunto).
4. Pressione [Entregar esta tarefa].
   Um terminal do VS Code é aberto, e a IA escolhida recebe a instrução e começa o trabalho.

> **Dica**
>
> A sessão do Claude Code vem acompanhada das ferramentas de trabalho (o servidor MCP `lunascape-docs`). A própria sessão pode obter a lista de documentos sem tradução e desatualizados, executar o docs-lint e registrar a atualidade após a tradução.

## Conferir o resultado

| Tipo de provedor | Destino do resultado |
|---|---|
| De sessão (Claude Code, Codex) | Grava diretamente na árvore de trabalho. **Confira nas diferenças do Git** |
| De API (modelos de linguagem do VS Code, Anthropic, compatíveis com OpenAI) | Retorna uma proposta por documento. Confira em [Abrir diferenças] e grave com [Salvar] |

### Conferir a proposta do tipo de API

Ao executar com um provedor do tipo de API, a proposta chega à aba [AI].

1. Pressione [Abrir diferenças] e veja as diferenças em relação ao conteúdo atual.
2. Se estiver tudo certo, pressione [Salvar]. No caso de uma tradução, a atualidade também é registrada. Para desistir, pressione [Descartar].
   Para interromper a geração no meio, pressione [Parar].

> **Nota**
>
> - O Lunascape Docs nunca faz stage nem commit no Git. Confira as alterações sempre nas diferenças.
> - Não é possível entregar tarefas em um espaço de trabalho não confiável nem na exibição temporária de uma pasta fora da raiz da documentação.

## Tópicos relacionados

- [Tarefas disponíveis](tasks.md)
- [Configurações de IA](settings.md)
- [O registro e seus dados](ledger.md)
