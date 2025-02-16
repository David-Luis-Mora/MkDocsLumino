## 1. Instrucciones Básicas

### Cómo instalar y configurar el software

Para comenzar a usar **Lumino**, sigue estos pasos para instalar y configurar el proyecto en tu máquina local:

#### 1.1. Instalación

1. **Clona el repositorio:**
   Clona el repositorio del proyecto desde GitHub:

```bash
git clone <repositorio_url>
Crea un entorno virtual: Es recomendable usar un entorno virtual para gestionar las dependencias:
```

Crear el entorno con el justfile del repositorio de github y activarlo:

```bash

just create-venv
source .venv/bin/activate
```

Instala las dependencias: Una vez que el entorno virtual esté activo, instala todas las dependencias necesarias para el proyecto:

```bash
just setup
```

Crea el proyecto Django: La instalación anterior crea automáticamente el entorno Django en la carpeta main y aplica las migraciones iniciales.

Crear un superusuario: Después de la configuración, crea un superusuario para acceder al panel de administración:

```bash
python manage.py createsuperuser
```

1.2. Primeros pasos con Lumino
Inicia el servidor de desarrollo: Inicia el servidor local para empezar a usar Lumino:

```bash
python manage.py runserver
```

Accede a la plataforma: Abre tu navegador y ve a http://127.0.0.1:8000/, donde podrás ver la página de inicio de Lumino.

Inicia sesión: Usa las credenciales de superusuario creadas anteriormente para acceder a la plataforma.

#### 2. Guías Avanzadas

2.1. Agregar Aplicaciones
Para agregar nuevas aplicaciones a Lumino, usa el siguiente comando:

```bash
just startapp <nombre_de_la_aplicación>
```

Este comando crea la carpeta de la aplicación y la agrega automáticamente a la variable INSTALLED_APPS en el archivo settings.py.

##### 2.2. Modelos en Lumino

Lumino usa varios modelos para gestionar usuarios, asignaturas y lecciones. A continuación se describen algunos de los modelos importantes:

subjects.Subject

code: Código del módulo.
name: Nombre del módulo.
teacher: Profesor encargado del módulo.
students: Estudiantes matriculados en el módulo.
subjects.Lesson

subject: Relación con la asignatura a la que pertenece la lección.
title: Título de la lección.
content: Contenido de la lección.
subjects.Enrollment

student: Estudiante matriculado.
subject: Módulo en el que está matriculado el estudiante.
mark: Calificación del estudiante en ese módulo.
users.Profile

user: Relación con el usuario.
role: Rol del usuario (estudiante o profesor).
avatar: Imagen de perfil del usuario.
bio: Biografía del usuario.
2.3. Comandos de Gestión
Lumino proporciona varios comandos de gestión personalizados. Por ejemplo, para mostrar las notas medias de los módulos:

```bash
just get_subject_stats
```

Este comando calcula la media de las calificaciones de los estudiantes en cada módulo.

#### 3. Solución de Problemas

##### 3.1. Preguntas Frecuentes (FAQ)

¿Cómo puedo cambiar el idioma de la plataforma?
Puedes cambiar el idioma de la interfaz a español o inglés. Para cambiar el idioma, ve a:

```bash
Copiar
/setlang/es/  # para español
/setlang/en/  # para inglés
```

La plataforma se redirigirá a la página correspondiente después de cambiar el idioma.

¿Cómo puedo recuperar mi contraseña?
Si has olvidado tu contraseña, puedes utilizar la funcionalidad de "Olvidé mi contraseña" en la página de inicio de sesión para restablecerla. Asegúrate de tener acceso al correo electrónico registrado.

¿Qué hago si no puedo iniciar sesión?
Si no puedes iniciar sesión, verifica lo siguiente:

Asegúrate de que estás utilizando el nombre de usuario y la contraseña correctos.
Si eres un nuevo usuario, asegúrate de haberte registrado correctamente.
Si sigues teniendo problemas, contacta con el administrador del sistema.

##### 3.2. Errores Comunes

Error 500 - Error Interno del Servidor
Este error puede deberse a una configuración incorrecta del servidor o un fallo en la base de datos. Para solucionarlo:

Revisa los registros de errores del servidor para identificar el problema.
Verifica que todas las migraciones se hayan aplicado correctamente:
bash
Copiar
python manage.py migrate
Problemas al cargar los datos
Si los datos no se cargan correctamente, verifica que hayas utilizado el comando adecuado para cargar los datos de prueba:

```bash
just load-data
```

Asegúrate de que el archivo de datos esté bien formateado y accesible.

#### 4. Otras Funcionalidades

##### 4.1. Gestión de Usuarios

Profesores y alumnos tienen diferentes roles en la plataforma, lo que les permite acceder a distintas funcionalidades:

Profesor: Puede añadir lecciones, calificar a los estudiantes y gestionar los módulos que enseña.
Alumno: Puede matricularse en módulos, ver sus lecciones y calificaciones, y solicitar certificados de calificaciones.

##### 4.2. Solicitud de Certificado

Los estudiantes pueden solicitar un certificado de calificaciones una vez hayan terminado un módulo. Este certificado será enviado por correo electrónico en formato PDF.

Para solicitar un certificado, ve a la página correspondiente:

```bash
/subjects/certificate/
```

5 Enlaces Útiles
Documentación oficial de Django
Lumino en GitHub
markdown
Copiar
