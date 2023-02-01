# Git 



Bom dia, boa tarde e boa noite a quem estiver lendo essa sinjela documentação. Este repositório está sendo criado e posteriormente melhorado com o intuito principal de estudos e de referencias futuras para minha pessoa e claro e de quem mais se interessar.

Segue a estrutura do documento: 

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

Depois de baixado, precisamos instalar e configurar o git. Abaixo foram listados comandos que podem ser usados para configurar o git a primeiro momento.

O git trabalha as configurações em três diferentes escopos de atuação:

1. --system: válido para todos os usuários no sistema e todos os seus repositórios;
2. --global: válido somente para seu usuário e os repositórios desse usuário;
3. config: válido somente para o repositório que se está executando esse comando;

A seguir eu tentei listar de forma simples três comandos que podemos usar para configurar username, email e o editor principal que podemos usar no git, lembrando que este ultimo pode ser configurado no momento da instalação.

É uma boa ideia se apresentar ao git com seu nome de usuário e seu email antes de fazer qualquer alteração. A maneira mais fácil de fazer isso é com os próximos dois comandos.

### Configurando usuário/username git

Troque a string "< username >" pelo nome de seu usuário. Lembrando que, ao utilizar o parametro --global estamos configurando este usuário para todos respositórios do usuário do computador. 

```
    git config --global user.name "<username>"
```

### Configurando email

Troque a string "< exemple@email.com >" pelo seu email. 

```
    git config --global user.email "<exemple@email.com>"
```

### Configurar editor principal do git

Esse passo é importante caso se queira usar um editor de texto diferente do padrão do git. Para fazer isso basta trocar < editor > pelo nome do seu editor favorito.

```
    git config --global core.editor <editor>
```

### Exibe usuário configurado no git

Esse e os próximos dois comandos funcionam como uma checagem, para vermos se está tudo Ok com as informações que acabamos de configurar. 

No comando abaixo exibimos o nome do nosso usuário

```
    git config user.name
```

### Exibe email configurado no git

Já no comando abaixo, exibimos o email do usuário que foi configurado.

```
    git config user.email
```

### Exibe todas as configurações do git

Com o comando abaixo podemos exibir todas as configurações do nosso usuário Git.

```
    git config --list
```


## Inicializando um repositorio

Passando da etapa inicial de instalar e configurar o Git iremos bricar agora com repositórios. Como podemos criar um repositório na nossa máquina? Ao criá-lo já podemos fazer um commit? Temos que configurar algo a mais? Essas são uma das duvidas iniciais que eu tive quando comecei a estudar git e talvez sejam duvidas comuns entre jovens desenvolvedores que estão dando seus primeiros passos. Enfim, abaixo listei alguns comandos que são como "rituais" que devemos seguir para criar e configurar um repositório usando o Git. Vamos lá!

### Criar uma pasta

Primeiro iremos criar um diretório que servirá como base para nosso repositório. Lembrando que o comando abaixo não é necessariamente um comando git, mas sim um comando tipico do um terminal linux.

```
    mkdir <nome da pasta>
```

### Inicializando repositorio

Digamos que no passo acima criamos um diretorio chamado rep-test com o comando `mkdir rep-test`, ainda com a janela do terminal aberta termos que entrar nesse diretório usando o comando `cd rep-test`. Logo após fazermos isso estaremos dentro de nada mais nada menos do que uma pasta vazia. Para transformar esta página em um repositório usamos o comando abaixo.

```
    git init
```

Logo após executar esse comando, voce irá receber uma mensagem parecida com essa: 

`Initialized empty Git repository in C:/Users/Leonardo/Desktop/rep-test/.git/`

O que acabamos de fazer foi inicializar um repositório vazio na nossa máquina e deixá-lo pronto para iniciar nossos trabalhos de controle de versão da nossa aplicação.

## Manipulando um repositorio

As coisas estão fáceis até agora e adivinha, irão continuar fáceis. O que vamos fazer nesses próximos passos é lidar com um fluxo simples de controle de versão do git: verificando o que foi alterado, adicionandos nossos arquivos modificados na zona de staged e, finalmente fazendo nossos tão famigerados commits.

### Reportar status do repositorio

Olha, logo após adicionarmos ou modificarmos um ou vários arquivos do nosso projeto podemos listar todos os arquivos que, de fato, sofreram alguma modificação usando o seguinte comando: 

```
    git status
```

Então, digamos que queremos adicionar um arquivo chamado teste.txt no nosso repositório e fazê-lo ter uma mensagem "testando o comando git status" basta digitarmos no terminal:

`echo "Testando o comando git status" >> teste.txt`

Logo depois de executarmos o comando acima veremos que ele já aparece na nossa arvore do respositório como um arquivo adicionado, para ver isso basta executar o comando `git status`. Uma mensagem parecida com a seguinte será exibida: 

```
    On branch master

    No commits yet

    Untracked files:
    (use "git add <file>..." to include in what will be committed)
            teste.txt

    nothing added to commit but untracked files present (use "git add" to track)
```

Viram? Nosso arquivo apareceu logo abaixo da mensagem `(use "git add <file>..." to include in what will be committed)` e essa mensagem merece ser lida e significada, porque agora, se seguirmos o que essa mensagem nos diz veremos que ela nos pede para prepararmos nosso arquivo para ser commitado. Então vamos lá!

### Adicionar um arquivo ou arquivos em um grupo de versionamento

Lembra do nosso arquivo teste.txt? O que devemos fazer com ele para que possamos monitorá-lo com nosso versionador de código? É isso ai, temos que executar o comando abaixo. Bora lá, executar o comando pra ver o que acontece.

```
    git add <nome do arquivo>
```

Ué, mas não aconteceu nada. Será que deu alguma coisa errada? Que tal executar o comando `git status` novamente? Provavelmente apareceu no seu terminal algo parecido com:

```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   teste.txt

```

Parece que algo de diferente foi exibido. Vamos ver o que foi? Então, logo abaixo da mensagem `Changes to be commited:` vemos o nosso arquivo novamente. E ai, o que aconteceu? O que aconteceu foi que seu arquivo teste.txt digievoluiu de untracked file para ready to commit file (arquivo pronto para ser commitado). E ai, o que eu faço agora? Simples, commita ele ... o que pode dar de errado? (rs)

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







