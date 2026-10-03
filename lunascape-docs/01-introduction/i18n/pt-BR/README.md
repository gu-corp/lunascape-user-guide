# O que é o Lunascape Docs

O Lunascape Docs é uma ferramenta que trata os documentos Markdown de um repositório Git como um “site de especificações”, do jeito que estão. Não é preciso build prévio, servidor de documentos nem banco de dados dedicado.

## O que você pode fazer

| Objetivo | Principais recursos |
|---|---|
| Ler | INDEX (sumário), links no texto, trilha de navegação, voltar/avançar, sumário da página, busca com filtro |
| Visualizar | Tabelas, blocos de código, ajuste automático de imagens, fórmulas KaTeX, diagramas Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, exibição recolhida das tabelas de controle de documentos |
| Escrever | Alternância entre edição visual e edição do código-fonte Markdown; criação, duplicação, renomeação e reordenação a partir do INDEX |
| Verificar | Verificação de documentos com docs-lint, conferência de documentos, seções e termos obrigatórios com base no Standard Pack, criação a partir de modelos |
| Traduzir | Geração de propostas de tradução por página ou em lote, salvas após revisão <!-- ai-only --> |
| Usar a partir de IA | Ferramenta de especificações somente leitura que os agentes do VS Code podem consultar <!-- ai-only --> |

## Onde você pode usar

| Ambiente | Uso |
|---|---|
| Extensão do VS Code | Leitura, edição, verificação e tradução do repositório local. É o foco desta ajuda |
| Versão para navegador web | Leitura de documentos no GitHub (públicos ou privados), rascunhos no dispositivo, leitura de pastas locais |
| Extensão para Chromium | Abre a versão para navegador web em uma aba do navegador |

## Princípios básicos

- **O Markdown é o original.** Os documentos continuam sendo arquivos Markdown gerenciados pelo Git. O Lunascape Docs nunca os converte nem os guarda em outro formato.
- **Quem salva é você.** As edições só são gravadas no arquivo quando você pressiona [Salvar]. O stage e o commit no Git nunca são feitos automaticamente.
- **Os documentos são processados no seu dispositivo.** Nenhum documento é enviado para fora para ser lido ou editado. Somente na tradução o destino e o conteúdo são mostrados antes, e o envio acontece após a sua aprovação.
- **As traduções ficam em `i18n/<idioma>/`.** Os documentos no idioma padrão permanecem no local original; as traduções usam o mesmo caminho relativo em `i18n/en/` e assim por diante.
- **A IA só faz propostas.** As propostas de tradução são salvas depois que você revisa as diferenças. Os documentos nunca são reescritos sem aviso. <!-- ai-only -->

## Tópicos relacionados

- [Nomes e funções das partes da tela](screen.md)
- [Instalar a extensão](install.md)
- [Operações básicas](../02-reading/README.md)
