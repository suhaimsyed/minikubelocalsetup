1. Introduction to Minikube

Reference : https://kubernetes.io/docs/tutorials/hello-minikube/

Run  ```minikube start``` and   ```minikube dashboard```
To start the minikube and open a minikube dashboard

Run ```kubectl create deployment spring-boot-demo --image=realstore/springbootdemo:latest```
Use the kubectl create command to create a Deployment that manages a Pod. The Pod runs a Container based on the provided Docker image.

```kubectl get deployments``` and ```kubectl get pods``` 
can be used to view deployments and the pods

Other commands that can be used
kubectl config view
kubectl get events

Expose the Pod to the public internet using the kubectl expose command
```kubectl expose deployment spring-boot-demo --type=LoadBalancer --port=8080```
```minikube service spring-boot-demo```
```kubectl get services```


```minikube addons list
minikube addons enable metrics-server
minikube addons disable metrics-server```
