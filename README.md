# Wisecow Application Deployment on Kubernetes & System Monitoring Scripts

![Wisecow Application]([https://your-image-link.com/wisecow-logo](https://github.com/nyrahul/wisecow)

## Project Overview

This repository contains two major components:

1. **Containerization and Deployment of the Wisecow Application on Kubernetes**  
   The goal of this project is to containerize the Wisecow application, hosted in the [Wisecow GitHub Repository](https://github.com/nyrahul/wisecow), and deploy it on a Kubernetes environment with secure TLS communication. Additionally, we will automate the build and deployment process using CI/CD via GitHub Actions.

2. **System Monitoring and Backup Scripts (Bash/Python)**  
   The second part of the project involves the creation of two scripts:
   - **System Health Monitoring Script**: Monitors the health of a Linux system (CPU usage, memory usage, disk space, and running processes) and sends an alert if any metric exceeds predefined thresholds.
   - **Automated Backup Solution**: Automates the backup of a specified directory to a remote server or cloud storage solution, with a success or failure report.

---

## Problem Statement 1: Containerization and Deployment of Wisecow Application on Kubernetes

### Objective

To containerize the Wisecow application, deploy it on a Kubernetes environment, and ensure secure TLS communication. The goal includes automating the CI/CD pipeline for continuous integration and deployment.

### Steps to Achieve the Objective

#### 1. Dockerization
- **Dockerfile**: A `Dockerfile` has been created to containerize the Wisecow application.
- The Docker image is built using this Dockerfile and pushed to a container registry.

#### 2. Kubernetes Deployment
- Kubernetes manifest files (`deployment.yaml`, `service.yaml`) are created to deploy the application to a Kubernetes cluster.
- The application is exposed as a Kubernetes service for easy accessibility.

#### 3. Continuous Integration and Deployment (CI/CD)
- A GitHub Actions workflow is set up to automate:
  - The build and push of the Docker image to the container registry.
  - The continuous deployment of the updated application to the Kubernetes environment after a successful image build.

#### 4. TLS Implementation
- Configured the Wisecow application to support TLS communication, ensuring secure data transmission.

### Files in this section:
- `Dockerfile` - Defines the containerization of the Wisecow app.
- `deployment.yaml` - Kubernetes manifest for deploying the app.
- `service.yaml` - Kubernetes service definition for exposing the app.
- `.github/workflows/ci-cd-pipeline.yml` - GitHub Actions workflow for CI/CD automation.

---

## Problem Statement 2: System Health Monitoring and Automated Backup Solution

### Objective

Choose two of the following objectives and implement them using either Bash or Python:

1. **System Health Monitoring Script**:
   - This script monitors the following system metrics:
     - CPU usage
     - Memory usage
     - Disk space
     - Running processes
   - If any of these metrics exceed predefined thresholds (e.g., CPU usage > 80%), an alert is generated and logged.

2. **Automated Backup Solution**:
   - This script automates backing up a specified directory to a remote server or cloud storage. It ensures that backups are completed successfully and provides reports on the status.

### Solution Implementation

#### 1. **System Health Monitoring Script** (Python)

This script monitors the following system metrics:
- CPU usage
- Memory usage
- Disk space
- Running processes

If any of these metrics exceed predefined thresholds (e.g., CPU usage > 80%), an alert is generated and logged.

**Key Features**:
- CPU usage alert when usage exceeds 80%.
- Memory usage alert when usage exceeds 90%.
- Disk space alert if disk usage exceeds 75%.
- Process monitoring with a customizable threshold.

#### 2. **Automated Backup Solution** (Bash/Python)

This script automates the backup of a specified directory to a remote server or cloud storage. It ensures that backups are completed successfully and provides reports on the status.

**Key Features**:
- Automates backup of a user-defined directory.
- Supports backing up to remote servers or cloud storage solutions.
- Provides success or failure reports on the backup process.

### Files in this section:
- `system_health_monitor.py` - Python script for monitoring system health.
- `automated_backup.sh` - Bash script for automated backups.

---

## Getting Started

### Prerequisites

1. **Docker**: Installed on your local machine or CI/CD environment.
2. **Kubernetes**: A Kubernetes cluster (local or cloud-based) to deploy the application.
3. **GitHub Actions**: For CI/CD pipeline automation.
4. **TLS Certificates**: Ensure that you have TLS certificates for securing communication.
5. **Python** (for System Health Monitoring Script).
6. **Bash** (for Automated Backup Script).

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/wisecow-app-deployment.git
   cd wisecow-app-deployment





# Wisecow Application Deployment and System Monitoring Scripts

## Project Overview

This repository contains two major components:

1. **Containerization and Deployment of the Wisecow Application on Kubernetes**
   - The goal of this project is to containerize the Wisecow application and deploy it on a Kubernetes environment with secure TLS communication. The project also automates the build and deployment process using CI/CD via GitHub Actions.

2. **System Health Monitoring and Automated Backup Solution**
   - The second part of the project involves the creation of two scripts:
     - **System Health Monitoring Script**: Monitors the health of a Linux system (CPU usage, memory usage, disk space, and running processes) and sends an alert if any metric exceeds predefined thresholds.
     - **Automated Backup Solution**: Automates the backup of a specified directory to a remote server or cloud storage solution, with a success or failure report.

---

## Containerization and Deployment of Wisecow Application on Kubernetes

### Steps to Achieve the Objective

1. **Build the Docker Image**:
   - To build the Docker image for the Wisecow application, run the following command:

     ```bash
     docker build -t wisecow-app .
     ```

2. **Push the Docker Image to a Container Registry**:
   - Push the created Docker image to your container registry:

     ```bash
     docker push <your-registry>/wisecow-app
     ```

3. **Apply Kubernetes Manifests to Deploy the App**:
   - Use the following commands to deploy the app using Kubernetes:

     ```bash
     kubectl apply -f deployment.yaml
     kubectl apply -f service.yaml
     ```

4. **Set Up GitHub Actions for CI/CD**:
   - Add the `.github/workflows/ci-cd-pipeline.yml` file to your repository for automating the CI/CD pipeline.

---

## Run the System Health Monitoring Script

1. **Ensure that you have Python installed on your machine.**
2. **Run the Script**:
   - To run the system health monitoring script, execute the following command:

     ```bash
     python system_health_monitor.py
     ```

---

## Run the Automated Backup Script

1. **Ensure that you have Bash or Python installed (depending on the version you want to run).**
2. **Run the Script**:
   - For the Bash version:

     ```bash
     bash automated_backup.sh
     ```

   - For the Python version (if available):

     ```bash
     python automated_backup.py
     ```

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Kubernetes documentation for deployment setup.
- Docker documentation for containerization.
- GitHub Actions documentation for CI/CD pipelines.
