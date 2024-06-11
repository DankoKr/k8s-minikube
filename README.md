# k8s-minikube

This project contains YAML files for deploying a simple application stack using Minikube. The stack includes MongoDB, Express, ConfigMap, and Secret configurations.

## Overview

This project sets up a single Node managed by Minikube, containing a MongoDB database and an Express.js application as Pods, with configuration and secrets managed via ConfigMap and Secret.

## Getting Started

  1. Start minikube

   ```bash
   minikube start
   ```


  2. Apply Configurations


```bash
kubectl apply -f configMap.yaml
kubectl apply -f secret.yaml
kubectl apply -f mongodb.yaml
kubectl apply -f express.yaml
```

## Verify Deployment


```bash
kubectl get pods
kubectl get services
```

## Access Application:
Use Minikube to get the URL for the Express application


```bash
minikube service mongo-express-service --url
```
