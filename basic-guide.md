List item

### Create a Deployment
A Kubernetes Pod is a group of one or more Containers, tied together for the purposes of administration and networking.
1. Use the `kubectl create` command to create a Deployment that manages a Pod. The Pod runs a Container based on the provided Docker image.
````shell
kubectl create deployment hello-node --image=k8s.gcr.io/echoserver:1.4
````
2. View the Deployment:
````shell
kubectl get deployments
````
3. View the Pod:
````shell
kubectl get pods
````
4. View cluster events:
````shell
kubectl get events
````
5. View the `kubectl` configuration:
```shell
kubectl config view
```
