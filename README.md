# 🚀 Financial RAG Platform

> **Production-ready AI Retrieval-Augmented Generation (RAG) platform built with FastAPI, React, ChromaDB, Google Gemini, Docker, AWS EC2, Prometheus, Grafana and GitHub Actions CI/CD.**

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI/CD-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector_DB-5B21B6?style=for-the-badge)
![Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)

</div>

---

# 📌 Project Overview

Financial RAG Platform is an end-to-end **Generative AI** application that demonstrates how modern **LLM-powered systems** can be engineered, containerized, monitored and deployed using production-inspired software engineering practices.

Instead of relying only on a Large Language Model, the platform implements **Retrieval-Augmented Generation (RAG)** to provide grounded responses from uploaded financial documents. Users can upload PDF reports, annual statements or investment documents, build a semantic vector database and interact with them through natural language.

Beyond the AI workflow, this project focuses heavily on **Cloud Engineering, DevOps, Backend Engineering and Observability** by implementing automated CI/CD pipelines, Dockerized services, AWS deployment, monitoring dashboards and production health checks.

---

# 🎯 Project Objectives

The primary objective of this project was to understand how production AI systems are built rather than simply calling an LLM API.

The project explores multiple engineering domains simultaneously:

- Artificial Intelligence Engineering
- Retrieval-Augmented Generation (RAG)
- Backend API Development
- Cloud Computing
- DevOps Engineering
- Infrastructure Automation
- Monitoring & Observability
- Containerized Deployments
- Continuous Integration & Continuous Deployment (CI/CD)
- Production Debugging

Rather than treating AI as a standalone component, the application demonstrates how intelligent systems are integrated into reliable production environments.

---

# ⭐ Key Highlights

## 🤖 AI Engineering

- Retrieval-Augmented Generation (RAG)
- Financial Document Question Answering
- Sentence Transformer Embeddings
- ChromaDB Vector Database
- Semantic Similarity Search
- Context-aware Prompt Construction
- Source Grounded Gemini Responses
- Multi-document Knowledge Base
- Intelligent Document Chunking
- Retrieval-only fallback mode

---

## ☁ Cloud & DevOps Engineering

- Dockerized Microservice Architecture
- Docker Compose Orchestration
- AWS EC2 Deployment
- Nginx Reverse Proxy
- GitHub Actions CI/CD
- Automated Docker Hub Publishing
- Health Checks
- Persistent Volumes
- Prometheus Monitoring
- Grafana Dashboards
- Automated Deployment Verification
- Container Lifecycle Management

---

# 🧠 Why Retrieval-Augmented Generation?

Large Language Models are extremely capable but cannot reliably answer questions about private documents they have never seen.

Retrieval-Augmented Generation solves this problem by retrieving relevant document chunks before generating a response.

Instead of asking Gemini to hallucinate an answer, the application performs semantic retrieval against a vector database and supplies the retrieved context to the model.

Benefits include:

- Higher factual accuracy
- Reduced hallucinations
- Source-grounded responses
- Support for private datasets
- Domain-specific knowledge
- Explainable AI outputs

---

# 🏗 High Level System Architecture

```text
                           GitHub Repository
                                  │
                                  ▼
                        GitHub Actions Workflow
                                  │
               ┌──────────────────┴──────────────────┐
               ▼                                     ▼
      Backend Docker Image                 Frontend Docker Image
               │                                     │
               └──────────────────┬──────────────────┘
                                  ▼
                             Docker Hub
                                  │
                                  ▼
                           AWS EC2 Instance
                                  │
                           Docker Compose
                                  │
        ┌─────────────┬───────────────┬───────────────┐
        ▼             ▼               ▼               ▼
     Nginx        React UI       FastAPI API     Prometheus
                                        │               │
                                        ▼               ▼
                                  RAG Pipeline      Grafana
                                        │
                     ┌──────────────────┴─────────────────┐
                     ▼                                    ▼
                ChromaDB                         Google Gemini
                     │
                     ▼
         Sentence Transformer Embeddings
```

---

# 🧠 Retrieval-Augmented Generation Pipeline

```text
                    Upload Financial PDF
                             │
                             ▼
                    Extract PDF Content
                             │
                             ▼
                   Intelligent Text Chunking
                             │
                             ▼
          Generate Sentence Transformer Embeddings
                             │
                             ▼
                    Store in ChromaDB
                             │
                             ▼
                  User asks a Question
                             │
                             ▼
                  Semantic Similarity Search
                             │
                             ▼
              Retrieve Most Relevant Chunks
                             │
                             ▼
      Build Prompt using Retrieved Context
                             │
                             ▼
                  Google Gemini LLM
                             │
                             ▼
         Source Grounded Financial Response
```

