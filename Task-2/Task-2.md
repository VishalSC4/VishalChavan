# Task 3 – AWS EC2 Deployment with Docker

## Task Overview
This document contains **both explanation and screenshots** for **Task 3: AWS EC2 Deployment**.  
The objective of this task is to launch a cost-optimized EC2 instance, install Docker on it, and run Docker containers successfully.

---

## Task Requirements
- Launch EC2 instance (t2.micro)
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

![EC2 Instances Running](./t6.png)

---

## Step 2: Connect to EC2 & Update System
The instance was accessed using SSH, and system packages were updated.

```bash
ssh -i Vishal.pem ec2-user@<Public-IP>
sudo yum update -y
