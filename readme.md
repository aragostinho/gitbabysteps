#Primeiros passos

1. Instalar o Git Bash
http://git-scm.com/downloads
2. Acesse o gitbash e crie um diretorio exemplo
3. Usar o comando git init para iniar o repositorio e começar
4. Aplicando configurações globais nome e email

  `git config --global user.name "Nome Completo"`
  
  `git config --global user.email "emaildasuacontanogithub"`
  
5. Amigão -> `git status` (explicar WD, Stanging, Local Repo, Server Repo)
6. Usando o git add (-A adiciona, . não adiciona alterações e remoções)

   `git add -A`

   `git add .`

7. Usando o `git log` e `git show` (--name-only [checksum]  ex: `git show -name-only f27b`)
8. Para commitar

   `git commit -am "mensagem para o commit"`

   `git commit -m "mensagem para o commit"`


#Trabalhando com repositorio remoto

1) Adicionando um repositorio remoto (Ex: git remote add origin git@github.com:aragostinho/pm87-caelum.git)
   - Explicar possibilidades de se trabalhar com mais repositorios remotos
   - Explicar a montagem da url git@github.com:[conta]/[repositorio].git
2) git remote show
3) Criando certificado publico e usando ssh-keygen para acesso ao repositorio 
   - ssh-keygen -C "email da conta git" -t rsa
   - abrindo pasta de certificado no diretorio do usuario local, copiando o seu conteudo e aplicando em Settings Account no Git
   - testando ssh -T git@github.com
4) Primeiro push  (git push -u origin master) e demais pushs 



#Trabalhando com branchs

#### Definição de Branch
 Ex: Ramos, ramificação...

#### Conceito
 Criar ramificações no repositorio que partem de uma determinada origem (master ou outra branch ) com o intuito
 de isolar o controle de versão e permitir posteriormente a sua regressão e unificação.

#### Branch local: Vida curta. deve ser excluida logo apos a sua utilizacao
 Ex: Branch de bugs, Branch de correções

#### Branch remota: Utilizada para grandes alterações e projetos
 Ex: Novas funcionalides para a conta de usuário, Novo sistema de cotações


 1. `git branch` //lista todas as branchs do repositorio
 2. `git branch nome_da_branch`  //cria uma branch no repositorio
 3. `git checkout nome_da_branch`  //move o ponteiro HEAD para uma determinda branch
 4. // demonstrar alterações no mesmo arquivo + troca de branchs (demostração prática do conceito)
 5. `git checkout -b nome_da_branch`  //cria e move o ponteiro para a branch
 6. `git merge nome_da_branch` //aplicando merge
 7. `git branch -d nome_da_branch` // apaga a branch 


#Resolvendo conflitos

###Passos 
1. Editar arquivo listado no conflito ou seja remover o conflito
2. Adicionar o arquivo alterado no stanging (add)
3. Commitar o arquivo alterado

//fazer demonstrações de conflito
