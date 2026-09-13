# Criando seus primeiros documentos

Em um projeto que ainda não tem uma pasta de documentação, você pode criar um conjunto inicial de documentos pela Paleta de Comandos.

1. Abra a pasta do projeto no VS Code e confie no espaço de trabalho.
2. Na Paleta de Comandos (`⇧⌘P` / `Ctrl+Shift+P`), execute "Lunascape Docs: Criar documentação a partir de modelo".
   Se o espaço de trabalho tiver várias pastas, escolha aquela em que os documentos serão criados.
3. Escolha a estrutura a criar.
   - [Documento de uma página]: apenas o `README.md`. Adequado para uma especificação curta, anotações ou um documento explicativo isolado.
   - [Conjunto de documentação]: uma página inicial e as páginas de entrada de `specification/` (especificação), `manual/` (manual) e `help/` (ajuda).
4. Digite o título da documentação. Ele é usado no README e nos títulos de cada documento.
5. Digite a pasta de documentação a criar, em caminho relativo ao espaço de trabalho. O padrão é `docs`.
6. Confira a lista de arquivos que serão criados e pressione [Criar].
   Quando a criação terminar, o novo `README.md` abre no visualizador.

> **Nota**
>
> - Arquivos existentes nunca são sobrescritos. Se um único dos arquivos a criar já existir, nada é criado e a operação é interrompida.
> - Não é possível criar em um espaço de trabalho não confiável.

> **Dica**
>
> - Se você já tem uma pasta de documentação, pule esta etapa e vá para [Operações básicas](../02-reading/README.md).
> - Conforme a documentação cresce, você pode adicionar documentos um a um, escolhendo um modelo na aba [Criar] das Ferramentas de documento.

## Tópicos relacionados

- [Criar um documento a partir de um modelo](../04-document-tools/templates.md)
- [Raízes da documentação e convenções de arquivos](../04-document-tools/structure.md)
