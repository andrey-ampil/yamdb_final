### Описание проекта

Сайт на джанго с минималистичным интерфейсом.

Хранилище информации о музыкальных произведениях. 

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/andrey-ampil/infra_sp2
```

```
cd infra_sp2/infra
```

Написать файлик .env по шаблону:

```
DB_NAME=
POSTGRES_USER=
POSTGRES_PASSWORD=
DB_HOST=
DB_PORT=
```

Cоздать и активировать группу контейнеров:

```
docker-compose up -d --build
```

Мигрируем:
```
docker-compose exec web python manage.py migrate
```
```
docker-compose run --rm web bash
python manage.py createsuperuser
exit
```
```
docker-compose exec web python manage.py collectstatic --no-input
```

https://github.com/andrey-ampil
2022 ©andrey-ampil

![example workflow](https://github.com/andrey-ampil/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

Check that it's work: http://84.252.143.26:8000/admin
