# Task-3: Docker Implementation on AWS EC2

## Objective
The objective of this task is to containerize a Flask application using Docker, deploy it on an AWS EC2 instance, expose the required ports, and ensure that the Docker container automatically starts on system reboot.

---

## Technologies Used
- AWS EC2 (Amazon Linux 2023)
- Docker
- Python (Flask)
- GitHub

---

## Task Requirements
- Create Docker file(s)
- Run application using Docker containers
- Expose required ports
- Ensure containers auto-start on reboot

---

## EC2 Instance Setup
- Launched an EC2 instance in the **Asia Pacific (Mumbai)** region
- Connected to the instance using SSH
- Updated system packages
- Installed Docker on Amazon Linux 2023

**Screenshot:** `t6.png`  
**Description:** AWS EC2 dashboard showing running and stopped instances used for this task.

---

## Docker Installation
Docker was installed and verified on the EC2 instance using the following commands:

```bash
sudo yum update -y
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
