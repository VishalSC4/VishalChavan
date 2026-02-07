# AWS EC2 Deployment – Troubleshooting 🛠️

## 📌 Task Overview

This task focuses on identifying and resolving common issues encountered during application deployment on **AWS EC2** with **Docker** and **Load Balancer (ALB)**.  
The goal is to ensure applications remain accessible, containers are properly exposed, and ALB health checks succeed.

---

## 🛠️ Troubleshooting Scenarios

### 1. Application Not Accessible
**Issue:**
- Application is deployed but not accessible via browser or public IP.

**Possible Causes:**
- Security Group not allowing inbound traffic on required ports (e.g., 80/443).
- Application not bound to the correct host (`0.0.0.0` instead of `localhost`).
- Firewall rules blocking traffic.

**Resolution:**
- Update EC2 Security Group to allow inbound traffic on HTTP (80) and HTTPS (443).
- Ensure Flask/NGINX/Apache is configured to listen on `0.0.0.0`.
- Verify instance health and restart services if needed.

---

### 2. Container Running but Port Not Reachable
**Issue:**
- Docker container is running, but application port is not accessible externally.

**Possible Causes:**
- Port mapping not configured correctly (`-p 80:5000` missing or incorrect).
- Application inside container not listening on the exposed port.
- EC2 firewall/security group not allowing traffic.

**Resolution:**
- Run container with proper port mapping:
  ```bash
  docker run -d -p 80:5000 ec2-flask-app
