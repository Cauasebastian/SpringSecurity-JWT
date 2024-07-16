# Autenticação e Autorização com Spring Security e JWT

Esse projeto foi feito como uma forma simples de estudar e implementar uma aplicação com Spring Security e JWT.

## Tecnologias Utilizadas
- Spring Boot
- Spring MVC
- Spring Security
- Spring Data JDBC
- H2 (banco de dados em memória)

## Como Executar o Projeto

### Clonar o Repositório Git:
```bash
git clone https://github.com/giuliana-bezerra/spring-security-jwt.git
```
### Construir o Projeto:
```bash
./mvnw clean package
```
### Executar o Aplicativo:
```bash
java -jar ./target/spring-security-jwt-0.0.1-SNAPSHOT.jar
```
## Testar as Requisições (usando Postman):
Faça uma requisição POST para ```bash http://localhost:8080/authenticate ``` com as credenciais no formato username:password. O token JWT gerado será retornado na resposta.

Acessar Rota Protegida com Bearer Token:
Faça uma requisição GET para ```bash http://localhost:8080/private ``` .No cabeçalho da requisição, inclua o token JWT gerado anteriormente no formato Bearer <token>.

# Aviso
Para conseguir fazer uma requisição, o banco de dados também deve estar populado. No caso deste projeto, há dois arquivos SQL populando o banco de dados:

### Script de Criação da Tabela:
```bash
CREATE TABLE IF NOT EXISTS `users` (
  `username` VARCHAR(255) NOT NULL PRIMARY KEY,
  `password` VARCHAR(255) NOT NULL
);
```
### Script de Inserção de Usuário:
```bash
INSERT INTO USERS (username, password) VALUES ('username', '$2a$10$GiseHkdvwOFr7A9KRWbeiOmg/
```