---

# ☁ Production Deployment Architecture

```text
                     Developer
                          │
                          ▼
                  Push to GitHub
                          │
                          ▼
                 GitHub Actions CI/CD
                          │
                          ▼
               Build Docker Images
                          │
                          ▼
                 Push to Docker Hub
                          │
                          ▼
              Connect to AWS EC2 via SSH
                          │
                          ▼
                Pull Latest Docker Images
                          │
                          ▼
                Docker Compose Deployment
                          │
                          ▼
                 Health Check Verification
                          │
                          ▼
               Production Application Live
```

---

# 📊 Monitoring Architecture

```text
                  FastAPI Application
                           │
                           ▼
              Prometheus Instrumentation
                           │
                           ▼
                    /metrics Endpoint
                           │
                           ▼
                  Prometheus Scraping
                           │
                           ▼
                  Time Series Database
                           │
                           ▼
                  Grafana Dashboards
                           │
                           ▼
              Performance Visualization
```

---

# ⚙ Technology Stack

| Category | Technologies |
|-----------|--------------|
| Programming Language | Python, JavaScript |
| Backend Framework | FastAPI |
| Frontend | React + Vite |
| AI Model | Google Gemini |
| Embedding Model | Sentence Transformers |
| Vector Database | ChromaDB |
| PDF Processing | PyPDF |
| API Server | Uvicorn |
| Monitoring | Prometheus |
| Visualization | Grafana |
| Containerization | Docker |
| Orchestration | Docker Compose |
| Reverse Proxy | Nginx |
| CI/CD | GitHub Actions |
| Container Registry | Docker Hub |
| Cloud Platform | AWS EC2 |
| Version Control | Git & GitHub |

---

# 📁 Repository Structure

```text
financial-rag-platform/

│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── rag_pipeline.py
│   │   ├── vector_store.py
│   │   ├── pdf_loader.py
│   │   ├── text_splitter.py
│   │   ├── config.py
│   │   └── schemas.py
│   │
│   ├── Dockerfile
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── Dockerfile
│
├── monitoring/
│   ├── prometheus.yml
│   └── grafana/
│
├── nginx/
│   ├── nginx.conf
│   └── default.conf
│
├── screenshots/
│
├── .github/
│   └── workflows/
│       └── deployment.yml
│
├── docker-compose.yml
├── docker-compose.prod.yml
└── README.md
```

---

# 📸 Project Walkthrough

The following screenshots showcase the complete lifecycle of the application—from uploading financial documents and generating AI-powered responses to production deployment, monitoring, and cloud infrastructure.

---

## 1️⃣ Live Application Running on AWS EC2

Demonstrates the production application successfully deployed on an AWS EC2 instance.

![Live Application](screenshots/application-home-aws.png)

---

## 2️⃣ Upload Financial Document

Upload a financial PDF to build the knowledge base for Retrieval-Augmented Generation (RAG).

![Upload Success](screenshots/pdf-upload-success.png)

---

## 3️⃣ AI Generated Response with Retrieved Source Chunks

Question answering powered by semantic search with source-grounded responses generated using Google Gemini.

![AI Response](screenshots/rag-answer-with-sources.png)

---

## 4️⃣ Reset Vector Database

Clear all uploaded documents and vector embeddings to start with a fresh knowledge base.

![Vector Database Reset](screenshots/vector-db-reset.png)

---

## 5️⃣ Production Docker Containers

Docker Compose running the complete production stack, including the frontend, backend, Nginx, Prometheus, and Grafana services.

![Docker Containers](screenshots/docker-containers-production.png)

---

## 6️⃣ Production Health Endpoint

Production health endpoint used by Docker health checks and the CI/CD deployment pipeline.

![Production Health Endpoint](screenshots/production-health-endpoint.png)

---

## 7️⃣ GitHub Actions CI/CD Pipeline

Successful automated pipeline for validation, testing, Docker image publishing, and deployment to AWS.

![GitHub Actions Pipeline](screenshots/github-actions-pipeline-success.png)

---

## 8️⃣ Docker Hub Published Images

Automatically published production Docker images for deployment and version management.

![Docker Hub Images](screenshots/dockerhub-frontend-image.png)

---

## 9️⃣ Prometheus Monitoring

Prometheus continuously collecting metrics from the FastAPI backend for monitoring and observability.

![Prometheus Targets](screenshots/prometheus-targets.png)

---

## 🔟 Grafana Dashboard

Grafana dashboard visualizing application performance, request metrics, and service health.

![Grafana Dashboard](screenshots/grafana-dashboard.png)

---

## 1️⃣1️⃣ AWS EC2 Production Infrastructure

