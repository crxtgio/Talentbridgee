# Manual de Instalación, Configuración y Ejecución (SysAdmin y Desarrolladores) - TalentBridge

Este documento describe los requisitos previos, la arquitectura del software, la estructura del proyecto y los pasos para configurar e ingresar a **TalentBridge** desde el código fuente.

---

## 1. Visión General, Arquitectura y Tecnologías

Para desarrollar **TalentBridge**, se utilizó un stack tecnológico moderno y robusto:

* **Backend:** **ASP.NET Core MVC con C#**, un framework que permite construir aplicaciones web escalables, organizadas y seguras.
* **Base de Datos:** **SQL Server**, sistema encargado de gestionar de forma confiable los datos de usuarios, vacantes, postulaciones y notificaciones (`TalentBridgeDB`).
* **Frontend:** **Bootstrap 5, HTML5, CSS3 y JavaScript**, que permiten crear una interfaz de usuario limpia, responsiva e intuitiva, basada en los wireframes diseñados previamente.
* **ORM:** **Entity Framework Core**, que actúa como puente entre el código C# y SQL Server, facilitando las operaciones de lectura, escritura y consulta de datos sin escribir SQL directo en la lógica.

---

## 2. Requisitos Previos del Sistema

Para ejecutar el proyecto en un entorno local o de servidor, asegúrese de tener instalado:

* **IDE / Editor:** Visual Studio 2022 (con la carga de trabajo *Desarrollo web y ASP.NET*) o Visual Studio Code.
* **SDK:** .NET 8.0 SDK (o superior).
* **Motor de Base de Datos:** SQL Server 2019+ o SQL Server Express.
* **Herramienta de BD:** SQL Server Management Studio (SSMS).
* **Control de Versiones:** Git.

---

## 3. Estructura del Proyecto (Patrón MVC)

El proyecto sigue el patrón **Modelo-Vista-Controlador (MVC)**, el estándar de la industria. Esto permite separar la lógica de negocio (Modelos), la interfaz de usuario (Vistas) y el flujo de la aplicación (Controladores), logrando un código ordenado y mantenible[cite: 1].

Al abrir la solución en Visual Studio, la estructura de carpetas se organiza de la siguiente manera[cite: 1]:

```text
TalentBridge/
├── Controllers/         # Gestiona las peticiones del usuario y el flujo de la app
│   ├── AuthController.cs        # Maneja el registro y login de usuarios
│   ├── EstudiantesController.cs # Maneja perfil, CV y postulaciones
│   └── EmpresasController.cs    # Maneja perfil corporativo y publicación de vacantes
├── Models/              # Clases C# que representan las tablas de la base de datos
│   ├── Usuario.cs
│   ├── Vacante.cs
│   ├── Postulacion.cs
│   └── TalentBridgeDbContext.cs # Contexto de Entity Framework Core
├── Views/               # Vistas HTML con Razor y lógica de presentación
│   ├── Home/
│   ├── Auth/
│   ├── Estudiantes/
│   └── Empresas/
├── wwwroot/             # Archivos estáticos (CSS, JS, imágenes, Bootstrap)
├── appsettings.json     # Configuración de variables y cadenas de conexión
└── Program.cs           # Punto de entrada y configuración de servicios

{
  "ConnectionStrings": {
    "DefaultConnection": "Server=LOCALHOST\\SQLEXPRESS;Database=TalentBridgeDB;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}

