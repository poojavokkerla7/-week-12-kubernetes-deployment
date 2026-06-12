# Week 12 - Kubernetes Deployment Guide

## Environment Setup
- Docker Desktop installed
- Kubernetes enabled in Docker Desktop
- kubectl CLI configured and working

---

## Step 1: Build Docker Image
Build application image:

```bash
docker build -t user-service:v1 .
