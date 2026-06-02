#  Resume Previewer using DevOps Tools & CI/CD Pipeline

A full-stack DevOps project demonstrating automated software deployment using **Docker**, **Jenkins**, **GitHub Actions**, **Render**, and **Vercel**.

The project showcases a complete CI/CD workflow where code changes pushed to GitHub automatically trigger build, containerization, and deployment processes.

---

##  Project Overview

The **Resume Previewer** is a web application developed to demonstrate modern DevOps practices and deployment automation.

The project consists of:

* Frontend Application
* Backend API Service
* Docker Containerization
* Jenkins CI/CD Pipeline
* GitHub Actions Workflow
* Docker Hub Integration
* Cloud Deployment using Render and Vercel

The primary objective is to automate software build and deployment processes while reducing manual effort.

---

##  Objectives

* Develop a Resume Previewer web application
* Learn and implement DevOps workflows
* Automate deployment using CI/CD pipelines
* Containerize applications using Docker
* Integrate GitHub with Jenkins
* Deploy applications on cloud platforms
* Reduce manual deployment effort
* Gain practical experience with modern DevOps tools

---

##  System Architecture

```text
Developer
    │
    ▼
 GitHub Repository
    │
    ▼
 Jenkins Pipeline
    │
 ┌──┴──┐
 ▼     ▼
Maven Docker Build
    │
    ▼
 Docker Hub
    │
 ┌──┴──────────┐
 ▼             ▼
Render       Vercel
Backend      Frontend
    │             │
    └─────┬───────┘
          ▼
        Users
```

---

##  Tech Stack

| Technology     | Purpose                 |
| -------------- | ----------------------- |
| HTML           | Frontend Development    |
| Spring Boot    | Backend Development     |
| Docker         | Containerization        |
| Jenkins        | CI/CD Automation        |
| Git            | Version Control         |
| GitHub         | Source Code Management  |
| GitHub Actions | Workflow Automation     |
| Docker Hub     | Image Repository        |
| Render         | Backend Deployment      |
| Vercel         | Frontend Deployment     |
| Maven          | Build Management        |
| Ubuntu / WSL   | Development Environment |

---

##  Project Structure

```text
resume-previewer-devops/
│
├── frontend/
│   ├── index.html
│   └── Dockerfile
│
├── backend/
│   └── previewer/
│       ├── src/
│       ├── pom.xml
│       └── Dockerfile
│
├── docker-compose.yml
│
├── Jenkinsfile
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
└── README.md
```

---

##  CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins detects repository changes
3. Maven builds the backend application
4. Docker images are created
5. Images are pushed to Docker Hub
6. Backend is deployed on Render
7. Frontend is deployed on Vercel
8. Users access the live application

---

##  Docker Containerization

### Build Containers

```bash
docker compose build
```

### Start Containers

```bash
docker compose up -d
```

### Stop Containers

```bash
docker compose down
```

---

##  Jenkins Pipeline

The Jenkins pipeline performs:

* Repository Checkout
* Maven Build
* Docker Image Build
* Container Deployment
* Pipeline Monitoring

Example:

```groovy
pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/your-username/repository.git'
            }
        }

        stage('Build Maven Project') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Build Docker Containers') {
            steps {
                sh 'docker compose build'
            }
        }

        stage('Deploy Containers') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}
```

---

##  Deployment

### Backend Deployment

* Platform: Render
* Containerized using Docker
* Automatically deployed from Docker Hub

### Frontend Deployment

* Platform: Vercel
* Automatically deployed from GitHub

---

##  Testing

### Functional Testing

✔ Frontend Loading

✔ Backend API Response

✔ Jenkins Pipeline Execution

✔ Docker Image Build

✔ Docker Hub Push

✔ Render Deployment

✔ Vercel Deployment

### Integration Testing

✔ GitHub ↔ Jenkins

✔ Jenkins ↔ Docker

✔ Docker Hub ↔ Deployment Platforms

---


```

Example:

```markdown
![Jenkins Dashboard](screenshots/jenkins-dashboard.png)
```

---

##  Key Features

* Automated CI/CD Pipeline
* Docker Containerization
* GitHub Integration
* Jenkins Automation
* Docker Hub Image Management
* Cloud Deployment
* Reduced Manual Configuration
* Faster Deployment Process
* Real-World DevOps Workflow

---

##  Future Enhancements

* Resume Upload Functionality
* PDF Preview Support
* User Authentication
* Database Integration
* Kubernetes Deployment
* Monitoring Dashboards
* Automated Testing
* HTTPS Security Enhancements

---

##  Learning Outcomes

Through this project, I gained practical experience in:

* DevOps Fundamentals
* CI/CD Pipeline Design
* Docker & Docker Compose
* Jenkins Automation
* GitHub Actions
* Cloud Deployment
* Linux Administration
* Software Deployment Automation

---

##  Author

**Buchupalle Purna Tejeshwara Reddy**

B.Tech Computer Science and Engineering

Lovely Professional University

GitHub: https://github.com/Purnatejeshwarareddyb

LinkedIn: https://linkedin.com/in/purna-t-reddy56

---

##  License

This project was developed for academic and learning purposes as part of DevOps and Cloud Deployment studies.

 If you found this project useful, consider giving it a star on GitHub.
