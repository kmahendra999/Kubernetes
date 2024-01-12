we will deploy service and expose it on a port in local area network.
<code>
## recreting cluster
minikube status
minikube delete
minikube start
</code>

<code>
##checking pods and deployment and services
kubectl get pods
kubectl get deploy
kubectl get services
</code>

<code>
##creating new deployment and scale
kubectl create deploy myd1 --image=vimal13/apache-webserver-php
kubectl get pods -o wide
kubectl scale deploy myd1 --replicas=4
kubectl scale deployment myd1 --replicas=10
</code>

<code>
kubectl expose deployment myd1 --type=NodePort --port=80
</code>

<code>
kubectl get services
</code>

<code>
minikube ip
</code>

<code>
kubectl scale deploy myd1 --replicas=10
</code>

<code>
curl in browser :

minikube ip  : port which we got in kubectl get svc command after :

