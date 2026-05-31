# День 16 — GitHub Actions Checkout

## Главная идея
GitHub runner сам по себе пустой. Чтобы получить файлы репозитория, нужен checkout.

## Что делает actions/checkout@v4
Скачивает содержимое репозитория в рабочую директорию runner.

## Разница между run и uses
run выполняет shell-команду.
uses подключает готовое GitHub Action.

## Что я проверил
- pipeline с checkout видит файлы репозитория
- pipeline без checkout не видит папку projects
- после возврата checkout pipeline снова работает

## Почему это важно
Для Docker build pipeline должен видеть Dockerfile и файлы проекта.
