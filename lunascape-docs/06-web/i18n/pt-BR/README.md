# O que o visualizador Web faz

O visualizador Web do Lunascape Docs está disponível em <https://docs.lunascape.org/>. Sem instalar nada, você pode ler documentos no GitHub como se fossem um site.

## Recursos

| Recurso | Descrição |
|---|---|
| Repositórios públicos | Abre os documentos de um repositório público do GitHub sem entrar |
| Repositórios privados | Depois de entrar com o GitHub, abre os repositórios aos quais você tem acesso de leitura |
| Pastas locais | Em [Abrir documentos], use [Abrir documentos de uma pasta local] para abrir uma pasta no seu dispositivo (somente navegadores compatíveis) |
| Leitura | INDEX, links, histórico, filtragem, sumário da página, troca de idioma e troca de tema. Igual ao VS Code |
| Diagramas e fórmulas matemáticas | Mermaid, Vega-Lite, Markmap, WaveDrom, Svgbob, Penrose e fórmulas matemáticas KaTeX |
| Rascunhos | Edite documentos e mantenha as alterações como rascunhos no seu dispositivo. Nada é gravado no repositório |
| Links diretos para páginas | A URL pode indicar o repositório e a página, abrindo uma página específica diretamente |

## Diferenças em relação à extensão do VS Code

- Verificação de documentos, criação a partir de modelos, geração de propostas de tradução e organização pelo INDEX não estão disponíveis no visualizador Web.
- Figuras TikZ não são renderizadas.
- As edições não são gravadas no repositório; elas se tornam rascunhos no seu dispositivo. A "solicitação de publicação", que envia rascunhos como pull request, está implementada, mas não está ativada no visualizador público. Para alterar o repositório, edite com a extensão do VS Code ou em um clone local.

## Tópicos relacionados

- [Abrir um repositório do GitHub](open-repository.md)
- [Ler um repositório privado](private-repository.md)
- [Salvar rascunhos](drafts.md)
