# Dockerized Node.js Express Application

[![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org)

A simple Express.js application containerized using Docker, demonstrating basic Docker workflows.

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [API Endpoint](#api-endpoint)
- [Project Structure](#project-structure)
- [Docker Commands](#docker-commands)
- [License](#license)

## Features
- Simple Express.js server
- Docker containerization
- Environment configuration
- Production-ready Docker setup

## Prerequisites
- [Node.js](https://nodejs.org/) (v14+ recommended)
- [Docker](https://www.docker.com/get-started)
- [Git](https://git-scm.com/)

## Getting Started

### Local Development
```bash
# Clone repository
git clone https://github.com/your-username/docker-app.git
cd docker-app

# Install dependencies
npm install

# Start development server
npm start
## docker-commands
# Build Docker image
docker build -t docker-demo .

# Run container
docker run -p 5000:8080 docker-demo
## api-endpoint
GET /: Returns JSON response
{
  "message": "Docker is easy"
}
## project-structure
docker-app/
├── Dockerfile
├── package.json
├── package-lock.json
├── README.md
└── src/
    └── index.js
# List running containers
docker ps

# List all containers (including stopped)
docker ps -a

# Stop a container
docker stop <container-id>

# Remove a container
docker rm <container-id>

# List images
docker images

# Remove an image
docker rmi <image-id>

# Clean up unused resources
docker system prune
## Docker Commands Cheatsheet 🐳

### Project-Specific Commands
```bash
# Build the Docker image
docker build -t docker-demo .

# Run the container with port mapping
docker run -p 5000:8080 docker-demo

# Run in detached mode
docker run -d -p 5000:8080 --name my-container docker-demo

# View container logs
docker logs my-container

# Push to Docker Hub (replace with your username)
docker tag docker-demo your-dockerhub-username/docker-demo:latest
docker push your-dockerhub-username/docker-demo:latest
