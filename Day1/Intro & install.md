**What is Kubetnetes / k8 ?**

Kubernetes automates operational tasks of container management and includes built-in commands for deploying applications, rolling out changes to your applications, scaling your applications up and down to fit changing needs, monitoring your applications, and more—making it easier to manage applications.

''Populer Kubernetes Distributions:''

![image](https://github.com/kmahendra999/Kubernetes/assets/9668316/c685214a-194e-49fb-9731-c0338913f0bd)

**Why need K8 ?**

When we are creating / launching containers of our application the application will work but if in badluck


Components of Kubernetes Distribution

Kubernetes Distributions should contain particular elements in order to effectively develop and oversee a Kubernetes ecosystem. Among the essential elements of a Kubernetes Distribution are:

1.) Container run time

2.) Storage

3.) Networking


![1_30JgJtH4ZEs0HkFQJdUKRw](https://github.com/kmahendra999/Kubernetes/assets/9668316/13401d94-2b64-40c7-bdb7-a64d845892d8)

### Kubernetes install for local

![minikube-kind-k3s-local-kubernetes-cluster-1 -squaremedium](https://github.com/kmahendra999/Kubernetes/assets/9668316/70ffc2e0-f758-472f-9c7a-0d874c674c06)


#### install minicube for windows :

https://kubernetes.io/docs/tasks/tools/

Click button View minikube Get Started! Guide

Select plateform and download

![image](https://github.com/kmahendra999/Kubernetes/assets/9668316/a89f0d0d-a2ee-4c90-8581-c0403ad383c2)

Now click on **latest release** for Download

download and open

Copy : Destination Folder path for future use.

ex : C:\Program Files\Kubernetes\Minikube

open cmd 

cd C:\Program Files\Kubernetes\Minikube

----
NOTE :

enable hyper -v in your windows 

So during installetion machine will create in hyper -v

----

in cmd >> minikube.ese start

add path in Mycomputer (This pc) >> properties >> advance system setting >> advance tab >> Environment variables >> select path >> click on edit >>  click on new for add new path >> give value C:\Program Files\Kubernetes\Minikube

So you can add commands directoly from anywhere from cmd.

download kubectl and save in folder.

curl.exe -LO "https://dl.k8s.io/release/v1.29.0/bin/windows/amd64/kubectl.exe"

or download https://dl.k8s.io/release/v1.29.0/bin/windows/amd64/kubectl.exe from this url and save to same folder

<code>
C:\Program Files\Kubernetes\Minikube>doskey/history
cd C:\Program Files\Kubernetes\Minikube

minikube start
minikube delete
  
minikube start
kubectl get pods
kubectl create deployment mywebserver1 --image=httpd
kubectl get pods

kubectl delete pod mywebserver1-96 mywebserver1-9655b979-tmnxs
kubectl get pods

</code>

******************

Install minikube on linux

login with non root user

<code>IN RHEL 8
##download minikube
  curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

##minikube cluster create
minikube start

When got error : sudo usermod -a -G docker $USER && reboot

##kubectl command


     cd ~
   
     curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
   
     chmod a+x kubectl 
    
     sudo mv kubectl /usr/bin/
  
     kubectl get pods

</code>