AWS EC2 instance hosting the production deployment of the application.

![AWS EC2 Instance](screenshots/aws-ec2-instance.png)

---

## 1️⃣2️⃣ AWS Security Group Configuration

Inbound security rules configured to securely expose HTTP, HTTPS, and SSH access for the production environment.

![AWS Security Group](screenshots/aws-security-group.png)

---

# 💡 Skills Demonstrated

This project demonstrates practical experience in:

- Artificial Intelligence Engineering
- LLM Application Development
- Retrieval-Augmented Generation
- Semantic Search
- Vector Databases
- Backend API Development
- REST API Design
- Cloud Deployment
- DevOps Engineering
- Docker
- Docker Compose
- GitHub Actions
- CI/CD
- AWS EC2
- Monitoring
- Observability
- Infrastructure Automation
- Production Debugging

---
# 🚀 Running the Project Locally

## Prerequisites

Before running the application, ensure the following software is installed:

| Software | Version |
|-----------|----------|
| Python | 3.10+ |
| Docker | Latest |
| Docker Compose | Latest |
| Git | Latest |

You will also require a valid Google Gemini API Key.

---

## Clone Repository

```bash
git clone https://github.com/aadi090204/financial-rag-platform.git

cd financial-rag-platform
```

---

## Configure Environment Variables

Create an environment file.

```bash
cp .env.example .env
```

Add your Gemini API Key.

```env
GEMINI_API_KEY=YOUR_API_KEY
```

---

## Build Docker Images

```bash
docker compose build
```

---

## Start the Complete Application

```bash
docker compose up -d
```

---

## Verify Running Containers

```bash
docker ps
```

Expected services:

- Frontend
- Backend
- Nginx
- Prometheus
- Grafana

---

# 🌐 Application Services

| Service | URL |
|----------|-----|
| Frontend | http://localhost |
| Backend API | http://localhost:8000 |
| Swagger UI | http://localhost:8000/docs |
| Health Endpoint | http://localhost/health |
| Metrics | http://localhost:8000/metrics |
| Prometheus | http://localhost:9090 |
| Grafana | http://localhost:3001 |

---

# 🔌 REST API

## Upload Document

```http
POST /upload
```

Uploads financial PDF documents.

---

## Ask Question

```http
POST /ask
```

Queries uploaded financial documents using semantic search and Gemini.

---

## Reset Vector Database

```http
DELETE /documents/reset
```

Deletes all stored embeddings and uploaded documents.

---

## Health Check

```http
GET /health
```

Used by Docker health checks and deployment verification.

---

## Metrics Endpoint

```http
GET /metrics
```

Exports Prometheus metrics.

---

# 🔄 GitHub Actions CI/CD Pipeline

The deployment pipeline follows a production-inspired workflow.

```
Developer Push
      │
      ▼
GitHub Repository
      │
      ▼
GitHub Actions
      │
      ▼
Validate Docker Compose
      │
      ▼
Integration Tests
      │
      ▼
Build Backend Image
      │
      ▼
Build Frontend Image
      │
      ▼
Publish Docker Images
      │
      ▼
Sync Production Configuration
      │
      ▼
Deploy to AWS EC2
      │
      ▼
Health Verification
      │
      ▼
Docker Image Cleanup
```

The workflow performs:

- Docker Compose validation
- Integration testing
- Docker image creation
- Docker Hub publishing
- Automated AWS deployment
- Health verification
- Automatic cleanup of dangling images

---

# ☁ AWS Deployment

The production environment runs on an AWS EC2 instance.

Deployment stack:

- Amazon EC2
- Docker Compose
- Nginx Reverse Proxy
- Docker Hub
- GitHub Actions
- Prometheus
- Grafana

The deployment process is fully automated.

Each push to the `main` branch triggers a deployment pipeline that:

1. Builds Docker images.
2. Publishes them to Docker Hub.
3. Connects securely to EC2.
4. Pulls updated images.
5. Restarts containers.
6. Verifies service health.
7. Cleans unused Docker images.

---

# 🐳 Docker Architecture

Each application component runs as an isolated container.

```
Docker Compose

├── Nginx
│
├── React Frontend
│
├── FastAPI Backend
│      │
│      ▼
│   ChromaDB
│
├── Prometheus
│
└── Grafana
```

Benefits:

- Service isolation
- Easy scaling
- Reproducible environments
- Simplified deployment
- Independent updates

---

# 📈 Monitoring & Observability

Monitoring was integrated from the beginning to simulate a production environment.

Prometheus periodically scrapes metrics exposed by the FastAPI application.

Grafana visualizes these metrics using dashboards.

Collected metrics include:

- Request count
- Request duration
- API latency
- Endpoint availability
- Container health
- Service uptime

