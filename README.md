# 🚀 Dockerized Multi-Tier Application

A **full-stack Dockerized application** featuring a frontend, backend, and MySQL database running in separate containers.  
Designed for **scalable, portable deployment** on cloud platforms like AWS EC2 with **automated CI/CD** via GitHub Actions.

---

## 🏗️ Project Overview

- **Frontend:** React + Redux for a responsive UI (Port 3000)  
- **Backend:** Spring Boot REST API (Port 8080)  
- **Database:** MySQL for persistent data storage (Port 3306)  
- **Infrastructure:** Docker & Docker Compose, deployable on AWS EC2  
- **Automation:** CI/CD pipeline using GitHub Actions for automatic deployment  

---

## 🎯 Key Features

- 🖥️ **Frontend:** React-based responsive UI  
- ⚙️ **Backend:** Spring Boot REST API  
- 🗃️ **Database:** MySQL, running in its own container  
- 🔧 **Dockerized:** Each component isolated in its own container  
- 🔄 **CI/CD:** Automatic deployment to EC2 using GitHub Actions  
- 🌍 **Scalable & Portable:** Easily deploy on any cloud environment  
- 📦 **Modular Structure:** Frontend, backend, and DB decoupled for easier maintenance  

---

## 🗂️ Project Structure

```text
project-root/
├── backend/
│   ├── src/main/java/com/example/backend/BackendApplication.java  
│   ├── pom.xml                                                    
│   └── Dockerfile                                                 
├── frontend/
│   ├── src/
│   │   └── App.js                                                 
│   ├── package.json                                               
│   └── Dockerfile                                                 
├── db/
│   └── Dockerfile                                                 
├── .github/
│   └── workflows/
│       └── deploy.yml                                             
├── docker-compose.yml                                             
```

---

## ⚙️ Deployment on AWS EC2

1. Launch an **Ubuntu-based EC2 instance**.
2. SSH into the instance and install Docker & Docker Compose:

```bash
sudo apt update
sudo apt install -y docker.io docker-compose
sudo systemctl enable docker
sudo systemctl start docker
```

3. Clone the repository:

```bash
git clone https://github.com/adeel-aws/Multi-tier-Dockerized.git
cd Dockerized_Multi-Tier_App
```

4. Build and start the containers:

```bash
docker-compose up --build -d
```

5. Access the **frontend** at `http://<EC2_PUBLIC_IP>:3000`.

---

## 🔧 CI/CD Pipeline

- Uses **GitHub Actions** to automatically deploy changes to your EC2 instance.  
- Pipeline located in `.github/workflows/deploy.yml`.  
- Pushing updates to the main branch triggers automatic rebuild and redeployment of all containers.  

  ```
# **📸 Project Screenshots**


![WhatsApp Image 2025-01-26 at 23 20 29_0f4f6540](https://github.com/user-attachments/assets/5889c38b-3709-4556-9502-f4f18312e3fc)

![WhatsApp Image 2025-01-26 at 23 20 29_43fd542f](https://github.com/user-attachments/assets/b7fb3b49-af65-4db0-bdd9-7e3809ac8f93)


