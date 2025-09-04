# Terraform Project Command Reference

## Complete Command History

### 1. Initial Terraform Setup
\\\ash
# Initialize Terraform
terraform init

# Plan the infrastructure
terraform plan

# Apply the configuration (first attempt - failed due to key pair)
terraform apply

# Destroy failed deployment
terraform destroy

# Apply again with fixed configuration
terraform apply

# Verify successful deployment
terraform show
\\\

### 2. GitHub Repository Setup
\\\ash
# Initialize Git repository
git init

# Create .gitignore file for Terraform
@\\\"
# Terraform files
.terraform/
*.tfstate
*.tfstate.backup
*.tfvars
.terraform.lock.hcl

# Sensitive files
*.pem
*.key
*.secret
*.priv

# IDE files
.vscode/
.idea/
*.swp
*.swo

# OS files
.DS_Store
Thumbs.db

# Logs
*.log
\\\"@ | Out-File -FilePath .gitignore -Encoding UTF8

# Create README.md
@\\\"
# Terraform VPC Project

## Description
Terraform configuration for AWS VPC infrastructure with public and private subnets.

## Infrastructure Components
- VPC with public and private subnets
- Internet Gateway
- NAT Gateway
- Route Tables
- EC2 Instances
- Security Groups

## Usage
\\\\\\\\\ash
terraform init
terraform plan
terraform apply
\\\\\\\\\

## Requirements
- Terraform >= 1.0
- AWS CLI configured
\\\"@ | Out-File -FilePath README.md -Encoding UTF8

# Check files to be tracked
git status

# Add all files to staging
git add .

# Commit the code
git commit -m \\\"Initial commit: Complete Terraform VPC infrastructure with VPC, subnets, routing, EC2 instances, and security groups\\\"

# Configure git user (if not done already)
git config --global user.name \\\"Your Name\\\"
git config --global user.email \\\"your.email@example.com\\\"
\\\

### 3. GitHub Repository Creation & Push
\\\ash
# Remove any incorrect remote (if exists)
git remote remove origin

# Add correct GitHub remote (HTTPS version)
git remote add origin https://github.com/nanado002/terraform-vpc-project.git

# Rename branch to main
git branch -M main

# Push to GitHub
git push -u origin main

# If using SSH instead:
git remote remove origin
git remote add origin git@github.com:nanado002/terraform-vpc-project.git
git push -u origin main
\\\

### 4. Verification Commands
\\\ash
# Verify git status
git status

# Check remote configuration
git remote -v

# View commit history
git log --oneline

# Check what's pushed to remote
git push --dry-run

# Verify files are tracked
git ls-files
\\\

### 5. Terraform Management Commands
\\\ash
# Format Terraform code
terraform fmt

# Validate configuration
terraform validate

# Check current state
terraform state list

# Destroy infrastructure (when needed)
terraform destroy

# Plan specific changes
terraform plan -out=tfplan

# Apply specific plan
terraform apply tfplan
\\\

### 6. Troubleshooting Commands Used
\\\ash
# When key pair error occurred:
terraform destroy

# After fixing key pair in main.tf:
terraform apply

# When remote URL had error:
git remote remove origin
git remote add origin https://github.com/nanado002/terraform-vpc-project.git
\\\

## Quick Reference Cheat Sheet

### Terraform Essentials
\\\ash
terraform init      # Initialize Terraform
terraform plan      # Preview changes
terraform apply     # Apply changes (yes)
terraform destroy   # Destroy infrastructure
terraform fmt       # Format code
terraform validate  # Validate configuration
\\\

### Git Essentials
\\\ash
git init            # Initialize git repository
git add .           # Stage all files
git commit -m \"message\" # Commit changes
git status          # Check status
git log --oneline   # View commit history
git remote add origin https://github.com/username/repo.git # Add remote
git push -u origin main # Push to GitHub
git remote -v       # View remote URLs
\\\

### Common Fixes
\\\ash
# If remote URL is wrong:
git remote remove origin
git remote add origin correct_url

# If authentication fails:
# Use Personal Access Token instead of password
# Or switch to SSH: git@github.com:username/repo.git

# If Terraform fails:
terraform destroy   # Clean up
# Fix configuration
terraform apply     # Try again
\\\

## Project Structure
\\\
terraform-vpc-project/
├── main.tf          # Main infrastructure code
├── variables.tf     # Variable definitions
├── outputs.tf       # Output values
├── providers.tf     # Provider configuration
├── .gitignore      # Git ignore rules
├── README.md       # Project documentation
├── COMMANDS.md     # This reference file
└── terraform.tfstate # (ignored) State file
\\\

## Authentication Notes
- **HTTPS**: Use GitHub username + Personal Access Token
- **SSH**: Requires SSH key setup (recommended)
- **GitHub CLI**: Use \gh auth login\ for easy authentication

---

*Last Updated: *
