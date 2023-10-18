# Desafio Santander Bootcamp 2023 - JAVA
Repositório contendo a replicação do Desafio Santander Bootcamp 2023 em Java. Nesta tarefa, reproduzi com sucesso o desafio proposto, 
criando uma API RESTful em Java com o poder do Spring Boot 3. Explore o código para descobrir as inovações implementadas! 🚀

## Diagrama de Classes (Domínio da API)
```mermaid
classDiagram
  class User {
    -String name
    -Account account
    -Feature[] features
    -Card card
    -News[] news
  }

  class Account {
    -String number
    -String agency
    -Number balance
    -Number limit
  }

  class Feature {
    -String icon
    -String description
  }

  class Card {
    -String number
    -Number limit
  }

  class News {
    -String icon
    -String description
  }

  User "1" *-- "1" Account 
  User "1" *-- "N" Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News
