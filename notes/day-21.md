# День 21 — CI/CD Mini Project

## Что я собрал
Мини-проект, где GitHub Actions автоматически собирает Docker image.

## Цепочка
Изменение index.html
→ git commit
→ git push
→ GitHub Actions
→ checkout
→ docker build
→ зелёный или красный pipeline

## Docker project
projects/my-nginx-image/
- Dockerfile
- index.html

## Workflow
.github/workflows/hello.yml

## Что проверяет pipeline
- Docker доступен на runner
- файлы проекта существуют
- Docker image успешно собирается

## Почему это CI
Потому что pipeline проверяет изменение после push.

## Почему это ещё не CD
Потому что image пока не отправляется в registry и не деплоится на сервер.
