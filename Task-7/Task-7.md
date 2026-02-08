# Task-7 – Troubleshooting

## Task Overview

This task focuses on identifying and fixing common issues while deploying applications on AWS EC2 using Docker and an Application Load Balancer (ALB).  
The main goal was to make sure the application is accessible, Docker containers are configured properly, and ALB health checks pass without errors.

---

## Troubleshooting Scenarios

### 1. Application Not Accessible

**Issue:**  
The application is deployed, but it does not open in the browser using the public IP or domain.

**Possible Causes:**  
- Security Group does not allow traffic on port 80 or 443  
- Application is running on `localhost` instead of `0.0.0.0`  
- Service is not running or crashed  

**Fix:**  
- Update EC2 Security Group to allow inbound traffic on ports 80 and 443  
- Configure Flask/NGINX/Apache to listen on `0.0.0.0`  
- Restart the application or web server and check logs  

---

### 2. Docker Container Running but Port Not Reachable

**Issue:**  
Docker container is running, but the application port cannot be accessed from outside.

**Possible Causes:**  
- Incorrect or missing port mapping  
- Application inside the container is not listening on the correct port  
- Security Group or firewall blocking traffic  

**Fix:**  
- Run the container with correct port mapping:
```bash
docker run -d -p 80:5000 ec2-flask-app
