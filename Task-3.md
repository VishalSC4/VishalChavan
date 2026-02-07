# Task 3 – AWS EC2 Deployment with Docker

## Task Overview
This document contains **both explanation and screenshots** for **Task 3: AWS EC2 Deployment**.  
The objective of this task is to launch a cost-optimized EC2 instance, install Docker on it, and run Docker containers successfully.

---

## Task Requirements
- Launch EC2 instance (t2.micro / t3.micro)
- Install Docker on EC2
- Run Docker containers on EC2

---

## AWS Region & Instance Details
- **Region:** Asia Pacific (Mumbai) – ap-south-1  
- **Instance Type:** t2.micro (cost optimized)  
- **OS:** Amazon Linux 2023  

---

## Step 1: Launch EC2 Instance
An EC2 instance was launched from the AWS Management Console using Amazon Linux 2023 AMI and t2.micro instance type.

![EC2 Instances Running](task3-ec2.png)

---

## Step 2: Connect to EC2 & Update System
The instance was accessed using SSH, and system packages were updated.

```bash
ssh -i Vishal.pem ec2-user@<Public-IP>
sudo yum update -y
```

![EC2 SSH & System Update](task3-ssh.png)

---

## Step 3: Install Docker on EC2
Docker was installed using the yum package manager.

```bash
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
```

Docker installation was verified successfully.

![Docker Installation](task3-docker-install.png)

---

## Step 4: Build Docker Image
The application directory was accessed, and a Docker image was built using the Dockerfile.

```bash
cd docker-demo
docker build -t ec2-flask-app .
```

The image was built successfully without errors.

![Docker Image Build](task3-docker-build.png)

---

## Step 5: Run Docker Container on EC2
The Docker container was launched in detached mode with port mapping and restart policy enabled.

```bash
docker run -d \
--name ec2-container \
-p 80:5000 \
--restart unless-stopped \
ec2-flask-app
```

Container started successfully.

![Docker Container Running](task3-docker-run.png)

---

## Step 6: Application Verification
The application was accessed using the EC2 Public IP address in a browser.

```text
http://<EC2-Public-IP>
```

The application responded successfully, confirming container deployment.

![Application Running in Browser](task3-browser.png)

---

## Conclusion
- EC2 instance launched successfully using a cost-optimized instance type
- Docker installed and configured on EC2
- Application container built and deployed successfully
- Application accessible via browser using EC2 public IP

**Task 3 completed successfully**

---

**Author:** Vishal Chavan  
AWS & DevOps Intern Candidate
