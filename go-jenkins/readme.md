#  Jenkins CI/CD Pipeline

<p align="center">
  <img src="https://img.shields.io/badge/Jenkins-Declarative%20Pipeline-D24939?style=for-the-badge&logo=jenkins&logoColor=white" alt="Jenkins" />
  <img src="https://img.shields.io/badge/Language-Golang-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Golang" />
  <img src="https://img.shields.io/badge/Code%20Quality-SonarCloud-4E9BCD?style=for-the-badge&logo=sonarcloud&logoColor=white" alt="SonarCloud" />
  <img src="https://img.shields.io/badge/Registry-Docker%20Hub-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Hub" />
</p>

<p align="center">
  A fully automated, declarative Jenkins pipeline that builds, scans, and ships a Golang application — from checkout to container registry — with zero manual steps.
</p>

---

##  Overview

This repository contains a **declarative Jenkins pipeline** designed to automate the integration and deployment workflow for a Golang application. It handles everything from source checkout to pushing a production-ready Docker image, with built-in code quality gates along the way.

---

## Pipeline Workflow

The pipeline runs through five well-defined stages:

| # | Stage | Description |
|---|-------|-------------|
| 1 | **Checkout** | Clones the target GitHub repository using specified credentials. |
| 2️ | **SonarQube Analysis** | Executes a code quality and security scan via SonarCloud. |
| 3️ | **Docker Build** | Packages the application into a Docker image tagged with the unique Jenkins build ID. |
| 4️ | **Push to Docker Hub** | Logs into Docker Hub and pushes the newly built application image. |
| 5️ | **Post-Actions** | Cleans up the workspace to maintain runner disk space. |

###  Flow Diagram

```
┌───────────┐     ┌───────────────────┐     ┌──────────────┐     ┌────────────────────┐     ┌───────────────┐
│  Checkout │ --> │ SonarQube Analysis│ --> │ Docker Build │ --> │ Push to Docker Hub │ --> │ Post-Actions  │
└───────────┘     └───────────────────┘     └──────────────┘     └────────────────────┘     └───────────────┘
```


---

<p align="center">Made with ⚙️ and ☕ for smoother deployments</p>
