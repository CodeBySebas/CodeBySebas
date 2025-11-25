
# Mi Primera Página Web (Proyecto Estudiante)

Descripción corta
-----------------
Página web clásica construida como proyecto de estudiante usando Python (Flask), HTML, pandas y PostgreSQL. Ideal como primer proyecto para aprender desarrollo web full-stack a pequeña escala, usando VS Code como editor/IDE.

Qué aprenderás
--------------
- Configurar un entorno de desarrollo en VS Code.
- Crear una app web con Flask.
- Mostrar y procesar datos con pandas.
- Conectar la app a una base de datos PostgreSQL.
- Servir plantillas HTML y gestionar rutas básicas.

Tecnologías
-----------
- Python 3.x
- Flask
- pandas
- PostgreSQL
- HTML/CSS (plantillas Jinja2)
- VS Code (IDE recomendado)

Requisitos previos
------------------
- Python 3 instalado
- PostgreSQL instalado y en ejecución
- VS Code (opcional, recomendado)
- git

Instalación y configuración
---------------------------
1. Clona el repositorio:
```bash
git clone https://github.com/tu-usuario/mi-primera-pagina-web.git
cd mi-primera-pagina-web
```

2. Crea y activa un entorno virtual:
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

3. Instala dependencias:
```bash
pip install -r requirements.txt
```
(Si no tienes requirements.txt, instala: `pip install flask pandas psycopg2-binary python-dotenv`)

4. Configura PostgreSQL:
- Crea una base de datos y un usuario:
```sql
CREATE DATABASE mi_web_db;
CREATE USER mi_usuario WITH PASSWORD 'tu_contraseña';
GRANT ALL PRIVILEGES ON DATABASE mi_web_db TO mi_usuario;
```
- Alternativamente usa pgAdmin o la herramienta que prefieras.

5. Variables de entorno
- Crea un archivo `.env` en la raíz con algo así:
```
FLASK_APP=app.py
FLASK_ENV=development
DATABASE_URL=postgresql://mi_usuario:tu_contraseña@localhost/mi_web_db
SECRET_KEY=una_clave_segura
```
- VS Code puede usar la extensión "Python" y "dotenv" para cargar estas variables.

Ejecutar la aplicación
---------------------
Con el entorno activado y las variables configuradas:
```bash
# opción 1 (Flask)
flask run

# opción 2 (si en app.py tienes app.run)
python app.py
```
Abre: http://127.0.0.1:5000

Estructura sugerida del repositorio
-----------------------------------
- app.py                      # punto de entrada de Flask
- requirements.txt            # dependencias
- .env                       # variables de entorno (no subirlo al repo)
- /templates                  # HTML (Jinja2)
  - base.html
  - index.html
- /static                     # CSS, JS, imágenes
- /data                       # CSV de ejemplo o datasets
- /utils                      # helpers (p. ej. funciones con pandas)
- README.md
- .gitignore

Buenas prácticas
----------------
- No subas credenciales ni `.env` al repositorio público. Añade `.env` a `.gitignore`.
- Haz commits pequeños y descriptivos.
- Usa ramas para features o experimentos: `git checkout -b feature/nueva-pagina`.
- Documenta funciones importantes y rutas en el código.

Ideas para ampliar el proyecto
-----------------------------
- Formularios para añadir registros a PostgreSQL.
- Páginas de visualización de datos con pandas (tablas y gráficas).
- Autenticación básica (registro/login).
- Despliegue en Heroku, Railway o Render (con ajustes para PostgreSQL).

Contribuir
----------
Eres estudiante y este repo es tu diario de aprendizaje. Si otro compañero quiere ayudar:
- Haz fork y PR.
- Mantén formato de código y documenta cambios.
- Incluye ejemplos y capturas si añades UI.

Licencia
--------
Elige una licencia sencilla para proyectos educativos, por ejemplo MIT. (Archivo LICENSE opcional)

Contacto
--------
Tu nombre — tu-email@example.com  
Repositorio: https://github.com/tu-usuario/mi-primera-pagina-web

Notas finales
--------------
He dejado instrucciones básicas y minimalistas para que puedas arrancar rápido en VS Code y entender cada pieza del proyecto. Si quieres, puedo generarte también un archivo requirements.txt, un .gitignore ideal para Python, o una plantilla básica de app.py y templates para que arranques en 1 clic.
