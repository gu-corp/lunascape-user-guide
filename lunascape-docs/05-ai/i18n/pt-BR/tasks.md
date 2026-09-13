# Trabalhos disponíveis

Escolha em [Trabalho] na aba [IA]. Cada trabalho muda a instrução entregue e a verificação feita em seguida.

| Trabalho | Conteúdo | Requisitos | Tipo de API |
|---|---|---|---|
| Traduzir esta página | Traduz o documento exibido para o idioma escolhido | O documento aberto, um idioma de destino | ○ |
| Traduzir o que falta | Traduz, em ordem, os documentos sem tradução e desatualizados do idioma escolhido | Um idioma de destino | Somente sessão |
| Revisar esta página | Verifica e corrige a terminologia, o estilo e as seções exigidas pelo padrão de documentos | O documento aberto | ○ |
| Criar um documento | Cria um documento seguindo o padrão de documentos e seus modelos | Um assunto (opcional) | Somente sessão |

## O que a instrução contém

| Nº | Conteúdo |
|---|---|
| 1 | A raiz da documentação, com a instrução de não alterar nada fora dela |
| 2 | O idioma padrão (canônico) e o local das traduções (a pasta `i18n/<idioma>/` ao lado do documento) |
| 3 | Que `navigation.order` pertence apenas ao documento canônico e que uma tradução só pode sobrescrever `navigation.title` |
| 4 | Que os IDs de requisito, os links, o código, o Mermaid, o TeX e a estrutura do front matter não devem ser alterados |
| 5 | O padrão de documentos e o glossário (`terminology` em `docs-lint.config.json`) |
| 6 | Executar a verificação de documentos ao terminar, relatar os arquivos alterados e não realizar operações no Git |

> **Dica**
>
> Os alvos de "Traduzir o que falta" vêm do registro, até 200 documentos por execução. Execute novamente para os demais.

## Tópicos relacionados

- [Entregar trabalho a uma IA](README.md)
- [O registro e seus dados](ledger.md)
