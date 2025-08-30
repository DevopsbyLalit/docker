# 🚀 Docker & AWS ECR Guide

This repository contains a simple guide on how to **install Docker**, run **basic Docker commands**, and **push images to AWS Elastic Container Registry (ECR)**.  
Just follow the steps below 👇

---

## 📌 1. Install Docker on Amazon Linux / EC2
```bash
# Update system
sudo yum update -y

# Install Docker
sudo yum install -y docker

# Start Docker service
sudo systemctl start docker

# Enable Docker on boot
sudo systemctl enable docker

# Add current user to docker group (so no need to use sudo)
sudo usermod -aG docker ec2-user

# Log out and log back in (or run: newgrp docker)

📌 2. Verify Installation

docker --version             # Check Docker version
systemctl is-active docker   # Check if Docker is active
docker ps                    # List running containers

📌 3. Common Docker Commands

docker images                  # List images
docker rmi <image_id>          # Remove an image
docker ps                      # List running containers
docker ps -a                   # List all (stopped + running)
docker stop <id>               # Stop a container
docker rm <id>                 # Remove a container
