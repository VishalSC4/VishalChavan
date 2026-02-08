# Task-2 - Docker Setup and Application Deployment

## Step 1: Create Dockerfile
A Dockerfile was made inside the project folder.  
It sets the base image, copies the app files, installs the needed packages, and sets the working directory.  
This makes sure the Flask app can run inside a container.

![EC2 Instance Setup](t1.png)  
This screenshot shows the EC2 instance setup before Docker was installed.

---

## Step 2: Install and Configure Docker
Docker was installed on the Amazon Linux 2023 instance.  
The installation was checked with `docker --version`.  
A folder named `docker-demo` was created, and files like `app.py`, `requirements.txt`, and `Dockerfile` were added.

![Docker Installation](t2.png)  
This screenshot shows Docker being installed and the project files being created.

---

## Step 3: Build Docker Image
The image was built with the command:  
```bash
docker build -t flask-demo-app .
