Backend Project with Spring Boot

This project is a backend application built with Spring Boot 3, which exposes a REST API for managing users, orders, and products.  

Main Features

Architecture based on Controller – Service – Repository.
Sample data loaded from a JSON file in memory.
Integration with MongoDB using Spring Data.
Unit tests implemented for controllers, services, and models.
REST endpoints to:
Get the list of users.
Retrieve a user's orders.
List products from a specific order.

Project Structure

src/main/java/org/proyectdemo/
├── controller # Controladores REST
├── model # Entidades: Usuario, Orden, Producto
├── repository # Repositorio de datos (MongoDB)
├── service # Lógica de negocio
└── Application # Clase principal de Spring Boot

src/test/java/org/proyectdemo/
├── model
│ ├── OrdenTest
│ ├── ProductoTest
│ └── UsuarioTest
├── UsuarioControllerTest
├── UsuarioServiceMongoDbTest
└── UsuarioServiceTest


Example Endpoints
- `GET /usuarios/picker` → Lista de usuarios simplificada.  
- `GET /usuarios/{id}/ordenes/picker` → Órdenes de un usuario.  
- `GET /usuarios/{idUsuario}/ordenes/{idOrden}/productos` → Productos de una orden.  

Technologies Used
- Java 17 
- Spring Boot 3  
- Spring Web  
- Spring Data MongoDB  
- Maven  
- JUnit 5 (para tests)  
- Mockito (para mocks en los tests)  

 Unit Tests
The project includes unit tests to ensure code quality and proper functionality:

- Modelos:`OrdenTest`, `ProductoTest`, `UsuarioTest`  
- Controladores: `UsuarioControllerTest`  
- Servicios: `UsuarioServiceTest`, `UsuarioServiceMongoDbTest`  
  
To run the tests:
```bash
mvn test

Project Architecture

flowchart TD
    C[Cliente / Frontend] -->|HTTP REST| A[Controladores REST]
    A --> B[Servicios]
    B --> D[Repositorio]
    D --> M[(MongoDB)]
    B --> J[Datos JSON de prueba]

Run
mvn spring-boot:run

Run the Test
mvn test

The service will be available at:
 http://localhost:8080

Contact
Phone Number: +54 9 341 586-3212

Email: bpstyga@gmail.com

LinkedIn: Bruno Pstyga

 GitHub: @brunopstyga










