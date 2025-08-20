🧠 ForumHub

API de fórum de perguntas e respostas desenvolvida em Java com Spring Boot, inspirada em fóruns como o da Alura.
O objetivo é praticar a construção de APIs REST seguras, com autenticação JWT, persistência com JPA, e controle de versão do banco com Flyway.

🚀 Tecnologias utilizadas

Java 21

Spring Boot 3.5

Spring Web

Spring Security

Spring Data JPA

MySQL

Flyway (controle de versões do banco)

Swagger UI (documentação da API)

Maven

JWT (JSON Web Token)

⚙️ Funcionalidades

Cadastro e autenticação de usuários

Criação, listagem, atualização e exclusão de tópicos

Respostas em tópicos

Proteção de rotas com JWT

Validações com Bean Validation (@Valid)

Documentação de endpoints com Swagger

Migrations com Flyway

🛠️ Como executar localmente
✅ Pré-requisitos

Java 21

MySQL rodando na porta padrão (3306)

Maven

📥 Passos
# 1. Clone o repositório
git clone https://github.com/seu-usuario/forumhub.git
cd forumhub

# 2. Configure o banco de dados em src/main/resources/application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/forumhub
spring.datasource.username=root
spring.datasource.password=sua_senha

# 3. Rode a aplicação
./mvnw spring-boot:run

📖 Documentação com Swagger

Após rodar o projeto, acesse:

👉 http://localhost:8080/swagger-ui.html

Por lá é possível testar os endpoints diretamente pela interface.

🔐 Autenticação JWT

Endpoint de login: POST /auth/login

Envie usuário e senha válidos

Receba um token JWT e utilize-o no cabeçalho das requisições:

Authorization: Bearer seu_token_aqui

🧾 Migrations com Flyway

A estrutura do banco de dados é controlada pelo Flyway.
As migrations estão na pasta:

src/main/resources/db/migration/


Se uma migration falhar, rode:

./mvnw flyway:repair

🗂️ Estrutura do projeto
forumhub
├── controller   # Endpoints REST
├── dto          # Objetos de transferência de dados
├── entity       # Entidades JPA
├── repository   # Interfaces de acesso ao banco
├── service      # Regras de negócio
└── infra        # Segurança, exceções e configs

📌 Status do projeto

🟡 Em desenvolvimento