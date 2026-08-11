# Acta de Constitución y Especificación de Requerimientos - TalentBridge

## 1. Información General del Proyecto

* **Nombre del Proyecto:** TalentBridge
* **Propósito:** Plataforma web para conectar a jóvenes talentos, estudiantes y recién graduados con empresas que ofrecen oportunidades laborales, prácticas profesionales y pasantías.

---

## 2. Objetivos del Proyecto

### Objetivo General
Desarrollar una plataforma web accesible, intuitiva y eficiente que facilite la conexión directa entre estudiantes/recién graduados y empresas del sector laboral.

### Objetivos Específicos
* Implementar un módulo de registro y gestión de perfiles diferenciado para estudiantes y empresas.
* Desarrollar un motor de publicación, búsqueda y postulación a vacantes con filtros avanzados.
* Incorporar un sistema de notificaciones y seguimiento del estado de las postulaciones y entrevistas.

---

## 3. Requerimientos Funcionales (RF)

Los requerimientos funcionales definen las acciones específicas que el sistema debe realizar:

### Módulo de Autenticación y Perfiles
* **RF-01 (Registro de Usuarios):** El sistema debe permitir el registro de usuarios clasificándolos en el rol de **Estudiante** o **Empresa**.
* **RF-02 (Inicio de Sesión):** El sistema debe permitir la autenticación segura mediante correo electrónico y contraseña.
* **RF-03 (Perfil de Estudiante):** El usuario estudiante debe poder editar su información personal, formación académica, habilidades técnicas/blandas y adjuntar/descargar su Curriculum Vitae en PDF.
* **RF-04 (Perfil de Empresa):** La empresa debe poder configurar su perfil corporativo (nombre, sector, descripción, sitio web y contacto).

### Módulo de Vacantes y Postulaciones
* **RF-05 (Publicación de Vacantes):** Las empresas deben poder crear, editar y publicar vacantes detallando título, descripción, requisitos, modalidad, rango salarial y fecha de expiración.
* **RF-06 (Búsqueda y Filtros):** Los estudiantes deben poder buscar ofertas por palabra clave, categoría, modalidad y salario.
* **RF-07 (Postulación):** El estudiante puede postularse a vacantes activas adjuntando su CV registrado.

### Módulo de Gestión y Entrevistas
* **RF-08 (Programación de Entrevistas):** Las empresas deben poder agendar entrevistas con candidatos postulados (fecha, hora, modalidad y enlace de reunión).
* **RF-09 (Notificaciones):** El sistema debe notificar a los usuarios sobre cambios en el estado de sus postulaciones o agendamiento de entrevistas.

---

## 4. Requerimientos No Funcionales (RNF)

Los requerimientos no funcionales definen los criterios de calidad, rendimiento y seguridad:

* **RNF-01 (Usabilidad):** La interfaz de usuario debe ser intuitiva, moderna y adaptable a distintos tamaños de pantalla (diseño responsivo).
* **RNF-02 (Rendimiento):** El tiempo de respuesta de las consultas principales (búsqueda de vacantes, carga de perfil) no debe superar los 2 segundos en condiciones normales.
* **RNF-03 (Seguridad):** Las contraseñas de los usuarios deben guardarse encriptadas en la base de datos (mediante algoritmos de hashing seguros como bcrypt).
* **RNF-04 (Disponibilidad):** La plataforma debe mantenerse disponible para los usuarios con un tiempo de actividad del 99%.
* **RNF-05 (Mantenibilidad):** El código fuente del proyecto debe estar estructurado de forma modular y documentado bajo los estándares de GitHub/Markdown.
