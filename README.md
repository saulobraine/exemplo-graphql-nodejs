# Exemplo GraphQL com NodeJS

Requisitos:
- Docker
- Container (com mongodb)
- Node.js


Para testar, basta rodar no terminal

```node src/server.js```

Se não der nenhum erro, ir no navegador para:

```http://localhost:4000```

Para cadastrar um usuário:

```
mutation {
  createUser(name: "Nome usuário", email: "email@usuario.com") {
    id
  }
}
```

Para retornar um usuário, você precisara do ID de algum usuário cadastrado, no exemplo retornando nome e e-mail.


```
query {
  user(id: "5eb332c35123301288f3d15b") {
    name
    email
  }
}
```

Para retornar todos os usuários:
```
query {
  users {
    id
    name
    email
  }
}
```

Para mais detalhes:

[![GraphQL aplicado no Node.js | Diego Fernandes](http://img.youtube.com/vi/oD8GqurXZ-0/0.jpg)](http://www.youtube.com/watch?v=oD8GqurXZ-0 "GraphQL aplicado no Node.js | Diego Fernandes")
