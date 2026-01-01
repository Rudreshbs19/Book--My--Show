BookMyShow – CI/CD Automation with Kubernetes Deployment

This project is a BookMyShow clone application deployed using a complete DevOps automation workflow. It demonstrates CI/CD implementation using Jenkins, Docker, and Kubernetes to automate build, test, and deployment processes.

The objective is to replicate a production-grade deployment pipeline with minimal manual intervention.

Features

 CI/CD pipeline using Jenkins
 Automated Docker image build & push
 Deployment on Kubernetes cluster
 Microservice architecture-ready
Version-controlled infrastructure & automation configs
 Real-world DevOps demonstration project
 
| Layer            | Tools & Tech                               |
| ---------------- | ------------------------------------------ |
| Frontend         | HTML, CSS, JS (inside bookmyshow-app)      |
| Backend          | Node.js *(as per available code patterns)* |
| Containerization | Docker                                     |
| CI/CD            | Jenkins                                    |
| Orchestration    | Kubernetes (deployment.yml, service.yml)   |
| Repo & SCM       | Git + GitHub                               |



 CI/CD Workflow
Developer Commit →GitHub Webhook →Jenkins Pipeline →Build & Test App →Docker Build →Push to Registry →Deploy on Kubernetes →Service Available via NodePort/Ingress


Repository Structure
.
├── bookmyshow-app/        # Web app source code
├── Jenkinsfile1           # CI/CD pipeline with basic steps
├── Jenkinsfile2           # Enhanced pipeline variant
├── deployment.yml         # Kubernetes deployment config
├── service.yml            # Kubernetes service exposure config
└── README.md              # Project documentation

⚙️ Jenkinsfile Pipeline (Overview)
Stage	Description
SCM Checkout	Fetch latest code from GitHub
Build	Install dependencies, package app
Dockerize	Build Docker image
Push to Registry	Push image to Docker Hub
Deploy	Apply Kubernetes deployment & service

The Jenkinsfile can be modified to support AWS ECR or private registries.

Docker
Example usage:

docker build -t bookmyshow-app .
docker run -p 3000:3000 bookmyshow-app

 Kubernetes Deployment

Apply Kubernetes configs:
kubectl apply -f deployment.yml
kubectl apply -f service.yml

Check status:
kubectl get pods
kubectl get svc

Access the application:
http://<Node-IP>:<NodePort>

 Improvements in Progress
Adding Terraform to automate cluster provisioning
Implementing monitoring (Prometheus + Grafana)
Adding rolling deployments & rollback strategy
CI/CD GitHub Actions version
Jenkins pipeline success
Pods & services running on K8s

App working in browser

 Shows practical CI/CD + Kubernetes skills
 Demonstrates scalable deployment automation
 Matches real industry DevOps workflows

 Author
Rudresh BS
DevOps & Cloud Engineering Enthusiast
