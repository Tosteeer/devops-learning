# День 19 — Deployment Thinking

## Текущий pipeline

git push
→ GitHub Actions
→ checkout
→ docker build
→ success/failure

## Важно
Сейчас Docker image собирается внутри временного GitHub runner.
После завершения pipeline runner удаляется, и image исчезает.

## Почему это не deploy
Потому что image не отправляется в registry и не запускается на сервере.
