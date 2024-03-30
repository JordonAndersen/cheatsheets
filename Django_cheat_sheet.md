## Django Cheat Sheet

This cheat sheet provides a quick reference for setting up Django on your machine and using common commands.

**Setting Up Django:**

1. **Create a virtual environment (recommended):**
   - Isolates project dependencies.
   - Use `python -m venv <venv_name>` to create a virtual environment.
   - Activate it using `source <venv_name>/bin/activate` (Linux/macOS) or `<venv_name>\Scripts\activate.bat` (Windows).

2. **Install Django:**
   - `pip install django` in the activated virtual environment.

**Creating requirements.txt:**
    -Install packages in your activated virtual environment using pip install <package_name>.
    -After installing all required packages, run pip freeze > requirements.txt in your project's root directory. This creates a requirements.txt file containing the installed packages and   versions.


**Installing Dependencies from requirements.txt:**
    -Activate your virtual environment.
    -Navigate to your project's root directory.
    -Run pip install -r requirements.txt. This installs all packages listed in requirements.txt according to their specified versions.

**Common Commands:**

* **Project and App Management:**
   - Create a Django project: `django-admin startproject <project_name>`
   - Create a Django app: `python manage.py startapp <app_name>` within the project directory
   - Register an app in `settings.py`: Add `<app_name>` to `INSTALLED_APPS`

* **Models:**
   - Define models in `models.py`: Create classes representing your data structure.
   - Generate migrations: `python manage.py makemigrations <app_name>` (after model changes)
   - Apply migrations: `python manage.py migrate` (applies pending migrations)

* **Views:**
   - Define views in `views.py`: Functions handling user requests and returning responses.
   - Use `HttpResponse` for simple text responses.
   - Render templates with `render` function: `from django.shortcuts import render`

* **Urls:**
   - Define URL patterns in `urls.py`: Map URLs to views.
   - Use `path` function (Django 2+) or `url` function (older versions).
   - Include app URLs in the main project `urls.py`: `from django.urls import include`

* **Templates:**
   - Create templates in the `templates` folder within your app.
   - Use Django templating language for dynamic content.
   - Access model data with template variables (`{{ variable_name }}`).

* **Development Server:**
   - Run the development server: `python manage.py runserver`

* **Admin Panel:**
   - Create an admin user: `python manage.py createsuperuser`
   - Access the admin panel: `http://127.0.0.1:8000/admin/` (default URL)

* **Additional Resources:**
   - Django documentation: [https://docs.djangoproject.com/en/5.0/](https://docs.djangoproject.com/en/5.0/)
   - Django tutorial: [https://docs.djangoproject.com/en/5.0/](https://docs.djangoproject.com/en/5.0/)

**Remember:** This is a basic cheat sheet. Refer to the official Django documentation for detailed explanations and advanced functionalities.
