# Terraform Fundamentals - Google Cloud Infrastructure as Code

This repository demonstrates how to use Terraform to create and manage Google Cloud infrastructure as code. The project implements a simple VM instance creation in Google Cloud Platform using Terraform configuration files.

## Overview

Terraform enables you to safely and predictably create, change, and improve infrastructure. It is an open source tool that codifies APIs into declarative configuration files that can be shared among co-workers, treated as code, edited, reviewed, and versioned.

## Prerequisites

Before getting started, ensure you have:
- A Google Cloud Platform account with billing enabled
- Access to Google Cloud Console or Google Cloud SDK installed locally
- Terraform installed on your local machine (or use Cloud Shell which has it pre-installed)

## Setup Instructions

### 1. Install Terraform (Skip if using Google Cloud Shell)

If you're not using Google Cloud Shell (which comes with Terraform pre-installed), download and install Terraform:
- Visit [Terraform's download page](https://www.terraform.io/downloads.html)
- Download the appropriate version for your operating system
- Extract the downloaded file and move the terraform binary to a directory included in your system's PATH

Verify the installation:
```bash
terraform --version
```

### 2. Clone this Repository

```bash
git clone https://github.com/YOUR_USERNAME/terraform-gcp-fundamentals.git
cd terraform-gcp-fundamentals
```

### 3. Authenticate with Google Cloud

If working locally:
```bash
gcloud auth application-default login
```

### 4. Initialize Terraform

```bash
terraform init
```

### 5. Create an Execution Plan

```bash
terraform plan
```

### 6. Apply Changes

```bash
terraform apply
```
When prompted, type `yes` to confirm and create the resources.

### 7. Verify Resources

You can verify that your VM instance was created by checking the Google Cloud Console under Compute Engine > VM instances.

Alternatively, use the command:
```bash
terraform show
```

### 8. Clean Up Resources

When you're done, you can destroy the created resources:
```bash
terraform destroy
```
When prompted, type `yes` to confirm.

## Project Structure

```
├── README.md           # This file
├── instance.tf         # Main Terraform configuration file
├── terraform.tfstate   # State file (generated after terraform apply)
└── .gitignore          # Git ignore file
```

## Key Terraform Concepts

- **Configuration**: The set of files used to describe infrastructure in Terraform
- **Initialization**: The `terraform init` command downloads and installs provider plugins
- **Execution Plan**: The `terraform plan` command shows what actions Terraform will take
- **Apply Changes**: The `terraform apply` command creates or updates infrastructure
- **State**: Terraform keeps track of resource IDs in the terraform.tfstate file

## Benefits of Infrastructure as Code

1. **Version Control**: Infrastructure definitions can be versioned and tracked
2. **Reusability**: Code can be shared and reused across projects
3. **Consistency**: Ensures consistent infrastructure deployments
4. **Automation**: Reduces manual intervention and human error
5. **Documentation**: The code itself serves as documentation

## Contributing

Feel free to fork this repository and submit pull requests to contribute.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
