Arquitectura del Sistema

El proyecto está dividido en varias aplicaciones Django:

    accounts: Gestión de autenticación.
    shared: Artefactos compartidos.
    users: Gestión de usuarios.
    subjects: Gestión de módulos y lecciones.

Diagrama de Arquitectura

(Tu diagrama de la arquitectura se incluiría aquí, mostrando las relaciones entre las aplicaciones y los usuarios).
Modelo de Datos

Los modelos incluyen:

    Subject: Representa un módulo académico, con campos como código, nombre, profesor y estudiantes.
    Lesson: Representa una lección de un módulo.
    Enrollment: Relaciona estudiantes con los módulos en los que están matriculados.
    Profile: Información adicional sobre el usuario, como su rol (estudiante/profesor) y avatar.

Relaciones entre los Modelos:

    Un Subject tiene un profesor (FK a User) y múltiples estudiantes (M2M a User a través de Enrollment).
    Un Profile está relacionado con un User (uno a uno).
