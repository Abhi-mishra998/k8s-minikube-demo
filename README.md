# Kubernetes Minikube Demo

## 📌 Project Overview
This project demonstrates deploying and managing applications in a **Kubernetes** cluster running locally on **Minikube**.  
It covers the complete lifecycle — from creating deployments and services to scaling pods and inspecting logs — giving hands-on experience with Kubernetes basics

## 🛠 Tools & Technologies
- **Kubernetes** (Minikube, kubectl)
- **Docker**
- **YAML** for Kubernetes manifests
- **Linux CLI**
## 📂 Project Structure
```
k8s-minikube-demo/
│── deployment.yaml   # Kubernetes Deployment for the application
│── service.yaml      # Kubernetes Service to expose the app
│── README.md         # Project documentation
```

## 🚀 Steps to Reproduce

### 1️⃣ Install Minikube & kubectl
```bash
# Install kubectl
curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/

# Install Minikube
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
### 2️⃣ Start Minikube Cluster
```bash
minikube start
```

### 3️⃣ Deploy Application
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 4️⃣ Verify Resources
```bash
kubectl get pods
kubectl get svc
```
### 5️⃣ Scale Deployment
```bash
kubectl scale deployment <deployment-name> --replicas=3
```
### 6️⃣ Inspect Logs & Describe
```bash
kubectl logs <pod-name>
kubectl describe pod <pod-name>
```

## 📷 Screenshots
> Add screenshots of:
> - `kubectl get pods`
> - `kubectl get svc`
> - Browser output if the service is exposed


<img width="1920" height="1080" alt="Screenshot_2025-08-11_13_44_36" src="https://github.com/user-attachments/assets/25cae4bf-a0c9-4c10-8ef6-589e385721fc" />

<img width="1920" height="1080" alt="Screenshot_2025-08-11_13_46_41" src="https://github.com/user-attachments/assets/e93879b1-a06b-4828-b6f8-40ddbbbb32b5" />


## 🎯 Learning Outcome
By completing this task, I gained hands-on experience with:
- Creating Kubernetes deployments & services
- Exposing applications to the network
- Scaling workloads dynamically
- Managing Kubernetes resources using `kubectl`

## 👨‍💻 Author
**Abhishek Mishra**  
💼 DevOps Enthusiast | 🚀 Passionate about Automation & Cloud Technologies  

