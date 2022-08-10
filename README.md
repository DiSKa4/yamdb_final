![example workflow](https://github.com/github/docs/actions/workflows/main.yml/badge.svg)
# YaMDb API
    Проект YaMDb собирает отзывы пользователей на произведения.

## Шаблон наполнения .env:
    DB_ENGINE=django.db.backends.postgresql
    DB_NAME=postgres
    POSTGRES_USER=postgres
    POSTGRES_PASSWORD=postgres
    DB_HOST=db
    DB_PORT=5432

## Описание команд для запуска:
    Из папки /infra:

        docker-compose up -d

    Выполните миграции:

        docker-compose exec web python manage.py migrate

    Создайте суперпользователя:

        docker-compose exec web python manage.py createsuperuser

    Выполните команду collectstatic:

        docker-compose exec web python manage.py collectstatic --no-input

    Команда позволяет наполнить базу данных тестовыми данными:

        docker-compose exec web python3 manage.py loaddata fixtures.json

## Автор:
    Андрей Алексеевич
