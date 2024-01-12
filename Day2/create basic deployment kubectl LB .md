we will deploy service and expose it on a port in local area network.

## recreting cluster
minikube status
minikube delete
minikube start

##checking pods and deployment and services
kubectl get pods
kubectl get deploy
kubectl get services

##creating new deployment and scale
kubectl create deploy myd1 --image=vimal13/apache-webserver-php
kubectl get pods -o wide
kubectl scale deploy myd1 --replicas=4
kubectl scale deployment myd1 --replicas=10

kubectl expose deployment myd1 --type=NodePort --port=80

kubectl get services

minikube ip

kubectl scale deploy myd1 --replicas=10

curl in browser :

minikube ip  : port which we got in kubectl get svc command after :

