<h1 align="center"> Back-End Todo List </h1>

<p align="center">
  <a href="#-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-projeto">Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/static/v1?label=license&message=MIT&color=49AA26&labelColor=000000">
</p>

<br>

## 🚀 Tecnologias

Esse projeto foi desenvolvido com as seguintes tecnologias:

- Java
- SpringBoot

## 💻 Projeto

O Projeto Back-End Todo List é uma API Restfull que permite realizar o cadastro de tarefas. Os usuários podem criar uma conta e cadastrar e alterar tarefas. Qualquer operação no sistema deve ser realizadas por um usuário com credenciais válidas. 

## Rotas

### GET /tasks

- Descrição: Retorna um array com as tasks cadastras do usuário cadastrado. Necessário o usuário estar autenticado.
- Request Body:
```js
```
- Response Body:
```js
{
	[
	{
		"id": "764f9ca3-109f-46bf-871d-32a523c3b444",
		"description": "Teste de tarefa com nova descrição",
		"title": "Nova Tarefa",
		"startAt": "2023-10-16T12:30:00",
		"endAt": "2023-10-16T13:30:00",
		"priority": "ALTA",
		"createdAt": "2023-10-16T09:34:34.885115",
		"idUser": "bf78ecea-3b03-4083-a04b-2d35618ecde3"
	}
]
}
```

### PUT /tasks/{id}

- Descrição: Realiza a alteração de uma tarefa já cadastrada. Retorna um Json com a tarefa atualizada. Necessário o usuário estar autenticado.
- Request Body:
```js
{
	"description": "Teste de tarefa com nova descrição hahahaha",
	"title": "Nova Tarefa Test"
}
```
- Response Body:
```js
{
	"id": "822599f1-023a-47a3-bfb6-eb36ee2239dd",
	"description": "Teste de tarefa com nova descrição hahahaha",
	"title": "Nova Tarefa Test",
	"startAt": "2023-10-16T12:30:00",
	"endAt": "2023-10-16T13:30:00",
	"priority": "ALTA",
	"createdAt": "2023-10-16T09:58:58.294783",
	"idUser": "01a1548b-8821-440a-851e-871568533aec"
}
```

### POST /tasks/

- Descrição: Cria uma nova tarefa. Retorna um Json com a tarefa criada. Necessário o usuário estar autenticado.
- Request Body:
```js
{
	"description":"Teste de tarefa" ,
	"title":"Nova Tarefa",
	"priority":"ALTA",
	"startAt":"2023-10-16T12:30:00",
	"endAt":"2023-10-16T13:30:00"
}
```
- Response Body:
```js
{
	"id": "822599f1-023a-47a3-bfb6-eb36ee2239dd",
	"description": "Teste de tarefa",
	"title": "Nova Tarefa",
	"startAt": "2023-10-16T12:30:00",
	"endAt": "2023-10-16T13:30:00",
	"priority": "ALTA",
	"createdAt": "2023-10-16T09:58:58.2947832",
	"idUser": "01a1548b-8821-440a-851e-871568533aec"
}
```

### POST /users/

- Descrição: Criação de novos usuários. Retorna um objeto do usuário criado..
- Request Body:
```js
{
	"name":"Edgar Rocha",
	"username": "Edpow",
	"password": "12345"
}
```

- Response Body:
```js
{
	"id": "14397a28-eda2-4680-89f2-28cd327800bf",
	"username": "Edpow",
	"name": "Edgar Rocha",
	"password": "$2a$12$t1.vH/4RJW/An6ZI/sgOZeKBLmn6J3s4LpIJ/i4VynoxRRudspx66",
	"createdAt": "2023-10-16T10:42:45.3031748"
}
```

## :memo: Licença

Esse projeto está sob a licença MIT.
