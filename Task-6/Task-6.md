# Task-6 – Cost Optimization

## Task Overview

This task focuses on optimizing costs while deploying applications on AWS EC2.  
The goal was to use free-tier eligible instances, allocate minimal resources, and configure Auto Scaling to avoid over-provisioning.

## Requirements Completed

- Used free-tier eligible instances (t2.micro / t3.micro)
- Allocated minimal resources for deployment
- Configured Auto Scaling to dynamically adjust capacity
- Ensured scaling policies prevent unnecessary costs

## Infrastructure Details

- Cloud Provider: AWS
- Services: EC2, Auto Scaling
- Instance Type: t2.micro (Free-tier eligible)
- Operating System: Amazon Linux 2023
- Region: ap-south-1 (Mumbai)
- Scaling Metric: CPU Utilization
- Auto Scaling Group (ASG): Configured to scale between 1–3 instances

## Cost Optimization Strategy

1. Free-Tier Eligible Instances  
   - Selected t2.micro instances which are free-tier eligible.  
   - This helps keep the baseline cost minimal.

2. Minimal Resources  
   - Deployed lightweight applications (Flask/NGINX).  
   - Optimized Docker containers to reduce memory and CPU usage.

3. Auto Scaling  
   - Configured ASG with:  
     - Minimum Instances: 1  
     - Desired Capacity: 1  
     - Maximum Instances: 3  
   - Scaling policy based on CPU utilization:  
     - Scale out when CPU > 70%  
     - Scale in when CPU < 30%  

4. Avoid Over-Provisioning  
   - Ensured resources scale only when required.  
   - Prevents idle instances and reduces unnecessary costs.

## Result

- Application deployed successfully on AWS EC2 with cost-optimized configuration.  
- Free-tier eligible instances were used to minimize expenses.  
- Auto Scaling ensures efficient resource usage and avoids over-provisioning.  
- Deployment is scalable, reliable, and cost-effective.
