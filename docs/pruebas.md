## 1. Estrategia de Pruebas

La estrategia de pruebas de **Lumino** está diseñada para garantizar que todas las funcionalidades críticas del sistema se comporten como se espera, tanto en entornos de desarrollo como en producción. Para ello, se emplean diversas técnicas de pruebas, que incluyen pruebas unitarias, de integración y de aceptación.

### 1.1. Métodos Utilizados

- **Pruebas Unitarias**: Se han implementado pruebas unitarias para verificar que cada función o componente del sistema, como los modelos, vistas o utilidades, funciona correctamente de manera aislada. Estas pruebas aseguran que el comportamiento esperado se mantenga cuando se realiza un cambio en el código.
- **Pruebas de Integración**: Estas pruebas se realizan para asegurar que diferentes partes del sistema interactúan de manera correcta. Por ejemplo, se comprueba la correcta integración de la base de datos, la comunicación entre los modelos y la capa de presentación.

- **Pruebas de Aceptación**: Se enfocan en validar que el sistema cumpla con los requisitos establecidos en el proyecto y que las características de la aplicación estén alineadas con las expectativas del usuario final. Se simulan escenarios completos que los usuarios finales podrían realizar, como el registro, la matrícula y la calificación.

---

## 2. Casos de Prueba

A continuación se detallan algunos ejemplos específicos de los casos de prueba realizados y los resultados esperados:

### 2.1. Casos de Prueba Comunes

#### 2.1.1. Registro de Usuario

- **Objetivo**: Verificar que el sistema permita registrar un nuevo usuario.
- **Acción**: El usuario ingresa su nombre de usuario, contraseña, correo electrónico y otros campos requeridos en el formulario de registro.
- **Resultado Esperado**: El sistema crea una nueva cuenta de usuario, muestra un mensaje de bienvenida y redirige al usuario a la página principal.

#### 2.1.2. Matrícula de Estudiantes en un Módulo

- **Objetivo**: Comprobar que los estudiantes puedan matricularse en módulos correctamente.
- **Acción**: El estudiante selecciona los módulos disponibles y se matricula en ellos.
- **Resultado Esperado**: El sistema actualiza el estado de la matrícula del estudiante y muestra un mensaje de confirmación.

#### 2.1.3. Añadir Lección a un Módulo

- **Objetivo**: Verificar que los profesores puedan añadir nuevas lecciones a un módulo.
- **Acción**: El profesor crea una nueva lección, asigna un título y contenido (en formato Markdown) y la asocia a un módulo específico.
- **Resultado Esperado**: La lección aparece en la lista de lecciones del módulo y el sistema muestra un mensaje de éxito.

#### 2.1.4. Calificación de Estudiantes

- **Objetivo**: Validar que el profesor pueda asignar calificaciones a los estudiantes.
- **Acción**: El profesor asigna una calificación a un estudiante en un módulo en el que está matriculado.
- **Resultado Esperado**: El sistema guarda la calificación correctamente y el estudiante puede verla en su perfil.

---

## 3. Cobertura de Pruebas

### 3.1. Indicadores de Cobertura

La cobertura de pruebas se mide para asegurar que las funcionalidades clave del proyecto estén completamente verificadas. Los siguientes indicadores reflejan la cobertura alcanzada:

- **Cobertura de Modelos**: Se realizan pruebas unitarias sobre los modelos `User`, `Subject`, `Lesson`, `Enrollment` y `Profile`, para asegurar que las migraciones y validadores de campos funcionen correctamente.
- **Cobertura de Vistas**: Se cubren las vistas críticas de la plataforma, como las relacionadas con la visualización de módulos, matriculación y el proceso de calificación de estudiantes.
- **Cobertura de Formularios**: Se verifica que los formularios de registro, inicio de sesión, matrícula y edición de perfil funcionen correctamente y validen las entradas de los usuarios.

- **Cobertura de Seguridad**: Se realizan pruebas específicas para verificar que las medidas de seguridad, como la autenticación y autorización de usuarios, funcionen correctamente, evitando accesos no autorizados.

---

## 4. Automatización de Pruebas

### 4.1. Herramientas y Scripts Utilizados

Para mejorar la eficiencia en la ejecución de pruebas y garantizar la consistencia a lo largo del tiempo, se utilizan diversas herramientas de automatización:

- **Pytest**: Se emplea **pytest** para la ejecución de pruebas unitarias y de integración. Se ha configurado para que se ejecute automáticamente al hacer cambios en el código, lo que permite detectar errores de manera temprana.

- **Selenium**: Se usa **Selenium** para realizar pruebas de aceptación y pruebas de integración en el navegador. Estas pruebas validan que las funcionalidades más importantes de la interfaz de usuario funcionen correctamente, como la navegación entre módulos y el registro de usuario.

- **Django Test Framework**: Django proporciona un conjunto de herramientas para crear pruebas automatizadas de los modelos, vistas y formularios. Se utiliza para simular las interacciones con la base de datos y comprobar que las funcionalidades de **Lumino** estén implementadas correctamente.

### 4.2. Scripts de Automatización

Los scripts de automatización se ejecutan como parte del proceso de integración continua (CI) cada vez que se hace un cambio en el repositorio de código. El flujo de trabajo de CI incluye:

1. **Instalación de Dependencias**: Las dependencias necesarias para las pruebas se instalan automáticamente en un entorno de prueba aislado.

2. **Ejecución de Pruebas**: Los tests se ejecutan automáticamente en función de los cambios realizados en el código. Las pruebas unitarias, de integración y de aceptación se ejecutan para asegurar que el código sigue siendo válido.

3. **Informes de Resultados**: Al finalizar las pruebas, se generan informes detallados sobre los resultados de las pruebas, incluyendo las pruebas fallidas y los errores encontrados, lo que permite a los desarrolladores corregir rápidamente los problemas.

---
