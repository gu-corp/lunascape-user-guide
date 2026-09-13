# Configurações de IA

Escolha a IA e o modelo que vão receber o trabalho. A escolha é feita nas listas suspensas desta tela, e não na seleção rápida do VS Code.

1. Pressione [Ferramentas de documento] → guia [IA] → [Configurações de IA…].
2. Escolha o [Provedor].
   Os provedores que não podem ser usados neste ambiente aparecem como não selecionáveis, acompanhados do motivo.
3. Escolha o [Modelo]. As opções mudam conforme o provedor.
4. Feche a tela. A escolha é salva por usuário e reutilizada na próxima vez.

## Provedores

| Provedor | Tipo | Forma de detecção |
|---|---|---|
| Claude Code | Sessão | Presença do comando `claude` |
| Codex | Sessão | Presença do comando `codex` |
| Modelos de linguagem do VS Code | API | Modelos registrados na VS Code Language Model API |
| Anthropic API | API | Chave de API registrada |
| API compatível com OpenAI | API | Chave de API e endpoint registrados |

Um provedor de **sessão** lê e grava os arquivos por conta própria e também executa a verificação do documento. Os resultados são gravados diretamente na árvore de trabalho e conferidos no diff do Git.

Um provedor de **API** devolve o Markdown de um documento, e a extensão mostra o diff antes de salvar.

## Registrar uma chave de API

A Anthropic API e as APIs compatíveis com OpenAI ficam disponíveis quando uma chave de API é registrada.

1. Escolha o destino do registro em [Provedor]. O campo da chave de API aparece.
2. Digite a [Chave de API]. No caso da API compatível com OpenAI, digite também o [Endpoint] (por exemplo, `https://api.openai.com/v1`).
3. Pressione [Salvar]. É exibida a mensagem “Chave registrada”.

> **Nota**
>
> - A chave é guardada no SecretStorage do VS Code e não é exibida novamente. Ela também não é gravada em `settings.json` nem em nenhum documento. Use [Excluir chave] para removê-la.
> - A lista de modelos é obtida de cada serviço com a chave registrada. Enquanto isso não é possível, uma lista conhecida é exibida.
> - Um provedor de API executa apenas “Traduzir esta página” e “Revisar esta página”. Para percorrer vários documentos ou criar documentos, use um provedor de sessão.

> **Dica**
>
> Se nenhum provedor for encontrado, instale o Claude Code ou o Codex, ou registre uma chave de API. Ao reabrir [Configurações de IA…], ele é detectado.

## Tópicos relacionados

- [Passar o trabalho para a IA](README.md)
- [Lista de configurações do VS Code](../08-reference/settings.md)
