# SpendSmart — Personal Expense Tracker

Beginner-friendly portfolio project using Python, Django, SQLite, Django REST Framework and Bootstrap.

## Features
- User registration, login and logout
- Add, view, edit and delete income/expense transactions
- Monthly income, expenses and balance summary
- Search and filter transactions
- Per-user record isolation
- Authenticated REST API, Django admin and automated tests

## Windows / VS Code setup
Open the extracted folder containing `manage.py` and run each command separately:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python manage.py makemigrations transactions
python manage.py migrate
python manage.py runserver
```

Open http://127.0.0.1:8000/ and register an account.

If PowerShell blocks activation, switch the VS Code terminal to Command Prompt and run `.venv\Scripts\activate.bat`.

## Useful URLs
- `/` dashboard
- `/accounts/register/` registration
- `/accounts/login/` login
- `/admin/` admin site
- `/api/transactions/` REST API list/create
- `/api/transactions/<id>/` retrieve/update/delete

## Admin and tests
```bash
python manage.py createsuperuser
python manage.py test
```

## Security
This is a learning project. Before deployment, move `SECRET_KEY` to an environment variable, set `DEBUG=False`, configure `ALLOWED_HOSTS`, use HTTPS, and configure production hosting/database settings. Do not enter real sensitive financial information into a demo app.
