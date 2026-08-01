# jenkins-nginx-demo
# CI/CD Automation using Jenkins Freestyle Project, GitHub & Nginx on Azure VM

## Overview

This project demonstrates a basic Continuous Integration and Continuous Deployment (CI/CD) workflow using a Jenkins Freestyle Project integrated with GitHub and Nginx on an Azure Ubuntu Virtual Machine.

The project automates the deployment of a static website by fetching the latest source code from GitHub and deploying it to the Nginx web server.

---

## Architecture

text
Developer
     │
     ▼
GitHub Repository
     │
     ▼
Jenkins Freestyle Project
     │
     ▼
Azure Ubuntu Virtual Machine
     │
     ▼
Nginx Web Server
     │
     ▼
Website


---

## Technologies Used

- Microsoft Azure
- Ubuntu 22.04 LTS
- Jenkins (Freestyle Project)
- Git
- GitHub
- Nginx
- Linux

---

## Prerequisites

- Azure Virtual Machine
- Ubuntu 22.04 LTS
- Java (OpenJDK)
- Git
- Jenkins
- Nginx

---

## Project Workflow

1. Created an Azure Ubuntu Virtual Machine.
2. Installed Java as a prerequisite for Jenkins.
3. Added the official Jenkins repository and GPG signing key.
4. Installed and configured Jenkins.
5. Installed and configured the Nginx web server.
6. Created a GitHub repository containing the website source code.
7. Configured a Jenkins Freestyle Project to clone the GitHub repository.
8. Executed a shell script to deploy the website to the Nginx web root.
9. Restarted the Nginx service after deployment.

---

## Jenkins Build Script

bash
#!/bin/bash

sudo cp $WORKSPACE/index.html /var/www/html/index.html
sudo systemctl restart nginx


---

## Installation Summary

- Updated Ubuntu packages
- Installed OpenJDK
- Added Jenkins GPG signing key
- Added Jenkins APT repository
- Installed Jenkins
- Started and enabled Jenkins service
- Installed Nginx
- Configured Jenkins deployment job

---

## Skills Demonstrated

- Linux Administration
- Jenkins Installation & Configuration
- Git & GitHub Integration
- Azure Virtual Machine Management
- Nginx Web Hosting
- Basic CI/CD Implementation
- Shell Scripting
- Service Management using systemctl

---

## Project Output

The website is successfully deployed on an Azure Ubuntu Virtual Machine.

Whenever a build is triggered in Jenkins, the latest source code is fetched from GitHub and deployed automatically to the Nginx web server.

---

## Future Enhancements

- Configure GitHub Webhooks for automatic build triggering.
- Convert the Jenkins Freestyle Project into a Jenkins Pipeline using a Jenkinsfile.
- Containerize the application using Docker.
- Deploy the application on Kubernetes.
- Integrate Prometheus and Grafana for monitoring.

---

## Repository Structure


jenkins-nginx-demo/
│── index.html
├── README.md
└── screenshots/
    ├── jenkins-dashboard.png
    ├── build-success.png
    ├── website-output.png
    └── azure-vm.png


---

## Author

*Devwarth
