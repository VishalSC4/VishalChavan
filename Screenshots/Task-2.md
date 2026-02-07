# Task 2 – Dockerized Flask Application on AWS EC2

## Overview
This document contains **both explanations and screenshots** for Task 2.  
It demonstrates creating Docker files, running the application in Docker containers, exposing ports, and ensuring containers auto-start on reboot.

---

## Objectives Covered
- Create Dockerfile
- Build Docker image
- Run app using Docker containers
- Expose required ports
- Ensure containers auto-start on reboot

---

## Tech Stack
- AWS EC2 (Amazon Linux 2023)
- Docker
- Python (Flask)

---

## Project Structure
```
docker-demo/
├── app.py
├── requirements.txt
└── Dockerfile
```

---

## Step 1: EC2 Instance Setup
An EC2 instance was launched in the Mumbai region and accessed via SSH.

![EC2 Instances](t1.png)

---

## Step 2: Docker Installation
System packages were updated and Docker was installed and verified.

```bash
sudo yum update -y
sudo yum install docker -y
docker --version
```

![Docker Installation](t2.png)

---

## Step 3: Docker Image Creation
A Dockerfile was created and the Flask application image was built successfully.

```bash
docker build -t flask-demo-app .
```

![Docker Build](t3.png)

---

## Step 4: Running Docker Container
The Docker container was started with port mapping and auto-restart enabled.

```bash
docker run -d \
--name flask-container \
-p 80:5000 \
--restart unless-stopped \
flask-demo-app
```

Container status verification:

```bash
docker ps
```

![Running Container](t4.png)

---

## Step 5: Application Verification
The Flask application was accessed using the EC2 public IP from a browser.

```
http://<EC2-Public-IP>
```

![Application Output](t5.png)

---

## Auto-Start on Reboot
The container uses:
```
--restart unless-stopped
```
This ensures the container starts automatically after a system reboot.

---

## Conclusion
The Flask application was successfully dockerized, deployed on AWS EC2, exposed via browser, and configured to auto-start on reboot.

## Task 2 completed successfully.

---

**Author:** Vishal Chavan
