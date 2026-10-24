# Flask To-Do App

A To-Do application built using Python, Flask, Flask-SQLAlchemy, SQLite, HTML and CSS.

## Features

- User registration and login
- Password hashing
- Session-based authentication
- Add new tasks
- View all tasks
- Update task status: Pending → Working → Done
- Clear all tasks
- Flash messages for success and errors

## Tech Stack

- Python
- Flask
- Flask-SQLAlchemy
- SQLite
- HTML and CSS
- Jinja2 Templates

## Project Structure

```text
TO DO App/
├── app/
│   ├── __init__.py
│   ├── models.py
│   └── routes/
│       ├── __init__.py
│       ├── auth.py
│       ├── tasks.py
│       └── templates/
│           ├── base.html
│           ├── login.html
│           ├── register.html
│           └── tasks.html
├── static/
│   └── css/
│       └── style.css
├── run.py
├── requirements.txt
├── API_ENDPOINTS.md
└── README.md
```

## Installation

1. Clone the repository.
2. Create and activate a Python virtual environment.
3. Install dependencies:

```bash
python -m pip install -r requirements.txt
```

## Run the Application

```bash
python run.py
```

Open `http://127.0.0.1:5000/` in your browser.

## API and Routes

See [API_ENDPOINTS.md](API_ENDPOINTS.md) for the application's routes, HTTP methods and behavior.

## Security Notes

- Passwords should be stored as hashes.
- Keep secret keys outside source control in production.
- Protect authenticated routes and validate user input.
