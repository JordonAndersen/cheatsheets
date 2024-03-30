## Django with Docker Compose Cheat Sheet

This cheat sheet summarizes key concepts, focusing on Django project setup, Docker Compose usage, and interacting with a PostgreSQL database.

**Setting Up with Docker Compose:**

1. **Create a `docker-compose.yml` file:** This file defines the services (containers) your application will use.
   - Example: Create a PostgreSQL service named `db` with image `postgres:15`.
   - Set environment variables, ports, and volumes for the service.

   **Example docker-compse.yml (at the root of your project):**
                version: '3'
                services:
                db:
                    image: postgres:15
                    environment:
                    - POSTGRES_USER=postgres
                    - POSTGRES_PASSWORD=postgres
                    - POSTGRES_DB=pokedex_db
                    ports:
                    - '5454:5432'
                    volumes: 
                    - postgres_data:/var/lib/postgresql/data

                volumes:
                postgres_data:

**Using Docker Compose:**

2. **Start the application:** Run `docker-compose up -d` to start all defined services in the background.
3. **Stop the application:** Run `docker-compose down` to stop and remove all running containers.

**Virtual Environments and Package Management:**

1. **Create a virtual environment:** Use `python -m venv <env_name>` to isolate project dependencies.
   - Activate it:
     - Mac/Linux: `source <env_name>/bin/activate`
     - Windows: `<env_name>\Scripts\activate`
2. **Install Django:** Run `pip install django` within the activated environment.

**Creating a Django Project:**

1. **Start a new project:** Use `python -m django startproject <project_name>` to create a project directory.
2. **Create a Django app:** Use `python manage.py startapp <app_name>` to create an app within the project.
3. **Register the app:** Add `<app_name>` to `INSTALLED_APPS` in `settings.py` to connect the app to the project.
4. **Create a `requirements.txt` file:** Run `pip freeze > requirements.txt` to record project dependencies.

**Linking Django with PostgreSQL:**

1. **Use Docker Compose:** Run a PostgreSQL service as described earlier.
2. **Configure Django settings:**
   - Set `DATABASES` in `settings.py` to specify the PostgreSQL connection details:
     - Engine: `django.db.backends.postgresql`
     - Host: `localhost` (or container IP for Docker Compose)
     - Port: `5432` (default)
     - Database name: Choose a name for your database (e.g., `pokedex_db`).
     - User and password for the database.
3. **Install `psycopg2`:** Use `pip install psycopg2` to install the adapter library for connecting Django to PostgreSQL.

**Creating Models and Interacting with Data:**

1. **Define models in `models.py`:** Use Django models to represent your data structure.
2. **Generate migrations:** Run `python manage.py makemigrations <app_name>` to create migration files after model changes.
3. **Apply migrations:** Run `python manage.py migrate` to apply pending migrations and update the database schema.
4. **Django shell:** Use `python manage.py shell` to interact with your models and database using Python.
   - Create model instances, query data, and save changes.

**Additional Notes:**

- Remember to replace placeholders like `<project_name>` and `<app_name>` with your actual project and app names.
- Explore the Django documentation ([https://docs.djangoproject.com/en/5.0/](https://docs.djangoproject.com/en/5.0/)) for in-depth explanations and advanced functionalities.
- Validators documentation: https://docs.djangoproject.com/en/2.2/ref/validators/
- Django QuerySets Cheatsheet: https://github.com/chrisdl/Django-QuerySet-Cheatsheet?tab=readme-ov-file

