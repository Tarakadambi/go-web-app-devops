DevOps GitOps CI/CD Pipeline — Go Web App
📌 Overview

This project demonstrates a complete end-to-end DevOps pipeline using:

GitHub (Source Control)
GitHub Actions (CI)
Docker (Containerization)
Helm (Kubernetes packaging)
Argo CD (GitOps Continuous Deployment)
Kubernetes (Minikube cluster)

The system automatically builds, tests, containerizes, and deploys the Go web application on every code change.

**Architecture**

Developer → GitHub → GitHub Actions (CI)
                         ↓
                   Docker Image
                         ↓
                 Docker Hub Registry
                         ↓
                    GitOps (Argo CD)
                         ↓
                 Kubernetes Cluster
                         ↓
                  Running Application


**Tech Stack**
Layer	Technology
App	Go (Golang)
CI	GitHub Actions
CD	Argo CD
Container	Docker
Orchestration	Kubernetes (Minikube)
Packaging	Helm
Registry	Docker Hub

CI/CD Workflow
CI (GitHub Actions)

On every push to main:

Build Go application
Run unit tests
Build Docker image
Push image to Docker Hub
CD (Argo CD GitOps)
Watches GitHub repo
Detects Helm chart changes
Automatically syncs Kubernetes cluster
Deploys updated application
**📦 Project Structure**
go-web-app-devops/
│
├── .github/workflows/        # CI pipeline (GitHub Actions)
├── go-web-app-chart/         # Helm chart (K8s deployment)
├── argocd/                   # Argo CD applications
├── screenshots/              # UI & deployment screenshots
├── main.go                   # Go application
├── Dockerfile                # Container build
└── README.md
📸 Application Screenshots
🏠 Home Page

**🔍 Argo CD Dashboard**

**🚀 How to Run Locally**
1. Clone repo
git clone https://github.com/Tarakadambi/go-web-app-devops.git
cd go-web-app-devops
2. Run application locally
go run main.go
3. Build Docker image
docker build -t go-web-app .
docker run -p 8080:8080 go-web-app
4. Access application
http://localhost:8080/home
☸️ Kubernetes Deployment (Helm)
helm install go-web-app go-web-app-chart/
🔁 Argo CD Sync

**Argo CD automatically syncs changes from GitHub:**

Dev environment
Stage environment
Prod environment
📈 Key Features
✅ Full CI/CD automation
✅ GitOps-based deployment
✅ Multi-environment setup (dev/stage/prod)
✅ Dockerized application
✅ Kubernetes Helm deployment
✅ Auto rollback capability (Argo CD)
✅ Self-healing deployments
**🧠 What I Learned**
GitOps workflow using Argo CD
Kubernetes deployment using Helm
CI/CD automation with GitHub Actions
Docker image lifecycle management
Multi-environment deployment strategy
**🏆 Project Status**
✔ CI pipeline working
✔ CD via Argo CD working
✔ Kubernetes deployments healthy
✔ Full GitOps workflow implemented

**📌 Author**
**Tara Kadambi**

