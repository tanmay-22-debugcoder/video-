# Video Conferencing Application

A full-stack **video conferencing web application** built using the **MERN stack**, with Docker containerization and Kubernetes deployment.

## 🚀 Features

* User authentication
* Create and join video meetings
* Real-time video and audio communication
* Meeting history
* Real-time signaling using Socket.IO
* Responsive React frontend
* Node.js and Express backend
* MongoDB database

## 🛠️ Technology Stack

### Frontend

* React.js
* Material UI
* Axios
* Socket.IO Client
* WebRTC

### Backend

* Node.js
* Express.js
* Socket.IO
* Mongoose

### Database

* MongoDB

### DevOps & Deployment

* Docker
* Docker Hub
* Kubernetes
* Kubernetes Deployments
* Kubernetes Pods
* Kubernetes Services
* Kubernetes Ingress
* Persistent Volumes (PV)
* Persistent Volume Claims (PVC)

## 🐳 Docker

The application is containerized using Docker.

Separate Docker images are created for the frontend and backend:

```text
Frontend → Dockerfile → Docker Image → Container
Backend  → Dockerfile → Docker Image → Container
MongoDB  → MongoDB Image → Container
```

## ☸️ Kubernetes Deployment

The Docker images are deployed and managed using Kubernetes.

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
     ↓
Ingress
```

### Kubernetes Architecture

![Kubernetes Architecture](docs/architecture.png)

The deployment contains:

* **Frontend** – React application served using Nginx
* **Backend** – Node.js/Express application
* **MongoDB** – database with persistent storage
* **Docker** – containerizes each application component
* **Pods** – run the application containers
* **Deployments** – manage and maintain Pods
* **Services** – enable communication between components
* **Ingress** – manages external traffic to the application
* **PV/PVC** – provides persistent MongoDB storage

### Architecture Flow

```text
User
 ↓
Ingress
 ├──→ Frontend Service → Frontend Deployment → Frontend Pod → Docker Container
 │
 └──→ Backend Service → Backend Deployment → Backend Pod → Docker Container
                                                    ↓
                                             MongoDB Service
                                                    ↓
                                             MongoDB Pod
                                                    ↓
                                                 PV/PVC
```

## 🔄 Deployment Flow

```text
Source Code
    ↓
Dockerfile
    ↓
Docker Image
    ↓
Docker Hub
    ↓
Kubernetes Deployment
    ↓
Pod
    ↓
Container
    ↓
Service
    ↓
Ingress
    ↓
User
```

## 🎯 Project Objective

The objective of this project is to develop a scalable video conferencing application while gaining practical experience in **Docker containerization and Kubernetes orchestration**.

The project demonstrates how a full-stack MERN application can be containerized using Docker and deployed using Kubernetes resources such as **Deployments, Pods, Services, Ingress, PV and PVC**.

## 👨‍💻 Author

**Tanmay Shivaji Lashkar**
