# Lab No 8: Cloud Computing

**Submitted By:** Rabeea Fatima  
**Registration No:** 2023-BSE-049  
**Section:** B  

---

## Project Overview
[cite_start]This laboratory exercise covers the foundational steps for setting up and managing resources within Amazon Web Services (AWS)[cite: 1, 6]. [cite_start]The tasks include account creation, Identity and Access Management (IAM) configuration, Virtual Private Cloud (VPC) inspection, and the deployment of a Gitea instance using Docker on an EC2 virtual machine[cite: 2, 4].

## Tasks Performed

### Task 01: AWS Account Setup
* [cite_start]Created a new AWS account via the signup page[cite: 1, 2].
* [cite_start]Accessed the AWS Management Console home page[cite: 2].
* [cite_start]Enabled the required AWS region for resource deployment[cite: 2].

### Task 02: IAM User Management
* [cite_start]Created an IAM admin user and a secondary user named `Lab8User` with console access[cite: 2, 17].
* [cite_start]Configured user permissions and reviewed settings[cite: 3, 21].
* [cite_start]Downloaded the `.csv` credentials file for secure access[cite: 3, 24].
* [cite_start]Verified access by signing in with the newly created user `Lab8Rabeea`[cite: 3, 27].

### Task 03: VPC Resource Inspection
* [cite_start]Accessed the VPC console to inspect network resources[cite: 3, 30].
* Viewed and verified the following components:
    * [cite_start]VPC List [cite: 4, 31]
    * [cite_start]Subnets [cite: 4, 32]
    * [cite_start]Route Tables [cite: 4]
    * [cite_start]Network ACLs [cite: 4]
    * [cite_start]VPC Dashboard [cite: 4]

### Task 04: EC2 Deployment & Gitea Setup
* [cite_start]**Instance Launch:** Launched an EC2 instance by configuring the AMI, instance type, and network settings[cite: 4].
* [cite_start]**Security:** Configured storage and set up a key pair for secure SSH access[cite: 4].
* [cite_start]**Connectivity:** Connected to the instance via SSH using the command prompt[cite: 4].
* [cite_start]**Docker Installation:** Installed Docker and Docker Compose on the EC2 instance[cite: 4].
* **Environment Setup:**
    * [cite_start]Added `ec2-user` to the Docker group[cite: 4].
    * [cite_start]Created and edited a `compose.yaml` file on the instance[cite: 4].
* **Gitea Deployment:**
    * [cite_start]Deployed Gitea using Docker Compose[cite: 4].
    * [cite_start]Updated inbound security group rules to allow traffic to Gitea[cite: 4].
    * [cite_start]Completed Gitea initial configuration and verified repository creation[cite: 4].

### Task 05: Resource Cleanup
* [cite_start]Terminated the EC2 lab machine instance[cite: 4].
* [cite_start]Deleted the associated security groups[cite: 5].
* [cite_start]Removed the IAM users created during the lab[cite: 5].
