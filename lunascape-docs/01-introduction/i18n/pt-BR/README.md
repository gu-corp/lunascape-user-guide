# O que é o Lunascape Docs

O Lunascape Docs transforma os documentos Markdown de um repositório Git em um "site de especificações", tal como estão. Não é necessário nenhum passo de compilação, servidor de documentação ou banco de dados dedicado.

## O que é possível fazer

| Objetivo | Principais recursos |
|---|---|
| Ler | INDEX (sumário), links no texto, trilha de navegação, Voltar/Avançar, sumário da página, busca com filtro |
| Visualizar | Tabelas, blocos de código, ajuste automático de imagens, fórmulas matemáticas KaTeX, diagramas Mermaid/Vega-Lite/Markmap/WaveDrom/Svgbob, tabelas de controle de documentos recolhidas |
| Escrever | Alternar entre edição visual e edição do código-fonte Markdown; criar, duplicar, renomear e reordenar a partir do INDEX |
| Verificar | Verificação de documentos com o docs-lint, conferência de documentos, capítulos e termos obrigatórios com base no Standard Pack, criação a partir de modelos |
| Traduzir | Geração de propostas de tradução por página ou em lote. Revise antes de salvar <!-- ai-only --> |
| Usar a partir da IA | Uma ferramenta de especificações somente leitura que os agentes do VS Code podem consultar <!-- ai-only --> |

## Ambientes disponíveis

| Ambiente | Finalidade |
|---|---|
| Extensão do VS Code | Leitura, edição, verificação e tradução do repositório na sua máquina. É o foco desta ajuda |
| Versão para navegador web | Leitura de documentos no GitHub (públicos ou privados), rascunhos no seu dispositivo, leitura de pastas locais |
| Extensão para Chromium | Abre a versão para navegador web em uma aba do navegador |
| Navegador Lunascape | Incorporará o mesmo modelo de documentos |

## Conceitos básicos

- **O Markdown é o original.** Os documentos permanecem como os arquivos Markdown gerenciados pelo Git. O Lunascape Docs não converte nem mantém uma cópia em outro formato.
- **Quem salva é você.** O conteúdo editado só é gravado no arquivo quando você pressiona [Salvar]. O Lunascape Docs não faz o staging nem o commit no Git automaticamente.
- **Os documentos são processados no seu dispositivo.** Nada é enviado para fora para ler ou editar um documento. Somente na tradução há envio: o destino e o conteúdo são exibidos antes e o envio ocorre após sua aprovação.
- **As traduções ficam em `i18n/<idioma>/`.** Os documentos no idioma padrão permanecem onde estão; as traduções usam o mesmo caminho relativo em `i18n/en/` e assim por diante.
- **A IA apenas propõe.** As propostas de tradução são salvas depois que você confere as diferenças. Nenhum documento é reescrito silenciosamente. <!-- ai-only -->

## Tópicos relacionados

- [Nomes e funções das partes da tela](screen.md)
- [Instalar a extensão](install.md)
- [Operações básicas](../02-reading/README.md)
