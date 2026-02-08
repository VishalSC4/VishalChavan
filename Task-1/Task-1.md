# AWS EC2 Deployment – Application

## Task Overview
This task shows how to deploy a simple frontend and backend application on AWS EC2 with a MySQL (MariaDB) database.  
The goal was to connect the application to the database and confirm it works through a browser.

## Requirements
- Create a simple frontend and backend app  
- Use one database (MySQL/MariaDB)  
- Make sure the app connects to the database  
- Test the application in the browser  

## Infrastructure
- Cloud Provider: AWS  
- Service: EC2  
- Instance Type: t2.micro  
- OS: Amazon Linux 2023  
- Region: ap-south-1 (Mumbai)  
- Web Server: NGINX  
- Database: MySQL (MariaDB)  
- Application: PHP + HTML frontend with MySQL backend  

## Screenshots

### EC2 Instances Dashboard
![EC2 Instances](t24.png)

### EC2 Terminal and NGINX Setup
![EC2 Terminal](t25.png)

### Frontend Application – Register User
![Register User](t26.png)

### MySQL Database Connection
![MySQL Database](t27.png)

## Application Details

### Frontend
- Simple HTML form for user registration  
- Fields: Username and Password  
- Sends data to backend (PHP)  

### Backend
- PHP scripts handle form submission  
- Connects to MySQL database  
- Saves user credentials in `users` table  

### Database
- Database Name: `userdb`  
- Table: `users`  
- Columns: `id`, `username`, `password`  
- Example entry stored successfully  
