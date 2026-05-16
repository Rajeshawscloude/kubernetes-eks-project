# Kubernetes on AWS EKS ☸️

## Overview
Containerized web application deployed on AWS 
Elastic Kubernetes Service (EKS) demonstrating 
container orchestration and cloud-native deployment.

## Architecture

## What I Built:
- EKS Cluster with managed node groups
- Kubernetes Deployment (2 replicas)
- LoadBalancer Service for external access
- Auto-healing pods
- Horizontal scaling capability

## Commands Used:
```bash
# Create EKS Cluster
eksctl create cluster \
  --name rajesh-eks-cluster \
  --region us-east-1 \
  --nodegroup-name rajesh-nodes \
  --node-type t3.small \
  --nodes 2

# Deploy Application
kubectl apply -f app-deployment.yaml

# Check Status
kubectl get pods
kubectl get nodes
kubectl get services

# Delete Cluster
eksctl delete cluster \
  --name rajesh-eks-cluster \
  --region us-east-1
```

## Key Kubernetes Concepts Used:
- **Deployment** — Manages pod replicas
- **Service** — Exposes app via LoadBalancer
- **Pods** — Running containers
- **Nodes** — EC2 worker machines
- **Cluster** — Complete K8s environment

## Results:
- 2 pods running successfully
- LoadBalancer URL accessible
- Auto-healing verified
- Cluster deleted after testing

## Services Used:
AWS EKS, EC2, ALB, IAM, 
kubectl, eksctl, Docker, nginx

## Screenshots
https://github.com/Rajeshawscloude/kubernetes-eks-project/tree/main/screenshots
