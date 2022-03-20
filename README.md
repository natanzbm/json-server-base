# Kenzie Shop - API / Capstone - API

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do M3 e outras aplicações que necessitem de um back-end teste.

## Endpoints

Existem 4 endpoints que podem ser utilizados nesta API, 1 para cadastro, 1 para login e 2 endpoints para interação do usuário com o site, dessas 2 endpoints de interação, 1 necessita que o usuário esteja logado para ler os dados e a outra não.

### Cadastro

`POST /register`

Este endpoint irá cadastrar o usuário na lista de "Users", sendo que os campos **obrigatórios** são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

**Exemplo:**

```
{
    "name": "example",
    "email": "example@example.com",
    "password": "example123",
    "age": 15
}
```

### Login

`POST /login`

Este endpoint deve ser usado para realizar login com um dos usuários cadastrados na lista de "Users".

**Exemplo:**

```
{
    "email": "example@example.com",
    "password": "example123"
}
```

### Catalogue

`POST /catalogue`

Com este endpoint você pode registrar qualquer jogo que você queira adicionar ao seu catálogo pessoal, os campos **obrigatórios** são título (_title_) e plataforma (_platform_), você pode adicionar outros campos caso ache necessário.

**Exemplo:**

```
{
    "title": "God of War",
    "platform": "Playstation 5",
	"genre": "Action RPG"
}
```

### Trade

`POST /trade`

Este endpoint permite que você registre jogos que deseja trocar ou vender, os campos **obrigatórios** são título (_title_), plataforma (_platform_) e preço (_price_), podendo adicionar outros campos caso necessário.

**Exemplo:**

```
{
    "title": "Bloodborne",
    "platform": "Playstation 4",
    "price": 80,
	"genre": "Action RPG"
}
```
