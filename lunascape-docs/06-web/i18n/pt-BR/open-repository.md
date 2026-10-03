# Abrir um repositório do GitHub

Na versão web, você pode abrir e ler um repositório do GitHub diretamente, sem cloná-lo. Em repositórios públicos, não é preciso entrar.

## Abrir pela tela

1. Pressione [Abrir documentos] (o ícone de pasta) na barra de ferramentas. A tela “Abrir documentos” é aberta.
2. Na coluna da esquerda, escolha o local que deseja abrir.

   | Local | O que aparece |
   |---|---|
   | Tudo | Tudo o que está abaixo. Os itens abertos recentemente aparecem primeiro |
   | Abertos recentemente | Os repositórios e as pastas que você já abriu |
   | Destaques | Os manuais apresentados pelo site |
   | Repositórios do GitHub | Quando você entrou com o GitHub, os repositórios que você pode ler |
   | Este computador | As pastas deste dispositivo |

3. Pressione [Abrir] na linha que deseja abrir. Digite em [Filtrar por nome do documento ou do repositório], na parte superior, para filtrar as linhas.

Para um repositório que não está na lista, indique-o em [Digitar owner/repo para abrir], na coluna da esquerda.

> **Dica**
>
> - Os repositórios do GitHub exibidos na lista são aqueles em que o GitHub App “Lunascape Docs” está instalado e que você tem permissão para ler. Se um repositório não aparecer, peça ao proprietário dele que adicione o App.

## Verificar onde está o documento

O pequeno ícone no lado esquerdo da barra de ferramentas (o chip de local) mostra onde está o documento que você está lendo.

| Ícone | Local |
|---|---|
| Marca do GitHub | O documento é lido do GitHub. Nada fica salvo neste dispositivo |
| Pasta | Uma pasta deste dispositivo |

Pressione o ícone para ver o local, o status e as operações disponíveis a partir dali ([Ver no GitHub], [Copiar link] etc.).

## Abrir por URL

O endereço é formado pelo repositório seguido da localização do documento. Como o caminho é a localização dentro do repositório, a ordem é a mesma da URL do GitHub.

```text
https://docs.lunascape.org/github/owner/repo/docs/01-product/vision.md
```

| O que especificar | Como escrever |
|---|---|
| Somente o repositório (branch padrão) | `/github/owner/repo` |
| Um documento dentro do repositório | `/github/owner/repo/docs/01-product/vision.md` |
| Uma branch ou tag | Acrescente `?ref=v1.2.0` ao final |

Ao mudar de página, o endereço também muda. Pressione [Compartilhar este documento] na barra de ferramentas para enviar o link da página que você está lendo. Os botões [Voltar] e [Avançar] do navegador também funcionam.

O formato antigo `?source=` continua abrindo normalmente. Depois de aberto, o endereço é reescrito no novo formato.

```text
https://docs.lunascape.org/?source=github:owner/repo@main/docs#/01-product/vision.md
```

> **Observação**
>
> - Sem entrar, aplica-se o limite de uso da API do GitHub (60 solicitações por hora). Para repositórios com muitos documentos ou para leituras repetidas, use [Entrar com o GitHub].
> - Nomes de branch que contêm `/` (como `feature/xxx`) podem ser especificados com `?ref=` no formato de endereço acima. Eles não podem ser escritos no formato `?source=`.
> - Os documentos são carregados com as permissões do GitHub de quem os lê. Quem não tem permissão de leitura não os vê.

## Abrir documentos de uma pasta local

Pressione [Abrir documentos] na barra de ferramentas, depois [Abrir documentos de uma pasta local] na coluna da esquerda, e escolha uma pasta do dispositivo. Os arquivos são processados dentro do navegador e nunca são enviados para fora. Esse recurso funciona em navegadores compatíveis com a seleção de pastas (Chrome, Edge etc.).

## Tópicos relacionados

- [Visualizar um repositório privado](private-repository.md)
- [Não é possível abrir nem entrar na versão web](../07-troubleshooting/web.md)
