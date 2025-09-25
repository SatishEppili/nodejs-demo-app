CI/CD Pipeline for Node.js App with DockerHub Deployment
Overview

This repository demonstrates a CI/CD pipeline using GitHub Actions to automate the build and deployment of a Node.js application as a Docker image. The pipeline automates the following steps:

Checkout the code from the repository.
Build a Docker image for the Node.js app.
Push the Docker image to DockerHub.
The pipeline is triggered automatically whenever changes are pushed to the main branch.
The CI/CD workflow is defined in:

.github/workflows/main.yml


Features:

Trigger: Push to main branch.

Jobs:

Checkout repository.
Verify DockerHub secrets.
Build Docker image.
Push Docker image to DockerHub.
Secrets Required:

How It Works

Push to main: Triggers the GitHub Actions workflow.

Checkout: Pulls the repository code.

Docker Login: Authenticates to DockerHub using secrets.

Build Image: Creates Docker image tagged as DOCKER_USERNAME/nodejs-demo-app:latest.

Push Image: Uploads the image to DockerHub automatically.

Usage

Create a DockerHub repository named nodejs-demo-app.

Add GitHub secrets: DOCKER_USERNAME and DOCKER_PASSWORD.

Push changes to main.

The workflow automatically builds and pushes the Docker image to DockerHub.

DOCKER_USERNAME → DockerHub username

DOCKER_PASSWORD → DockerHub Personal Access Token (with write access)
