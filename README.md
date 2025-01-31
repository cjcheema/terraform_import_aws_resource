# Terraform Import AWS Resources

This repository provides Terraform scripts to import existing AWS resources into Terraform state. It helps manage infrastructure as code (IaC) by allowing users to bring unmanaged AWS resources under Terraform control.

## Features

- Import existing AWS resources into Terraform

- Generate Terraform configurations for imported resources

- Maintain consistency between AWS infrastructure and Terraform state

## Prerequisites

Before using this repository, ensure you have the following:

- Terraform v1.x installed

- AWS CLI installed and configured with appropriate permissions

- AWS IAM Role/Access with permissions to describe and import resources

## Usage

* Clone the Repository

```bash
git clone https://github.com/cjcheema/terraform_import_aws_resource.git
cd terraform_import_aws_resource
```

* Initialize Terraform

```bash
terraform init
```

* Import AWS Resources

- Run import command manually. Example:

```bash

terraform import aws_instance.example i-0abcdef1234567890
```

- Replace i-0abcdef1234567890 with your actual AWS resource ID.



* Generate Terraform Configuration

Use terraform show -json or terraform state list to inspect the imported resources and manually create a .tf file.

```bash 
terraform show -json > imported_resources.json
```

* Plan and Apply Changes

```bash
terraform plan
terraform apply
```

## Files Overview

- provider.tf: Contain AWS Provider information
- terraform_resource_importer.tf: Defines AWS provider and resource structure.
- variables.tf: Defines sensitive variables for AWS configurations.


## Best Practices

* Always take a backup of your Terraform state before importing.
* Verify imported resource configurations and update .tf files accordingly.
* Use Terraform workspaces for managing multiple environments.


# Author

This project is created and maintained by Charanjit Singh.
* Email: charanjit.singh@outlook.in/charanjit.cheema@cjcheema.com
* Website: https://www.cjcheema.com
* LinkedIn: https://www.linkedin.com/in/cjcheema/

Feel free to connect for any questions, suggestions, or feedback.