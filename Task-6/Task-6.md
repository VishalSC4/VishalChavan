# Task-6 – Cost Optimization

## Task Overview

This task focuses on reducing cost while deploying applications on AWS EC2.  
The main goal was to use free-tier instances, keep resource usage low, and use Auto Scaling so that extra instances are created only when needed.

---

## Requirements Completed

The following steps were completed successfully:

- Used free-tier eligible EC2 instances (t2.micro / t3.micro)
- Allocated minimum resources for application deployment
- Configured Auto Scaling to adjust capacity automatically
- Applied scaling rules to avoid unnecessary cost

---

## Infrastructure Details

- **Cloud Provider:** AWS
- **Services Used:** EC2, Auto Scaling
- **Instance Type:** t2.micro (Free-tier eligible)
- **Operating System:** Amazon Linux 2023
- **Region:** ap-south-1 (Mumbai)
- **Scaling Metric:** CPU Utilization
- **Auto Scaling Group:** Minimum 1 and Maximum 3 instances

---

## Cost Optimization Strategy

### 1. Free-Tier Eligible Instances
- t2.micro instances were selected as they are free-tier eligible.
- This helps keep the overall cost very low.

### 2. Minimal Resource Usage
- Lightweight applications like Flask and NGINX were used.
- Applications were optimized to use less CPU and memory.

### 3. Auto Scaling Configuration
- Auto Scaling Group was configured with:
  - Minimum Instances: 1
  - Desired Capacity: 1
  - Maximum Instances: 3
- Scaling policy based on CPU usage:
  - Scale out when CPU is above 70%
  - Scale in when CPU is below 30%

### 4. Avoid Over-Provisioning
- Instances are launched only when required.
- Idle instances are terminated automatically.
- This avoids paying for unused resources.

---

## Result

- Application was successfully deployed with a cost-optimized setup.
- Free-tier eligible instances helped reduce expenses.
- Auto Scaling ensured efficient use of resources.
- The setup is scalable, reliable, and cost-effective.
