# Prompts for Backend

## 1. GitHub Copilot Agent Prompt

Generate a `docker-compose.yaml` file for deploying a PostgreSQL database. Requirements:
- Use the **latest image**.
- Add `restart: unless-stopped`.
- Assign a **container name**.
- Set environment variables for **Postgres**.

## 2. Project Initialization

- Initialize a new project using **uv**.

## 3. Dependency Installation

Install the following dependencies using `uv`:
```
fastapi uvicorn sqlmodel alembic psycopg2-binary
```

## 4. App Structure

Create an `/app` folder and add the following files:
- `config.py`
- `crud.py`
- `database.py`
- `main.py`
- `models.py`
- `__init__.py`

## 5. Configuration

- In `config.py`, load the `DATABASE_URL` from the `.env` file in the root.

## 6. Basic FastAPI App

- Using the current environment and dependencies, in `main.py` (inside `/app`), create a FastAPI app with **one test endpoint** to verify the setup.

## 7. Run the Application

- Start the application.

## 8. Step-by-Step Guide for Creating a Todo App

Provide a structured set of steps:

### Project Setup
- Initialize Python project (done with `uv`).
- Install dependencies:
  ```
  fastapi, uvicorn, sqlmodel, alembic, psycopg2-binary
  ```

### Database Configuration
- Set up **PostgreSQL** using Docker Compose (already done).
- Add a `.env` file with your `DATABASE_URL`.

### App Structure
- Create an `app` directory with:
  - `main.py` – FastAPI entry point
  - `models.py` – SQLModel models
  - `database.py` – DB session and engine
  - `crud.py` – CRUD operations
  - `config.py` – Settings/config
  - `__init__.py`

### Define Models
- In `models.py`, define a `Todo` model with fields:
  - `id`
  - `title`
  - `description`
  - `completed`
  - `priority`

### Database Engine & Session
- In `database.py`:
  - Set up SQLModel engine using `DATABASE_URL`.
  - Create a session dependency for FastAPI routes.

### CRUD Operations
- In `crud.py`, implement functions to:
  - Create
  - Read
  - Update
  - Delete todos using SQLModel sessions.

### API Endpoints
- In `main.py`, create FastAPI routes:
  - **POST** `/todos` – Create a todo
  - **GET** `/todos` – List todos
  - **GET** `/todos/{id}` – Get single todo
  - **PUT** `/todos/{id}` – Update todo
  - **DELETE** `/todos/{id}` – Delete todo

### Alembic Setup for Migrations
- Initialize Alembic:
  ```
  alembic init alembic
  ```
- Configure:
  - `alembic.ini` → Set `sqlalchemy.url`
  - `env.py` → Set `target_metadata = SQLModel.metadata`
  - Import `sqlmodel` in `env.py`

- Generate and apply migration:
  ```
  alembic revision --autogenerate -m "initial migration"
  alembic upgrade head
  ```

### Run the Application
- Start FastAPI app:
  ```
  uvicorn app.main:app --reload
  ```
- Visit Swagger UI at: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 9. Follow All Steps

Ensure each section is completed in sequence.

## 10. Notes When Starting Alembic

- Verify `sqlalchemy.url` in `alembic.ini`.
- Ensure `target_metadata = SQLModel.metadata` in `env.py`.
- Import `sqlmodel` in Alembic environment.
