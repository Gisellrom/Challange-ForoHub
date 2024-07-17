# Challenge-Foro-Hub


## Objetivo: 

Construir el back end de un foro mediante la creación de una API REST con las siguientes funcionalidades:

- Rutas de la API diseñadas siguiendo las mejores prácticas del modelo REST.
- Validaciones aplicadas de acuerdo a las reglas de negocio.
- Implementación de una base de datos relacional para asegurar la persistencia de los datos.
- Servicio de autenticación y autorización para controlar el acceso a la información.
  
## Tecnologias utilizadas

- IDE (Entorno de desenvolvimento integrado) IntelliJ IDEA- opcional -

- Java JDK: versión: 17 en adelante 

- Maven: versión 4 en adelante

- Spring: versión 3.2.3 - https://start.spring.io/

- MySQL: versión 8 en adelante 



Configuración al crear el proyecto en Spring Initializr:

- Java (versión 17 en adelante)

- Maven (Initializr utiliza la versión 4)

- Spring Boot (versión 3.2.3)

- Proyecto en JAR

Dependencias para agregar al crear el proyecto con Spring Initializr:

- Lombok

- Spring Security
  
- Spring Web

- MySQL Driver

- Spring Data JPA

- Spring Boot DevTools

- Flyway Migration

- Validation




## Cómo probar esta API


- Modificar el archivo: [application.properties](./literalura/src/main/resources/application.properties) reemplazando las varibles
  DB_NAME -> por el nombre de una base de datos creada
  DB_USER -> el nombre de usuario
  DB_PASSWORD -> Contraseña

- Luego, ejecutar el archivo principal


## Funcionalidad

**Registro (con permiso USER por defecto)**

- Ruta:

```
POST: /api/auth/registro 
```

- Parametros para enviar en el cuerpo del json:

```
{
    "nombre":"Juan Perez",
    "email":"juanp@mail.com",
    "clave":"password1234"
}	

```

**Autenticarse**

- Ruta:

```
POST: /auth/login

```
- En el cuerpo:

```
{
    "email":"juanp@gmail.com",
    "clave":"password1234"
}
```
---

**Crear un tema**

- Ruta:

```
POST: /api/temas
```

- Cuerpo:

```
{
    "titulo":"Tengo un problema",
    "mensaje":"Borré la base de datos",
    "usuario_id": "1",
    "nombre_curso":"Bases de Datos Avanzadas"
}
```

**Obtener todos los temas**


- Ruta:

```
GET: /api/temas
```

- Cuerpo:

```
{ 
}
```
**Obtener un tema por id**
- Ruta:

```
GET: /api/temas/{id}
```

- Cuerpo:

```
{   
}
```
**Actualizar un tema**
- Ruta:

```
UPDATE: /api/temas/{id}
```

- Cuerpo:

```
{
    "id": 0,
    "titulo": "string",
    "mensaje": "string",
    "status": "ABIERTO/CERRADO"
}
```

**Borrar un tema (borrado lógico)**

- Ruta:

```
DELETE: /api/temas/{id}
```

- Cuerpo:

```
{   
}
```

---


## Proyecto en construccion

Los endpoints usuarios/respuestas ya son funcionales pero todavia se están trabajando
