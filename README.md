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

### 🔧 Pré-requisitos

- Java 11+ instalado
- MariaDB instalado e rodando
- IDE (VS Code, IntelliJ ou outro)
- Maven

### 📁 Banco de dados

Crie o banco de dados no MariaDB:

```sql
CREATE DATABASE usuariosdb;
Usuário e senha padrão estão definidos em src/main/resources/application.properties:

ini
Copiar
Editar
spring.datasource.url=jdbc:mariadb://localhost:3306/usuariosdb
spring.datasource.username=root
spring.datasource.password=1234
Altere conforme necessário.

▶️ Rodando a aplicação
No terminal, execute:

bash
Copiar
Editar
mvn spring-boot:run
A aplicação estará disponível em: http://localhost:8080

📫 Endpoints disponíveis
🔹 Listar todos os usuários
bash
Copiar
Editar
GET /users
🔹 Buscar usuário por ID
bash
Copiar
Editar
GET /users/{id}
🔹 Criar novo usuário
bash
Copiar
Editar
POST /users
Content-Type: application/json

{
  "name": "Rafa",
  "email": "rafa@email.com"
}
🔹 Deletar usuário
bash
Copiar
Editar
DELETE /users/{id}
🧪 Executando os testes unitários
Para rodar os testes unitários com JUnit e Mockito:

bash
Copiar
Editar
mvn test
✔️ Teste implementado
A classe UserServiceTest realiza o teste do método getAllUsers usando Mockito para simular o repositório.

Esperado:

Os testes devem rodar com sucesso

Saída esperada:

yaml
Copiar
Editar
[INFO] Tests run: 1, Failures: 0, Errors: 0, Skipped: 0
[INFO] BUILD SUCCESS
📁 Estrutura do projeto
swift
Copiar
Editar
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
