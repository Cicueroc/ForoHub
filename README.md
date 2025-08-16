
[README.md](https://github.com/user-attachments/files/21818516/README.md)
# API ForoHub

La **API ForoHub** es una solución backend para gestionar tópicos de discusión en una
plataforma de foro. Desarrollada con **Java** y **Spring Boot**, incluye un sistema de
autenticación con **JWT** y permite realizar operaciones CRUD sobre los tópicos, usuarios y respuestas.

## Tecnologías Usadas

* **Java 17+**: Lenguaje de programación.
* **Spring Boot**: Framework para desarrollo ágil.
* **Spring Security & JWT**: Autenticación y autorización.
* **Spring Data JPA**: Mapeo ORM.
* **MySQL/MariaDB**: Base de datos.
* **Flyway**: Gestión de migraciones.
* **Maven**: Gestión de dependencias.

## Funcionalidades

* **Gestión de Usuarios**: Registro, autenticación y CRUD de usuarios.
* **Gestión de Tópicos**: Crear, consultar, actualizar y eliminar tópicos.
* **Gestión de Respuestas**: CRUD completo para respuestas.

## Configuración y Ejecución

### Requisitos

* **Java 17+**, **Maven**, **MySQL/MariaDB**.

### Pasos:

1. Clona el repositorio:

   ```bash
   git clone https://github.com/tu-usuario/api-forohub.git
   cd api-forohub
   ```

2. Configura `application.properties` con tus credenciales de base de datos:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/forohub_db
   spring.datasource.username=usuario_db
   spring.datasource.password=contraseña_db
   ```

3. Construye el proyecto:

   ```bash
   mvn clean install
   ```

4. Ejecuta la aplicación:

   ```bash
   mvn spring-boot:run
   ```

## Uso de la API

### Registro de Usuario

**POST** `/usuarios/registrar`

Body:

```json
{
  "nombre": "usuario",
  "email": "usuario@example.com",
  "password": "mi_password_segura"
}
```

### Login y Obtener Token JWT

**POST** `/usuarios/login`

Body:

```json
{
  "email": "usuario@example.com",
  "password": "mi_password_segura"
}
```



## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.
