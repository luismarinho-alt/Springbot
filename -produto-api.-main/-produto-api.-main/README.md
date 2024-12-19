# Produto API - Sistema de Cadastro de Produtos

Este é um projeto de backend para o **Cadastro de Produtos** usando **Spring Boot** e **Flyway** para versionamento de banco de dados. O sistema permite a criação, leitura, atualização e exclusão (CRUD) de produtos no banco de dados.

## Funcionalidades

- Cadastro de produtos
- Edição de produtos
- Exclusão de produtos
- Listagem de produtos
- Exibição de detalhes de um produto

## Tecnologias Utilizadas

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.
- **Flyway**: Ferramenta para versionamento de banco de dados.
- **JPA (Java Persistence API)**: Para mapeamento objeto-relacional e interação com o banco de dados.
- **MySQL**: Banco de dados para armazenamento dos dados dos produtos.
- **Git**: Controle de versão.

## Como Rodar o Projeto

### 1. Pré-requisitos

Certifique-se de que você tem o **Java 17** ou superior, **MySQL**, e **Maven** instalados no seu computador.

- **Java**: [Download Java](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- **MySQL**: [Download MySQL](https://dev.mysql.com/downloads/installer/)
- **Maven**: [Download Maven](https://maven.apache.org/download.cgi)

### 2. Clonar o Repositório

```bash
git clone https://github.com/luismarinho-alt/produto-api.git
```

### 3. Configurar o Banco de Dados

1. Abra o **XAMPP** e inicie o MySQL.
2. Crie o banco de dados com o comando:

```sql
CREATE DATABASE produto_db;
```

3. Configure a conexão com o banco de dados no arquivo `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/produto_db
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
```

> **Nota:** Certifique-se de que as portas 8080 e 3306 estejam livres.

### 4. Rodar a Aplicação

Após configurar o banco de dados, você pode rodar a aplicação usando Maven:

```bash
mvn spring-boot:run
```

O servidor será iniciado e estará disponível em: [http://localhost:8080](http://localhost:8080).

---

## Endpoints da API

Aqui estão os principais endpoints da API para gerenciamento de produtos:

### 1. Listar Produtos

- **URL:** `/api/produtos`
- **Método:** `GET`
- **Descrição:** Lista todos os produtos cadastrados.

#### Exemplo de cURL:

```bash
curl -X GET http://localhost:8080/api/produtos
```

#### Exemplo de Resposta:

```json
[
  {
    "id": 1,
    "nome": "Produto Exemplo",
    "descricao": "Descrição do produto",
    "preco": 29.99
  }
]
```

### 2. Cadastrar Produto

- **URL:** `/api/produtos`
- **Método:** `POST`
- **Descrição:** Cadastrar um novo produto.

#### Corpo da Requisição (JSON):

```json
{
  "nome": "Produto Exemplo",
  "descricao": "Descrição do produto",
  "preco": 29.99
}
```

#### Exemplo de cURL:

```bash
curl -X POST http://localhost:8080/api/produtos -H "Content-Type: application/json" -d '{"nome": "Produto Exemplo", "descricao": "Descrição do produto", "preco": 29.99}'
```

#### Exemplo de Resposta:

```json
{
  "id": 1,
  "nome": "Produto Exemplo",
  "descricao": "Descrição do produto",
  "preco": 29.99
}
```

### 3. Atualizar Produto

- **URL:** `/api/produtos/{id}`
- **Método:** `PUT`
- **Descrição:** Atualiza as informações de um produto existente.

#### Corpo da Requisição (JSON):

```json
{
  "nome": "Produto Atualizado",
  "descricao": "Nova descrição do produto",
  "preco": 39.99
}
```

#### Exemplo de cURL:

```bash
curl -X PUT http://localhost:8080/api/produtos/1 -H "Content-Type: application/json" -d '{"nome": "Produto Atualizado", "descricao": "Nova descrição do produto", "preco": 39.99}'
```

#### Exemplo de Resposta:

```json
{
  "id": 1,
  "nome": "Produto Atualizado",
  "descricao": "Nova descrição do produto",
  "preco": 39.99
}
```

### 4. Deletar Produto

- **URL:** `/api/produtos/{id}`
- **Método:** `DELETE`
- **Descrição:** Remove um produto pelo seu ID.

#### Exemplo de cURL:

```bash
curl -X DELETE http://localhost:8080/api/produtos/1
```

#### Exemplo de Resposta:

```json
{
  "mensagem": "Produto removido com sucesso."
}
```

---

## Considerações Finais

Este projeto é uma API REST simples para o gerenciamento de produtos. Sinta-se à vontade para fazer melhorias, adicionar novas funcionalidades e implementar boas práticas de segurança e autenticação. Se tiver dúvidas, abra uma issue no repositório.

**Desenvolvido por:** Luis Guilhermy

**GitHub:**[https://github.com/luismarinho-alt]

# Produto API - Sistema de Cadastro de Produtos

Este é um projeto de backend para o **Cadastro de Produtos** usando **Spring Boot** e **Flyway** para versionamento de banco de dados. O sistema permite a criação, leitura, atualização e exclusão (CRUD) de produtos no banco de dados.

## Funcionalidades

- Cadastro de produtos
- Edição de produtos
- Exclusão de produtos
- Listagem de produtos
- Exibição de detalhes de um produto

## Tecnologias Utilizadas

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.
- **Flyway**: Ferramenta para versionamento de banco de dados.
- **JPA (Java Persistence API)**: Para mapeamento objeto-relacional e interação com o banco de dados.
- **MySQL**: Banco de dados para armazenamento dos dados dos produtos.
- **Git**: Controle de versão.

## Como Rodar o Projeto

### 1. Pré-requisitos

Certifique-se de que você tem o **Java 17** ou superior, **MySQL**, e **Maven** instalados no seu computador.

- **Java**: [Download Java](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- **MySQL**: [Download MySQL](https://dev.mysql.com/downloads/installer/)
- **Maven**: [Download Maven](https://maven.apache.org/download.cgi)

### 2. Clonar o Repositório

```bash
git clone https://github.com/srjoaovitorsouzas/produto-api.git
```

### 3. Configurar o Banco de Dados

1. Abra o **XAMPP** e inicie o MySQL.
2. Crie o banco de dados com o comando:

```sql
CREATE DATABASE produto_db;
```

3. Configure a conexão com o banco de dados no arquivo `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/produto_db
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
```

> **Nota:** Certifique-se de que as portas 8080 e 3306 estejam livres.

### 4. Rodar a Aplicação

Após configurar o banco de dados, você pode rodar a aplicação usando Maven:

```bash
mvn spring-boot:run
```

O servidor será iniciado e estará disponível em: [http://localhost:8080](http://localhost:8080).

---

## Endpoints da API

Aqui estão os principais endpoints da API para gerenciamento de produtos:

### 1. Listar Produtos

- **URL:** `/api/produtos`
- **Método:** `GET`
- **Descrição:** Lista todos os produtos cadastrados.

#### Exemplo de cURL:

```bash
curl -X GET http://localhost:8080/api/produtos
```

#### Exemplo de Resposta:

```json
[
  {
    "id": 1,
    "nome": "Produto Exemplo",
    "descricao": "Descrição do produto",
    "preco": 29.99
  }
]
```

### 2. Cadastrar Produto

- **URL:** `/api/produtos`
- **Método:** `POST`
- **Descrição:** Cadastrar um novo produto.

#### Corpo da Requisição (JSON):

```json
{
  "nome": "Produto Exemplo",
  "descricao": "Descrição do produto",
  "preco": 29.99
}
```

#### Exemplo de cURL:

```bash
curl -X POST http://localhost:8080/api/produtos -H "Content-Type: application/json" -d '{"nome": "Produto Exemplo", "descricao": "Descrição do produto", "preco": 29.99}'
```

#### Exemplo de Resposta:

```json
{
  "id": 1,
  "nome": "Produto Exemplo",
  "descricao": "Descrição do produto",
  "preco": 29.99
}
```

### 3. Atualizar Produto

- **URL:** `/api/produtos/{id}`
- **Método:** `PUT`
- **Descrição:** Atualiza as informações de um produto existente.

#### Corpo da Requisição (JSON):

```json
{
  "nome": "Produto Atualizado",
  "descricao": "Nova descrição do produto",
  "preco": 39.99
}
```

#### Exemplo de cURL:

```bash
curl -X PUT http://localhost:8080/api/produtos/1 -H "Content-Type: application/json" -d '{"nome": "Produto Atualizado", "descricao": "Nova descrição do produto", "preco": 39.99}'
```

#### Exemplo de Resposta:

```json
{
  "id": 1,
  "nome": "Produto Atualizado",
  "descricao": "Nova descrição do produto",
  "preco": 39.99
}
```

### 4. Deletar Produto

- **URL:** `/api/produtos/{id}`
- **Método:** `DELETE`
- **Descrição:** Remove um produto pelo seu ID.

#### Exemplo de cURL:

```bash
curl -X DELETE http://localhost:8080/api/produtos/1
```

#### Exemplo de Resposta:

```json
{
  "mensagem": "Produto removido com sucesso."
}
