# Criar um documento a partir de um modelo

Na aba [Criar] das Ferramentas de documento, você escolhe um modelo, visualiza o conteúdo e, em seguida, cria um novo documento.

1. Pressione [Ferramentas de documento] na barra de ferramentas e abra a aba [Criar].
2. Pressione [Criar a partir de um modelo] e escolha um modelo.
3. Preencha os campos (título, resumo etc.). Os campos obrigatórios são marcados com "obrigatório".
4. Digite o destino como um caminho relativo à raiz da documentação (por exemplo, `03-design/api.md`).
5. Pressione [Visualizar] e confira o Markdown gerado.
6. Pressione [Criar com este conteúdo].
   O documento é criado e exibido no visualizador. Em seguida, toda a raiz da documentação é verificada.

## Modelos disponíveis

| Modelo | Conteúdo |
|---|---|
| Documento de uma página | Uma especificação curta, anotações ou um texto explicativo independente em um único arquivo |
| Especificação, manual, ajuda | Um único arquivo com uma estrutura de capítulos genérica, adequada a especificações, manuais e ajuda |
| Modelos do Standard Pack | Quando o Standard Pack está selecionado em `lunascape-docs.json`, acrescentam-se os tipos de documento permitidos por esse perfil (documento de requisitos, documento de design etc.) |

> **Nota**
>
> - A criação exige um espaço de trabalho confiável.
> - Arquivos existentes nunca são sobrescritos. Não é possível criar o documento se já houver um com o mesmo nome no destino.
> - O destino precisa ter a extensão `.md` ou `.mdx`. Não é possível criar nada sob `i18n` (onde ficam as traduções).
> - Depois de alterar os campos, pressione [Visualizar] novamente antes de criar.

> **Dica**
>
> Em um projeto que ainda não tem uma pasta de documentos, você pode criar o primeiro conjunto com "Lunascape Docs: criar documentação a partir de um modelo" na paleta de comandos. Consulte [Criar seus primeiros documentos](../01-introduction/first-documents.md).

## Tópicos relacionados

- [Usar as Ferramentas de documento](README.md)
- [Alterar as regras de verificação](rules.md)
