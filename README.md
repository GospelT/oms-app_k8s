Here’s a simple README.txt you can add to your OMS Kubernetes project 👇

README.txt
OMS App - Kubernetes Deployment

This project contains Kubernetes YAML files for deploying a simple OMS (Order Management System) application.

It includes:

- Frontend (React app)
- Backend (API server)
- MongoDB (database using StatefulSet)

---

## Components

Frontend:
- Deployment: frontend-deployment
- Service: frontend service
- Runs on port 3000

Backend:
- Deployment: backend-deployment
- Service: backend service
- Runs on port 5000

Database:
- MongoDB StatefulSet
- Service: mongo
- Runs on port 27017

---

## How to deploy

1. Create namespace:
   kubectl create namespace oms

2. Apply all YAML files:
   kubectl apply -f .

3. Check resources:
   kubectl get all -n oms

---

## Communication

Frontend → Backend:
http://backend:5000

Backend → MongoDB:
mongodb://mongo:27017

---

## Notes

- Ensure Docker images are pushed to Docker Hub
- Ensure MongoDB is deployed before backend
- Use correct service names for communication
