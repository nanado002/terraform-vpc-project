# Terraform AWS VPC Project

This project creates a VPC with public and private subnets, EC2 instances, and all required networking components.

## Architecture
- VPC: 10.0.0.0/16
- 2 Public Subnets
- 2 Private Subnets
- NAT Gateway for private subnet internet access
- Internet Gateway for public subnets
- Jump server in public subnet
- Private instance in private subnet

## Usage

1. Initialize Terraform:
   ```bash
   terraform init