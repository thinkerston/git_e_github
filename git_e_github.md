# Git e Github

_O conteúdo apresentado neste material segue como referências as aulas do professor José de Assis que estão disponíveis no Youtube_

- _Este material busca uma forma de sintetizar o conteudo apresentado nas aulas, para que se torne mais facil a consulta e o estudo_

## Configurações inicias 
As configurações inicias do git são necessárias que os commits sejam efetuados

configurando o nome

```git config --global user.nome "seu nome"```

configurando o seu email

```git config --global user.email "seu email@email.com```

### Aula 03

para verificar o status da pasta em que os arquivos sem encontram deve se usar o seguinte comando 

    git status

para adicionar os arquivos no container deve se usar o comando 

    git add nome_do_arquivo

para adicionar todos os arquivos de uma unica vez, deve se fazer da seguinte forma

    git add .
    git add *

o proximo passo após adicionar os arquivos ao container é identificar esse commit e armazenar ele ao repositório, para fazer isso deve se usar o seguinte comando

    git commit -m "escreva o seu comentário"

outro comando muito importante é o ```git log``` serve para vermos todas as modificações que são feitas no código, outra forma de ver o os logs é o comando ```git log --oneline```

### criando ramificações no projeto

para se  criar ramificações em seus projetos usa-se o seguinte comando

    git checkout -b nome_da_ramificação

A ramificação criada herda todos os commits da ramificação criada

para retornar ao ramo master tem que usar o seguinte comando

    git checkout master

para ver os grafos gerados pelo github, voce pode usar os seguintes comandos

    git --log --oneline --graph
    git --log --oneline --graph -all

para se fazer a fusão o branch criado deve se estar no ramo master e para isso usa-se o seguinte comando

    git merge nome_do_ramo_criado

    


### Enviando um projeto local para o github

para verificar se existe um repositório remoto, usa-se o seguinte comando

    git remote

para fazer um link do repositório local com um repositório remoto, tem que usar o seguinte comando

    git remote add origin link_do_repositório_web

#### configurando o tokem para envio para o repositório web

 para isso é necessário gerar o tokem de acesso no site do github. Após isso você ao usar o comando ```git push -u origin master``` ele vai pedir seu username e token, você pode estar configurando o tokem para evitar de ser pedido toda a vez que envia um repositório web, para isso usa-se o seguinte comando

    git config --global credential.helper cache

e para excluir, só usar:

    git config --global unset credential.helper 
    


