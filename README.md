# Challenge Foro Hub

API REST desarrollada con **Java y Spring Boot** que permite gestionar discusiones en un foro.
Los usuarios pueden crear temas, consultar discusiones y participar en conversaciones dentro de la plataforma.

Este proyecto fue desarrollado como práctica de backend utilizando arquitectura en capas y buenas prácticas de desarrollo con Spring.

---

## Tecnologías utilizadas

* Java 18
* Spring Boot
* Spring Data JPA
* Spring Security
* MySQL
* Maven
* Lombok

---

## Arquitectura del proyecto

El proyecto sigue una arquitectura en capas común en aplicaciones Spring Boot.

```
controller
service
repository
model
dto
config
security
```

### Descripción de capas

**Controller**

Gestiona las peticiones HTTP de la API.

**Service**

Contiene la lógica de negocio de la aplicación.

**Repository**

Se encarga de la comunicación con la base de datos mediante JPA.

**Entity**

Representa las tablas de la base de datos.

---

## Endpoints principales

### Obtener todos los threads

```
GET /threads
```

### Crear un thread

```
POST /threads
```

Ejemplo de request:

```json
{
  "title": "Primer tema del foro",
  "content": "Este es un mensaje de prueba"
}
```

---

## Configuración de base de datos

Archivo `application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/devforum
spring.datasource.username=root
spring.datasource.password=root

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## Ejecutar el proyecto

Clonar el repositorio:

```
git clone https://github.com/TU-USUARIO/devforum-api.git
```

Entrar al proyecto:

```
cd devforum-api
```

Ejecutar la aplicación:

```
mvn spring-boot:run
```

La API estará disponible en:

```
http://localhost:8080
```

---

