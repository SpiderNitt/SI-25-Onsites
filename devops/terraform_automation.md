# Cloud Infrastructure Automation Using Terraform on Azure or GCP

## Problem Statement

To ensure a scalable, maintainable, and production-ready deployment environment for a containerized microservices application, this problem statment focuses on automating cloud infrastructure provisioning using Terraform on either Microsoft Azure or Google Cloud Platform (GCP). The aim is to adopt Infrastructure as Code (IaC) principles to make infrastructure version-controlled, reproducible, and environment-specific, while seamlessly integrating into CI/CD pipelines.

---

## Objectives

### 1. Cloud Provider Setup

Choose a cloud platform:
- **Azure** using the `azurerm` provider
- **GCP** using the `google` provider

Set up secure authentication:
- **Azure:** Service principal or Azure CLI
- **GCP:** Service account key or gcloud CLI

---

### 2. Infrastructure as Code

Use Terraform to define and provision the following core infrastructure components as reusable modules:

#### Compute
- **GCP:** Compute Engine VMs or Google Kubernetes Engine (GKE)
- **Azure:** Virtual Machines or Azure Kubernetes Service (AKS)

#### Database
- **GCP:** Cloud SQL (PostgreSQL/MySQL)
- **Azure:** Azure Database for PostgreSQL/MySQL

#### Networking
- VPC (GCP) or VNet (Azure)
- Subnets, firewall rules, and network security groups (NSGs)

#### Storage
- **GCP:** Cloud Storage
- **Azure:** Blob Storage

---

### 3. State Management

- Configure a **remote backend** for secure Terraform state storage:
  - **GCP:** Google Cloud Storage (GCS)
  - **Azure:** Azure Blob Storage

- Enable **state locking** and **versioning** for safe collaboration and consistency.

---

### 4. Environment Separation

- Use **Terraform workspaces** or `.tfvars` files to manage different environments (e.g., staging, production).
- Tag all resources with metadata for:
  - Environment (dev/staging/prod)
  - Team ownership
  - Cost tracking and governance

---

### 5. CI/CD Integration

- Integrate Terraform workflows into CI/CD tools such as:
  - GitHub Actions
  - GitLab CI
  - Jenkins

- Automate:
  - `terraform init`, `plan`, and `apply` steps on push to `main` or `develop`
  - Approval gates for production applies
  - Ephemeral environments for feature branches with auto-destroy capabilities

---

### 6. Secrets and Configuration Management

- Inject secrets securely using:
  - **Azure:** Azure Key Vault
  - **GCP:** Secret Manager
  - **CI/CD tools:** GitHub Secrets, GitLab CI/CD Variables, etc.

---

### 7. Documentation

Provide a complete `README.md` including:
- Authentication setup and prerequisites
- Terraform command usage (`init`, `plan`, `apply`, `destroy`)
- Codebase structure (modules, variables, outputs)
- Environment-specific deployment instructions

---

## Expected Deliverables

- A modular, reusable Terraform codebase targeting **Azure** or **GCP**
- Remote backend setup for secure and versioned Terraform state
- CI/CD pipeline integration for infrastructure automation
- Isolated and tagged environments for staging and production
- Full documentation for setup, usage, and contribution
