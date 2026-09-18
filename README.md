# MesajilApi — Backend REST

API REST desarrollada en **ASP.NET Core (.NET 8)** para la gestión del aplicativo E-Commerce de **Mesajil Hnos.** Proporciona soporte a la aplicación móvil (Android) y gestiona operaciones de catálogo, ventas, inventario, autenticación y carritos de compras.

Desplegada en la nube a través de **Render**.

---

## 🛠️ Tecnologías y Arquitectura

* **Framework:** ASP.NET Core Web API (.NET 8)
* **Base de datos / ORM:** MySQL con Entity Framework Core
* **Seguridad & Autenticación:** JWT (JSON Web Tokens) y BCrypt.Net
* **Documentación API:** Swagger / OpenAPI UI
* **Contenedores:** Docker
* **Inyección de Dependencias:** Contenedor nativo de .NET
* **Patrón de Arquitectura:** Arquitectura por capas desacoplada
  * **Controllers:** Exposición de endpoints HTTP/REST.
  * **Services:** Lógica de negocio y reglas del sistema.
  * **Repositories:** Capa de persistencia y consultas Entity Framework.
  * **DTOs & Mappings:** Desacoplamiento entre modelos de base de datos y contrato de la API.

---

## 📁 Estructura del Proyecto

```text
MesajilApi/
├── Controllers/      # Endpoints REST (Usuario, Producto, Pedido, Carrito, etc.)
├── Services/         # Lógica de negocio e integración
├── Repositories/     # Patrón Repository y consultas a DB
├── Models/           # Entidades del dominio de la Base de Datos
├── DTOs/             # Objetos de transferencia de datos
├── Mappings/         # Configuración de mapeo entre Entidades y DTOs
├── Data/             # DbContext y configuraciones de Entity Framework
├── Dockerfile        # Configuración de compilación para despliegue en Render
└── Program.cs       # Configuración del pipeline HTTP, Middleware y Servicios
