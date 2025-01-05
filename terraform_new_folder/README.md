# terraform-aws-vpc-network

This repository sets up a simple AWS VPC with two subnets, an internet gateway, and a route table. It uses Terraform to define and deploy these resources in the `us-east-1` region.

## Prerequisites

- Terraform `>= 1.1.0`
- AWS credentials configured locally (e.g., via the AWS CLI or environment variables)
- An ARM-compatible Terraform build if you’re on an Apple Silicon Mac (M1/M2). Make sure you’re running a native ARM shell.

## How to Use

1. **Clone** this repository.
2. **Navigate** into the project directory.
3. Run `terraform init` to download required providers.
4. Run `terraform plan` to see the resources to be created.
5. Run `terraform apply` to create the VPC, subnets, and other resources.
6. When finished, run `terraform destroy` to remove all resources.

## Notes

- The `main.tf` file contains the AWS provider configuration and the resource definitions.
- By default, the VPC uses `192.168.0.0/16` and creates two subnets in `us-east-1a` and `us-east-1b`.
- The route table includes a default route to the internet gateway for outbound traffic.

Feel free to adjust CIDR blocks, availability zones, and other settings in the `main.tf` file as needed.
