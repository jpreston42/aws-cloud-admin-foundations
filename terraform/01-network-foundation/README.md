# 01 - Network Foundation (Terraform)

Goal: Build a minimal AWS VPC foundation with public/private segmentation and clear routing boundaries.

Planned resources:
- VPC
- Public subnet + route table + IGW
- Private subnet (no internet route initially)
- Outputs for verification

Progress to Date:

This repository currently implements a foundational AWS networking layer using Terraform, with a focus on reusable, security-aware infrastructure patterns.

Completed work includes:
- Configured Terraform with the AWS provider using modern AWS CLI SSO authentication (IAM Identity Center)
- Parameterized AWS region selection (currently targeting ca-west-1)
- Created a dedicated Virtual Private Cloud (VPC) with DNS support enabled
- Implemented public and private subnets within the VPC
- Attached an Internet Gateway to enable outbound connectivity
- Created a public route table with a default route to the Internet Gateway
- Associated the public subnet with the public route table
- Applied consistent resource tagging for environment, project, and ownership
- Refactored subnet availability zone selection to be configurable and reusable
- Validated infrastructure changes using terraform plan before applying
- Successfully deployed the network foundation using terraform apply
This work establishes a solid baseline for future additions such as security groups, NAT gateways, IAM roles, compute resources, and further automation.
