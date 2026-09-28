# Video Conferencing Application

A full-stack **video conferencing application** built using the MERN stack and deployed as a containerized application using **Docker and Kubernetes**. The project also includes **Prometheus and Grafana monitoring**, installed and managed using **Helm**.

## 🚀 Features

* User authentication
* Create and join video meetings
* Real-time video and audio communication
* Meeting history
* Real-time signaling using Socket.IO
* Responsive React frontend
* Node.js and Express backend
* MongoDB database
* Docker containerization
* Kubernetes deployment
* Kubernetes Ingress
* Persistent MongoDB storage
* Prometheus monitoring
* Grafana dashboards
* Helm-based monitoring installation

## 🛠️ Technology Stack

### Frontend

* React.js
* Material UI
* Axios
* Socket.IO Client
* WebRTC
* Nginx

### Backend

* Node.js
* Express.js
* Socket.IO
* Mongoose

### Database

* MongoDB

### DevOps & Monitoring

* Docker
* Docker Hub
* Kubernetes
* Kubernetes Pods
* Kubernetes Deployments
* Kubernetes Services
* Kubernetes Ingress
* Persistent Volumes (PV)
* Persistent Volume Claims (PVC)
* Helm
* Prometheus
* Grafana

---

## 🐳 Docker Containerization

The frontend and backend are packaged into separate Docker images.

```text
Frontend Code
     ↓
Frontend Dockerfile
     ↓
Docker Image
     ↓
Frontend Container

Backend Code
     ↓
Backend Dockerfile
     ↓
Docker Image
     ↓
Backend Container
```

MongoDB uses a MongoDB Docker image with persistent storage.

---

## ☸️ Kubernetes Deployment

Docker images are deployed on Kubernetes using Deployments.

```text
Docker Image
     ↓
Kubernetes Deployment
     ↓
Pod
     ↓
Container
     ↓
Service
```

### Kubernetes Components

* **Frontend Deployment** – manages React/Nginx Pods
* **Backend Deployment** – manages Node.js/Express Pods
* **MongoDB Deployment** – manages MongoDB Pod
* **Services** – provide communication between Pods
* **Ingress** – routes external traffic
* **PV/PVC** – provides persistent MongoDB storage
* **Namespace** – isolates application resources

### Kubernetes Architecture



---

## 📊 Monitoring with Prometheus & Grafana

The Kubernetes cluster is monitored using **Prometheus and Grafana**.

Prometheus collects Kubernetes metrics, while Grafana provides dashboards for visualizing cluster and application resource usage.

### Helm

The Prometheus and Grafana monitoring stack was installed using the **kube-prometheus-stack Helm chart**.

Example:

```bash
helm install prometheus-stack \
  prometheus-community/kube-prometheus-stack \
  --namespace monitoring
```

The monitoring stack includes:

* Prometheus
* Grafana
* Alertmanager
* Kubernetes metrics exporters
* Prometheus Operator

### Grafana Dashboard

Grafana is used to monitor Kubernetes resources such as:

* CPU utilization
* Memory utilization
* CPU requests
* CPU limits
* Pod count
* Namespace resource usage
* Kubernetes workloads



The dashboard provides visibility into namespaces such as:

```text
ingress-nginx
kube-system
monitoring
zoom-app
```

---

## 🔄 Complete Deployment & Monitoring Flow

```text
                 Source Code
                      │
                      ▼
                Dockerfile
                      │
                      ▼
                Docker Image
                      │
                      ▼
                 Docker Hub
                      │
                      ▼
             Kubernetes Deployment
                      │
                      ▼
                     Pod
                      │
                ┌─────┴─────┐
                ▼           ▼
           Container    Container
                │
                ▼
              Service
                │
                ▼
             Ingress
                │
                ▼
               User


       Kubernetes Monitoring
                │
                ▼
              Helm
                │
        ┌───────┴────────┐
        ▼                ▼
   Prometheus          Grafana
   Metrics             Dashboard
        │                │
        └───────┬────────┘
                ▼
       Cluster Monitoring
```

## 🎯 Project Objective

The objective of this project is to develop and deploy a video conferencing application while gaining practical experience in **full-stack development, containerization, Kubernetes orchestration, and cloud-native monitoring**.

The project demonstrates the complete workflow from application source code to Docker images, Kubernetes deployment, external access through Ingress, persistent database storage, and monitoring through Prometheus and Grafana.

## 📌 DevOps Workflow

```text
Code
 ↓
Docker
 ↓
Docker Image
 ↓
Docker Hub
 ↓
Kubernetes
 ↓
Deployment
 ↓
Pods
 ↓
Services
 ↓
Ingress
 ↓
Prometheus
 ↓
Grafana
```

****************************************************
