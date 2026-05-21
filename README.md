# Containerised Microservices Deployment using Docker & Kubernetes

````markdown
# 🚀 Containerised Microservices Deployment using Docker & Kubernetes

A cloud-native microservices project built using Docker, Kubernetes, Minikube, Flask, Prometheus, Grafana, and GitHub Actions CI/CD.

This project demonstrates how modern applications are containerized, orchestrated, monitored, and automated using DevOps and Cloud technologies.

---

# 📌 Project Overview

This project implements a multi-microservice architecture where independent services communicate inside a Kubernetes cluster.

The project includes:

- Docker containerization
- Kubernetes orchestration
- Multi-service deployment
- Service discovery
- Ingress controller
- Monitoring with Prometheus & Grafana
- CI/CD pipeline using GitHub Actions

---

# 🏗️ Architecture

Internet
↓
Ingress Controller
↓
Kubernetes Cluster (Minikube)
↓
Microservices
├── User Service
├── Product Service
└── Order Service
↓
Prometheus + Grafana Monitoring

---

# ⚙️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Python Flask | Backend Microservices |
| Docker | Containerization |
| Kubernetes | Container Orchestration |
| Minikube | Local Kubernetes Cluster |
| kubectl | Kubernetes CLI |
| Docker Hub | Image Repository |
| GitHub Actions | CI/CD Automation |
| Prometheus | Monitoring |
| Grafana | Visualization Dashboard |
| Ingress NGINX | API Routing |

---

# 📂 Project Structure

containerised-microservices/
│
├── user-service/
│ ├── app.py
│ ├── Dockerfile
│ └── requirements.txt
│
├── product-service/
│ ├── app.py
│ ├── Dockerfile
│ └── requirements.txt
│
├── order-service/
│ ├── app.py
│ ├── Dockerfile
│ └── requirements.txt
│
├── kubernetes/
│ ├── user-deployment.yaml
│ ├── user-service.yaml
│ ├── product-deployment.yaml
│ ├── product-service.yaml
│ ├── order-deployment.yaml
│ ├── order-service.yaml
│ └── ingress.yaml
│
└── .github/workflows/
└── deploy.yml

---

# 🔥 Features Implemented

## ✅ Docker Containerization
- Created Docker images for all microservices
- Exposed services using custom ports
- Built lightweight containerized applications

## ✅ Kubernetes Deployment
- Created Deployments & Services
- Implemented replica scaling
- NodePort service exposure

## ✅ Multi-Microservice Architecture
- User Service
- Product Service
- Order Service

## ✅ Service Discovery
- Internal Kubernetes DNS communication
- Microservice-to-microservice API calls

## ✅ Monitoring Stack
- Installed Prometheus using Helm
- Configured Grafana dashboards
- Monitored Kubernetes cluster metrics

## ✅ Ingress Controller
- Configured NGINX ingress
- Centralized API routing

## ✅ CI/CD Pipeline
- Automated Docker image build
- Automated Docker Hub push
- GitHub Actions workflow integration

---

# 🚀 Setup Instructions

## 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/containerised-microservices-deployment.git

cd containerised-microservices-deployment
````

---

## 2️⃣ Start Minikube

```bash
minikube start
```

---

## 3️⃣ Build Docker Images

### User Service

```bash
cd user-service
docker build -t user-service:v1 .
```

### Product Service

```bash
cd ../product-service
docker build -t product-service:v1 .
```

### Order Service

```bash
cd ../order-service
docker build -t order-service:v1 .
```

---

## 4️⃣ Load Images into Minikube

```bash
minikube image load user-service:v1
minikube image load product-service:v1
minikube image load order-service:v1
```

---

## 5️⃣ Deploy Kubernetes Resources

```bash
cd ../kubernetes

kubectl apply -f .
```

---

## 6️⃣ Verify Deployment

```bash
kubectl get pods
kubectl get services
```

---

## 7️⃣ Access Services

### User Service

```bash
minikube service user-service
```

### Product Service

```bash
minikube service product-service
```

### Order Service

```bash
minikube service order-service
```

---

# 📊 Monitoring Setup

## Install Prometheus & Grafana

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm install prometheus prometheus-community/kube-prometheus-stack
```

---

## Access Grafana

```bash
kubectl port-forward svc/prometheus-grafana 3000:80
```

Open:

```text
http://localhost:3000
```

---

# 🔄 CI/CD Pipeline

GitHub Actions pipeline automatically:

* Builds Docker images
* Pushes images to Docker Hub
* Automates deployment workflow

Workflow file:

```text
.github/workflows/deploy.yml
```

---

# 📈 Future Enhancements

* AWS EKS Deployment
* Horizontal Pod Autoscaler
* Helm Charts
* API Gateway
* Terraform Infrastructure
* Secrets & ConfigMaps
* Rolling Updates
* Blue-Green Deployment

---

# 🎯 Learning Outcomes

Through this project, I gained hands-on experience in:

* Docker Containerization
* Kubernetes Orchestration
* Microservices Architecture
* DevOps Automation
* Monitoring & Logging
* CI/CD Pipelines
* Cloud-Native Deployment

---

# 👨‍💻 Author

Ashoka R

Final Year CSE Student
Cloud Computing Intern at Rooman Technologies

Passionate about:

* Cloud Engineering
* DevOps
* Kubernetes
* Scalable Infrastructure
* Automation

---

# ⭐ Conclusion

This project demonstrates a complete cloud-native microservices deployment workflow using modern DevOps tools and practices. It showcases containerization, orchestration, monitoring, and CI/CD automation in a scalable Kubernetes environment.

```
```
