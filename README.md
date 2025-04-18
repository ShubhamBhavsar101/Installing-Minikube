# Installing-Minikube

1. Execute the following commands to install minikube on Linux
curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

2. Install Kubectl
sudo snap install kubectl --classic

3. Install Docker
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker

4. To run with --driver=none
sudo apt update
sudo apt install iptables

sudo apt install -y conntrack

VERSION="v1.29.0"  # or change this to match your Kubernetes version
curl -LO https://github.com/kubernetes-sigs/cri-tools/releases/download/${VERSION}/crictl-${VERSION}-linux-amd64.tar.gz
sudo tar -C /usr/local/bin -xzf crictl-${VERSION}-linux-amd64.tar.gz
rm crictl-${VERSION}-linux-amd64.tar.gz



