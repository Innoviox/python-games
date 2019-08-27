# python-games

## Setup Guide

### Initialize Project

First, you need to initialize the project from https://github.com/tiangolo/full-stack-fastapi-postgresql. 

```bash
$ pip install cookiecutter
$ cookiecutter https://github.com/tiangolo/full-stack-fastapi-postgresql
```

Input this information:

```html
project_name [Base Project]: games
project_slug [games]: 
domain_main [games.com]: games.derekthesnake.me
domain_staging [stag.games.derekthesnake.me]: 
docker_swarm_stack_name_main [games-derekthesnake-me]: 
docker_swarm_stack_name_staging [stag-games-derekthesnake-me]: 
secret_key [changethis]: 1e29a5c0044841737ef76fb0b7151cda0e91c7e4ccaef192848b7f3bcb38c6c9
first_superuser [admin@games.derekthesnake.me]: awefjiop
first_superuser_password [changethis]: awefjioP
backend_cors_origins [http://localhost, http://localhost:4200, http://localhost:3000, http://localhost:8080, https://localhost, https://localhost:4200, https://localhost:3000, https://localhost:8080, http://dev.games.derekthesnake.me, https://stag.games.derekthesnake.me, https://games.derekthesnake.me, http://local.dockertoolbox.tiangolo.com, http://localhost.tiangolo.com]: 
smtp_port [587]: 
smtp_host []: 
smtp_user []: 
smtp_password []: 
smtp_emails_from_email [info@games.derekthesnake.me]: 
postgres_password [changethis]: awefjioP
pgadmin_default_user [awefjiop]: 
pgadmin_default_user_password [awefjioP]: 
traefik_constraint_tag [games.derekthesnake.me]: 
traefik_constraint_tag_staging [stag.games.derekthesnake.me]: 
traefik_public_network [traefik-public]: 
traefik_public_constraint_tag [traefik-public]: 
flower_auth [admin:awefjioP]: 
sentry_dsn []: 
docker_image_prefix []: 
docker_image_backend [backend]: 
docker_image_celeryworker [celeryworker]: 
docker_image_frontend [frontend]: 
```

(Note that secret_key is the output of `openssl rand -hex 32`.)

### How to run project locally

This project is built and run with `docker-compose`. You have to install docker and docker-compose, look it up. Then, in the `/games` directory, run:

```bash
$ docker-compose up -d --build
```

Several useful commands:

To run a command within the backend: `docker-compose exec backend bash`

To get logs from the backend: `docker-compose logs backend`

​	add `-f` for real-time logs



