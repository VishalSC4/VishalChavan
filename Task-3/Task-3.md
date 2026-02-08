# Task-3 - AWS EC2 Deployment

## Task Overview

This task shows how to deploy a Flask app on an AWS EC2 instance using Docker.  
It includes launching EC2, installing Docker, building an image, running the container, exposing ports, and checking the app in the browser.

## Task Requirements

- Launch EC2 instance (t2.micro / t3.micro for cost saving)  
- Install Docker on EC2  
- Build Docker image  
- Run the app inside a Docker container  
- Expose the needed ports  
- Make sure the container starts again if the server reboots  

## Infrastructure Details

- Cloud Provider: AWS  
- Service: EC2  
- Instance Type: t2.micro  
- Operating System: Amazon Linux 2023  
- Region: ap-south-1 (Mumbai)  
- Application: Python Flask App  
- Container Platform: Docker  

## Screenshots Reference

| Image   | Description |
|---------|-------------|
| t6.png  | AWS EC2 dashboard showing instances running/stopped |
| t7.png  | EC2 terminal setup and Docker installation |
| t8.png  | Docker image build process for Flask app |
| t9.png  | Running Docker container and Flask app output in browser |

## Screenshots

### EC2 Instances Dashboard
![EC2 Instances](t6.png)

### Docker Installation on EC2
![Docker Installation](t7.png)

### Docker Image Build
![Docker Build](t8.png)

### Docker Container Running and Flask Output
![Docker Run](t9.png)

## Dockerfile

The Dockerfile used for the Flask app:

```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY app.py .
COPY requirements.txt .

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python", "app.py"]
