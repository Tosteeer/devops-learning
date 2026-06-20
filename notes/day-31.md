# День 31 — Docker Registry и GHCR

## Главная идея
Registry хранит Docker images.

## Зачем нужен registry
Docker image, собранный в GitHub Actions runner, исчезает после завершения pipeline.
Чтобы image можно было использовать дальше, его нужно отправить в registry.

## Что такое GHCR
GHCR — GitHub Container Registry.
Адрес: ghcr.io

## Цепочка
git push
→ GitHub Actions
→ checkout
→ docker login ghcr.io
→ docker build
→ docker push
→ image сохранён в GHCR

## Почему нужен GITHUB_TOKEN
GitHub Actions использует GITHUB_TOKEN для публикации package/image в GHCR.

## Почему нужны permissions
contents: read — читать репозиторий.
packages: write — публиковать package/image.

## Что такое image tag
Tag — версия image.

Примеры:
- latest
- commit SHA

## Почему commit SHA полезен
Можно точно понять, из какого commit собран image.
Это важно для audit, rollback и troubleshooting.
