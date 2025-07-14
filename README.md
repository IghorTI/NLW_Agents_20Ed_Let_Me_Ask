# NLW Agents 20 Ed - Backend

O NLW foi um treinamento de desenvolvimento fornecido pela Rocketseat. O objetivo do projeto **Let Me Ask** é criar salas de perguntas, mas quando um usuário fizer uma perguntar utilizar IA (Gemini) para tentar prever a resposta baseada no banco de dados existente. O projeto também possui um sistema de gravação, em que o usuário utiliza para gravar possíveis repostas no banco de dados. Esse foi o projeto de backend.

## Installation

Abaixo são os passos necessários para executar o projeto localmente. 

1)  Clone o repositório

> git clone 'https://github.com/IghorTI/NLW_Agents_20Ed_Let_Me_Ask'
> cd server

2) Configure o banco de dados

> docker compose up -d
> Irá iniciar os serviços definidos no arquivo docket.compose.yml. 

3) Configure as variáveis de ambiente

> Crie o arquivo .env
> Utilize o arquivo .env.example como exemplo 
> Gere uma API Key do Gemini: https://aistudio.google.com/apikey

4) Instale as dependências
> npm install --no -optional
> Todas as dependências necessárias serão instaladas; 


5) Gere os script para o banco de dados

> npm run db:generate
> Irá gerar os scripts para criação do banco de dados.
> Obs: O comando acima é um atalho criado no package.json --> "db:generate": "drizzle-kit generate"

6) Execute as migrações do banco

> npm run db:migrate
> Irá executar os migrations para criação das tabelas do banco de dados
Obs: O comando acima é um atalho criado no package.json --> "db:migrate": "drizzle-kit migrate"

7) Popule o banco com dados de exemplo
> npm run db:seed
> Irá popular o banco de dados com os dadas fictícios. Esse comando é fundamental para quando rodar o frontend ele tenha dados para serem mostrados em tela. 

8) Pare a execução do servidor se ele estiver executando.

9) Execute o projeto
**Desenvolvimento:**
> npm run dev

**Produção:**
npm start

> O servidor será iniciado. Para realizar os testes basta utilizar o arquivo client.http ou executar o front.
> Para utilizar o client.http é necessário ter a extensão REST Client instalada no VS Code
> https://marketplace.visualstudio.com/items?itemName=humao.rest-client


## 🌐 Endpoints

A API estará disponível em `http://localhost:3333`

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

___ 

 ## 🚀 Tecnologias

- **Node.js** com TypeScript nativo (experimental strip types)
- **Fastify** - Framework web rápido e eficiente
- **PostgreSQL** com extensão **pgvector** para vetores
- **Drizzle ORM** - Type-safe database operations
- **Zod** - Schema validation
- **Docker** - Containerização do banco de dados
- **Biome** - Linting e formatação de código

## 🏗️ Arquitetura

O projeto segue uma arquitetura modular com:

- **Separação de responsabilidades** entre rotas, schemas e conexão com banco
- **Validação de schemas** com Zod para type safety
- **ORM type-safe** com Drizzle para operações de banco de dados
- **Validação de variáveis de ambiente** centralizadas