# 📝 Blog Pessoal API

<br />

<div align="center">
  <img src="https://img.shields.io/github/languages/top/raissa-sf/blogpessoal?style=flat-square" />
  <img src="https://img.shields.io/github/repo-size/raissa-sf/blogpessoal?style=flat-square" />
  <img src="https://img.shields.io/github/languages/count/raissa-sf/blogpessoal?style=flat-square" />
  <img src="https://img.shields.io/github/last-commit/raissa-sf/blogpessoal?style=flat-square" />
</div>

---

## 📖 Sobre o Projeto

O **Blog Pessoal API** é uma aplicação backend desenvolvida com **Java 21** e **Spring Boot**, responsável pelo gerenciamento de usuários, temas e postagens de um blog.

A aplicação segue os princípios de uma arquitetura REST e implementa autenticação e autorização utilizando **Spring Security** e **JWT (JSON Web Token)**.

Este projeto foi desenvolvido com o objetivo de praticar conceitos fundamentais do desenvolvimento backend moderno, incluindo:

* APIs REST;
* Persistência de dados com JPA/Hibernate;
* Relacionamentos entre entidades;
* Spring Security;
* JWT Authentication;
* Documentação com Swagger/OpenAPI;
* Boas práticas de organização em camadas.

---

## 🏗️ Arquitetura do Sistema

O projeto está organizado nas seguintes classes e pacotes:

| Classe / Componente        | Descrição                                                                   |
| :------------------------- | :-------------------------------------------------------------------------- |
| **BlogpessoalApplication** | Classe principal responsável pela inicialização da aplicação Spring Boot.   |
| **UsuarioController**      | Gerencia os endpoints relacionados aos usuários.                            |
| **TemaController**         | Gerencia os endpoints relacionados aos temas.                               |
| **PostagemController**     | Gerencia os endpoints relacionados às postagens.                            |
| **UsuarioService**         | Implementa as regras de negócio relacionadas aos usuários e autenticação.   |
| **UsuarioRepository**      | Responsável pelo acesso aos dados dos usuários.                             |
| **TemaRepository**         | Responsável pelo acesso aos dados dos temas.                                |
| **PostagemRepository**     | Responsável pelo acesso aos dados das postagens.                            |
| **Usuario**                | Entidade que representa os usuários da aplicação.                           |
| **Tema**                   | Entidade responsável pela categorização das postagens.                      |
| **Postagem**               | Entidade que representa as publicações do blog.                             |
| **UsuarioLogin**           | DTO utilizado durante o processo de autenticação.                           |
| **SecurityConfig**         | Configuração de segurança da aplicação.                                     |
| **JwtService**             | Serviço responsável pela geração e validação de tokens JWT.                 |
| **JwtAuthFilter**          | Filtro de autenticação baseado em JWT.                                      |
| **UserDetailsImpl**        | Implementação das informações de autenticação do usuário.                   |
| **UserDetailsServiceImpl** | Serviço utilizado pelo Spring Security para carregar usuários autenticados. |
| **SwaggerConfig**          | Configuração da documentação da API utilizando Swagger/OpenAPI.             |

---

## 📂 Modelo de Dados

### Usuário

* id
* nome
* usuario
* senha
* foto

### Tema

* id
* descricao

### Postagem

* id
* titulo
* texto
* data

### Relacionamentos

* Um usuário pode criar várias postagens.
* Um tema pode estar associado a várias postagens.
* Cada postagem pertence a um usuário e a um tema.

---

## 🚀 Tecnologias Utilizadas

* Java 21
* Spring Boot 3
* Spring Data JPA
* Hibernate
* Spring Security
* JWT
* PostgreSQL
* MySQL
* Maven
* Swagger/OpenAPI

---

## 📋 Requisitos

Para executar o projeto localmente você precisará de:

* Java JDK 21
* Maven
* PostgreSQL ou MySQL
* STS (Spring Tool Suite) ou IntelliJ IDEA

---

## ⚙️ Configuração do Banco de Dados

Configure o arquivo:

```properties
src/main/resources/application.properties
```

Exemplo:

```properties
spring.datasource.url=jdbc:postgresql://localhost/blogpessoal
spring.datasource.username=postgres
spring.datasource.password=senha

spring.jpa.hibernate.ddl-auto=update
```

---

## ▶️ Como Executar o Projeto

### 1. Clonar o Repositório

```bash
git clone https://github.com/raissa-sf/blogpessoal.git
```

### 2. Importar no STS

1. Abra o STS.
2. Clique em:
   File → Import...
3. Selecione:
   Maven → Existing Maven Projects
4. Escolha a pasta do projeto.
5. Clique em Finish.

### 3. Executar a Aplicação

Abra a classe:

```java
BlogpessoalApplication.java
```

Execute como:

```text
Spring Boot App
```

A aplicação ficará disponível em:

```text
http://localhost:8080
```

---

## 📚 Documentação da API

Após iniciar a aplicação, a documentação Swagger estará disponível em:

```text
http://localhost:8080/swagger-ui.html
```

ou

```text
http://localhost:8080/swagger-ui/index.html
```

---

## 🔒 Segurança

A API utiliza:

* Spring Security
* JWT Authentication
* Criptografia de senhas com BCrypt
* Controle de autenticação por token

---

## 🤝 Contribuições

Este projeto possui fins educacionais, mas contribuições são sempre bem-vindas.

Você pode:

* Criar uma issue para relatar bugs;
* Sugerir melhorias;
* Enviar pull requests.

### Como contribuir

1. Faça um Fork do projeto.
2. Crie uma Branch:

```bash
git checkout -b feature/NovaFuncionalidade
```

3. Faça suas alterações:

```bash
git commit -m "Adiciona nova funcionalidade"
```

4. Envie para o GitHub:

```bash
git push origin feature/NovaFuncionalidade
```

5. Abra um Pull Request.

---

## 👩‍💻 Autora

Desenvolvido por **Raissa Santos Feitosa**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/raissa-santos-feitosa-73485b1a3/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/raissa-sf)


