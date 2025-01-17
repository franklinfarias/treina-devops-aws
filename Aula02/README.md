# Aula 02

Kubernetes com K3D.

Comandos utilizados:

````
kubectl get all
kubectl api-resources
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/deployment.yaml && watch 'kubectl get pod'
kubectl port-forward pod/<pod_name> 8080:5000
kubectl rollout history deployment conversao-distancia
kubectl rollout undo deployment conversao-distancia
````

## K3D

k3d is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.

Comandos utilizados:

````
k3d cluster create meucluster --servers 1 --agents 2
k3d cluster create meucluster --servers 1 --agents 2 -p "8080:30000@loadbalancer"
````

Fonte: https://k3d.io/stable/