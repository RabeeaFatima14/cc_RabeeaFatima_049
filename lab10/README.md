# Lab No 10: Cloud Computing

[cite_start]**Submitted By:** Rabeea Fatima [cite: 6, 8]  
[cite_start]**Registration No:** 2023-BSE-049 [cite: 8]  
[cite_start]**Section:** B [cite: 9]  
[cite_start]**Subject:** Cloud Computing [cite: 9]  

---

## Project Overview
This laboratory exercise focuses on Infrastructure as Code (IaC) using Terraform. [cite_start]It covers the setup of GitHub CLI and AWS CLI within a Codespace, the installation and initialization of Terraform, and the management of AWS resources such as VPCs and subnets through Terraform configurations. [cite: 1, 2, 3]

## Tasks Performed

### Task 01: GitHub CLI Codespace Setup & Authentication
* [cite_start]Installed the GitHub CLI. [cite: 12]
* [cite_start]Authenticated the GitHub CLI for use with Codespaces. [cite: 13]
* [cite_start]Listed available Codespaces and established a connection via SSH. [cite: 14, 15]

### Task 02: Tool Installation & Provider Setup
* [cite_start]**AWS CLI:** Installed and configured the AWS CLI within the Codespace shell and verified connectivity. [cite: 18, 19, 20, 21]
* [cite_start]**Terraform CLI:** Installed the Terraform CLI. [cite: 22, 23]
* [cite_start]**Configuration:** * Created a `main.tf` file using Vim to define the provider. [cite: 25]
    * [cite_start]Initialized Terraform to download necessary providers. [cite: 26]
    * [cite_start]Inspected the `.terraform.lock.hcl` file and the `.terraform/` directory. [cite: 27, 28]

### Task 03: VPC & Subnet Management
* [cite_start]Modified `main.tf` to define VPC and Subnet resources. [cite: 3, 4]
* [cite_start]Applied the configuration to create resources in AWS. [cite: 4]
* [cite_start]Verified the newly created resources using AWS CLI commands. [cite: 4]

### Task 04: Data Sources, Targeted Destroy, and Tagging
* [cite_start]Utilized **Data Sources** to fetch existing AWS information. [cite: 4]
* [cite_start]Performed a **Targeted Destroy** to remove a specific resource without affecting others. [cite: 4]
* [cite_start]Refreshed the state and re-applied configurations. [cite: 4]
* [cite_start]Implemented **Resource Tagging** and practiced modifying tags (e.g., removing `vpc_env = "dev"`) followed by re-planning and applying changes. [cite: 4]

### Task 05: State File Inspection
* [cite_start]Inspected Terraform state files (`terraform.tfstate`) before and after resource destruction. [cite: 4]
* [cite_start]Used Terraform state commands to list resources and show full attributes of managed infrastructure. [cite: 4]

### Task 06: Outputs & Reporting
* [cite_start]Defined **Outputs** in `main.tf` to extract and display specific resource attributes (like IDs or IPs) after deployment. [cite: 4]
* [cite_start]Verified output reporting in the terminal. [cite: 4]

### Final Cleanup
* [cite_start]Destroyed all remaining resources to ensure no unnecessary AWS charges. [cite: 4]
* [cite_start]Deleted local state files as part of the final cleanup process. [cite: 4]
