# O registro e seus dados

O registro no topo da aba [IA] mostra o estado da tradução em cada idioma compatível. Ele é útil mesmo sem usar a IA: indica o que está faltando.

| Exibição | Significado |
|---|---|
| Sem tradução | Número de documentos que ainda não têm versão traduzida |
| Desatualizado | Número de documentos cuja tradução existe, mas cujo documento canônico é mais recente que o registro |
| Traduzido | Número de traduções que acompanham o documento canônico |

O registro é calculado percorrendo a raiz da documentação. Nenhuma IA e nenhum modelo de linguagem participa disso.

## Atualizar os registros de tradução

Para determinar o estado "desatualizado", é preciso registrar o documento canônico e a tradução tal como estavam no momento da tradução. Uma IA do tipo sessão grava os arquivos diretamente, portanto o registro não é criado automaticamente.

1. Quando a tradução estiver concluída e você tiver conferido o conteúdo, pressione [Atualizar os registros de tradução].
2. As traduções sem registro passam a constar como correspondentes ao documento canônico atual.

As sessões do Claude Code e os salvamentos pelo tipo API criam o registro automaticamente (a sessão é instruída a usar a ferramenta MCP `record_translation_freshness`). Este botão é necessário quando você traduziu com o Codex ou com o chat do VS Code.

A partir daí, ao alterar um documento canônico, sua tradução passa a aparecer como "desatualizado".

> **Nota**
>
> - As traduções que já têm registro não são sobrescritas, para não apagar um estado "desatualizado" existente.
> - Os registros ficam em `.lunascape-docs/translation-freshness.json` e guardam apenas caminhos relativos, idiomas, hashes do conteúdo e a data e hora — nunca o texto do documento.

## Tópicos relacionados

- [Trabalhos disponíveis](tasks.md)
- [Ler em outro idioma](../02-reading/languages.md)
