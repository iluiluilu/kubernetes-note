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

### Create a Service
By default, the Pod is only accessible by its internal IP address within the Kubernetes cluster. To make the `hello-node` Container accessible from outside the Kubernetes virtual network, you have to expose the Pod as a Kubernetes Service.
1. Expose the Pod to the public internet using the `kubectl` expose command:
  `kubectl expose deployment hello-node --type=LoadBalancer --port=8080`
  The --type=LoadBalancer flag indicates that you want to expose your Service outside of the cluster.
