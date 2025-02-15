Entorno de Producción

El entorno de producción debe incluir:

    Ubuntu Server: Como sistema operativo.
    NGINX: Para servir la aplicación web.
    PostgreSQL: Para la base de datos.

Proceso de Despliegue

    Configura tu servidor Ubuntu y asegúrate de que tiene NGINX y PostgreSQL instalados.
    Sube el código al servidor.
    Configura el archivo settings.py para el entorno de producción (base de datos, secretos, etc.).
    Corre las migraciones y el servidor:

    python manage.py migrate
    python manage.py runserver

Planes de Recuperación

En caso de fallo, se debe tener un sistema de backup de la base de datos y la capacidad de reiniciar el servidor rápidamente.
