# 🧩 Course Service Microservice - Cloud Computing Assignment (SE4010)

This repository contains the **Course Service** microservice developed as a part of the **Cloud Computing Assignment** for the module _Current Trends in Software Engineering (SE4010)_ at **SLIIT** (2025 | Year 01 | Semester 2).

> 🎯 **Objective:** Design and implement a secure, cloud-based, microservice architecture component using fundamental DevOps and DevSecOps practices on a public cloud platform.

---

## 🧱 Microservice Overview

The **Course Service** is a key component of a potential Learning Management System (LMS). It provides RESTful API endpoints to manage course-related data and operations.

### 📌 Features & Endpoints

| Endpoint                                 | Method | Description                              |
|------------------------------------------|--------|------------------------------------------|
| `/api/courses/`                          | POST   | Create a new course                      |
| `/api/courses/`                          | GET    | Get all courses                          |
| `/api/courses/:courseId`                | GET    | Get course by Course ID                  |
| `/api/courses/instructor/:instructorId` | GET    | Get courses by Instructor ID             |
| `/api/courses/:courseId`                | PATCH  | Update course by Course ID               |
| `/api/courses/:courseId`                | DELETE | Delete course by Course ID               |

- **Tech Stack:** Node.js, Express.js, MongoDB
- **Containerized:** Docker
- **Cloud Provider:** AWS ECS

---

## 🔧 DevOps Implementation

### ✅ Version Control
- Code is hosted publicly on **GitHub**.

### ✅ CI/CD Pipelines
- Implemented via **GitHub Actions**.
- Automates:
  - Docker image build
  - Push to Docker Hub
  - Deploy to AWS ECS

### ✅ Containerization
- Microservice is fully containerized using **Docker**.
- Public Image: [`kalingajayathilaka/course-service:latest`](https://hub.docker.com/repository/docker/kalingajayathilaka/course-service)

---

## 🚀 Deployment on AWS ECS

- **Platform:** Amazon ECS (Fargate)
- **Container Registry:** Docker Hub
- **Deployment:** Automated via GitHub Actions CI/CD pipeline
- **Public Access:** Microservice is accessible via IP

**🟢 Live URL:** `http://54.204.109.143:5000/`  
_(Note: IP may change on redeployment)_

---

## 🔒 Security & DevSecOps

### 🔐 Environment Variables
- All sensitive information (e.g., MongoDB URI) is stored in `.env`.
- Excluded from the repo and container via `.dockerignore`.

### 🔐 AWS IAM & Least Privilege
- IAM roles created with limited permissions for ECS, ECR, and Secrets Manager.
- Access keys used only via **GitHub Secrets**.

### 🔐 GitHub Secrets
- Managed secrets:
  - Docker Hub credentials
  - AWS Access & Secret keys
  - SonarCloud Token

### 🔐 CI/CD Pipeline Security
- Pipelines run in **isolated GitHub Action containers**.
- No secrets exposed in any logs or workflow files.

### 🔐 Static Application Security Testing (SAST)
- Integrated **SonarCloud**:
  - Scans code for vulnerabilities
  - Identifies code smells and bad practices
  - Promotes maintainable and secure codebase

### 🔐 Docker Image Security
- Public Docker image contains no secrets.
- `.env` excluded using `.dockerignore`.

### 🔐 ECS Network Security
- Configured **Security Groups** to allow only required ports (e.g., 5000).
- Deployments only occur via CI/CD—manual access is restricted.

---

## 📊 Code Quality & SAST Dashboard

View your live SonarCloud dashboard here:  
🔗 [SonarCloud Project](https://sonarcloud.io/project/information?id=IT21252990_CTSE_Assignment_01)

---

## 👥 Authors


| 👤 Name | 🆔 Student ID | 🌐 GitHub |
|--------|---------|-----------|
| Kalinga Jayathilaka | IT21252990 | [![Kalinga's GitHub](https://img.shields.io/badge/@kalingajayathilaka-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/IT21252990) |
| Vihangi Rathnayake | IT21271182 | [![Vihangi's GitHub](https://img.shields.io/badge/@vihangirathnayake-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/IT21271182) |
| Ashen Savinda | IT21373916 | [![Ashen's GitHub](https://img.shields.io/badge/@ashensavinda-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Ashen-Savinda) |
| Sithara Pramodini | IT21306754 | [![Sithara's GitHub](https://img.shields.io/badge/@sitharapramodini-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/SitharaPramodini) |

---