# Task -5 Load Balancer and Auto Scaling

## Task Overview

This task demonstrates how to configure an Application Load Balancer (ALB), attach an Auto Scaling Group (ASG), and scale EC2 instances automatically based on CPU utilization.

## Requirements Completed

- Configured Application Load Balancer (ALB)
- Attached Auto Scaling Group (ASG)
- Defined scaling policies based on CPU utilization
- Verified scaling and load balancing functionality

## Infrastructure Details

- Cloud Provider: AWS
- Services: EC2, ALB, Auto Scaling
- Instance Type: t2.micro
- Operating System: Amazon Linux 2023
- Region: ap-south-1 (Mumbai)
- Scaling Metric: CPU Utilization
- Load Balancer Type: Application Load Balancer (ALB)

## Screenshots Reference

| Image   | Description |
|---------|-------------|
| t15.png | EC2 Instances dashboard showing Task-5 running |
| t16.png | Creating AMI from Task-5 instance |
| t17.png | Registering EC2 instances to Target Group |
| t18.png | Auto Scaling Group configuration |
| t19.png | Launch Template for Auto Scaling |
| t20.png | Application Load Balancer configuration |
| t21.png | NGINX installation and configuration logs |
| t22.png | Target Group details linked to ALB |
| t23.png | Browser output confirming Task-5 application is live via ALB |

## Screenshots

### EC2 Instances Dashboard
![EC2 Instances](t15.png)

### Creating AMI from Instance
![AMI Creation](t16.png)

### Registering Instances to Target Group
![Target Group Registration](t17.png)

### Auto Scaling Group Configuration
![ASG Config](t18.png)

### Launch Template for ASG
![Launch Template](t19.png)

### Application Load Balancer Configuration
![ALB Config](t20.png)

### NGINX Installation and Configuration
![NGINX Setup](t21.png)

### Target Group Details
![Target Group](t22.png)

### Application Live via ALB
![Application Live](t23.png)

## Scaling Policy

- Metric: CPU Utilization
- Threshold: Scale out when CPU > 70%
- Desired Capacity: 1
- Minimum Instances: 1
- Maximum Instances: 3
- Scaling Action: Launch new EC2 instances using Launch Template when threshold is breached

## Result

The application was successfully deployed with:
- Application Load Balancer distributing traffic
- Auto Scaling Group managing EC2 instances
- Scaling policy based on CPU utilization

Browser output confirmed the application is live with the message:  
"This Is Task-5"
