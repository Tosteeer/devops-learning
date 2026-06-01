# День 23 — kubectl и minikube

## Главная идея
kubectl — CLI для управления Kubernetes.
minikube — локальный Kubernetes cluster для обучения.

## Что такое kubectl
kubectl отправляет команды в Kubernetes API Server.

## Что такое minikube
minikube поднимает локальный Kubernetes cluster на моей машине.

## Что я установил
- kubectl
- minikube

## Команды
kubectl version --client
minikube version
minikube start --driver=docker
kubectl get nodes
kubectl get pods -A
kubectl config current-context
minikube status

## Что такое node
Node — сервер, на котором Kubernetes запускает workloads.

## Что такое context
Context показывает, с каким cluster сейчас работает kubectl.
