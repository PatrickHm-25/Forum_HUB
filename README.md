# 📚 FórumHub - API de Fórum com Spring Boot

## 📌 Sobre o Projeto
O **FórumHub** é uma API REST desenvolvida em **Java** com **Spring Boot**, criada com o objetivo de simular um sistema de fórum.  
Nele é possível realizar operações de cadastro de usuários, autenticação via **JWT**, além do gerenciamento de tópicos (criação, atualização, listagem e detalhamento).

⚠️ **Atenção:** Este projeto foi desenvolvido **exclusivamente para fins acadêmicos** e de aprendizado, não devendo ser utilizado em produção.

---

## 🚀 Tecnologias Utilizadas
- **Java 17+**
- **Spring Boot 3+**
- **Spring Security + JWT**
- **Spring Data JPA / Hibernate**
- **MySQL**
- **Flyway** (migrações do banco)
- **Insomnia/Postman** (para testes)

---

## 🔑 Funcionalidades
- Cadastro de usuários
- Login e autenticação com **JWT**
- CRUD de tópicos:
  - Criar novo tópico
  - Atualizar tópico
  - Listar tópicos
  - Detalhar tópico por ID
- Segurança aplicada via **Spring Security** (apenas usuários autenticados podem acessar os endpoints protegidos)

---

## ⚙️ Como Executar o Projeto

### 1. Clonar o repositório
```bash
git clone https://github.com/seu-usuario/forumhub.git
```

### 2. Configurar o banco de dados
Crie um banco no MySQL (por exemplo `forumhub_db`) e configure o arquivo `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/forumhub_db
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=validate
spring.flyway.enabled=true
```

### 3. Rodar a aplicação
```bash
./mvnw spring-boot:run
```
A aplicação estará disponível em:  
👉 `http://localhost:8080`

---

## 🔐 Autenticação
1. Realize o **login** enviando `login` e `senha` no endpoint:
   ```
   POST /login
   ```
2. Copie o **token JWT** retornado.
3. Para acessar os endpoints protegidos, adicione no **Header**:
   ```
   Authorization: Bearer seu_token_aqui
   ```

---

## 📌 Exemplos de Endpoints

### Criar usuário
```
POST /usuarios
{
  "login": "patrick",
  "senha": "123456"
}
```

### Criar tópico
```
POST /topicos
{
  "autor": "Patrick",
  "titulo": "Título do Tópico",
  "mensagem": "Conteúdo da mensagem",
  "curso": "Nome do Curso",
  "status": "Ativo",
  "dataCriacao": "16/08/2025"
}
```

---

## 📖 Observação Importante
Este projeto foi desenvolvido apenas para **estudo** das seguintes práticas:
- Estruturação de APIs REST com **Spring Boot**  
- Autenticação e autorização com **JWT**  
- Versionamento de banco de dados com **Flyway**  
- Boas práticas de **segurança e organização de código**

---

## 👨‍💻 Autor
Desenvolvido por **Patrick Henrique**  
📌 Projeto acadêmico - 2025
