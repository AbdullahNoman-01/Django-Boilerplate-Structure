# Django Boilerplate 🚀

A clean and reusable **Django Boilerplate** to quickly start new Django projects with a structured and production-ready foundation.

## ✨ Features

* 🐍 Django project structure
* 🗄️ PostgreSQL database
* 🔐 `.env` environment configuration
* 🎨 Static & Media files setup
* ⚙️ Django Admin
* 📦 `requirements.txt`
* 🚫 `.gitignore` configuration

## 🛠️ Tech Stack

**Python · Django · PostgreSQL · python-dotenv · Git**

## 📁 Structure

```text
Django-Boilerplate/
├── .env
├── .gitignore
├── manage.py
├── requirements.txt
├── media/
├── static/
└── core/
    ├── settings.py
    ├── urls.py
    ├── asgi.py
    └── wsgi.py
```

## ⚡ Quick Start

```bash
git clone <repository-url>
cd Django-Boilerplate

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt

python manage.py migrate
python manage.py runserver
```

## 🔐 Environment Setup

Create a `.env` file:

```env
SECRET_KEY=your-secret-key

DB_NAME=your_database
DB_USER=your_username
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
```

> ⚠️ Never commit your `.env` file to GitHub.

## 👨‍💻 Author

**Abdullah Al Noman**

Built with ❤️ using Django.
