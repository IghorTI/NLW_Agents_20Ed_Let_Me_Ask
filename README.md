# NLW Agents 20 Ed

O NLW foi um treinamento de desenvolvimento fornecido pela Rocketseat. O objetivo do projeto **Let Me Ask** é criar salas de perguntas, mas quando um usuário fizer uma perguntar utilizar IA (Gemini) para tentar prever a resposta baseada no banco de dados existente. O projeto também possui um sistema de gravação, em que o usuário utiliza para gravar possíveis repostas no banco de dados. 

# Installation

Abaixo são os passos necessários para executar o projeto localmente. 

1) npm install --no -optional

> Todas as dependências necessárias serão instaladas; 

2) docker compose up -d

> Irá iniciar os serviços definidos no arquivo docket.compose.yml. 

3) npm run db:generate

> Irá gerar os scripts para criação do banco de dados.
> Obs: O comando acima é um atalho criado no package.json --> "db:generate": "drizzle-kit generate"

4) npm run db:migrate

> Irá executar os migrations para criação das tabelas do banco de dados
Obs: O comando acima é um atalho criado no package.json --> "db:migrate": "drizzle-kit migrate"

5) npm run db:seed

> Irá popular o banco de dados com os dadas fictícios. Esse comando é fundamental para quando rodar o frontend ele tenha dados para serem mostrados em tela. 

6) Pare a execução do servidor 

7) Crie o arquivo .env
> Utilize o arquivo .env.example como exemplo 

8) Gere uma API Key do Gemini 

> https://aistudio.google.com/apikey

9) Adicione a chave no arquivo .env

10) npm run dev

> O servidor será iniciado. Para realizar os testes basta utilizar o arquivo client.http ou executar o front.
> Para utilizar o client.http é necessário ter a extensão REST Client instalada no VS Code
> https://marketplace.visualstudio.com/items?itemName=humao.rest-client



