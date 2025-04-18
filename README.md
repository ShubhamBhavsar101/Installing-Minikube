
# Installing Minikube on Linux

Follow these steps to set up Minikube along with required tools like `kubectl` and `Docker`.

---

## Install Minikube

```bash
curl -LO https://github.com/kubernetes/minikube/releases/latest/download/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
rm minikube-linux-amd64
```

---

## Install kubectl

```bash
sudo snap install kubectl --classic
```

### alias kubectl
```bash
alias k='kubectl'
source ~/.bashrc
```

---

## Install Docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

---

## Set Up for `--driver=none` (Optional)

```bash
sudo apt update
sudo apt install iptables
sudo apt install -y conntrack
```

### Install crictl (Optional - for Kubernetes compatibility)

> Make sure the version matches your Kubernetes version.

```bash
VERSION="v1.29.0"
curl -LO https://github.com/kubernetes-sigs/cri-tools/releases/download/${VERSION}/crictl-${VERSION}-linux-amd64.tar.gz
sudo tar -C /usr/local/bin -xzf crictl-${VERSION}-linux-amd64.tar.gz
rm crictl-${VERSION}-linux-amd64.tar.gz
```

---

## Install Kubeshark
```bash
sh <(curl -Ls https://kubeshark.co/install)  
kubeshark tap  
```


