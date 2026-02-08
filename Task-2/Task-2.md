# Task 3 – AWS EC2 Deployment with Docker

## Task Overview
This task shows how to deploy Docker on an AWS EC2 instance.  
The goal was to launch a cost‑optimized EC2 instance, install Docker, and run containers successfully.

## Requirements
- Launch EC2 instance (t2.micro)  
- Install Docker on EC2  
- Run Docker containers  

## AWS Region and Instance Details
- Region: Asia Pacific (Mumbai) – ap-south-1  
- Instance Type: t2.micro  
- Operating System: Amazon Linux 2023  

## Step 1: Launch EC2 Instance
An EC2 instance was launched from the AWS Management Console using Amazon Linux 2023 AMI and t2.micro instance type.

![EC2 Instances Running](./t6.png)

## Step 2: Connect to EC2 and Update System
The instance was accessed using SSH, and system packages were updated.

```bash
ssh -i Vishal.pem ec2-user@<Public-IP>
sudo yum update -y