This enables proactive monitoring and easier debugging.

---

# ❤️ Health Checks

The application implements health checks at multiple levels.

### Backend

Docker Healthcheck

```
GET /health
```

### Deployment

GitHub Actions verifies application readiness after deployment.

### Infrastructure

Prometheus continuously monitors application availability.

---

# 📂 Persistent Storage

Application data persists between deployments.

Persistent directories include:

```
uploads/
```

Stores uploaded PDF files.

```
chroma_db/
```

Stores vector embeddings.

This prevents data loss during container recreation.

---

# 🔐 Security Considerations

The project follows several production-oriented security practices.

- Environment variables stored outside source code
- Sensitive API keys excluded from Git
- Reverse proxy through Nginx
- Automated health verification
- Isolated Docker network
- Persistent storage mounted through Docker volumes

Future improvements include:

- JWT Authentication
- HTTPS using Let's Encrypt
- Secrets Manager
- IAM Roles

---

# ⚡ Performance Optimizations

Several optimizations were implemented throughout development.

### Backend

- Lazy initialization
- Optimized startup sequence
- Health endpoint
- Docker health checks

### Docker

- Multi-container architecture
- Automatic restart policies
- Docker image cleanup
- Persistent volumes

### Deployment

- Automated health verification
- Reduced deployment downtime
- Image reuse
- Pull policy optimization

---

# 🛠 Engineering Challenges Solved

Throughout development several real-world engineering problems were encountered and resolved.

### Docker

- Large image size
- Disk exhaustion on EC2
- Dangling image cleanup
- Container lifecycle management

### CI/CD

- Deployment synchronization
- Health verification timing
- SSH connectivity
- Automated deployment debugging

### AI

- PDF parsing reliability
- Embedding generation
- Semantic retrieval
- Prompt construction
- Gemini integration

### Monitoring

- Prometheus scraping
- Grafana dashboards
- Metrics instrumentation

### Infrastructure

- Docker networking
- Reverse proxy configuration
- Persistent volumes
- Production deployment

---

# 📚 Key Learnings

This project provided hands-on experience with modern AI and cloud-native engineering practices.

### Artificial Intelligence

- Retrieval-Augmented Generation
- Vector Databases
- Semantic Search
- Embedding Models
- Prompt Engineering
- Large Language Models

### Backend Development

- FastAPI
- REST APIs
- File Upload Handling
- Background Processing

### Cloud

- AWS EC2
- Linux Server Administration
- Nginx
- Docker Deployment

### DevOps

- Docker
- Docker Compose
- GitHub Actions
- Docker Hub
- CI/CD Pipelines
- Monitoring
- Observability

---

# 🚀 Future Improvements

Planned enhancements include:

- Kubernetes Deployment
- AWS ECS
- AWS EKS
- Terraform Infrastructure as Code
- Redis Caching
- JWT Authentication
- User Accounts
- Multi-user Document Collections
- OpenTelemetry
- Distributed Tracing
- Object Storage (Amazon S3)
- Horizontal Scaling
- Load Balancing
- Blue-Green Deployment
- Canary Releases
- Automated Unit Testing
- Integration Testing
- Security Scanning

---

# 💼 Skills Demonstrated

This project demonstrates practical experience in:

### Artificial Intelligence

- Retrieval-Augmented Generation (RAG)
- Generative AI
- LLM Integration
- Google Gemini
- Semantic Search
- ChromaDB
- Vector Databases

### Backend Engineering

- FastAPI
- REST API Development
- Python
- API Design
- File Processing

### Cloud Engineering

- AWS EC2
- Linux
- Docker Deployment
- Reverse Proxy
- Infrastructure Management

### DevOps Engineering

- Docker
- Docker Compose
- GitHub Actions
- CI/CD
- Docker Hub
- Monitoring
- Observability
- Health Checks

---

# 🤝 Contributing

Contributions are welcome.

Feel free to:

- Open issues
- Suggest improvements
- Submit pull requests

---

# 📄 License

This project is released under the MIT License.

---

# 👨‍💻 Author

## Adithya Anil

Software Engineer passionate about building production-ready AI systems that combine modern LLM technologies with cloud-native engineering practices.

### Areas of Interest

- Artificial Intelligence
- Generative AI
- Retrieval-Augmented Generation
- Backend Engineering
- Cloud Computing
- DevOps
- Platform Engineering
- Distributed Systems

### Connect

**GitHub**

https://github.com/aadi090204

**LinkedIn**

https://www.linkedin.com/in/adithya-anil-8a247a255/

---

# ⭐ If you found this project interesting, consider giving it a star!

It helps others discover the project and supports future development.

---

## Thank you for visiting the repository! 🚀
