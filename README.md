# Cloud_Project
"This project leverages Azure Cloud for infrastructure, Terraform for IaC, GitHub Actions for CI pipelines, Helm Charts for Kubernetes deployments, and ArgoCD for GitOps-based continuous delivery."

## Deploying Application on AKS using Terraform

This repository automates the deployment of a containerized application in **Azure Kubernetes Service (AKS)** using **Terraform**.
We are also using Helm chart for package manager and ArgoCD for continous deployment.

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

Azure Blob Storage: Azure Blob Storage is a service designed to store large amounts of unstructured data, such as text or binary data. It is highly scalable, secure, and accessible, making it ideal for backups and state management in infrastructure as code tools like Terraform.

## Why Use Azure Blob Storage for .tfstate?
Centralized State Management:

Terraform's state file (.tfstate) records the current state of your infrastructure. Storing it in Azure Blob Storage allows teams to work collaboratively and ensures consistent state management.
Versioning and Backup:

Azure Blob Storage supports blob snapshots, which can version your .tfstate files for recovery in case of accidental changes or corruption.
Locking Mechanism:

When integrated with Terraform, Azure Blob Storage enables state locking to prevent simultaneous state file modifications by multiple users.
Security:

You can secure the .tfstate file using Azure RBAC (Role-Based Access Control) and encryption at rest.
Access can be further restricted using Azure Private Endpoints.

## Advantages of Using Azure Blob Storage:
Reliability: Azure ensures high availability with replication options like LRS, ZRS, or GRS.
Scalability: Can handle growing infrastructure needs without requiring reconfiguration.
Integration: Works seamlessly with other Azure services and Terraform.

## Helm Chart 
A Helm Chart is like a recipe or a blueprint that describes how to deploy an application (or a set of applications) on Kubernetes. It contains all the configuration files and templates needed to set up the application.

## ArgoCD
ArgoCD is a declarative, GitOps continuous delivery tool for Kubernetes. It provides a platform for automating the deployment of Kubernetes applications and ensuring that the desired application state defined in Git is synchronized with the actual state in the cluster.

# Why Use Helm Charts?
1.Simplifies Kubernetes Deployments:
Instead of writing lengthy YAML files, you use a Helm Chart that bundles all the Kubernetes resources (like deployments, services, ingress) in one place.

2.Reusable:
You can reuse the same chart to deploy multiple instances of the same application, e.g., for dev, test, and prod environments.

3.Customization:
Charts allow configuration options. For example, you can specify different resource limits or environment variables without changing the core files.

4.Version Control:
Helm tracks versions of your deployed applications. If something goes wrong, you can roll back to a previous version.



