# Git

Git é uma ferramenta de versionamento de código. Utilizada em plataformas como Github, Gitlab e Azure devops.

## Principais comandos

### Git status

```
git status
```

Verifica todos arquivos que estão em staging (todos arquivos que foram modificados ou que não foram registrados no repositório)

### Git commit

```
git commit
```

Publica todas modificações que foram marcadas para serem publicadas.

### Git add

```
git add
```

Adiciona as modificações para serem publicadas com o comando ```git commit```

### Git push

```
git push
```

Envia todas as modificações para o repositório remoto

### Git pull

```
git pull
```

Atualiza o repositório local com todas as modificações do remoto. Ele faz um merge com as tuas modificações. Por baixo dos panos ele executa os seguintes comandos:

```
git fetch
git merge
```

### Git fetch

```
git fetch
```

Baixa todo conteúdo que está no repositório remoto para o seu repositório local, mas não atualiza nada. Para aplicar você deve fazer um ```git merge```

Detalhe: ao executar o git fetch, você também "baixa" novos branchs para o seu repositório local.


### Git branch WIP

```
git branch
```

Você visualiza todos os branchs do teu repositório local e pode utilziar para criar novos branchs

```
git branch novo-branch
```

ao criar um novo branch, você cria apontando do branch atual e não faz o switch para o novo branch.

### Git checkout WIP

```
git checkout
```


## Branching WIP

É a forma de organizar o versionamento utilizando ramificações. Uma boa prática é criar um branch novo para cada feature que você trabalha e depois que terminar abrir um Pull Request para um outro branch.

```
git branch
```

Lista todos os branchs do teu repositório (mostra apenas os que você tem local)

```
git checkout -b novo-branch
```

Cria um novo branch

```
git checkout antigo-branch
```

Volta para o branch antigo

## GitFlow

## Trunk base

## Referencias

- [git docs](https://git-scm.com/doc)
- [git add](https://git-scm.com/docs/git-add)
- [git pull](https://git-scm.com/docs/git-pull/pt_BR)
- [git fetch](https://git-scm.com/docs/git-fetch)
- [git fetch, Atlassian](https://www.atlassian.com/git/tutorials/syncing/git-fetch#:~:text=The%20git%20fetch%20command%20downloads,else%20has%20been%20working%20on.)
- [Git Branching - Basic Branching and Merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
- [git branch](https://git-scm.com/docs/git-branch)
