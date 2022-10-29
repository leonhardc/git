# Git 



Bom dia, boa tarde e boa noite a quem estiver lendo essa sinjela documentação. Este repositório está sendo criado e posteriormente melhorado com o intuito principal de estudos e de referencias futuras da minha pessoa e claro, de quem mais se interessar por esse repositório.

Segue a estrutura do documento e o que será nosso onjeto de estudo a primeiro momento. 

- [Git](#git)
  - [Configurando o git](#configurando-o-git)
    - [Configurando usuário/username git](#configurando-usuáriousername-git)
    - [Configurando email](#configurando-email)
    - [Configurar editor principal do git](#configurar-editor-principal-do-git)
    - [Exibe usuário configurado no git](#exibe-usuário-configurado-no-git)
    - [Exibe email configurado no git](#exibe-email-configurado-no-git)
    - [Exibe todas as configurações do git](#exibe-todas-as-configurações-do-git)
  - [Inicializando um repositorio](#inicializando-um-repositorio)
    - [Criar uma pasta](#criar-uma-pasta)
    - [Inicializando repositorio](#inicializando-repositorio)
  - [Manipulando um repositorio](#manipulando-um-repositorio)
    - [Reportar status do repositorio](#reportar-status-do-repositorio)
    - [Adicionar um arquivo ou arquivos em um grupo de versionamento](#adicionar-um-arquivo-ou-arquivos-em-um-grupo-de-versionamento)
    - [Commitar um arquivo ou diretorio](#commitar-um-arquivo-ou-diretorio)
    - [Mostra todos os commits já feitos](#mostra-todos-os-commits-já-feitos)
    - [Mostrar historico de commits detalhado](#mostrar-historico-de-commits-detalhado)
    - [Listar todos os commmits por autor](#listar-todos-os-commmits-por-autor)
    - [Lista o historico resumido por autor](#lista-o-historico-resumido-por-autor)
    - [Mostra historico gráfico de commits](#mostra-historico-gráfico-de-commits)
    - [Verificar mudanças em um arquivo já commitado](#verificar-mudanças-em-um-arquivo-já-commitado)
    - [Verificar mudanças em um arquivo antes de ser commitado](#verificar-mudanças-em-um-arquivo-antes-de-ser-commitado)
    - [Mostrar somente o nome do arquivo que foi modificado](#mostrar-somente-o-nome-do-arquivo-que-foi-modificado)
    - [Commit em arquivo que já existiu](#commit-em-arquivo-que-já-existiu)
  - [Desfazendo alterações](#desfazendo-alterações)
    - [Voltar ao status de um arquivo para antes da edição](#voltar-ao-status-de-um-arquivo-para-antes-da-edição)
    - [Remover arquivos da zona de staged](#remover-arquivos-da-zona-de-staged)
    - [Remover arquivos ja commitados](#remover-arquivos-ja-commitados)
    - [Reverter um commit](#reverter-um-commit)
  - [Repositorio Remoto](#repositorio-remoto)
    - [Mostra os respositorios remotos que existem](#mostra-os-respositorios-remotos-que-existem)
    - [Mostra os respositorios remotos que existem detalhado](#mostra-os-respositorios-remotos-que-existem-detalhado)
    - [Enviar para o repositorio remoto](#enviar-para-o-repositorio-remoto)
    - [Resgatar alterações do meu repositorio remoto](#resgatar-alterações-do-meu-repositorio-remoto)
    - [Clonar todo um repositorio meu ou de terceiros](#clonar-todo-um-repositorio-meu-ou-de-terceiros)
  - [Branchs](#branchs)
    - [Criando um branch](#criando-um-branch)
    - [Mostrar os branchs que eu tenho no respositorio](#mostrar-os-branchs-que-eu-tenho-no-respositorio)
    - [Mudar para outro branch no repositorio](#mudar-para-outro-branch-no-repositorio)
    - [Deletar branch que não é mais necessário](#deletar-branch-que-não-é-mais-necessário)
    - [Unir branchs](#unir-branchs)
      - [Merge](#merge)
      - [Rebase](#rebase)
  - [Salvando modificações temporariamente](#salvando-modificações-temporariamente)
    - [Salvando alterações em stash](#salvando-alterações-em-stash)
    - [Aplicar as mudanças guardadas anteriormente em stash](#aplicar-as-mudanças-guardadas-anteriormente-em-stash)
    - [Listar todos os stashs que se está fazendo](#listar-todos-os-stashs-que-se-está-fazendo)
    - [Limpar tudo que está no stash](#limpar-tudo-que-está-no-stash)
  - [Configurar alias/abreviação em um comando git](#configurar-aliasabreviação-em-um-comando-git)
    - [Configurando alias do comando status com s](#configurando-alias-do-comando-status-com-s)
  - [Criando tags](#criando-tags)
    - [Passar uma tag com uma anotação](#passar-uma-tag-com-uma-anotação)
    - [Subir uma tag](#subir-uma-tag)


## Configurando o git

O primeiro passo que todos nós damos logo após baixar uma ferramenta é instalá-la e configura-la, com o git não é diferente. Segue abaixo alguns comandos que podem ser usados para configurar o git a primeiro momento.

O git trabalha com configurações com três diferentes escopos de atuação, como veremos abaixo:

1. --system: válido para todos os usuários no sistema e todos os seus repositórios.
2. --global: válido somente para seu usuário e os repositórios desse usuário.
3. config: válido somente para o repositório que se está executando esse comando.

Os comandos apresentados abaixo são para configuração do seu usuário e de seus repositórios.

### Configurando usuário/username git

Troque a string "username" para o nome de seu usuário.

```gitconfig
    git config --global user.name "username"
```

### Configurando email



```
    git config --global user.email "exemple@email.com"
```

### Configurar editor principal do git

```
    git config --global core.editor <editor>
```

### Exibe usuário configurado no git


```
    git config user.name
```

### Exibe email configurado no git

```
    git config user.email
```

### Exibe todas as configurações do git

```
    git config --list
```


## Inicializando um repositorio

### Criar uma pasta

```
    mkdir <nome da pasta>
```

### Inicializando repositorio

Depois de entrar na página use:

```
    git init
```

## Manipulando um repositorio

### Reportar status do repositorio


```
    git status
```

### Adicionar um arquivo ou arquivos em um grupo de versionamento


```
    git add
```

### Commitar um arquivo ou diretorio


Avisa ao git para criar uma imagem/snapshop do status daquele arquivo

```
    git commit -m <filename>
```
### Mostra todos os commits já feitos


Mostra as modificações que ja foram realizadas no nosso repositorio

```
    git log
```

### Mostrar historico de commits detalhado 


Além das informações do comando anterior, este mostra mais algumas informações importantes

```
    git log --decorate
```

### Listar todos os commmits por autor


```
    git log --author="<author name>"
```

### Lista o historico resumido por autor


Lista commits mostrando quais autores fizeram commits, quantos commits cada autor fez e quais foram esses commits

```
    git shortlog
```

### Mostra historico gráfico de commits


Mostra de forma gráfica o que está acontecendo com os branchs no repositorio

```   
    git log --graph
```

### Verificar mudanças em um arquivo já commitado


É possivel ver o que foi modificado em um arquivo usando a hash do commit

```
    git show <hash>
```

### Verificar mudanças em um arquivo antes de ser commitado


Mostra as modificações realizadas em um determinado arquivo antes de ele ser adicionado em staged

```
    git diff <filename>
```

### Mostrar somente o nome do arquivo que foi modificado

```
    git diff --name-only
```

### Commit em arquivo que já existiu

Se o commit for feito em um arquivo que ja existiu podemos fazer 

```
    git commit -am "<mesage>"
```

## Desfazendo alterações

### Voltar ao status de um arquivo para antes da edição


```
    git checkout <filename>
```

### Remover arquivos da zona de staged 


```
    git reset HEAD <filename> 
```

### Remover arquivos ja commitados


```
    ex1: git reset --soft <hash>
    ex2: git reset --mixed <hash>
    ex3: git reset --hard <hash> 
```

* --soft: retorna o arquivo para zona de staged (pronto para commitar)
* --mixed: retorna o arquivo para zona de modified (pronto para addicionar ao stagied e commitar - ainda com as alterações do arquivo)
* --hard: mata o commit e todas as alterações feitas no arquivo

Obs: ao escolher uma hash, sempre pegamos a hash anterior ao commit que acabamos de fazer, pois é o ponto ao 
qual desejamos retornar

### Reverter um commit


```
    git revert <hash_do_commit>
```

## Repositorio Remoto

### Mostra os respositorios remotos que existem


```
    git remote 
```

### Mostra os respositorios remotos que existem detalhado

```
    git remote -v
```

### Enviar para o repositorio remoto

```
    git push [origin] [master]
```

* origin: nome do repositorio remoto
* master: branch que estou no momento

Obs.: Tanto origin quanto master são opcionais, um git pull também funciona.

### Resgatar alterações do meu repositorio remoto


```
    git pull [origin] [master]
```

### Clonar todo um repositorio meu ou de terceiros

```
    git clone <url do repositorio> [<outro nome>]
```

## Branchs

Branchs são ponteiros moveis que lavam a um commit

### Criando um branch

```
    git checkout -b <nome do branch>
```

### Mostrar os branchs que eu tenho no respositorio


```    
    git branch
```

### Mudar para outro branch no repositorio


```
    git checkout <nome do branch>
```

### Deletar branch que não é mais necessário


```
    git branch -D <nome do branch>
```

### Unir branchs


Existem basicamente duas maneiras de unir dois branchs, o 'merge' e o 'rebase'. Eles fazem basicamente a mesma coisa, mas só que de jeitos totalmente diferentes. É bom saber a diferença.

#### Merge

Ao fazer um merge se cria um um outro commit no ramo principal, onde esse commit apontará para as duas ramificações dos dois outros branchs.

* Pros: Operação não destrutiva;
* Contra: É necessário um commit extra; Histórico fica poluído

```
    git merge <branch-name>
```

#### Rebase 


Recoloca tudo que estava no branch separado e coloca no começo da fila 'matando' os commits que estavam no branch que foi feito o rebase

* Pros: Evita commits extras; Histórico Linear;
* Contra: Perca de ordem cronológica; Histórico fica poluído

```
    git rebase <branch-name>
```

## Salvando modificações temporariamente

### Salvando alterações em stash

Comando que salva as modificações de um arquivo temporariamente dentro de um stash, para que não seja necessário fazer um commit, caso se queira mudar de um branch para outro.

```
    git stash
```

### Aplicar as mudanças guardadas anteriormente em stash

```
    git stash apply
```

### Listar todos os stashs que se está fazendo

```
    git stash list
```

### Limpar tudo que está no stash

```
    git stash clear
```

## Configurar alias/abreviação em um comando git

### Configurando alias do comando status com s

```
    git config --global alias.s status
```

Depois dessa configuração acima podemos chamar o comando status como 

```
    git s
```

## Criando tags

### Passar uma tag com uma anotação

```
    git tag -a [<numero-da-versão>] -m "<anotação>"
```

### Subir uma tag

```
    git push origin master --tags
```







