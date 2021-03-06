# React-in-Heroku

<p align="center">
  <img src="https://user-images.githubusercontent.com/56132780/74364981-f3029300-4dab-11ea-84e9-a4aadc597782.png">
</p>

**Iniciando uma aplicação React Js no Heroku usando o CLI do Heroku**

*******
 ***Sumário*** 
 1. [Requisitos](#requirements)
 2. [Passos](#steps)
 3. [Ações adicionais](#actions)
*******
<div id='requirements' />

## Requisitos:
- Uma conta no [Heroku](https://www.heroku.com/)
- [Git](https://git-scm.com/)
- [NodeJs](https://nodejs.org/en)
#

<div id='steps' />

## Passos:

### Crie sua nova aplicação
`npx create-react-app new-app`

*Onde "new-app" é o nome de sua aplicação.*
#

### Inicie o Git dentro da pasta da aplicação
`git init`
#

### Faça login no Heroku
`heroku login`
#

### Crie o app no Heroku
`heroku create app-name --buildpack mars/create-react-app`

*Onde "app-name" é o nome que ficará na aplicação do Heroku.*
#

### Adicione os arquivos da pasta ao repositório local
`git add .`
#

### Faça o commit
`git commit -m "Initial commit"`
#

### Faça o push para o Heroku
`git push heroku master`
#

**Caso o push seja feito com sucesso, rode o seguinte comando que será aberto uma página em seu navegador com seu novo app**

`heroku open`

###### Alguns erros de push podem ocorrer se estiver fazendo o upload de uma aplicação que já possuí modificações. Se usou yarn e npm em uma mesma aplicação terá que apagar o arquivo de um dos dois pois o Heroku só permite usar um. Nesse caso faça o seguinte:

###### *Digite* `git rm yarn.lock` *para remover o yarn e usar o npm.*

###### *Digite* `git rm package-lock.json` *para remover o npm e usar o yarn.*

###### Execute `git add .` novamente, dê um `git commit -m "remove"` e rode `git push heroku master` de novo. O push deve funcionar agora.

<h4 align="center">All right? Espero que sim ;)</h4>
<p align="center">
  <img src="https://user-images.githubusercontent.com/56132780/80615599-42a14400-8a16-11ea-9fa0-9ecfe6ca33e2.gif">
</p>

#

<div id='actions' />

## Ações adicionais

### Atualizando modificações no projeto

- `git add .`

- `git status` *Serve apenas para ver quais arquivos foram modificados*

- `git commit -m "seu-commit"`

- `git push heroku master`
###### Lembre-se de executar os comandos dentro da pasta do projeto.
#

### Renomeando uma aplicação do Heroku

##### Renomeie a aplicação para o nome que deseja no painel do Heroku e rode o seguinte na pasta do seu projeto:

- ` git remote rm heroku`

- `heroku git:remote -a newname`

*Onde "newname" é o novo nome.*

