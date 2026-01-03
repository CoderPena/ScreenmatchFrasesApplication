# 🎬 ScreenMatch Frases API

Este projeto é um **backend em Spring Boot** desenvolvido como desafio prático para consolidação de conhecimentos em **APIs REST, Spring Data JPA e integração front-end/back-end**.

A aplicação fornece **frases aleatórias de filmes e séries**, permitindo que um front-end consuma essas informações de forma dinâmica a cada requisição.

---

## 🚀 Funcionalidades

- Retorno de frases aleatórias de filmes e séries
- Integração com front-end via API REST
- Persistência de dados com PostgreSQL
- Criação automática de tabelas com JPA
- Arquitetura organizada em camadas (Model, Repository, Service, Controller)

---

## 📡 Endpoint disponível

### Buscar frase aleatória

GET /series/frases

### Exemplo de resposta

```json
{
  "titulo": "Rocky Balboa",
  "frase": "Não importa o quão forte você bate, mas o quanto aguenta apanhar.",
  "personagem": "Rocky",
  "poster": "https://url-do-poster.com/rocky.jpg"
}
```

⚠️ **Atenção:** Os nomes dos campos devem ser exatamente esses, pois o front-end depende desse padrão.

---

## 🛠️ Tecnologias utilizadas

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- PostgreSQL
- Maven
- Hibernate

---

## ⚙️ Configuração do banco de dados

A aplicação utiliza **variáveis de ambiente** para configuração do banco:

```properties
spring.datasource.url=jdbc:postgresql://${DB_HOST}/${DB_NAME}
spring.datasource.username=${DB_USER}
spring.datasource.password=${DB_PASSWORD}
spring.datasource.driver-class-name=org.postgresql.Driver

spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.format-sql=true
```

### Variáveis esperadas

- DB_HOST → host do banco (ex: localhost:5432)
- DB_NAME → nome do banco
- DB_USER → usuário do PostgreSQL
- DB_PASSWORD → senha do PostgreSQL

📌 O banco de dados **deve ser criado manualmente** antes da execução.

---

## ▶️ Executando o projeto

1. Clone este repositório
2. Configure as variáveis de ambiente
3. Crie o banco `screenmatch_frases` no PostgreSQL
4. Execute a aplicação pela classe principal:

ScreenmatchFrasesApplication

A aplicação será iniciada em:

http://localhost:8080

---

## 🎯 Objetivo educacional

Este projeto foi desenvolvido como um **desafio de consolidação**, aplicando conceitos de:
- Modelagem de entidades
- Persistência com JPA
- Criação de APIs REST
- Integração com front-end
- Organização em camadas

---

🚀 **Bora evoluir!** Sinta-se à vontade para adicionar novas frases, endpoints ou melhorias.
