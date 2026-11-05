# Api-Odonto

API REST desenvolvida em **Java** com **Spring Boot** para gerenciamento de agendamentos odontológicos e dentistas, com autenticação via JWT, controle de migrações com Flyway e pipeline de CI/CD via GitHub Actions.

---

## Tecnologias Utilizadas

- **Java 21**
- **Spring Boot 3 / 4** (Spring Web, Spring Data JPA, Spring Security, Validation)
- **MySQL** (Banco de dados relacional)
- **Flyway** (Controle de versões e migrações do banco)
- **Auth0 Java JWT** (Geração e validação de tokens JWT)
- **Docker** (Conteinerização da aplicação)
- **GitHub Actions** (Integração e validação contínua - CI/CD)

---

## Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto (ou configure as variáveis no seu ambiente):

```env
DB_URL=jdbc:mysql://localhost:3306/nome_do_banco?createDatabaseIfNotExist=true&serverTimezone=UTC
DB_USERNAME=seu_usuario
DB_PASSWORD=sua_senha
JWT_SECRET=seu_segredo_jwt_super_seguro
```
---

## CI/CD (GitHub Actions)

O repositório conta com um fluxo de CI/CD automatizado em `.github/workflows/agendamento-odontologico-cicd.yml` que:
1. Faz o checkout do código a cada `push` na branch `main`.
2. Configura o ambiente com **Java 21**.
3. Executa os testes automatizados com `mvn clean verify`.
4. Valida a construção da imagem **Docker**.
