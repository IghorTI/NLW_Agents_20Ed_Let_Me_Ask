# Dependências: 

npm i typescript @types/node -D
npx tsc --init
https://github.com/tsconfig/bases?tab=readme-ov-file


## 1 - Configuração

tsconfig.json:

{
  "$schema": "https://json.schemastore.org/tsconfig",
  "_version": "22.0.0",

  "compilerOptions": {
    "lib": ["es2024", "ESNext.Array", "ESNext.Collection", "ESNext.Iterator"],
    "module": "nodenext",
    "target": "es2022",

    "noEmit": true,
    "allowImportingTsExtensions": true,

    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "moduleResolution": "node16"
  }
}

## 2 - Configuração

package.json
+add linha: 

>"type":"module",
> "scripts": {
>    "dev": "node --experimental-strip-types src/server.ts"
>  }


## Dependências:

npm i fastify @fastify/cors fastify-type-provider-zod zod
npm i @biomejs/biome -D
npx ultracite init
npm i postgres
npm i drizzle-orm
npm i drizzle-kit -D
npm i drizzle-seed -D

# Referências
https://hub.docker.com/r/pgvector/pgvector


## Database commands 

- npx drizzle-kit generate
- npx drizzle-kit migrate
- npx drizzle-kit studio
- npm run db:seed


## Database reference

- Drizzle Seed 
- https://orm.drizzle.team/docs/seed-overview