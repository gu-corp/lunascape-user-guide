# Especificações principais

## Requisitos

| Ambiente | Requisitos |
|---|---|
| Extensão do VS Code | VS Code 1.90 ou posterior. Os recursos que gravam arquivos funcionam em um espaço de trabalho confiável |
| Versão para navegador web | Chrome, Edge, Safari ou Firefox recentes. Para abrir uma pasta local, é necessário um navegador compatível com a seleção de pastas (File System Access API) |
| Extensão do Chromium | Manifest V3. Não solicita permissões de host |

## Documentos compatíveis

| Item | Detalhes |
|---|---|
| Arquivos | `.md`, `.markdown`, `.mdx` |
| Markdown | GitHub Flavored Markdown (tabelas, listas de tarefas, blocos de código, texto tachado), imagens locais, front matter YAML |
| MDX | Somente os componentes permitidos são exibidos. Nenhum script arbitrário é executado |
| HTML | Exibido após a sanitização com DOMPurify 3.4.14 |

## Diagramas e fórmulas matemáticas

| Tipo | Nome da linguagem | Observações |
|---|---|---|
| Fórmulas matemáticas | `$...$`, `$$...$$`, `\(...\)`, `\[...\]` | KaTeX. `trust: false`, `maxSize: 50`, `maxExpand: 1000` |
| Mermaid | `mermaid` | |
| Vega-Lite | `vega-lite` | Somente dados incorporados. Não são permitidos URLs externos nem marcas de imagem |
| Markmap | `markmap` | |
| WaveDrom | `wavedrom` | Somente JSON estrito |
| Svgbob | `svgbob` | |
| TikZ | `tikz` | Na versão distribuída, a fonte é exibida recolhida. Limites: 64 KiB de entrada, 15 segundos, SVG de 2 MiB |
| Penrose (experimental) | `penrose` | Somente a predefinição `set-theory` |

## Limites

| Item | Valor |
|---|---|
| Resultado da expansão do modelo | 4 MiB |
| Contexto de referência da tradução | 49.152 caracteres por padrão, 1.048.576 no máximo |
| Documentos por execução de tradução em lote | 1.000 documentos |
| Largura personalizada da imagem | 16 a 4096px |

## Arquivos

| Arquivo | Função | No Git |
|---|---|---|
| `lunascape-docs.json` | Configuração da raiz da documentação | Sim |
| `docs-lint.config.json` | Configuração das regras de verificação | Sim |
| `.lunascape-docs/translation-freshness.json` | Registro da atualidade das traduções (somente caminhos, idiomas, hashes e data/hora) | Sim |
| Configurações do VS Code e estado do espaço de trabalho | Configurações de exibição pessoais, escolha do provedor, estado de abertura do INDEX | Não |

## Standard Pack incluído

`builtin:gu-corp-software` — perfis: `base`, `web-application`, `api-service`, `regulated-financial-product`, `smart-contract`

## Tópicos relacionados

- [Lista de configurações do VS Code](settings.md)
- [Segurança e limites de gravação](security.md)
