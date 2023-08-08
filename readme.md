# DOCKER PHP/MYSQL/NGINX

## Установка (тестировалась только на mac m1)

- Клонировать репозиторий
- Настроить yml/.env/и тд под себя если есть необходимость
- docker-compose build
- docker-compose up -d
- есть папка app, в ней хранится проект, по желанию можно переименовать
- docker-compose run --rm php composer create-project --prefer-dist laravel/laravel . (установка лаварел из контейнера)


## Возможные ошибки
Ошибка
- failed to solve: rpc error: code = Unknown desc = failed to solve with frontend dockerfile.v0: failed to create LLB definition: rpc error: code = Unknown desc = error getting credentials - err: exit status 1, out: ``

Решение

- rm ~/.docker/config.json

Ошибка

- open /Users/n/.docker/buildx/current: permission denied

Решение

- sudo docker-compose build