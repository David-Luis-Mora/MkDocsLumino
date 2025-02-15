Estructura del Código

El proyecto está organizado en aplicaciones Django independientes:

lumino/
accounts/
shared/
users/
subjects/
manage.py
settings.py
...

Cada aplicación se encarga de un conjunto de funcionalidades específicas, lo que permite que el código esté organizado y modularizado.
Tecnologías y Herramientas

    Django: Framework web que permite la creación de aplicaciones rápidas y seguras.
    Material for MkDocs: Tema utilizado para generar esta documentación.
    Django-RQ: Para gestionar tareas asíncronas como la generación de certificados.

Instrucciones de Configuración

    Clona el repositorio:

git clone <repo_url>
cd lumino

Crea un entorno virtual y activa:

python3 -m venv venv
source venv/bin/activate

Instala las dependencias:

pip install -r requirements.txt
