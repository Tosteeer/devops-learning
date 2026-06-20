# День 30 — Итоговая архитектура DevOps pipeline

## Полный путь приложения

Developer
→ Git commit
→ Git push
→ GitHub Actions
→ Checkout repository
→ Docker build
→ Docker image
→ Docker registry
→ Kubernetes Deployment
→ Pod
→ Container
→ Service
→ User

## Что происходит на каждом этапе

### Developer
Разработчик меняет код приложения.

### Git
Git сохраняет историю изменений через commit.

### GitHub
GitHub хранит удалённый репозиторий.

### GitHub Actions
Pipeline автоматически запускается после push.

### Checkout
actions/checkout скачивает код репозитория в runner.

### Docker build
Pipeline собирает Docker image из Dockerfile.

### Docker registry
Registry хранит Docker images, чтобы серверы и Kubernetes могли их скачать.

### Kubernetes Deployment
Deployment описывает, какой image запускать и сколько Pod-ов поддерживать.

### Pod
Pod — минимальная единица запуска в Kubernetes.

### Container
Container запускается внутри Pod-а из Docker image.

### Service
Service даёт стабильный сетевой доступ к Pod-ам.

### User
Пользователь обращается к приложению через сетевой вход.
