# Postgres in Docker - Minimal Configuration

Goals
-----

- Create a new empty repository on our Gitlab for your code and clone it to your local machine
- Create a ``docker-compose.yml`` file to run the postgres Docker image with ``docker-compose up`` in development mode: https://hub.docker.com/_/postgres/
    - Map a docker volume called ``postgres`` to the folder ``/var/lib/postgresql/data`` into the container so that every change to the database stays persistant after container restart.
    - Map the port ``4777`` on the host to the container port ``5432``
- Create a ``docker-compose.prod.yml`` file to run your Docker image in production mode with ``docker-compose -f 'docker-compose.prod.yml' up -d``
    - Don`t map any ports into the container
    - Make sure you keep the volume mapping
