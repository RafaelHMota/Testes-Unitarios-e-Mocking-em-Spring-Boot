# 🧪 API de Usuários - Spring Boot + JUnit + Mockito

Este projeto é uma API RESTful simples para gerenciamento de usuários, desenvolvida com Spring Boot, MariaDB, JUnit 5 e Mockito. Inclui testes unitários para o serviço de usuário.

---

## ✅ Tecnologias utilizadas

- Java 11+
- Spring Boot (Web, Data JPA)
- MariaDB
- JUnit 5
- Mockito
- Maven

---

## 🚀 Como rodar a aplicação

### Pré-requisitos

- Java 11+ instalado
- MariaDB rodando localmente
- IDE (VS Code, IntelliJ ou outra)
- Maven instalado

### Configuração do banco de dados

1. Crie o banco de dados no MariaDB:

CREATE DATABASE usuariosdb;

2. Configure o arquivo src/main/resources/application.properties:
```sql
spring.datasource.url=jdbc:mariadb://localhost:3306/usuariosdb
spring.datasource.username=root
spring.datasource.password=1234

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

⚠️ Ajuste username e password conforme sua instalação do MariaDB.

Rodando a aplicação

No terminal, execute:
```
mvn spring-boot:run
```
A aplicação estará disponível em:
📍 http://localhost:8080

📫 Endpoints disponíveis
```
Método	Endpoint	Descrição
GET	/users	Lista todos os usuários
GET	/users/{id}	Busca usuário por ID
POST	/users	Cria um novo usuário
DELETE	/users/{id}	Deleta um usuário existente
```

Exemplo de requisição POST /users
```
{
  "name": "Rafa",
  "email": "rafa@email.com"
}
```

🧪 Executando os testes unitários
Para rodar os testes com JUnit e Mockito, utilize o comando:

```
mvn test
```

O que está sendo testado?
A classe UserServiceTest cobre o método getAllUsers usando mock do repositório.

Se tudo estiver certo, a saída será:

```
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] BUILD SUCCESS
```

📁 Estrutura do projeto
```
usuario-api/
├── src/
│   ├── main/
│   │   ├── java/com/exemplo/usuarioapi/
│   │   │   ├── UsuarioApiApplication.java
│   │   │   ├── model/User.java
│   │   │   ├── repository/UserRepository.java
│   │   │   ├── service/UserService.java
│   │   │   └── controller/UserController.java
│   └── test/
│       └── java/com/exemplo/usuarioapi/service/UserServiceTest.java
├── pom.xml
└── README.md
```
