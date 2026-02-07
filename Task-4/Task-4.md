# AWS EC2 Deployment – Application Access 🌐

## 📌 Task Overview

This task demonstrates how to access a deployed application on **AWS EC2** using different methods:
- Elastic IP
- EC2 Public IP
- Custom Domain via **GoDaddy** (`vishal4u.shop`)

---

## 🛠️ Task Requirements

The following objectives were completed:

- Associate Elastic IP with EC2 instance
- Access application via EC2 Public IP
- Configure DNS records in GoDaddy
- Access application via custom domain (`vishal4u.shop`)

---

## 🖥️ Infrastructure Details

- **Cloud Provider:** AWS
- **Service:** EC2
- **Instance Type:** t2.micro
- **OS:** Amazon Linux 2023
- **Region:** ap-south-1 (Mumbai)
- **Application Type:** Web Application (Flask / NGINX / Apache)
- **Domain Provider:** GoDaddy

---

## 📷 Screenshots Reference

| Image   | Description |
|---------|-------------|
| `t10.png` | AWS EC2 Instances dashboard showing running/stopped states |
| `t11.png` | EC2 terminal setup & NGINX installation |
| `t12.png` | NGINX configuration and service management |
| `t13.png` | GoDaddy DNS records pointing domain to EC2 Elastic IP |
| `t14.png` | Browser output confirming application is live via domain `vishal4u.shop` |

---

## 📸 Screenshots

### EC2 Instances Dashboard
![EC2 Instances](t10.png)

### NGINX Installation on EC2
![NGINX Installation](t11.png)

### NGINX Configuration & Service Management
![NGINX Config](t12.png)

### GoDaddy DNS Setup
![GoDaddy DNS](t13.png)

### Application Live via Domain
![Application Live](t14.png)

---

## 🌍 Application Access

The application can be accessed via:

- **Elastic IP:** `13.127.52.128`
- **EC2 Public IP:** (example) `65.1.131.134`
- **Custom Domain:** [http://vishal4u.shop](http://vishal4u.shop)

---

## ✅ Result

The application was successfully deployed and is accessible via:
- **Elastic IP**
- **EC2 Public IP**
- **Custom Domain (GoDaddy)**

Browser output confirms the app is live with the message:  
**"Task-4 AWS EC2 Application – Successfully Deployed"**
