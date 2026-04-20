# NewApp_CICD

A simple CI/CD demo project for deploying a static web application using **Docker**, **Kubernetes**, and **GitHub Actions**.

## Project Overview

This repository contains:
- A static frontend application (`index.html`)
- A `Dockerfile` to serve the app using Nginx
- Kubernetes deployment manifests in the `k8s` folder
- GitHub Actions workflow under `.github/workflows`

## Repository Structure

```bash
NewApp_CICD/
├── .github/
│   └── workflows/
├── k8s/
├── Dockerfile
├── index.html
└── README.md
```

## Features

- Static web application
- Containerized using Docker
- Deployable on Kubernetes
- CI/CD pipeline using GitHub Actions

## Prerequisites

Before you run or deploy this project, make sure you have:

- Docker installed
- Kubernetes cluster access
- Git installed
- GitHub account for CI/CD

## Run Locally with Docker

1. Build the Docker image:

```bash
docker build -t newapp-cicd .
```

2. Run the container:

```bash
docker run -d -p 8080:80 newapp-cicd
```

3. Open your browser and visit:

```bash
http://localhost:8080
```

## Kubernetes Deployment

Apply the Kubernetes manifests from the `k8s` folder:

```bash
kubectl apply -f k8s/
```

Check the pods and services:

```bash
kubectl get pods
kubectl get svc
```

## GitHub Actions CI/CD

The repository includes a GitHub Actions workflow to automate build and deployment tasks.

Typical pipeline stages:
- Checkout code
- Build Docker image
- Push image to registry
- Deploy to Kubernetes

## Dockerfile

The application is served using Nginx from the Docker container.

## Deployment Notes

- Update image names in Kubernetes manifests before deployment.
- Ensure your cluster has access to the container registry.
- Verify namespace, service type, and port mappings.

## Future Improvements

- Add backend support
- Add environment-specific deployment manifests
- Add monitoring and logging
- Add ingress for public access

## Author

Created by **abhijithgeorge008**
