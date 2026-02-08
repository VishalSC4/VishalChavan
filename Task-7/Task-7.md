# Task-7 – Troubleshooting

## Task Overview

This task is about finding and fixing common problems that come up when deploying applications on AWS EC2 with Docker and a Load Balancer (ALB).  
The aim was to make sure the app stays reachable, containers are exposed correctly, and the ALB health checks work.

## Troubleshooting Scenarios

### 1. Application Not Accessible

**Issue:**  
- The app is deployed but cannot be opened in the browser or through the public IP.

**Possible Causes:**  
- Security Group does not allow incoming traffic on ports 80/443.  
- The app is bound to `localhost` instead of `0.0.0.0`.  
- Firewall rules are blocking traffic.

**Fix:**  
- Update the EC2 Security Group to allow HTTP (80) and HTTPS (443).  
- Configure Flask/NGINX/Apache to listen on `0.0.0.0`.  
- Check the instance health and restart the service if needed.

---

### 2. Container Running but Port Not Reachable

**Issue:**  
- The Docker container is running, but the app port cannot be reached from outside.

**Possible Causes:**  
- Port mapping is missing or wrong (for example, `-p 80:5000` not set).  
- The app inside the container is not listening on the exposed port.  
- Security Group/firewall not allowing traffic.

**Fix:**  
- Run the container with correct port mapping:  
  ```bash
  docker run -d -p 80:5000 ec2-flask-app
