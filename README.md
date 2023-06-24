# Kubernetes-Minikube

1. Install minikube
2. To check minikube is installed.Type: minikube version
3. Create a cluster on your host machine using docker as VM. Type:  minikube start --driver=docker --network host
4. Make sure that the cluster has internet connection. Type: minikube ssh ping google.com
5. Create a demo deployment. Type: kubectl create deployment nginx-depl --image=nginx
6. Check that deployment and the pod is ready. Type: kubectl get deployment | kubectl get pod
7. Status should be ready
