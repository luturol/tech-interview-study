# Git

Git é uma ferramenta de versionamento de código. Utilizada em plataformas como Github, Gitlab e Azure devops.

## Principais comandos

### git status

```
git status
```

Verifica todos arquivos que estão em staging (todos arquivos que foram modificados ou que não foram registrados no repositório)

### git commit

```
git commit
```

Publica todas modificações que foram marcadas para serem publicadas. Se tu não passar o parâmetro ```-m``` ele irá abrir um editor de texto no teu terminal para tu adicionar uma mensagem de commit.

É possível commitar as modificação com uma linha de comando apenas usando o parâmentro ```-m``` e adicionando a mensagem

```bash
git commit -m 'teste'
```

Além do mais, é possível adicionar novas modificaçãos ao um commit já efetuado usando o parâmetro ```--amend```.

```bash
touch teste.txt

git add teste.txt

git commit -m 'adding teste file'

touch teste1.txt

git commit --amend
```

O uso do ```--amend``` deve ser somente para adicionar novas modificação num commit recém feito e que ainda não foi enviado para o repositório remoto. Após o uso do ```--amend``` dois arquivos estarão no mesmo commit. **Cuidado** porquê o amend altera a história do repositório, ou seja, fazer um --amend num commit que já foi enviado para o repositório remoto ocasionará na necessidade de fazer um ```push -f``` para subir essa modificação.

### git add

```
git add
```

Adiciona as modificações para serem publicadas com o comando ```git commit```

### git push

```
git push
```

Envia todas as modificações para o repositório remoto. É necessário configurar um repositório remoto para poder usar.

### git pull

```
git pull
```

Atualiza o repositório local com todas as modificações do remoto. Ele faz um merge com as tuas modificações. Por baixo dos panos ele executa os seguintes comandos:

```
git fetch
git merge
```

### git fetch

```
git fetch
```

Baixa todo conteúdo que está no repositório remoto para o seu repositório local, mas não faz o merge de nada. Para aplicar você deve fazer um ```git merge```

Detalhe: ao executar o git fetch, você também "baixa" novos branchs para o seu repositório local.

### git branch

```
git branch
```

Você visualiza todos os branchs do teu repositório local e pode utilziar para criar novos branchs

```
git branch novo-branch
```

Ao criar um novo branch, você cria apontando do branch atual e não faz o switch para o novo branch.

```git branch -f nomeDoBranch```

Reseta o brach para o ponto inicial dele.

```git branch -m novoNome```

Move ou renomeia o branch. ```-M``` é igual a ```--m --force```.

### git checkout

```
git checkout
```

Comando utilizado para criar branchs ou mover entre branchs dentro de um repositório.

```
git checkout -b novoBranch
```

Cria um novo branch. **Importante**: esse comando cria um novo branch a partir do branch atual, então é necessário voltar para um branch principal do projeto antes de criar um novo branch.

Para alterar entre branchs:

```
git checkout nomeDoBranch
```

### Branching

É a forma de organizar o versionamento utilizando ramificações. Uma boa prática é criar um branch novo para cada feature que você trabalha e depois que terminar abrir um Pull Request para um outro branch. Muito usado para desenvolvimento paralelo entre o time de desenvolvimento. Assim possibilita mais de um desenvolver atuar no código sem atrapalhar o desenvolvimento do outro, ou seja, um poderia estar atuando num bug enquanto outro numa feature. Além disso, cada modificação em um branch não afeta a outra branch, até elas serem mescladas (```git merge```) entre si e possibilita um histórico detalhado de cada modificação facilitando a revisão das tarefas desenvolvidas.

### Pull Request

Após todas as modificações serem feitas é possível realizar o ```push``` da sua branch para o repositório remoto e depois criar um Pull Request para abrir uma solicitação para revisar e mesclar as modificação num branch principal do seu projeto.

Ele serve para facilitar o controle das modificações que estão entrando no projeto e melhorar a qualidade do código disponibilizando uma ferramenta de fácil visualização do código. Dentro de um Pull Request é possível comentar em cima do código dos colaboradores para auxilia-los e melhorar a qualidade do código do projeto.

Muitas vezes as pessoas são atribuídas as Pull Requests dos colegas para darem um feedback ou aprovarem a modificação, liberando então a opção de mesclar (merge) no branch princial (pode ser tanto na master, main, quanto na develop).

## git reset

Faz tu apagar o último commit realizado e dependendo do comando deixa ele ou na stagin area, ou só marcados como modificados ou apaga tudo. Há outros parâmetros interessantes no git reset, mas iremos abordar somente esses três: --soft, --mixed e --hard

### --soft

Ele volta o último commit e deixa os arquivos commitados em stage, prontos para serem commitados.

```bash
git reset --soft HEAD~1
```

### --mixed

Ele volta o último commit, mas deixa todos os arquivos fora da staging area

```bash
git reset --mixed HEAD~1
```

### --hard

Ele **apaga todo o último commit**. Cuidado ao usar esse comando.

```
git reset --hard HEAD~1
```

## git rebase

É utilizado para reorganizar o histórico de commits de uma ramificação aplicando as modificações do outro nele. Ele permite fazer um histórico mais linear e mais limpo de modificações.

```
git rebase nomeDoBranch
```

Ele reorganiza as modificações do teu branch com o branch que foi informado como parâmetro no comando. Ele joga todas as tuas modificações para o topo e realiza os devidos merges que podem ser necessários caso alguma modifição tenha sido feita em algum arquivo que não estava atualizado no seu branch.

Além disso, ele é utilizado para atualizar o teu branch com o outro branch, facilitando depois o merge a partir de um Pull Request conflitos com o outro branch.

```
git rebase -i HEAD~X
```

No lugar do X, colocar o número de commits que deseja reorganizar. O comando ```-i``` permite que algumas alterações sejam feitas no histórico de commits da branch de forma interativa, sendo algumas delas: ```-r```, ```-s```, ```-e```

Muito cuidado ao utilizar o ```git rebase``` porquê ele altera o histórico de commits, então no final é necessário usar o ```push -f``` para enviar as modificações para o remoto.

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
