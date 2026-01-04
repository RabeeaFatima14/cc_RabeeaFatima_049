# Lab No 11: Cloud Computing

[cite_start]**Submitted By:** Rabeea Fatima [cite: 1]
[cite_start]**Registration No:** 2023-BSE-049 [cite: 1]
[cite_start]**Section:** B [cite: 1]
[cite_start]**Subject:** Cloud Computing [cite: 1]

---

## Project Overview
[cite_start]This laboratory exercise focuses on advanced Terraform concepts, specifically managing various types of variables, validation, sensitive data, and deploying a functional AWS infrastructure including a VPC, subnets, and an EC2 instance with Nginx. [cite: 5, 6]

## Tasks Performed

### Task 0 & 01: Setup and Basic Variables
* [cite_start]**Authentication:** Set up and authenticated the GitHub CLI within a Codespace environment. [cite: 1]
* [cite_start]**Provider Configuration:** Created `main.tf` to define the AWS provider and initialized the workspace. [cite: 2]
* [cite_start]**Variable Management:** Practiced defining variables and outputs, using default values, exporting environment variables, and overriding values using `terraform.tfvars` and the `-var` flag. [cite: 2]

### Task 02: Validation and Security
* [cite_start]**Variable Validation:** Implemented custom validation rules for variables like `subnet_cidr_block` and tested validation failures. [cite: 3]
* [cite_start]**Sensitive Data:** Created sensitive variables (e.g., `api_session_token`) and observed how Terraform handles sensitive outputs. [cite: 3]
* [cite_start]**Ephemeral Variables:** Configured variables as ephemeral to ensure they are hidden from the Terraform state file. [cite: 3]

### Task 03, 04 & 05: Project-Level Variables and Collections
* [cite_start]**Locals and Outputs:** Created a `local.tf` file to manage local values and project-level variables. [cite: 4]
* [cite_start]**Complex Data Types:** Implemented Maps and Objects within `main.tf` and populated them via `terraform.tfvars`. [cite: 5]
* [cite_start]**Collections and Mutation:** Experimented with lists, tuples, and sets, performing mutations via local values and comparison outputs. [cite: 5]

### Task 06 & 07: Dynamic Values and Workspace Safety
* [cite_start]**Dynamic Types:** Tested the `any` type variable with various inputs including strings, numbers, lists, and maps. [cite: 5]
* [cite_start]**Null Handling:** Practiced using null variables and merging tags in `locals.tf`. [cite: 5]
* [cite_start]**Git Integration:** Created a `.gitignore` file to prevent sensitive Terraform files from being tracked in version control. [cite: 5]

### Task 08 & 09: Real Infrastructure Deployment
* [cite_start]**Networking:** Built a real AWS infrastructure by defining and deploying a VPC, Subnet, Internet Gateway, and a custom Route Table. [cite: 5, 6]
* [cite_start]**Route Association:** Associated the Route Table with the subnet and updated the default route table to allow external traffic. [cite: 6]
* **Compute and Security:**
    * [cite_start]Defined variables for security groups and key pairs. [cite: 6]
    * [cite_start]Configured security group rules based on the public IP of the Codespace. [cite: 6]
    * [cite_start]Launched an EC2 instance and used `user_data` to automate the installation of Nginx. [cite: 7]

### Cleanup
* [cite_start]Performed a complete resource cleanup to ensure all AWS resources were destroyed after the lab. [cite: 7]
