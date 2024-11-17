# Cloud_Project
"This project leverages Azure Cloud for infrastructure, Terraform for IaC, GitHub Actions for CI pipelines, Helm Charts for Kubernetes deployments, and ArgoCD for GitOps-based continuous delivery."

## Deploying Application on AKS using Terraform

This repository automates the deployment of a containerized application in **Azure Kubernetes Service (AKS)** using **Terraform**.

### Steps:
1. **Infrastructure**: Terraform provisions AKS cluster and other Azure resources.
2. **Application Deployment**: The Kubernetes manifests deploy the application to the AKS cluster.

### Prerequisites:
- Azure CLI, Terraform, and Kubernetes CLI (kubectl) installed.
- Azure subscription with necessary permissions.

### Quick Start:
1. Configure `terraform.tfvars` with your Azure settings.
2. Run:
   ```bash
   terraform init
   terraform apply

## Use of Azure Blob storage :
Use of Azure blob to store .tfstate files


