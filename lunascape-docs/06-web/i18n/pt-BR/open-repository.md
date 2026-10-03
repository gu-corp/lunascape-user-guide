# Abrir um repositório do GitHub

Na versão web e no Lunascape, você pode abrir e ler um repositório do GitHub diretamente, sem duplicá-lo. Para repositórios públicos, não é preciso entrar no GitHub.

## Abrir pela tela

1. Pressione [Abrir documentos] (o ícone de pasta) na barra de ferramentas. A tela “Abrir documentos” é aberta.
2. Na coluna à esquerda, escolha onde procurar.

   | Local | O que aparece |
   |---|---|
   | Todos | Tudo o que está abaixo. Os itens abertos recentemente aparecem primeiro |
   | Abertos recentemente | Os repositórios e as pastas que você já abriu |
   | Recomendados | Os manuais indicados pelo site |
   | Repositórios do GitHub | Quando você entrou com o GitHub, os repositórios que você pode ler |
   | Este computador | As pastas deste dispositivo. No Lunascape, os repositórios duplicados também aparecem aqui |

3. Pressione [Abrir] na linha que deseja abrir. Para filtrar as linhas, digite em [Filtrar por nome do documento ou do repositório], na parte superior.

Para um repositório que não está na lista, indique-o em [Inserir owner/repo e abrir], na coluna à esquerda.

> **Dica**
>
> - Os repositórios do GitHub que aparecem na lista são aqueles em que o GitHub App “Lunascape Docs” está instalado e para os quais você tem permissão de leitura. Se um repositório não aparecer, peça ao proprietário que adicione o App.

## Verificar onde está o documento

O pequeno ícone no lado esquerdo da barra de ferramentas (o chip de local) mostra onde está o documento que você está lendo.

| Ícone | Local |
|---|---|
| Marca do GitHub | Você está lendo a partir do GitHub. Nada é salvo neste dispositivo |
| Computador | Uma pasta deste dispositivo gerenciada pelo Lunascape. O nome do branch do Git e o número de arquivos alterados também são exibidos |
| Pasta | Uma pasta deste dispositivo |

Pressione o ícone para ver o local, o estado e as operações disponíveis a partir dali, como [Ver no GitHub] e [Copiar link].

## Duplicar um repositório no Lunascape

No Lunascape, você pode duplicar um repositório do GitHub neste dispositivo, editá-lo e fazer commits com o Git.

- Na tela “Abrir documentos”, pressione [Duplicar] na linha do repositório.
- Se estiver lendo um repositório aberto a partir do GitHub, pressione o chip de local e depois [Duplicar neste computador]. Quando a duplicação terminar, o mesmo documento é aberto na versão deste dispositivo.

Um repositório duplicado aparece na lista com a indicação “Neste computador”, e [Abrir neste computador] aparece em primeiro lugar.

## Abrir por URL

O endereço mostra o repositório e a posição do documento, nessa ordem. Como o caminho é a posição dentro do repositório, a ordem é a mesma da URL do GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| O que indicar | Como escrever |
|---|---|
| Somente o repositório (branch padrão) | `/github/owner/repo` |
| Um documento dentro do repositório | `/github/owner/repo/docs/01-product/vision.md` |
| Um branch ou uma tag | Acrescente `?ref=v1.2.0` ao final |

O endereço muda quando você passa para outra página. Para enviar o link da página que você está lendo, pressione [Compartilhar este documento] na barra de ferramentas. Os botões [Voltar] e [Avançar] do navegador também funcionam.

O formato antigo com `?source=` continua abrindo normalmente. Depois que a página abre, o endereço é reescrito no novo formato.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Atenção**
>
> - Se você não entrou no GitHub, aplica-se o limite de uso da API do GitHub (60 solicitações por hora). Para repositórios com muitos documentos ou para leituras repetidas, use [Entrar com o GitHub].
> - Nomes de branch que contêm `/` (como `feature/xxx`) podem ser indicados com `?ref=` no formato de endereço acima. Não é possível escrevê-los no formato `?source=`.
> - Os documentos são carregados com as permissões do GitHub de quem os lê. Quem não tem permissão de leitura não consegue vê-los.

## Abrir documentos de uma pasta local

Pressione [Abrir documentos] na barra de ferramentas e, em [Abrir documentos de uma pasta local], na coluna à esquerda, escolha uma pasta do dispositivo. Os arquivos são processados dentro do navegador e nunca são enviados para fora. Esse recurso funciona em navegadores que permitem selecionar pastas (Chrome, Edge etc.).

## Tópicos relacionados

- [Visualizar um repositório privado](private-repository.md)
- [A versão web não abre ou não permite entrar](../07-troubleshooting/web.md)
