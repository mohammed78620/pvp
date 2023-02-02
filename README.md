[![Django CI](https://github.com/mohammed78620/pvp/workflows/Django%20CI/badge.svg?branch=master&event=push)](https://github.com/mohammed78620/pvp/actions?query=workflow%3A%22Django+CI%22)
[![Docker Image](https://github.com/mohammed78620/pvp/workflows/Docker%20Image/badge.svg?branch=master&event=push)](https://github.com/mohammed78620/pvp/actions?query=workflow%3A%22Docker+Image%22)
[![Version](https://img.shields.io/github/v/release/mohammed78620/pvp?include_prereleases)](https://github.com/mohammed78620/pvp/releases)

# PvP

## Run this project with docker-compose

Recommended way of running local server is using `docker-compose up`. It will install all python and system dependencies inside the container and run local server with live reload. You can configure it to use/not use PostgreSQL. PostgreSQL and SQLite are only options for now.

### Interact with container

With these command you can run executables in your container:

```
docker-compose exec <service-name> <executable>
```

- **Create superuser**

```
docker-compose exec pvp ./manage.py createsuperuser
```

- **Open python shell**

```
docker-compose exec pvp ./manage.py shell
```

## Run this project without docker-compose

### Prepare poetry

- Install poetry

```bash
# Clone repository
git clone https://github.com/mohammed78620/pvp.git

# Change directory into project
cd pvp

# Install poetry
python3 -m pip install poetry

# Activate poetry
poetry shell

# Install python packages
poetry install

# Migrate database
python manage.py migrate

# Run server
python manage.py runserver
```

## Further documentation

You can find more specific documentations in `/docs` folder.
