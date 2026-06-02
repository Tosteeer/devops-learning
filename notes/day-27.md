# День 27 — Kubernetes YAML manifests

## Главная идея
Kubernetes YAML описывает желаемое состояние ресурсов.

## Imperative vs Declarative
Imperative — выполнить команду действия.
Пример: kubectl create deployment ...

Declarative — описать состояние в YAML и применить.
Пример: kubectl apply -f deployment.yaml

## Что я создал
- deployment.yaml
- service.yaml

## Deployment
Deployment управляет Pod-ами и replicas.

## Service
Service даёт стабильный доступ к Pod-ам.

## Почему важны labels и selectors
Service находит Pod-ы по labels.
Если selector Service не совпадает с labels Pod-ов, endpoints будут пустыми.

## Команды
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get deployments
kubectl get pods --show-labels
kubectl get svc
kubectl get endpoints nginx-yaml-service
kubectl describe svc nginx-yaml-service
kubectl port-forward service/nginx-yaml-service 8088:80
kubectl delete -f service.yaml
kubectl delete -f deployment.yaml
