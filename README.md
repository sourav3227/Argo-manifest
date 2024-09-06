# Spring Boot App with AWS Secrets and Argo CD

This project demonstrates how to deploy a Spring Boot application on Kubernetes using Argo CD, where secrets are dynamically fetched from AWS Secrets Manager at deployment time.

## Prerequisites

- Kubernetes cluster (Minikube, EKS, etc.)
- Argo CD installed on your cluster
- AWS CLI installed and configured with permissions to access AWS Secrets Manager
- Git repository to hold the manifests

## Steps

1. Clone this repository.

2. Update `deployment.yaml` if needed to add any additional environment variables for secrets.

3. Deploy the Argo CD ConfigMap to configure the secret-fetcher plugin:
   ```bash
   kubectl apply -f manifests/argocd-cm.yaml
