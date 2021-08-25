1. Introduction to Minikube

Reference : https://kubernetes.io/docs/tutorials/hello-minikube/

Run  ```minikube start``` and   ```minikube dashboard```
To start the minikube and open a minikube dashboard

Run ```kubectl create deployment spring-boot-demo --image=realstore/springbootdemo:latest```
Use the kubectl create command to create a Deployment that manages a Pod. The Pod runs a Container based on the provided Docker image.

```kubectl get deployments``` and ```kubectl get pods -o wide``` 
can be used to view deployments and the pods

Other commands that can be used
kubectl config view
kubectl get events

Expose the Pod to the public internet using the kubectl expose command
```kubectl expose deployment spring-boot-demo --type=LoadBalancer --port=8080```
```minikube service spring-boot-demo```
```kubectl get services```


```minikube addons list```
```minikube addons enable metrics-server```
```minikube addons disable metrics-server```

To scale up the node
```kubectl scale deployments/spring-boot-demo --replicas=4```

To terminate all nodes
```kubectl scale deployments/spring-boot-demo --replicas=0```

Status of rolling update
```kubectl rollout status deployments/spring-boot-demo```

To start and undo a rolling update
```kubectl set image deployments/spring-boot-demo springbootdemo=jocatalin/kubernetes-bootcamp:v2```
```kubectl rollout undo deployments/spring-boot-demo```
