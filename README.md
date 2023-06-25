# Kubernetes-Minikube

1. Install minikube
2. To check minikube is installed.Type: **minikube version**
3. Create a cluster on your host machine using docker as VM. Type:  **minikube start --driver=docker --network host**
4. Make sure that the cluster has internet connection. Type: **minikube ssh ping google.com**
5. Create a demo deployment. Type: **kubectl create deployment nginx-depl --image=nginx**
6. Check that deployment and the pod is ready. Type: **kubectl get deployment | kubectl get pod**
7. Status should be ready

To create deployment by reading from a configuration file. Type: **kubectl apply -f nginx-deployment.yaml**
https://anuradha.hashnode.dev/kubernetes-with-mongo-express-app


**Kubectl Basic Commands**

**✏️ Get Status of K8s Components**

    kubectl get nodes : get the status of nodes

    kubectl version: get the latest version

    kubectl get services: get a list of all services

**✏️ Debugging Pods**

    kubectl logs [POD_NAME]: shows what the application inside the pod logs.
    
    kubectl describe pod [POD_NAME]: shows additional information about pods and all the state changes that happen inside the pod.
    
    kubectl exec -it [POD_NAME] -- bin/bash : start a shell session for containers running in a K8s cluster. It’s a bit like SSH for Kubernetes.

**✏️ CRUD Operations**

    kubectl create deployment [DEPLOYMENT_NAME]: to create a deployment
    
    kubectl get deployments: to get a list of all deployments
    
    kubectl edit deployment [DEPLOYMENT_NAME]: to update the deployment
    
    kubectl delete deployment [DEPLOYMENT_NAME]: to delete deployment

**✏️ Resource Metrics**

    kubectl top pod : Display resource (CPU/memory) usage of pods
    
    kubectl top node : Display resource (CPU/memory) usage of nodes
