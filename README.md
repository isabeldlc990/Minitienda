# 🛒 MiniTienda

¡Bienvenido a **MiniTienda**! Una aplicación web robusta y moderna desarrollada en Laravel para la gestión integral de productos, inventario, ventas y usuarios mediante un sistema de control de acceso basado en roles (RBAC). 

El sistema está diseñado para optimizar la administración de un negocio, permitiendo un control preciso del stock, registro de ventas en tiempo real y una experiencia de compra fluida para el cliente a través de un carrito de compras.

---

## 🎯 Objetivos del Proyecto

* **Administración Centralizada:** Gestionar productos y categorías de forma dinámica.
* **Control de Stock:** Mantener un monitoreo constante del inventario disponible.
* **Flujo de Ventas:** Registrar transacciones de manera eficiente y automatizada.
* **Experiencia de Usuario:** Ofrecer un carrito de compras intuitivo para los clientes.
* **Seguridad:** Garantizar el acceso protegido mediante roles y permisos específicos.

---

## 🛠️ Tecnologías Utilizadas

El proyecto está construido con las tecnologías más modernas del ecosistema PHP y desarrollo web:

* **Framework:** ![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white) v12
* **Lenguaje:** ![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white) v8.x
* **Base de Datos:** ![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
* **Frontend:** ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white) + Blade Templates
* **Autenticación:** Laravel Breeze
* **Permisos:** Spatie Laravel Permission

---

## 👥 Roles del Sistema

El sistema cuenta con tres niveles de acceso claramente definidos:

| Rol | Descripción y Permisos |
| :--- | :--- |
| **👑 Administrador** | Acceso total al sistema. Puede gestionar usuarios, asignar roles, administrar productos, categorías, inventario y visualizar el historial de ventas globales. |
| **📦 Gestor de Inventario** | Enfocado en la logística. Puede crear, editar y eliminar productos, gestionar categorías y controlar las existencias en stock. |
| **🛒 Cliente** | Usuario final. Puede registrarse, iniciar sesión, explorar el catálogo de productos, añadir elementos al carrito, realizar compras y consultar su historial de pedidos. |

---

## 🧩 Módulos Implementados

### 🔑 Módulo de Usuarios
* Operaciones CRUD (Crear, Leer, Actualizar, Eliminar) de usuarios.
* Asignación y modificación de roles en tiempo real.

### 📦 Módulo de Inventario
* Catálogo maestro de productos y categorías.
* Control estricto de existencias (mínimos y máximos).

### 💰 Módulo de Ventas
* Carrito de compras interactivo para el cliente.
* Pasarela de registro de ventas.
* **Descuento automático del inventario** al confirmar una compra.

### 🛍️ Módulo de Clientes
* Panel privado para el cliente.
* Historial detallado de compras y seguimiento del estado de pedidos.

---

## 🗄️ Estructura de la Base de Datos

Las principales tablas que componen la arquitectura del sistema son:

* `users`: Almacena la información de las cuentas de usuario.
* `roles` & `permissions`: Tablas del paquete Spatie para el control de acceso.
* `products` & `categories`: Estructura para el catálogo de artículos.
* `sales` & `sale_details`: Registro histórico de las transacciones y los productos asociados a cada venta.

---

## 🚀 Instalación y Configuración

Sigue estos pasos para montar el entorno de desarrollo local:

### 1. Clonar el repositorio
```bash
git clone URL_DEL_REPOSITORIO
cd minitienda
# 2. Instalar dependencias de PHP
composer install

# 3. Configurar el entorno
cp .env.example .env

# Nota: Recuerda abrir el archivo .env y configurar tus credenciales de base de datos
# (DB_DATABASE, DB_USERNAME, DB_PASSWORD) antes de continuar con el paso 4.

# 4. Preparar la aplicación
php artisan key_generate
php artisan migrate --seed

# 5. Configurar almacenamiento externo
php artisan storage:link

# 6. Iniciar el servidor
php artisan serve
