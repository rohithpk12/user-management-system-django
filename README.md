# User Management System

A Django-based user management application with role-based access control for administrators and customers.

## Features

- Admin and customer account roles
- Admin-only user creation, listing, updates, and deletion
- Customer registration and self-service profile updates
- Profile photo uploads with automatic compression for images larger than 1 MB
- Authentication, alert messages, navigation, sidebar, and dark dashboard theme
- Custom Django user model built on `AbstractUser`

## Technology

- Python 3.10
- Django 4.1.6
- SQLite for local development
- Bootstrap 5 and Django Crispy Forms
- Pillow for image handling

## Run locally

```bash
git clone https://github.com/rohithpk12/user-management-system-django.git
cd user-management-system-django
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
cp .env.example .env  # Windows: copy .env.example .env
python manage.py migrate
python manage.py runserver
```

Open `http://127.0.0.1:8000/` in your browser.

## Security notes

- The local SQLite database is intentionally excluded from version control.
- Set `DJANGO_SECRET_KEY` and `DJANGO_ALLOWED_HOSTS` with environment variables before deployment.
- Create an administrator account locally with `python manage.py createsuperuser`.

