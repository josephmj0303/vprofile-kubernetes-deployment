# VProfile Application Deployment on Kubernetes (AWS EKS / Self-Managed Cluster)

## 📌 Project Overview
This project demonstrates deploying the **VProfile Java Microservices Application** into a Kubernetes cluster using Infrastructure-as-Code and Kubernetes manifests.

The goal of this project is to showcase **container orchestration, persistent storage management, service discovery, secrets management, and ingress-based routing** in a production-like DevOps setup.

---

## 🏗 Architecture

### High Level Flow

Application Load Balancer → Ingress → Tomcat Service → Microservices → Backend Services


### Components
- Kubernetes Cluster
- Ingress Controller
- Tomcat Application Service
- RabbitMQ Message Broker
- Memcached Caching Layer
- MySQL Database with Persistent Storage
- Kubernetes Secrets
- Storage Class with AWS EBS

---

## 🧰 Technology Stack

| Category | Tools |
|-----------|------------|
| Containerization | Docker |
| Orchestration | Kubernetes |
| Cloud Provider | AWS |
| Storage | AWS EBS |
| Messaging | RabbitMQ |
| Cache | Memcached |
| Database | MySQL |
| CI/CD (Optional Extension) | GitHub Actions / Jenkins |
| IaC (Optional Extension) | Terraform / Kops |

---

## 📂 Repository Structure

```
vprofile-kubernetes-deployment/
│
├── kubernetes-manifests/
│ ├── db/
│ ├── cache/
│ ├── mq/
│ ├── app/
│ ├── ingress/
│ ├── storage/
│ └── secrets/
│
├── docs/
│ ├── architecture.md
│ ├── deployment-guide.md
│ ├── troubleshooting.md
│
├── scripts/
│ ├── cluster-setup.sh
│ ├── deploy.sh
│
└── README.md
```


---

## 🚀 Deployment Workflow

### Step 1: Setup Kubernetes Cluster
- Provision cluster using Kops / EKS
- Configure kubectl access

### Step 2: Create Storage Resources
- StorageClass
- PersistentVolumeClaim

### Step 3: Deploy Backend Services
- MySQL Database
- RabbitMQ
- Memcached

### Step 4: Deploy Application Layer
- Tomcat Application
- Service Resources

### Step 5: Configure Networking
- Ingress Controller
- Load Balancer

---

## 🔐 Secrets Management
Sensitive data like database credentials are stored securely using Kubernetes Secrets.

---

## 💾 Persistent Storage
MySQL uses:
- PersistentVolumeClaim
- AWS Elastic Block Storage

---

## 📊 Key DevOps Skills Demonstrated
- Kubernetes Resource Management
- Stateful Application Deployment
- Service Discovery
- Storage Orchestration
- Secure Secret Handling
- Cloud Native Application Deployment

---

## 📈 Future Enhancements
- Helm Chart Packaging
- GitOps using ArgoCD
- Monitoring using Prometheus & Grafana
- Automated CI/CD Pipelines

---

## 👨‍💻 Author
Joseph MJ
DevOps Engineer

