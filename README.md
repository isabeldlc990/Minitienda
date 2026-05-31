# Minitienda
MiniTienda es una aplicación web desarrollada en Laravel que permite gestionar productos, inventario, ventas y usuarios mediante roles de acceso.  El sistema está diseñado para facilitar la administración de una tienda, permitiendo controlar el stock de productos, registrar ventas y realizar compras mediante un carrito de compras.
Objetivos
Gestionar productos y categorías.
Controlar el inventario disponible.
Registrar ventas realizadas.
Permitir compras mediante carrito de compras.
Gestionar usuarios y roles del sistema.
Tecnologías Utilizadas
Laravel 12
PHP 8.x
MySQL
Blade Templates
Tailwind CSS
Laravel Breeze
Spatie Laravel Permission
Roles del Sistema
Administrador

Puede:

Gestionar usuarios.
Asignar roles.
Gestionar productos.
Gestionar categorías.
Gestionar inventario.
Gestionar ventas.
Gestor de Inventario

Puede:

Crear productos.
Editar productos.
Eliminar productos.
Gestionar categorías.
Controlar existencias.
Cliente

Puede:

Registrarse.
Iniciar sesión.
Visualizar productos.
Agregar productos al carrito.
Realizar compras.
Consultar historial de pedidos.

Módulos Implementados
Módulo de Usuarios
Crear usuarios.
Editar usuarios.
Eliminar usuarios.
Asignar roles.

Módulo de Inventario
Gestión de productos.
Gestión de categorías.
Control de stock.

Módulo de Ventas
Carrito de compras.
Registro de ventas.
Descuento automático de inventario.

Módulo de Clientes
Historial de compras.
Seguimiento de pedidos.

Base de Datos

Principales tablas:

users
roles
permissions
products
categories
sales
sale_details

Instalación del Proyecto
Clonar el repositorio
git clone URL_DEL_REPOSITORIO
Instalar dependencias
composer install

Configurar archivo .env
cp .env.example .env

Configurar:

Base de datos
Usuario MySQL
Contraseña
Generar clave
php artisan key:generate
Ejecutar migraciones
php artisan migrate
Ejecutar seeders
php artisan db:seed
Crear enlace simbólico
php artisan storage:link
Ejecutar el servidor
php artisan serve
Funcionalidades Principales
Autenticación de usuarios.
Control de acceso por roles.
Gestión de inventario.
Gestión de ventas.
Carrito de compras.
Historial de compras.
Administración de usuarios.
