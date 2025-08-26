# 404 Not Found – Backend

Este es el backend del proyecto **404 Not Found**, desarrollado con **Spring Boot** y **PostgreSQL**.  
Proporciona una API REST para gestionar **clientes, artistas y catálogos** de camisetas con estampas.

El frontend de este proyecto está en [404-notfound-frontend](https://github.com/dogeuf02/404-notfound-frontend).

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

```


## ▶️ Ejecución

Con Maven Wrapper:
```
./mvnw spring-boot:run
```
O con Maven:
```
mvn spring-boot:run
```

La aplicación quedará disponible en:

http://localhost:8080

---

## 📌 Endpoints principales

### -ClienteController (/clientes)
GET /clientes → Obtiene todos los clientes

POST /clientes → Crea un nuevo cliente

PUT /clientes/{id} → Actualiza un cliente existente

DELETE /clientes/{id} → Elimina un cliente

### -ArtistaController (/artistas)
GET /artistas → Lista todos los artistas

POST /artistas → Registra un artista

PUT /artistas/{id} → Edita un artista

DELETE /artistas/{id} → Elimina un artista

### -CatalogoController (/catalogo)
GET /catalogo → Obtiene el catálogo de camisetas/estampas

POST /catalogo → Añade un nuevo ítem al catálogo

PUT /catalogo/{id} → Modifica un ítem existente

DELETE /catalogo/{id} → Borra un ítem

---

## 📂 Estructura del proyecto
```
src/main/java/com/404notFound/demo
 ┣ controller
 ┃ ┣ ArtistaController.java
 ┃ ┣ ClienteController.java
 ┃ ┗ CatalogoController.java
 ┣ entity
 ┣ repository
 ┣ service
 ┗ DemoApplication.java
```

---

👤 Autores
Proyecto desarrollado por:

```
-David Stiven Muñoz Amaya 
-Jose Jesus Cespedes Rivera 
-Juan Diego Acosta Molina 
-Laura Daniela Cubillos Escobar 
-Sofía Lozano Martínez
```
