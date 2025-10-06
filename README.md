# DevOps-CI-CD
Implementing Continuous Integration, Deployment, and Monitoring for a Containerized Todo Application

## Overview

This project demonstrates a **containerized Flask TodoApp** deployed on a **Kubernetes cluster** with DevOps practices:  

- Docker containerization  
- Kubernetes orchestration  
- Persistent Volumes (PV/PVC) for data persistence  
- CI/CD pipeline using **GitHub Actions** (CI) → **ArgoCD** (CD)  
- Application and cluster monitoring with **Prometheus** and **Grafana**  



## Features

- Dockerized TodoApp with separate database container  
- Kubernetes Deployment and Service configuration  
- Persistent storage using PV and PVC  
- Automated CI/CD pipeline  
- Metrics collection and visualization  
- Alerts for proactive monitoring  


## Project Structure

todoapp-devops/
├── Dockerfile
├── docker-compose.yml
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── pv-pvc.yaml
│   └── helm-chart/
├── ci-cd/
│   ├── github-actions.yaml
│   └── argocd-config.yaml
├── monitoring/
│   ├── prometheus.yaml
│   └── grafana-dashboards/
├── images/           
└── README.md

Prerequisites
1.Ubuntu/Debian machine
2.Docker & Docker Compose
3.Kubernetes cluster (Minikube/kubeadm)
4.Helm
5.GitHub account
6.ArgoCD installed on Kubernetes
7.Prometheus & Grafana

Setup & Installation
1. Clone the repository
git clone https://github.com/c280819>/todo-app.git
cd todo-app

2. Docker (Optional local testing)
docker build -t todoapp .
docker-compose up -d

3. Kubernetes Deployment
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
kubectl apply -f k8s/pv-pvc.yaml
Access TodoApp service via ClusterIP / NodePort / Ingress as configured

4. CI/CD
GitHub Actions handles continuous integration (build & test)
ArgoCD automates deployment to Kubernetes cluster

5. Monitoring
Prometheus collects metrics from cluster and TodoApp
Grafana dashboards visualize metrics

Alerts configured for proactive monitoring
