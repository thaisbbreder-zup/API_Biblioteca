# Gerenciador de Biblioteca API

Esta é uma API simples para gerenciar uma biblioteca, permitindo a manipulação de livros com operações CRUD (Create, Read, Update e Delete). A API foi desenvolvida usando o framework Spring Boot e persiste os dados em um banco de dados relacional usando o Spring Data JPA.

## Funcionalidades
A API possui as seguintes funcionalidades:

__Exibir todos os livros:__ Recupera uma lista contendo todos os livros cadastrados na biblioteca.<br>
__Exibir um livro específico:__ Recupera as informações de um livro específico com base no seu ID.<br>
__Cadastro de um novo livro:__ Permite cadastrar um novo livro na biblioteca com informações como nome, autor, data de lançamento e código do livro.<br>
__Alteração de um livro:__ Permite alterar as informações de um livro existente com base no seu ID.<br>
__Deleção de um livro:__ Permite deletar um livro específico com base no seu ID.<br>

## Configuração do Banco de Dados
A API está configurada para utilizar um banco de dados relacional, como o PostgreSQL. A configuração do banco de dados é feita no arquivo application.properties.
Se você deseja utilizar um banco de dados específico, você pode modificar as configurações de conexão no arquivo application.properties antes de executar a aplicação.

## Endpoints da API
A API possui os seguintes endpoints:

__GET /livros:__ Retorna todos os livros cadastrados na biblioteca.<br>
__GET /livros/{id}:__ Retorna as informações de um livro específico com base no seu ID.<br>
__POST /livros:__ Cadastra um novo livro na biblioteca.<br>
__PUT /livros/{id}:__ Altera as informações de um livro existente com base no seu ID.<br>
__DELETE /livros/{id}:__ Deleta um livro específico com base no seu ID.<br>

## Como utilizar a API
Clone o repositório para sua máquina local.<br>
Importe o projeto em sua IDE preferida como um projeto Maven.<br>
Certifique-se de que você possui um banco de dados configurado (PostgreSQL) e atualize as configurações no arquivo application.properties se necessário.<br>
Execute a classe AgendaTelefonicaApplication.java como um aplicativo Spring Boot para iniciar o servidor.<br>
Use uma ferramenta como o Postman ou um cliente HTTP para enviar requisições para a API.<br>
Teste os endpoints da API para realizar operações CRUD em livros.<br>

## Exemplos de Requisições
- Exemplo de Requisição POST para cadastrar um novo livro:

POST http://localhost:8080/livros

{
    "nome": "Novo Livro",<br>
    "autor": "Novo Autor",<br>
    "dataLancamento": "2023-07-27",<br>
    "codigoLivro": "12345"<br>
}

- Exemplo de Requisição PUT para alterar um livro existente:

PUT http://localhost:8080/livros/{id}

{
    "nome": "Nome do Livro Atualizado",
    "autor": "Autor Atualizado",
    "dataLancamento": "2023-07-28",
    "codigoLivro": "54321"
}

- Exemplo de Requisição DELETE para deletar um livro específico:

DELETE http://localhost:8080/livros/{id}
Lembre-se de substituir {id} na URL pelo ID correto do livro que você deseja consultar, alterar ou deletar.
