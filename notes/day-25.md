# День 25 — Kubernetes Deployment

## Главная идея
Pod сам по себе одноразовый.
Deployment управляет Pod-ами и поддерживает desired state.

## Что такое Deployment
Deployment — объект Kubernetes, который управляет запуском и количеством Pod-ов.

## Что такое replicas
replicas — желаемое количество Pod-ов.

## Что я сделал
- создал Deployment nginx-deployment
- проверил Deployment
- посмотрел Pod-ы
- увеличил replicas до 3
- удалил один Pod вручную
- увидел, что Kubernetes создал новый Pod
- уменьшил replicas до 1
- посмотрел ReplicaSet
- удалил Deployment

## Команды
kubectl create deployment nginx-deployment --image=nginx
kubectl get deployments
kubectl get pods
kubectl get pods -o wide
kubectl describe deployment nginx-deployment
kubectl scale deployment nginx-deployment --replicas=3
kubectl delete pod <pod-name>
kubectl get rs
kubectl get deployment nginx-deployment -o yaml
kubectl delete deployment nginx-deployment

## Что такое desired state
Я описываю, сколько Pod-ов должно быть, а Kubernetes поддерживает это состояние.
