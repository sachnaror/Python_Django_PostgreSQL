# Django with PostgreSQL Database

This repository provides a basic structure for starting a Django project with a PostgreSQL database.



## Getting Started
1. Clone this repository.
2. Navigate into the project directory: `cd django_project_with_postgresql`.

3. Create a PostgreSQL database:
   - Open the PostgreSQL command line or use a GUI tool like pgAdmin.
   - Run the following SQL commands to create a database:

     ```sql
     CREATE DATABASE dbtest;
     ```
   Replace `dbtest` with your desired database name.

4. Configure the database settings:
   - Open `django_project_with_postgresql/settings.py`.
   - Replace the `DATABASES` configuration with your PostgreSQL database settings:

     ```python
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.postgresql',
             'NAME': 'dbtest',
             'USER': 'myuser',
             'PASSWORD': 'mypassword',
             'HOST': 'localhost',
             'PORT': '5432',
         }
     }
     ```
   Replace `dbtest`, `myuser`, `mypassword` with your PostgreSQL database name, username, and password respectively.

5. Run database migrations: `python manage.py migrate`.
6. Start the development server: `python manage.py runserver`.
7. Visit `http://localhost:5432` in your browser to view the application.

## Additional Notes
- Make sure PostgreSQL is running before starting the development server.
- Customize the Django project according to your requirements.

