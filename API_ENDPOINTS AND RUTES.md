# API Endpoints and Routes

Base URL: `http://127.0.0.1:5000`

This application currently uses Flask routes for HTML pages and form submissions. These are not necessarily JSON REST API endpoints.

| Method | Endpoint | Flask Endpoint | Description |
|---|---|---|---|
| GET | `/login` | `auth.login` | Display login form |
| POST | `/login` | `auth.login` | Authenticate user |
| GET | `/register` | `auth.register` | Display registration form |
| POST | `/register` | `auth.register` | Register a new user |
| GET | `/logout` | `auth.logout` | Log out the current user |
| GET | `/tasks` | `tasks.view_tasks` | Display tasks |
| POST | `/add` | `tasks.add_task` | Add a new task |
| POST | `/toggle/<task_id>` | `tasks.toggle_status` | Change task status |
| POST | `/clear` | `tasks.clear_tasks` | Delete all tasks |

## 1. User Registration

**Endpoint:** `/register`

**Method:** `GET`, `POST`

- `GET`: Returns the registration form.
- `POST`: Accepts the user's name, email, username and password, validates the data, hashes the password and saves the user.

## 2. User Login

**Endpoint:** `/login`

**Method:** `GET`, `POST`

- `GET`: Displays the login form.
- `POST`: Verifies the username and password and creates a session for a valid user.

## 3. View Tasks

**Endpoint:** `/tasks`

**Method:** `GET`

Displays the tasks for the application. Access should be restricted to authenticated users.

## 4. Add Task

**Endpoint:** `/add`

**Method:** `POST`

Expected form field:

- `title`: Task title

Creates a new task with the initial status `pending`.

## 5. Toggle Task Status

**Endpoint:** `/toggle/<task_id>`

**Method:** `POST`

Changes the task status through the following cycle:

`pending → working → done → pending`

## 6. Clear Tasks

**Endpoint:** `/clear`

**Method:** `POST`

Deletes tasks from the database. This operation should be restricted to authorized users.

## Important Notes

- Login and registration use HTML form submissions.
- The application uses session-based authentication.
- These routes currently return HTML pages or redirects rather than a documented JSON API.
- Verify route behavior against the current source code before publishing this documentation.
