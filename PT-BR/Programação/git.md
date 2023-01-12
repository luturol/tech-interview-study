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

Adiciona as modificações para serem publicadas com o comando ```commit```

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



## Branching

## GitFlow


## Referencias

- [git docs](https://git-scm.com/doc)
- [git add](https://git-scm.com/docs/git-add)
- [git pull](https://git-scm.com/docs/git-pull/pt_BR)
- [git fetch](https://git-scm.com/docs/git-fetch)
- [git fetch, Atlassian](https://www.atlassian.com/git/tutorials/syncing/git-fetch#:~:text=The%20git%20fetch%20command%20downloads,else%20has%20been%20working%20on.)
