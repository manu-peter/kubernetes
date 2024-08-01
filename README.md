What is kubernetes and its uses?

Kubernetes or K8s is an open source container orchestration engine for automating deployment, scaling, and management of containerized applications. 

The open source project is hosted by the Cloud Native Computing Foundation (CNCF).

Kubernetes is originally developed by Google.

Inspired by Google's internal cluster management system, Borg, Kubernetes makes everything associated with deploying and managing your application easier. 

Kubernetes Providies automated container orchestration, Kubernetes improves your reliability and reduces the time and resources attributed to daily operations.

Objects of Kubernetes or K8s .

(1). Pod :

  *  Smallest objects that can be created using Kubernetes .
  *  Containers lives/works inside a pod .
  *  We dont manage containers directly , we manage pods and the pods manage the containers for us .

(2). service :

  * Service is to group a set of Pod endpoints into a single resource .
  * You can configure various ways to access the grouping. By default, you get a stable cluster IP address that clients inside the cluster can use to contact Pods in the Service .

(3). Replica set :

 * To create cluster of pods or replicas (copy) of the same pod .

(4). Deployment :

 * Deployment tells Kubernetes how to create or modify instances of the pods that hold a containerized application .
 * Deployments can help to efficiently scale the number of replica pods, enable the rollout of updated code in a controlled manner, or roll back to an earlier deployment version if necessary .

(5). Config Map :

 * To store our variables and configuration .
 * ConfigMap is a built-in Kubernetes API object that's designed to store your application's non-sensitive key-value config data .
 * ConfigMaps allow you to keep config values separate from your code and container images. Values can be strings or Base64-encoded binary data .

(6). Secret :

 * To store confidential data not in a clear text format (encrypted) .
 * Secret is an object that stores sensitive information, such as passwords, OAuth tokens, and SSH keys .

(7). Volume :

 * volume is a directory containing data accessible to containers in a given pod, the smallest deployable unit in a Kubernetes cluster .
 * volumes provide a plugin mechanism that connects ephemeral containers with persistent data storage .

Basic command of Kubernetes/K8s are :

Cluster Management Commands :

* kubectl cluster-info --> To Display cluster information .
* kubectl config view --> To View kubeconfig settings .
* kubectl config use-context CONTEXT_NAME --> To Switch between different Kubernetes contexts .

Pod Management Commands :

* kubectl get pods --> To List all pods in the current namespace .
* kubectl describe pod POD_NAME --> To Show detailed information about a specific pod .
* kubectl logs POD_NAME --> To Print the logs from a pod .
* kubectl exec -it POD_NAME -- COMMAND --> To Execute a command inside a container of a pod .

Deployment and Service Management :

* kubectl get deployments --> List all deployments .
* kubectl describe deployment DEPLOYMENT_NAME --> Show detailed information about a deployment .
* kubectl apply -f FILE.yaml --> Apply configuration changes defined in a YAML file .
* kubectl delete -f FILE.yaml --> Delete resources defined in a YAML file .
* kubectl expose deployment DEPLOYMENT_NAME --port=PORT --target-port=TARGET_PORT --> Expose a deployment as a service .

Namespace Management :

* kubectl get namespaces --> List all namespaces .
* kubectl create namespace NAMESPACE_NAME --> Create a new namespace .
* kubectl delete namespace NAMESPACE_NAME --> Delete a namespace .

Resource Management :

* kubectl get services --> List all services .
* kubectl get nodes --> List all nodes in the cluster .
* kubectl describe service SERVICE_NAME --> Show detailed information about a service .
* kubectl top pod --> Show resource usage (CPU/Memory) for pods .

Configuration and Scaling :

* kubectl scale deployment DEPLOYMENT_NAME --replicas=NUM --> Scale a deployment to a specified number of replicas .
* kubectl rollout status deployment DEPLOYMENT_NAME --> Get the rollout status of a deployment .
* kubectl rollout undo deployment DEPLOYMENT_NAME --> Roll back to the previous version of a deployment .

Advanced Usage :

* kubectl get events --> View events in the cluster .
* kubectl port-forward POD_NAME LOCAL_PORT:REMOTE_PORT --> Forward a local port to a port on a pod .
* kubectl cp POD_NAME:SOURCE_PATH DEST_PATH --> Copy files or directories to and from containers .
