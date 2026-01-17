# Lab No 14: Cloud Computing

[cite_start]**Submitted By:** Rabeea Fatima [cite: 51]  
[cite_start]**Registration No:** 2023-BSE-049 [cite: 52]  
**Section:** B  
[cite_start]**Subject:** Cloud Computing [cite: 53]  

---

## Project Overview
This laboratory exercise focuses on automating infrastructure deployment and configuration using **Terraform** and **Ansible**. [cite_start]The tasks cover setting up an Ansible environment, managing static and dynamic inventories, deploying Nginx web servers, handling SSL certificates, and orchestrating Docker-based applications like Gitea. [cite: 120, 204, 257, 44, 45, 46]

## Tasks Performed

### Task 00: Lab Setup & Environment Verification
* [cite_start]Authenticated with GitHub CLI and connected to a Codespace via SSH. [cite: 67, 96]
* [cite_start]Verified installed tools: AWS CLI, Terraform, and identified that Ansible was not yet installed. [cite: 109, 111, 113]
* [cite_start]Confirmed AWS identity and account connectivity. [cite: 116]

### Task 01: SSH Key Generation & Initial Terraform Apply
* [cite_start]Generated an Ed25519 SSH key pair for secure instance access. [cite: 126]
* [cite_start]Configured `terraform.tfvars` with VPC, subnet, and instance settings. [cite: 154]
* [cite_start]Initialized Terraform and deployed two EC2 instances. [cite: 169, 187]

### Task 02 & 03: Ansible Installation & Inventory Management
* [cite_start]Installed `ansible-core` using `pipx`. [cite: 207]
* [cite_start]Created a static `hosts` inventory file with public IPs of the EC2 instances. [cite: 234]
* [cite_start]Scaled infrastructure to three instances and reorganized the inventory into groups (`ec2` and `droplet`). [cite: 259, 303]
* [cite_start]Verified connectivity to all managed hosts using the Ansible `ping` module. [cite: 319, 358]

### Task 04 & 05: Ansible Configuration & Nginx Playbook
* [cite_start]Configured a global `ansible.cfg` to disable host key checking. [cite: 26, 38]
* [cite_start]Created and executed a playbook (`my-playbook.yaml`) to install and start Nginx on the target groups. [cite: 29]
* [cite_start]Verified the Nginx default landing page via the server's public IP. [cite: 32, 41]

### Task 06 & 07: Advanced Web Deployment
* [cite_start]**SSL Management:** Implemented a play to manage SSL certificates via Ansible. [cite: 44]
* [cite_start]**Templates:** Deployed a PHP front-end using Jinja2 templates for Nginx configuration. [cite: 44]

### Task 08 & 09: Container Orchestration (Docker & Gitea)
* [cite_start]Provisioned Docker and Docker Compose on EC2 instances using Ansible. [cite: 44]
* [cite_start]Deployed a Gitea stack using a Docker Compose file managed by Ansible. [cite: 45]
* [cite_start]Updated AWS Security Groups via Terraform to allow traffic on port 3000 for Gitea access. [cite: 45]

### Task 10: Terraform-Ansible Integration
* [cite_start]Automated the execution of Ansible playbooks directly from Terraform using the `null_resource` provisioner. [cite: 45]
* [cite_start]Implemented a "wait" play to ensure instance readiness before Ansible configuration begins. [cite: 45]

### Task 11 & 12: Dynamic Inventory & Filtering
* [cite_start]Configured the `aws_ec2` plugin for dynamic inventory management. [cite: 46]
* [cite_start]Implemented inventory filtering to group instances by tags (e.g., `dev`, `prod`) and instance types (e.g., `t3.micro`). [cite: 46, 47]
* [cite_start]Updated `ansible.cfg` to use the dynamic inventory by default. [cite: 47]

## Cleanup
* [cite_start]Destroyed all deployed AWS resources to avoid unnecessary charges and verified the state cleanup. [cite: 47]
