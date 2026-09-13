# Publicar seus documentos na Web

Você pode publicar os documentos do seu próprio repositório como um site no GitHub Pages ou em qualquer hospedagem estática. Há duas maneiras de fazer isso. Estas instruções são para desenvolvedores que podem clonar o repositório do Lunascape Docs e usar o `npm`.

## Opção 1: colocar os dois arquivos do visualizador

Implante apenas o visualizador (`index.html` e `lsdoc.js`) e deixe que ele carregue os documentos do GitHub. Os documentos em si não fazem parte do site, portanto este método é seguro para repositórios privados (os leitores entram com o GitHub).

1. Execute o comando a seguir no repositório do Lunascape Docs.

   ```sh
   npm run build:viewer
   ```

   `index.html` e `lsdoc.js` são gerados em `dist/viewer/`.
2. Coloque os dois arquivos em `docs/` do repositório que você quer publicar.
3. Ative o GitHub Pages.

A raiz da documentação a ser exibida é determinada nesta ordem.

1. A configuração `source` dentro do `index.html`
2. O `repository` indicado no `lunascape-docs.json` da mesma pasta
3. A dedução a partir da URL `*.github.io` e da estrutura de branches

## Opção 2: exportar um site estático com os documentos

Exporte o visualizador junto com os arquivos dos documentos e hospede o resultado como está.

```sh
npm run export:web -- --root ./docs --out ./dist-site
```

A saída contém o visualizador, os documentos em `docs/`, o arquivo de índice `lunascape-docs-manifest.json` e o `.nojekyll`. Coloque o resultado no S3 ou no GitHub Pages para publicá-lo. Para um exemplo de publicação automática com o GitHub Actions, consulte `examples/workflows/publish-docs-pages.yml` no repositório.

> **Nota**
>
> - **Não exporte os documentos de um repositório privado para o GitHub Pages.** Fora do Enterprise Cloud, qualquer pessoa pode ler o GitHub Pages. Se você precisa de publicação restrita, use a opção 1 e peça aos leitores que entrem com o GitHub.
> - Abrir o `index.html` diretamente por `file://` não funciona, porque o navegador impede o carregamento de arquivos vizinhos e a execução de módulos ES desse modo. Para conferir o resultado na sua máquina, use a versão para VS Code ou um servidor HTTP.
> - As bibliotecas de renderização de TikZ, Vega-Lite, Markmap, WaveDrom, Svgbob e Penrose são carregadas no momento da exibição. No site exportado, coloque também a pasta `vendor/`.

## Tópicos relacionados

- [O que a versão Web faz](README.md)
- [Ler um repositório privado](private-repository.md)
