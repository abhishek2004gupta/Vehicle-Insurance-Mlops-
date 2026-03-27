# 🚀 Vehicle Insurance MLOps Project

An end-to-end **Production-Ready Machine Learning System** built with MLOps principles, integrating data pipelines, model training, cloud deployment, and CI/CD automation using AWS.

---

## 🌟 Overview

This project demonstrates a complete **Machine Learning lifecycle in production**, covering:

* 📥 Data Ingestion from MongoDB Atlas
* 🔍 Data Validation & Transformation
* 🤖 Model Training & Evaluation
* ☁️ Model Deployment using AWS (S3, ECR, EC2)
* 🔄 CI/CD Pipeline with GitHub Actions
* 🐳 Containerization using Docker
* 🌐 Web Application for Predictions

---

## 🧠 Key Features

✔️ Modular and scalable ML pipeline
✔️ Cloud-based data storage (MongoDB Atlas)
✔️ Automated model versioning with AWS S3
✔️ CI/CD deployment using GitHub Actions + Self-hosted runner
✔️ Dockerized application for portability
✔️ Real-time prediction via Flask web app

---

## 🏗️ Project Architecture

```
Data Source (MongoDB)
        ↓
Data Ingestion
        ↓
Data Validation
        ↓
Data Transformation
        ↓
Model Training
        ↓
Model Evaluation
        ↓
Model Registry (AWS S3)
        ↓
Deployment (Docker + EC2)
        ↓
User Interface (Flask App)
```

---

## ⚙️ Tech Stack

* **Programming:** Python
* **ML Libraries:** Scikit-learn, Pandas, NumPy
* **Database:** MongoDB Atlas
* **Cloud:** AWS (S3, ECR, EC2, IAM)
* **CI/CD:** GitHub Actions
* **Containerization:** Docker
* **Backend:** Flask

---

## 📂 Project Setup

### 1️⃣ Clone Repository

```bash
git clone <your-repo-link>
cd <project-folder>
```

### 2️⃣ Create Virtual Environment

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
```

---

## 🍃 MongoDB Setup

* Create cluster on MongoDB Atlas
* Add IP: `0.0.0.0/0`
* Get connection string
* Set environment variable:

```bash
export MONGODB_URL="your_mongodb_connection_string"
```

---

## ☁️ AWS Setup

* Create IAM user with admin access
* Configure:

```bash
export AWS_ACCESS_KEY_ID="your_key"
export AWS_SECRET_ACCESS_KEY="your_secret"
```

* Create S3 bucket for model storage
* Configure ECR for Docker images

---

## 🐳 Docker Setup

```bash
docker build -t vehicleproj .
docker run -d -p 5000:5000 vehicleproj
```

---

## 🔄 CI/CD Pipeline

This project uses **GitHub Actions + Self-hosted Runner on EC2**:

* Push code → triggers pipeline
* Build Docker image
* Push to AWS ECR
* Deploy on EC2 automatically

---

## 🌐 Deployment

* EC2 instance (Ubuntu)
* Docker installed
* Port exposed: `5000` (or `5080`)

Access app:

```
http://<EC2-PUBLIC-IP>:5000
```

---

## 📊 Training & Prediction

* Trigger training via:

```
/training
```

* Prediction via web interface

---

## 📁 Project Highlights

* Custom logging & exception handling
* Modular pipeline design
* Production-grade folder structure
* Fully automated deployment

---

## 🚧 Challenges Solved

* Managing environment variables across local + cloud
* Handling Dockerized ML pipelines
* Automating CI/CD with self-hosted runners
* Integrating MongoDB + AWS services

---

## 📌 Future Improvements

* Add monitoring (Prometheus/Grafana)
* Use Kubernetes for scaling
* Add model drift detection
* Improve UI/UX

---

## 👨‍💻 Author

**Abhishek Gupta**

* Passionate about ML Systems & Backend Engineering
* Focused on building scalable AI solutions

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to connect!

---
