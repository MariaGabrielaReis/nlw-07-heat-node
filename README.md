<p align="center">
  <img alt="DoWhileApp" title="DoWhileApp" src="DoWhileApp.png" width="230px" />
</p>

<p align="center">
  <a href="#projeto">Sobre a aplicação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#requisitos">Como rodar</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rotas">Rotas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#licenca">Licença</a>
</p>

<span id="projeto">
  
# :bookmark_tabs: Sobre a aplicação
Esta é um API para aplicativo "DoWhileApp" tem como objetivo proporcionar um ambiente onde os participantes do Do While 2021 possam comentar suas expectativas sobre o 
evento que acontecerá em dezembro, observando, em tempo real, as mensagens enviadas por outros participantes também.
- Aplicação construída na aula 01 (de Node) durante a Next Level Week #07: Heat (evento oferecido pela Rocketseat) :rocket:

### :hammer_and_wrench: Tecnologias
As seguintes tecnologias e ferramentas estão sendo utilizadas neste projeto: 
- NodeJS, Express, Insomnia, TypeScript, Web Socket

<span id="requisitos">

# :gear: Como rodar
Antes de começar, você vai precisar ter instalado algumas coisinhas, como o Node.js e o Yarn, é só seguir esse passo a passo [aqui](https://www.notion.so/Instala-o-das-ferramentas-405f3e8b014649cbb422dee6b5bd0535). Tenha também o [Git](https://git-scm.com/), para clonar este repositório!

Com o [Node](https://nodejs.org/en/) instalado em sua máquina, clone ou baixe este repositório e siga o passo a passo descrito abaixo:
- Cadastre o aplicativo no GitHub (em configurações < ferramentas de desenvolvedor < OAuth Apps),para conseguir acesso ao serviço de autenticação, 
colocando a homepage url como `http://localhost:4000` e o redirect como `http://localhost:4000/sign/callback`, não esquecendo de gerar uma chave secreta, 
definindo essas configurações também em um arquivo `.env` seguindo o exemplo abaixo:
```cl
GITHUB_CLIENT_SECRET=
GITHUB_CLIENT_ID=
JWT_SECRET=
```
Agora, por um terminal...
```bash
# Acesse a pasta do projeto em Node
$ cd nlw-07-heat-node

# Instale as dependências
$ yarn

# Rode as migrations
$ yarn prisma migrate dev

# Rode o projeto
$ yarn dev
```
O servidor inciará na porta:4000. Para utilizar as funcionalidades da aplicação, use o Insomnia para simular requisições e respostas das rotas

<span id="rotas">
  
# :railway_track: Rotas
| GET  | POST  |
|:--------- |:-----------|
|http://localhost:4000/github <br> retorna o código de autenticação do GitHub <br><br> http://localhost:4000/messages/last3 <br> lista as últimas 3 mensagens enviadas <br><br> http://localhost:4000/profile <br> retorna informações do usuário como nome, avatar, login...| http://localhost:4000/authenticate <br> verifica o token de autenticação do GitHub do usuário <br><br> http://localhost:4000/messages <br> cadastrar mensagem |

<span id="licenca">

## :page_with_curl: Licença
Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

[![image](https://img.shields.io/badge/✨%20Maria%20Gabriela%20Reis,%202021-LinkedIn-009973?style=flat-square)](https://www.linkedin.com/in/mariagabrielareis/)
