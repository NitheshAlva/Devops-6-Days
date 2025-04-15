# 🚀 DevOps Training - Day 5  
### Kubernetes Cluster Creation, Configuration, and Namespace Management

---

## 🐳 What is Kubernetes?

Kubernetes is a **container orchestration platform** designed to automate the deployment, scaling, and management of containerized applications. It allows us to handle large-scale applications easily by managing clusters of machines.

---

## 📦 Kubernetes Cluster Components

A Kubernetes cluster consists of two primary components:

### 🧑‍💻 Master Node
The "brain" of the cluster. It controls the overall state and makes decisions about the cluster.

- **API Server**: Manages all the API requests for the cluster.
- **ETCD**: A distributed key-value store that holds the cluster's state.
- **Controller Manager**: Maintains the desired state of the cluster.
- **Scheduler**: Decides where to run a pod in the cluster based on resource availability.

### 🧑‍🏭 Worker Node
The nodes where containers (pods) run.

- **Kubelet**: Ensures that containers run in a pod and are healthy.
- **Container Runtime**: Responsible for pulling the container image and running it.
- **Kube-proxy**: Manages networking and routing for services.

---

## 🔧 Kubernetes Cluster Creation on AWS (EKS)

### Step 1: Launch EC2 Instance
- Go to AWS EC2 console
- Select **Ubuntu** as the OS and choose an instance type like `t2.medium`.
- Configure the instance as needed and launch it.
- SSH into the instance using **PuTTY** or another SSH tool.

---

### Step 2: Install Dependencies

#### 1. Install `kubectl`:

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256
echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
chmod +x kubectl
