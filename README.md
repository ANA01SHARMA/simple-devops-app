# DevOps CI/CD Project using Jenkins and Docker

## Project Overview
This project demonstrates a complete DevOps CI/CD pipeline using:

- Git & GitHub
- Jenkins
- Docker
- Node.js

The application is automatically built and deployed using Jenkins and Docker containers.

---

# Technologies Used

- Node.js
- Express.js
- Git
- GitHub
- Jenkins
- Docker
- Ubuntu / WSL

---

# Project Workflow

GitHub → Jenkins → Docker Build → Docker Container → Application Deployment

---

# Features

- Source code management using GitHub
- Continuous Integration using Jenkins
- Automated dependency installation
- Docker image creation
- Automated container deployment
- Application deployment on localhost

---

# Project Structure

simple-devops-app/

├── app.js

├── package.json

├── package-lock.json

├── Dockerfile

├── Jenkinsfile

├── .gitignore

└── README.md

---

# Dockerfile Explanation

FROM node:22

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "app.js"]

---

# Jenkins Pipeline

The Jenkins pipeline performs:

1. Pull latest code from GitHub
2. Install dependencies
3. Build Docker image
4. Stop old container
5. Deploy new Docker container

---

# Commands Used

## Build Docker Image

docker build -t simple-devops-app .

## Run Docker Container

docker run -d -p 3000:3000 --name simple-devops-container simple-devops-app

## Check Running Containers

docker ps

---

# How to Run Project

## Step 1
Clone Repository

git clone https://github.com/ANA01SHARMA/simple-devops-app.git

## Step 2
Go to project directory

cd simple-devops-app

## Step 3
Install dependencies

npm install

## Step 4
Run application

node app.js

## Step 5
Open browser

http://localhost:3000

---

# CI/CD Automation

This project automates:
- build process
- dependency installation
- Docker image creation
- container deployment

using Jenkins.

---

# Learning Outcomes

Through this project I learned:
- CI/CD concepts
- Jenkins automation
- Docker containerization
- GitHub integration
- automated deployment workflow

---

# Author

Anamika Sharma
