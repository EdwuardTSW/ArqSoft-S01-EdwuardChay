# Catálogo de Motocicletas 2026

Aplicación web desarrollada como práctica académica universitaria para presentar un catálogo digital de motocicletas. El sistema permite consultar modelos disponibles, filtrar por marca, revisar información técnica detallada y registrar nuevas motocicletas dentro del catálogo durante la ejecución de la aplicación.

## Propósito del proyecto

El propósito de este proyecto es aplicar conceptos de desarrollo web con ASP.NET Core MVC, Razor Views, controladores, modelos, vistas, estilos personalizados y configuración básica de autenticación. La aplicación simula el funcionamiento de un catálogo para una agencia distribuidora de motos, manteniendo un enfoque educativo y práctico.

## Descripción general

El sistema presenta una página principal con información introductoria, una sección de catálogo con motocicletas organizadas en tarjetas visuales, filtros por marca, una vista de detalle para cada modelo y un formulario para agregar nuevas motocicletas.

La aplicación utiliza una interfaz responsive con estilo oscuro, componentes visuales personalizados y navegación mediante el patrón MVC. También incluye configuración de ASP.NET Core Identity para las funciones de registro e inicio de sesión.

## Funcionalidades principales

- Página de inicio con presentación del catálogo.
- Listado de motocicletas disponibles.
- Filtro de motocicletas por marca.
- Visualización de detalles técnicos por motocicleta.
- Formulario para agregar una nueva motocicleta.
- Navegación principal entre inicio y catálogo.
- Diseño responsive adaptable a escritorio y dispositivos móviles.

## Capturas de pantalla

Las siguientes secciones están reservadas para agregar capturas de pantalla del funcionamiento de la aplicación.

### Página de inicio

<!-- Agregar aquí la captura de la página de inicio -->
![Página de inicio](docs/screenshots/inicio.png)

### Catálogo de motocicletas

<!-- Agregar aquí la captura del catálogo completo -->
![Catálogo de motocicletas](docs/screenshots/catalogo.png)

### Filtro por marca

<!-- Agregar aquí la captura del catálogo filtrado por marca -->
![Filtro por marca](docs/screenshots/filtro-marca.png)

### Detalle de motocicleta

<!-- Agregar aquí la captura de la vista de detalle -->
![Detalle de motocicleta](docs/screenshots/detalle-motocicleta.png)

### Formulario para agregar motocicleta

<!-- Agregar aquí la captura del formulario de registro de motocicleta -->
![Formulario para agregar motocicleta](docs/screenshots/agregar-motocicleta.png)


## Tecnologías utilizadas

- C#
- .NET 10
- ASP.NET Core MVC
- Razor Views
- Entity Framework Core
- SQL Server LocalDB
- ASP.NET Core Identity
- Bootstrap
- jQuery
- CSS personalizado
- Google Fonts

## Estructura principal del proyecto

- `Controllers/`: contiene los controladores encargados de procesar las solicitudes y retornar las vistas correspondientes.
- `Models/`: contiene las clases que representan los datos utilizados por la aplicación.
- `Views/`: contiene las vistas Razor que forman la interfaz de usuario.
- `Data/`: contiene el contexto de base de datos utilizado por ASP.NET Core Identity.
- `wwwroot/`: contiene archivos estáticos como hojas de estilo, scripts, imágenes y librerías frontend.
- `Properties/`: contiene configuraciones de ejecución local del proyecto.
- `Program.cs`: define la configuración principal de servicios, middleware, rutas y autenticación.

## Modelo principal

El modelo principal del catálogo es `Item`, que representa una motocicleta dentro del sistema. Sus propiedades principales son:

- `Id`: identificador de la motocicleta.
- `Marca`: marca del fabricante.
- `Modelo`: nombre del modelo.
- `Año`: año del modelo.
- `Cilindrada`: capacidad del motor.
- `Precio`: precio de referencia.
- `Categoria`: tipo de motocicleta.
- `ImagenUrl`: dirección de la imagen utilizada en el catálogo.
- `Potencia`: potencia del motor.
- `Transmision`: tipo o cantidad de velocidades.
- `Color`: color principal.
- `Descripcion`: descripción general del modelo.

## Rutas principales

- `/`: muestra la página de inicio.
- `/Catalogo`: muestra el catálogo completo de motocicletas.
- `/Catalogo?marca=Yamaha`: muestra el catálogo filtrado por marca.
- `/Catalogo/Detalle/{id}`: muestra el detalle de una motocicleta específica.
- `/Catalogo/Agregar`: muestra el formulario para agregar una nueva motocicleta.
- `/Identity/Account/Login`: página de inicio de sesión.
- `/Identity/Account/Register`: página de registro de usuario.

## Requisitos para ejecutar el proyecto

- .NET 10 SDK instalado.
- SQL Server LocalDB instalado.
- Visual Studio, Visual Studio Code u otro editor compatible con proyectos .NET.

## Consideraciones del proyecto

- El catálogo inicial de motocicletas se encuentra definido en memoria dentro del controlador `CatalogoController`.
- Las motocicletas agregadas desde el formulario se guardan en la lista durante la ejecución de la aplicación.
- Al reiniciar la aplicación, los registros agregados manualmente no se conservan porque no están persistidos en base de datos.
- La base de datos configurada está orientada principalmente al sistema de autenticación de usuarios.

## Enfoque académico

Este proyecto fue desarrollado como una práctica universitaria para reforzar conocimientos de programación web con ASP.NET Core MVC. Su objetivo principal es demostrar la integración entre controladores, modelos, vistas, estilos personalizados, rutas, formularios y configuración básica de autenticación.
