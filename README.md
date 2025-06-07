# Django Boilerplate

This repository provides a minimal Docker setup for creating new Django
projects. It ships with a sample project called `backend` and a PostgreSQL
database service for local development.

## Getting Started

1. Build the Docker image:
   ```bash
   docker-compose build
   ```

2. Create a copy of the example environment file:
   ```bash
   cp .env.example .env
   ```
   Edit `.env` to customize `SECRET_KEY`, `DEBUG`, `ALLOWED_HOSTS` and the
   database settings if needed.
3. Start the services:
   ```bash
   docker-compose up
   ```
   This will start both the Django app and the database.

4. Apply migrations (in a separate terminal):
   ```bash
   docker-compose run --rm web python manage.py migrate
   ```

5. (Optional) Create a superuser account:
   ```bash
   docker-compose run --rm web python manage.py createsuperuser
   ```

You can now access the development server at `http://localhost:8000`.

To run additional Django commands, open a bash session in the container:
```bash
docker-compose run --rm web bash
```
