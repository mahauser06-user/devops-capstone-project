DevOps Capstone Project
📌 Project Overview

This project demonstrates a complete DevOps CI/CD pipeline that automates:

Application build

Docker image creation

Image push to Docker Hub

Deployment on AWS EC2

Monitoring using Prometheus, Grafana, and Node Exporter

The goal of this project is to implement real-world DevOps practices including automation, containerization, and monitoring.

🛠️ Tools & Technologies Used

GitHub – Source Code Management

Jenkins – Continuous Integration & Deployment

Docker – Containerization

Docker Hub – Image Registry

AWS EC2 – Cloud Hosting

Prometheus – Metrics Collection

Node Exporter – System Metrics

Grafana – Monitoring Dashboard

🏗️ Project Architecture
Developer
   ↓
GitHub Repository
   ↓
Jenkins Pipeline
   ↓
Docker Build
   ↓
Docker Hub
   ↓
Deploy on EC2
   ↓
Monitoring (Prometheus + Grafana + Node Exporter)
🔁 CI/CD Pipeline Stages

The Jenkins pipeline includes:

1️⃣ Checkout Code

Pulls latest source code from GitHub repository.

2️⃣ Build Docker Image

Builds the application into a Docker image.

docker build -t maha006/devops-capstone-app .
3️⃣ Push to Docker Hub

Pushes the built image to Docker Hub repository.

docker push maha006/devops-capstone-app
4️⃣ Deploy Container

Runs the container on AWS EC2.

docker run -d -p 3000:3000 maha006/devops-capstone-app
🐳 Docker Image Details

Docker Hub Repository: maha006/devops-capstone-app

Application Port: 3000

Access Application:

http://<EC2-PUBLIC-IP>:3000
📊 Monitoring Setup
🔹 Prometheus

Collects metrics from Node Exporter

Scrapes system performance data

Access:

http://<EC2-PUBLIC-IP>:9090
🔹 Node Exporter

Provides CPU, Memory, Disk, and Network metrics

Access:

http://<EC2-PUBLIC-IP>:9100/metrics
🔹 Grafana

Visualizes Prometheus metrics

Custom dashboards created for system monitoring

Access:

http://<EC2-PUBLIC-IP>:3000

Default Login:

Username: admin
Password: admin
📸 Screenshots

Include screenshots of:

✅ Jenkins Pipeline Success

✅ Docker Container Running

✅ Prometheus Targets (UP)

✅ Grafana Dashboard

✅ Node Exporter Metrics

Example:

![Jenkins Pipeline](images/jenkins.png)
![Grafana Dashboard](images/grafana.png)
☁️ AWS Setup

EC2 Instance (Ubuntu)

Security Group Ports Open:

22 (SSH)

8080 (Jenkins)

3000 (App / Grafana)

9090 (Prometheus)

9100 (Node Exporter)

🔐 Credentials Configuration

Configured securely in Jenkins:

GitHub credentials

Docker Hub credentials

AWS EC2 key pair

Note: No passwords are stored in the repository.

🎯 Project Outcome

✔ Automated CI/CD pipeline
✔ Dockerized application
✔ Successful deployment on AWS EC2
✔ Real-time monitoring dashboard
✔ Infrastructure monitoring with Prometheus & Grafana

🚧 Challenges Faced

Docker not found inside Jenkins container

Git branch mismatch issues

Port conflicts

Disk space errors while pulling monitoring images

🔮 Future Improvements

Kubernetes Deployment

Add Alertmanager

Infrastructure as Code using Terraform

Automated testing integration

GitHub Webhook trigger
