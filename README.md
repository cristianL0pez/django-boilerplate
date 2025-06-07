# django-boilerplate

This repository provides a simple Docker based environment with a pre-created
Django project named `backend`. The compose file also includes a PostgreSQL
container for local development.

## Setup

1. Build the Docker image:
   ```
   docker-compose build
   ```
2. Start the stack:
   ```
   docker-compose up
   ```
   This will start the Django app and a Postgres database.
3. Open a shell inside the web container if you need to run Django commands:
   ```
   docker-compose run --rm web bash
   ```
