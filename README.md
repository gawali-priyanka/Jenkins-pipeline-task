## Jenkins CI/CD Pipeline with Docker – Task 2

This project demonstrates a simple CI/CD pipeline using Jenkins and Docker.
It automates the process of building, testing, and deploying a static web application served via Nginx.

---

## Project Structure

├── screenshots/      # Contains screenshots of pipeline execution and output <br>
├── Dockerfile        # Defines Docker image (Nginx serving static page) <br>
├── Jenkinsfile       # Jenkins declarative pipeline configuration <br>
├── index.html        # Static web application <br>
└── README.md         # Project documentation <br>

---

## Components

Dockerfile → Creates a Docker image with Nginx serving index.html.

Jenkinsfile → Defines the Jenkins pipeline stages (Checkout → Build → Run).

index.html → Simple static web page (served on port 8081).

---

## Setup Instructions

git clone https://github.com/priyanka-gawali/jenkins-pipeline-task.git
cd jenkins-pipeline-task

---

## Configure Jenkins Pipeline

Open Jenkins Dashboard → New Item → Pipeline

Select Pipeline script from SCM

## Choose:

SCM: Git

Repository URL: https://github.com/priyanka-gawali/jenkins-pipeline-task.git

Branch: main


Run the Pipeline

Trigger the build manually or via GitHub webhook.

Jenkins will execute stages defined in Jenkinsfile.

---

## Example stages:

Checkout Code – Fetches code from GitHub

Build Docker Image – Builds image using Dockerfile

Deploy Container – Runs container on port 8081

Post-Build Actions – Clean up, notifications, etc.

---

## Screenshots

 Successful Pipeline Execution
 
 ![Screenshot](screenshot/Github-action.png)


 Static Web App Running on Port 8081

 ![Screenshot](screenshot/Github-action.png)


 ---

## Key Highlights

Fully automated pipeline (CI/CD).
Docker-based deployment (portable and lightweight).
Simple Nginx-based static web app.
Integration between GitHub → Jenkins → Docker.
