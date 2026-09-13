# Segurança e limites de gravação

Os limites que o Lunascape Docs mantém para proteger seus documentos e seu dispositivo.

## Exibição

- O HTML gerado a partir do Markdown e o SVG gerado a partir dos diagramas são higienizados com o DOMPurify 3.4.14 antes de serem exibidos.
- Scripts arbitrários contidos no MDX não são executados.
- O KaTeX é executado com `trust: false`, `maxSize: 50` e `maxExpand: 1000`, e não confia em HTML externo nem em comandos arbitrários.
- As bibliotecas de renderização Markmap, WaveDrom, Svgbob, Vega-Lite e Penrose são carregadas no próprio dispositivo, em versões fixas, apenas quando o bloco correspondente existe. Referências a recursos externos, HTML bruto e notações executáveis não são permitidos, e scripts, imagens externas, `link`, `style` e `foreignObject` são removidos do SVG gerado.
- A renderização de TikZ não inicia o LaTeX do sistema: ela é executada sequencialmente em um worker TeX em WebAssembly com sistema de arquivos em memória. Há limites de entrada, de fila de espera, de memória, de tempo de execução (15 segundos) e de saída SVG, e as instruções de E/S de arquivo são recusadas.

## Acesso a documentos e arquivos

- Os links dos documentos e as operações de arquivo não podem sair da raiz da documentação.
- As ações de criar, renomear, mover e excluir a partir do INDEX são reconferidas pela extensão — raiz da documentação, versão do INDEX, caminho do documento canônico, tipo do alvo, limites dos links simbólicos e documentos não salvos — antes de serem aplicadas. Pedidos vindos de um menu desatualizado ou de outra raiz da documentação não são aplicados.
- Durante a edição de um documento ou enquanto outra operação do INDEX está sendo aplicada, as operações de modificação do INDEX ficam desativadas.
- A criação a partir de um modelo reconfere, depois da pré-visualização, a confiança no espaço de trabalho, a identidade da raiz da documentação, a versão do INDEX, o Standard Pack e o conteúdo gerado, o destino e os limites dos links simbólicos. Ela não sobrescreve arquivos existentes e não cria conteúdo diferente da pré-visualização nem resultados expandidos acima de 4 MiB.
- Ao salvar um arquivo de configuração, a versão é verificada imediatamente antes da gravação, que é cancelada caso seja detectada uma alteração externa.

## Envio para fora

- Os documentos nunca são enviados para fora para leitura, edição ou verificação. As verificações de documento são executadas no próprio dispositivo, de forma determinística.
- Apenas a tradução (a tradução desta página e a tradução em lote) envia documentos para um modelo de linguagem, informando antes o destino e o alcance do envio e somente com aprovação explícita. <!-- ai-only -->
- As propostas de tradução são apresentadas como diferenças e, após a reconferência das versões do documento canônico e do documento de destino, só são aplicadas quando uma pessoa as salva explicitamente. <!-- ai-only -->
- A ferramenta de especificação para agentes de IA não devolve o conteúdo dos documentos, nomes de espaços de trabalho nem caminhos locais. <!-- ai-only -->

## Git

- Salvar apenas grava o arquivo. Nenhum recurso faz staging nem commit no Git automaticamente.
- Arquivos existentes como `_meta.json` nunca são excluídos ou alterados silenciosamente. Traduções órfãs também não são excluídas ou movidas automaticamente.

## Tópicos relacionados

- [Principais especificações](README.md)
- [Uso a partir de agentes de IA](ai-agents.md)
