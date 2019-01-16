# beg-graphQL-API
Una simple API GraphQL 
Crear una API eficiente utilizando GraphQL
https://graphql.org/

En el directorio graphql-server

npm init -y 

npm install --save-dev graphpack

En archivo package.json

" scripts " : {
    " dev " : " graphpack " ,
    " build " : " graphpack build "
}

Crear carpeta graphql-server/src

Crear en src archivo schema.graphql

type Query {
  holaGQL: String
}

Crear archivo resolvers.js

import { users } from "./db";

const resolvers = {
  Query: {
    holaGQL: () => "Hola GraphQL!"
  }
};

export default resolvers;

Crear archivo db.js

export let users = [
  { id: 1, name: "Carmen Doe", email: "carmen@gmail.com", age: 22 },
  { id: 2, name: "Ivon Doe", email: "ivon@gmail.com", age: 23 }
];

src
  |--db.js
  |--resolvers.js
  |--schema.graphql
  
  Ejecutar Comando 
  
  npm run dev
  
  Por Consola 
  
  ? Server ready at http://localhost:4000/
  
  Copiar URL al Navegador
  
  GraphQL IDE en  
  
  localhost:4000 
  
  Ejecutar en GraphQL IDE
  
  query {
   users {
    id
    name
    email
    age
  }
}
  
  
  
