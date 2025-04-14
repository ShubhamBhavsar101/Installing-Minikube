# Installing-Minikube

1. Execute the following commands to install minikube on Linux
curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

2. Install Kubectl
sudo snap install kubectl --classic

2. Commands after installation
minikube start

kubectl get nodes

kubectl create -f simple-pod.yaml

kubectl get pods -A
kubectl get pods -o wide

minikube ssh

kubectl delete pod nginx

kubectl logs nginx
kubectl describe pod nginx

