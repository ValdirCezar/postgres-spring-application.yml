# postgres-spring-application.yml

### A simple application.yml to configure postgres at Spring project

#### application.yml
```yml
server:
  port: ${PORT:9090}
spring:
  application:
    name: <APP-NAME>

  #Database
  datasource:
    driver-class-name: org.postgresql.Driver
    username: admin
    password: 123456
    url: jdbc:postgresql://localhost:5432/<DB-NAME>

  # JPA properties
  jpa:
    hibernate:
      ddl-auto: create-drop
    show-sql: true
    database: postgresql
    database-platform: org.hibernate.dialect.PostgreSQLDialect
    open-in-view: false
    generate-ddl: true

  # Logger configuration
  logging:
    pattern:
      console: "%d %-5level %logger : %msg%n"
    level:
      org.springframework: info
      org.hibernate: debug
```
