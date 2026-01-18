# Open-Ended Lab: Multi-Tier Web Architecture on AWS

**Submitted By:** Rabeea Fatima  
**Registration No:** 2023-BSE-049  
**Section:** B  
**Session:** 2023-27  
**Semester:** 5th  
**Instructor:** Sir M. Shoaib  

---

## Project Overview
This project implements a **production-grade multi-tier web architecture** on AWS using Infrastructure as Code (Terraform) and Configuration Management (Ansible). The system is designed for high availability and features automatic load balancing with a zero-downtime architecture.

### Key Features
* **Automated Infrastructure Provisioning:** Single-command deployment using Terraform.
* **Load Balancing:** Nginx reverse proxy distributing traffic across multiple backend servers.
* **High Availability:** Automatic failover to backup servers ensuring service continuity.
* **Configuration Management:** Ansible roles for consistent and repeatable server setup.
* **Infrastructure as Code (IaC):** Fully version-controlled and reproducible infrastructure.
* **Zero-Downtime:** Backend failures do not affect overall service availability.

## Technologies Used
| Component | Technology |
| :--- | :--- |
| **Infrastructure** | Terraform, AWS (VPC, EC2, Security Groups) |
| **Configuration** | Ansible (Roles, Playbooks, Templates) |
| **Load Balancer** | Nginx (Reverse Proxy with Upstream) |
| **Web Servers** | Apache HTTPD |
| **Operating System** | Amazon Linux 2023 |
| **Automation** | Terraform `null_resource`, Bash Scripting |

---

## Project Repository
[View Repository on GitHub](https://github.com/RabeeaFatima14/CC_RabeeaFatima_049_LabProject)

---

## Implementation Tasks

### Task 0 & 01: Environment & Provider Setup
* Authenticated GitHub CLI and set up the Codespace environment.
* Initialized Terraform and configured the AWS provider.

### Task 02: Networking Infrastructure
* Created a custom VPC and Subnet.
* Configured an Internet Gateway and Route Tables for public access.
* Implemented Security Groups for both the Frontend (Nginx) and Backend (Apache) tiers.

### Task 03: Compute Resources
* Deployed the Frontend EC2 instance (Load Balancer).
* Deployed multiple Backend EC2 instances (Web Servers).
* Configured an `outputs.tf` file to track resource IDs and Public IPs.
* Validated SSH connectivity to the deployed instances.

### Task 04: Ansible Setup
* Established a structured Ansible directory.
* Configured `ansible.cfg` to optimize connection settings.
* Created a static inventory file mapping the EC2 instances into groups.
* Verified connectivity using the Ansible `ping` module.

### Task 05: Backend Role (Apache)
* Developed an Ansible role to install and configure Apache HTTPD.
* Deployed distinct content to each backend server to verify load balancing.
* Verified individual backend availability via browser tests.

### Task 06: Frontend Role (Nginx)
* Developed an Ansible role for Nginx.
* Configured Nginx as a reverse proxy with an `upstream` block for load balancing.
* Implemented access logging and verified the upstream configuration.

### Task 07: Full Orchestration
* Created a master Ansible playbook to execute all roles.
* Integrated Ansible with Terraform using `null_resource` for a seamless "one-click" deployment.
* Conducted final testing to ensure the Frontend successfully distributes traffic across all active Backends.

---

## Cleanup
* Used `terraform destroy` to remove all AWS resources, ensuring no unnecessary costs were incurred.
