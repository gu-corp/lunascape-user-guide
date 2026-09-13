# Uso a partir de agentes de IA

A extensão registra a Language Model Tool somente leitura `lunascape_getDocsSpecification` no VS Code. Quando um agente compatível do VS Code é questionado sobre recursos, configurações ou convenções de documento do Lunascape Docs, ele pode obter o conteúdo desta ajuda (a especificação geral) por meio dessa ferramenta.

## Como usar

Faça a pergunta no chat do VS Code com `#lunascapeDocs`, ou simplesmente pergunte sobre as configurações ou a estrutura de documentos do Lunascape Docs.

```text
#lunascapeDocs Como habilito as traduções em inglês no lunascape-docs.json?
```

## Argumentos da ferramenta

| Argumento | Significado |
|---|---|
| `topic` | A seção a obter: `all`, `usage` (Operações básicas), `structure` (Raízes da documentação e convenções de arquivos), `editing` (Editar um documento), `configuration` (Configuração do projeto), `security` (Segurança e limites de gravação) ou `ai` (Uso a partir de agentes de IA) |
| `locale` | O idioma da ajuda (uma tag de idioma da ajuda incluída, como `ja` ou `en`). Se omitido, é usado o idioma de exibição do VS Code; na falta dele, retorna a ajuda em japonês |

> **Nota**
>
> - A ferramenta nunca envia o conteúdo do documento para lugar algum.
> - A ferramenta nunca retorna nomes de espaço de trabalho nem caminhos locais.
> - A ferramenta nunca modifica arquivos.
> - Ela funciona a partir de agentes compatíveis do VS Code mesmo sem um `AGENTS.md`. Não é compartilhada automaticamente com outros clientes de IA que não usam a API de ferramentas da extensão.

## Tópicos relacionados

- [Mostrar esta ajuda](../02-reading/help.md)
- [Segurança e limites de gravação](security.md)
