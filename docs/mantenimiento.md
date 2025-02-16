# Mantenimiento y Actualización de Lumino

---

## 1. Política de Mantenimiento

**Lumino** se compromete a mantener y actualizar regularmente la plataforma para asegurar que se mantenga funcional, segura y eficiente. A continuación se describen los aspectos clave de la política de mantenimiento.

### 1.1. Frecuencia de Actualizaciones

- **Actualizaciones menores**: Se realizarán actualizaciones menores cada mes para corregir errores, mejorar la seguridad y agregar pequeñas mejoras de funcionalidad.
- **Actualizaciones mayores**: Las actualizaciones mayores se implementarán trimestralmente. Estas actualizaciones pueden incluir nuevas funcionalidades, cambios importantes en la estructura de la base de datos o actualizaciones de dependencias que requieran migración.

- **Actualizaciones de seguridad**: Se implementarán de forma inmediata cuando sea necesario. La seguridad es una prioridad, y se realizarán correcciones tan pronto como se detecten vulnerabilidades críticas.

- **Soporte**: El equipo de desarrollo brindará soporte continuo para problemas críticos relacionados con el uso de la plataforma. Para problemas no críticos, el tiempo de respuesta estándar será de 48 horas.

### 1.2. Procedimientos de Mantenimiento

El mantenimiento se llevará a cabo durante las horas de menor tráfico para minimizar la interrupción del servicio. Se notificará a los usuarios con antelación sobre el mantenimiento programado mediante correos electrónicos y avisos en la plataforma.

---

## 2. Registro de Cambios (Changelog)

El **registro de cambios** proporciona un historial detallado de todas las versiones y mejoras realizadas en **Lumino**. A continuación se presentan algunos de los cambios más relevantes.

### 2.1. Versión 1.1.0 (Febrero 2025)

- **Nuevas funcionalidades**:

  - Se añadió la funcionalidad para que los estudiantes soliciten certificados de calificaciones en formato PDF.
  - Se implementó la opción de desmatriculación de módulos para los estudiantes.

- **Mejoras**:

  - Se mejoró el rendimiento de la base de datos al optimizar las consultas para la visualización de las calificaciones de los estudiantes.
  - Mejoras en la interfaz de usuario para facilitar la navegación de los profesores y estudiantes en la plataforma.

- **Correcciones**:
  - Se corrigió un error en el que algunos estudiantes no podían ver sus lecciones después de matricularse en un módulo.
  - Se solucionó un problema en el que los módulos sin lecciones no se mostraban correctamente en el perfil del profesor.

---

### 2.2. Versión 1.0.0 (Enero 2025)

- **Primer lanzamiento de Lumino**:
  - Implementación completa de la gestión de usuarios, con roles de estudiante y profesor.
  - Funcionalidad para añadir y gestionar módulos y lecciones.
  - Integración de calificaciones y visualización de notas para los estudiantes.
  - Creación de perfiles de usuario con imágenes de avatar y biografía.

---

## 3. Plan de Escalabilidad

A medida que Lumino crece, es fundamental que la plataforma sea capaz de soportar un mayor número de usuarios y funcionalidades. A continuación, se presentan las posibles áreas de mejora para asegurar que Lumino pueda escalar eficientemente.

### 3.1. Mejora de la Infraestructura

- **Optimización de la base de datos**:
  Para manejar un mayor volumen de usuarios y datos, se planea migrar la base de datos a un sistema de gestión de bases de datos más robusto y escalable, como **PostgreSQL**. También se implementarán técnicas de caché y partición de bases de datos para mejorar el rendimiento de las consultas.

- **Infraestructura en la nube**:
  Se planea migrar la infraestructura de **Lumino** a una plataforma de la nube como **AWS** o **Google Cloud** para manejar de manera más eficiente la carga de tráfico y permitir la escalabilidad automática según la demanda.

### 3.2. Nuevas Funcionalidades

- **Integración con plataformas de aprendizaje externas**:
  Se explorará la posibilidad de integrar Lumino con plataformas de aprendizaje externas como **Moodle** o **Google Classroom** para permitir la importación/exportación de contenidos y mejorar la experiencia de aprendizaje.

- **Mejoras en la gestión de clases y recursos**:
  Se implementarán nuevas funcionalidades para que los profesores puedan gestionar los materiales de los cursos de manera más eficiente, incluyendo la posibilidad de añadir archivos, enlaces externos y recursos interactivos dentro de las lecciones.

### 3.3. Soporte para Más Usuarios

- **Optimización de rendimiento**:
  Se trabajará en mejorar el rendimiento del sistema para soportar miles de usuarios simultáneos. Esto incluirá el uso de técnicas como balanceo de carga, servidores distribuidos y optimización de consultas a la base de datos.

- **Mejoras en la interfaz de usuario**:
  Se realizarán ajustes a la interfaz para que sea aún más intuitiva y capaz de gestionar grandes cantidades de datos, como listas de estudiantes, calificaciones y módulos de forma eficiente.

---
