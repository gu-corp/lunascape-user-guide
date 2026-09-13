# A verificação, a criação ou a tradução não funciona

## Verificação

### Aparece "docs-lint não está disponível"

- O ambiente de execução do docs-lint não está incluído na extensão ou há um problema na configuração. Reinstale a extensão.
- "Para carregar o Pack local e as configurações com segurança, confie neste espaço de trabalho no VS Code": para usar um Standard Pack local, é necessário um espaço de trabalho confiável.

### O resultado continua como "nova verificação necessária"

Ao alterar um documento ou uma configuração, o resultado anterior deixa de valer. Pressione [Verificar a raiz da documentação] novamente. Alterações não salvas não são consideradas.

### Pressionar uma indicação não abre nada

Os itens de "raiz da documentação inteira" não estão vinculados a um documento específico e, por isso, não têm posição. Verifique os documentos correspondentes conforme o conteúdo da indicação.

### Não é possível salvar as regras

- É necessário um espaço de trabalho confiável.
- "As configurações do Lint foram alteradas por outra operação": o arquivo `docs-lint.config.json` foi alterado externamente. Carregue o estado mais recente e tente de novo.
- Não é possível editar links simbólicos nem arquivos de configuração fora da raiz da documentação.

## Criação a partir de um modelo

- "A visualização do modelo expirou" / "O conteúdo informado foi alterado": pressione [Visualizar] novamente antes de criar.
- "Já existe um documento no destino": arquivos existentes não são substituídos. Indique outro destino.
- O destino precisa de um caminho relativo à raiz da documentação e da extensão `.md` / `.mdx`. Não é possível criar em `i18n`.
- "Confie no espaço de trabalho para criar documentos": confie no espaço de trabalho no VS Code.

<!-- ai-only:start -->
## Tradução

### Não é possível pressionar os botões de tradução

- "A tradução por IA não está ativada nesta raiz da documentação": defina `translation.enabled` como `true` em `lunascape-docs.json`.
- "O idioma padrão do projeto não está definido": salve o idioma padrão em [Alterar as configurações de exibição](../02-reading/display-settings.md).
- "Adicione o idioma de destino aos idiomas compatíveis": acrescente o idioma de destino a `locales`.
- "Nenhum documento canônico a traduzir": você está com uma página traduzida aberta. Mude para a página no idioma padrão.
- A tradução em lote não funciona quando a pasta está aberta temporariamente. Coloque um `lunascape-docs.json` nessa pasta para torná-la uma raiz da documentação.

### A proposta de tradução é recusada ou precisa ser refeita

- "O documento canônico foi alterado. Refaça a proposta de tradução": o documento canônico ou o destino mudou depois que a proposta foi gerada. Traduza novamente.
- Se faltarem identificadores protegidos ou código na resposta do modelo de linguagem, ela não é aceita. O conteúdo da resposta pode ser conferido no painel de saída "Lunascape Docs 翻訳".
- "A tradução em lote processa até 1000 documentos por vez": divida o alcance por pasta ou por seleção explícita.
<!-- ai-only:end -->

## Tópicos relacionados

- [Verificar documentos](../04-document-tools/check.md)
- [Criar um documento a partir de um modelo](../04-document-tools/templates.md)
- [Entregar o trabalho a uma IA](../05-ai/README.md)
