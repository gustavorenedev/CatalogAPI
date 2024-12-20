# ASP.NET Core MVC Catalog API

## Descrição do Projeto

API de Catálogo é uma API de produto com relacionamento com categorias que foi feita com Docker, utilizando Docker Compose e containers para o banco de dados não relacional MongoDB.

### Objetivo

O objetivo deste projeto é demonstrar a implementação do Docker em uma aplicação ASP.NET Core utilizando o Docker Compose para orquestrar os dockersfile, utilizando .NET 8, um banco de dados não relacional MongoDB e volumes

## Tecnologias Utilizadas

- **.NET 8**: Framework principal utilizado para o desenvolvimento da aplicação.
- **ASP.NET Core MVC**: Camada de apresentação para exibir e gerenciar as interações do usuário.
- **MongoDB Driver**: Para o mapeamento objeto-não-relacional (ORM) e gerenciamento de dados com o MongoDB.
- **Injeção de Dependência**: Configurada para garantir um código modular e testável.
- **Repository Pattern**: Para centralizar a lógica de acesso a dados e promover o encapsulamento.
- **Swagger**: Para documentar a API e facilitar a interação com os endpoints.

## Configuração e Execução

### Pré-requisitos

- **Docker**
- **Docker-Compose**

### Passos para Executar

1. **Clonar o Repositório**:
   ```bash
   git clone https://github.com/gustavorenedev/CatalogAPI
   cd CatalogAPI
   ```

2. **Restaurar as Dependências**:
   ```bash
   dotnet restore
   ```

3. **Rodar a Aplicação com o Docker**:
   ```bash
   docker-compose up --build
   ```
  
4. A aplicação estará disponível em `https://localhost` na porta configurada.

## Rotas da API

### 1. Products

| Método | Rota                  | Descrição                             |
|--------|-----------------------|---------------------------------------|
| GET    | `/api/v1/Product`       | Obtém todos os produtos|               
| GET    | `/api/v1/Product{id}`  | Obtém um produto por ID|             
| GET    | `/api/v1/Product/GetProductByCategory{id}`  | Obtém produtos pela categoria|
| POST   | `/api/v1/Product`       | Cria um novo produto|
| PUT    | `/api/v1/Product`       | Atualiza um produto existente|
| DELETE | `/api/v1/Product{id}`  | Remove um produto por ID|


## Funcionalidades

- Criação, leitura, atualização e exclusão (CRUD) de dados de exemplo.
- Injeção de dependências configurada e aplicada em todos os serviços.
- API RESTful documentada com Swagger.

## Conclusão

Este projeto integra ASP.NET Core MVC com MongoDB utilizando Docker e Docker Compose para criar uma API eficiente, escalável e de fácil manutenção. Com boas práticas como injeção de dependência, Repository Pattern e documentação via Swagger, ele demonstra a implementação moderna de containers e serve como base sólida para futuras aplicações distribuídas
