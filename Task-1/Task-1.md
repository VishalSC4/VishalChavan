# Task-1 – Application

## Task Overview

This task shows how to deploy a basic frontend and backend application on AWS EC2 with a MySQL (MariaDB) database.  
The goal was to connect the app to the database and check that it works in the browser.

## Requirements

- Create a simple frontend and backend app  
- Use one database (MySQL/MariaDB)  
- Make sure the app connects to the database  
- Test the app in the browser  

## Infrastructure

- Cloud Provider: AWS  
- Service: EC2  
- Instance Type: t2.micro  
- Operating System: Amazon Linux 2023  
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
- PHP script handles form submission  
- Connects to MySQL database  
- Saves user details in `users` table  

### Database
- Database Name: `userdb`  
- Table: `users`  
- Columns: `id`, `username`, `password`  
- Example entry stored successfully  

## Result

The app was deployed on AWS EC2.  
Users can register through the frontend form, and the data is saved in the MySQL database.  
The application worked as expected when tested in the browser.
