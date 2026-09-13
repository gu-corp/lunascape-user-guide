# Verificar documentos

Com o docs-lint, é possível verificar a estrutura dos títulos, links quebrados, ausência de documentos ou seções obrigatórios, divergências de terminologia e a consistência dos IDs de requisito. A verificação sempre abrange toda a raiz da documentação.

## Executar uma verificação

1. Na barra de ferramentas, pressione [Ferramentas de documento] e abra a aba [Verificação].
2. Pressione [Verificar a raiz da documentação].
   Também é possível executar "Lunascape Docs: Verificar a raiz da documentação" na paleta de comandos.
3. Confira a lista de resultados.

## Ler os resultados

- Acima da lista, use [Este documento] / [Tudo] para alternar o que é exibido. O escopo da verificação em si é sempre toda a raiz da documentação.
- As ocorrências têm quatro níveis: "erro", "aviso", "informação" e "sugestão". Em [Ferramentas de documento], na barra de ferramentas, aparece a quantidade de erros e avisos.
- Ao pressionar uma ocorrência, a posição correspondente na origem Markdown é aberta no editor do VS Code.
- As ocorrências relativas a toda a raiz da documentação (como a falta de um documento de teste) aparecem como itens de "toda a raiz da documentação" e não têm posição.
- As mesmas ocorrências também aparecem no painel "Problemas" do VS Code.

## Itens verificados

Pressione [Revisar e alterar as regras] para ver a lista de verificações ativas e a finalidade de cada uma. Os principais itens são estes:

| Item | Conteúdo |
|---|---|
| Estrutura dos títulos | Há um único H1 e os níveis de título não pulam etapas |
| Links internos | Os documentos de destino existem e não saem da raiz da documentação |
| Idioma dos blocos de código | Os blocos de código indicam o nome da linguagem |
| Pastas e documentos obrigatórios | As pastas e os documentos exigidos pelo perfil do Standard Pack estão presentes |
| Seções obrigatórias do documento | Cada tipo de documento tem as seções obrigatórias |
| Uniformidade da terminologia | Detecta expressões a evitar e incentiva o uso dos termos recomendados |
| Nomenclatura e duplicidade de IDs de requisito | Os IDs de requisito seguem a regra de nomenclatura e não estão definidos em duplicidade |
| Consistência das referências a IDs de requisito | Os IDs de requisito citados no projeto, nos testes e nas tabelas de situação existem de fato |
| Correspondência entre requisitos e testes | Os IDs de requisito são referenciados nos documentos de teste |

Os itens ativos dependem do Standard Pack e do perfil escolhidos em `lunascape-docs.json` e de `docs-lint.config.json`.

> **Nota**
>
> - Ao alterar um documento ou uma configuração, o resultado anterior passa a exigir nova verificação. Nada é considerado aprovado automaticamente. Pressione [Verificar a raiz da documentação] novamente.
> - Alterações não salvas não entram na verificação. Salve antes.
> - A verificação é executada no próprio equipamento, de forma determinística. Avaliações feitas por IA e resultados de tradução nunca se misturam aos resultados da verificação.

## Tópicos relacionados

- [Alterar as regras de verificação](rules.md)
- [Configuração do projeto](project-configuration.md)
- [Verificação, criação ou tradução não funcionam](../07-troubleshooting/tools.md)
