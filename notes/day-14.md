# День 14 — Docker Compose Mini Project

## Что я собрал
Мини-проект на Docker Compose:
- nginx
- bind mount
- port mapping
- custom HTML page

## Структура проекта
docker-mini-project/
├── docker-compose.yml
└── html/
    └── index.html

## Как запустить
docker compose up -d

## Как проверить
curl localhost:8085

## Как посмотреть логи
docker compose logs web

## Как зайти внутрь
docker compose exec web bash

## Что делает stop
Останавливает контейнеры.

## Что делает start
Запускает остановленные контейнеры.

## Что делает down
Удаляет контейнеры и сеть проекта.
