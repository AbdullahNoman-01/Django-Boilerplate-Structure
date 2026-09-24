# Django Boilerplate Structure

A clean and reusable **Django Boilerplate** designed to help developers quickly start new Django projects with a well-organized project structure, environment configuration, PostgreSQL support, static files, and media files.

## 🚀 Features

* Django project boilerplate structure
* PostgreSQL database configuration
* Environment variables using `.env`
* Static files configuration
* Media files configuration
* Django Admin panel
* Git and `.gitignore` setup
* Ready for future application development

## 🛠️ Technologies Used

* Python
* Django
* PostgreSQL
* python-dotenv
* HTML
* CSS
* Git & GitHub

## 📁 Project Structure

```text
Django-Boilerplate-Structure/
│
├── .env
├── .gitignore
├── manage.py
├── requirements.txt
│
├── media/
│
├── static/
│
└── core/
    ├── __init__.py
    ├── settings.py
    ├── urls.py
    ├── asgi.py
    └── wsgi.py
```

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

Go to the project directory:

```bash
cd Django-Boilerplate-Structure
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If you don't have a `requirements.txt` file yet:

```bash
pip install django psycopg python-dotenv
```

### 4. Configure environment variables

Create a `.env` file in the project root:

```env
SECRET_KEY=your-secret-key

DB_NAME=your_database_name
DB_USER=your_database_user
DB_PASSWORD=your_database_password
DB_HOST=localhost
DB_PORT=5432
```

> Never upload your `.env` file to GitHub.

### 5. Apply migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Create a superuser

```bash
python manage.py createsuperuser
```

### 7. Run the development server

```bash
python manage.py runserver
```

Open the project in your browser:

```text
http://127.0.0.1:8000/
```

## 🗄️ Database Configuration

This boilerplate is configured to use **PostgreSQL**.

The database credentials are loaded from the `.env` file instead of being written directly inside `settings.py`.

Example:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': os.getenv('DB_NAME'),
        'USER': os.getenv('DB_USER'),
        'PASSWORD': os.getenv('DB_PASSWORD'),
        'HOST': os.getenv('DB_HOST'),
        'PORT': os.getenv('DB_PORT'),
    }
}
```

## 📦 Static & Media Files

### Static Files

Static files such as CSS, JavaScript, and fixed images are configured using:

```python
STATIC_URL = 'static/'
```

### Media Files

User-uploaded files are configured using:

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'
```

During development, media files are served through the project's URL configuration.

## 🔐 Environment Variables

Sensitive information such as:

* Django `SECRET_KEY`
* Database password
* Database credentials

should be stored in `.env`.

Make sure `.env` is included in `.gitignore`:

```gitignore
.env
venv/
__pycache__/
*.pyc
```

## 🎯 Purpose

The purpose of this boilerplate is to provide a **ready-to-use Django starting point** so developers don't need to configure the same basic project settings repeatedly.

It can be extended with:

* Authentication
* REST API
* Django REST Framework
* User profiles
* CRUD applications
* Email services
* Deployment configuration
* Third-party APIs

## 👨‍💻 Author

**Abdullah Al Noman**

Python & Django Developer

## ⭐ Support

If you find this boilerplate useful, consider giving the repository a ⭐ on GitHub.
