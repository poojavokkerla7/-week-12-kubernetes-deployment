# Week 12 - Kubernetes Deployment Project

## Overview
This project demonstrates container orchestration using Kubernetes by deploying a Dockerized microservice application with scalable deployment, service exposure, and rolling updates.

## Objectives
- Understand Kubernetes architecture
- Deploy Dockerized applications into Kubernetes cluster
- Configure Pods, Deployments, and Services
- Implement scaling and rolling updates

## Tech Stack
- Kubernetes
- Docker
- kubectl
- YAML

## Kubernetes Components Used

### Deployment
Manages application lifecycle and replicas.

### Service
Exposes application to network using NodePort.

### Pod
Smallest deployable unit in Kubernetes.

## Files
- deployment.yaml → Kubernetes deployment configuration
- service.yaml → Service configuration
- documentation/ → Deployment steps and guide

---

## Deployment Steps

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

## Verify Deployment
```bash
kubectl get pods
kubectl get services

## Scaling
```bash
kubectl scale deployment user-service --replicas=4

## Rolling Update
```bash id="r1"
kubectl set image deployment/user-service user-service=user-service:v2
kubectl rollout status deployment/user-service
