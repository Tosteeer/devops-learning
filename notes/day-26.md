# День 26 — Kubernetes Service

## Главная идея
Pod-ы временные, их IP может меняться.
Service даёт стабильный сетевой доступ к Pod-ам.

## Что такое Service
Service — объект Kubernetes, который направляет трафик к Pod-ам.

## Почему Service нужен
Pod может быть удалён и создан заново.
IP Pod-а может измениться.
Service остаётся стабильной точкой доступа.

## Что такое label
Label — метка объекта Kubernetes.
Service находит Pod-ы по labels.

## Что такое ClusterIP
Внутренний Service, доступный только внутри cluster.

## Что такое NodePort
Service, который открывает порт на Kubernetes node.

## Что такое Endpoint
Реальный Pod IP, куда Service отправляет трафик.

## Что я сделал
- создал Deployment nginx-deployment
- посмотрел labels Pod-а
- создал ClusterIP Service
- проверил доступ из curl-test Pod
- создал NodePort Service
- проверил доступ через minikube service или port-forward
- увеличил replicas до 3
- посмотрел endpoints
- удалил один Pod
- увидел, что Service продолжает работать
- удалил Service и Deployment

## Команды
kubectl create deployment nginx-deployment --image=nginx
kubectl get pods --show-labels
kubectl expose deployment nginx-deployment --port=80 --target-port=80 --type=ClusterIP
kubectl get svc
kubectl run curl-test --image=curlimages/curl -it --rm -- sh
curl nginx-deployment
kubectl delete service nginx-deployment
kubectl expose deployment nginx-deployment --port=80 --target-port=80 --type=NodePort
minikube service nginx-deployment --url
kubectl port-forward service/nginx-deployment 8088:80
kubectl describe service nginx-deployment
kubectl get endpoints nginx-deployment
kubectl scale deployment nginx-deployment --replicas=3
kubectl delete service nginx-deployment
kubectl delete deployment nginx-deployment
