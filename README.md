# 404 Not Found – Backend

Este es el backend del proyecto **404 Not Found**, desarrollado con **Spring Boot** y **PostgreSQL**.  
Proporciona una API REST para gestionar **clientes, artistas y catálogos** de camisetas estampadas.

---

## 🚀 Tecnologías usadas
- **Java 17**
- **Spring Boot 3.3.5**
  - Spring Web
  - Spring Data JPA
  - Spring Data REST
  - Spring Boot Actuator
- **PostgreSQL** (driver JDBC)
- **Maven**
- **Lombok**

---

## ⚙️ Requisitos previos
- Tener instalado:
  - Java 17+
  - Maven 3.9+
  - PostgreSQL
- Crear una base de datos en PostgreSQL (ejemplo: `notfound_db`).

---

## 🔧 Configuración

En `src/main/resources/application.properties` debes configurar tu conexión a PostgreSQL:  

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/notfound_db
spring.datasource.username=YOUR_USER
spring.datasource.password=YOUR_PASSWORD
spring.datasource.driver-class-name=org.postgresql.Driver

# JPA / Hibernate
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

# Puerto del servidor
server.port=8080
