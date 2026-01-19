# Exam Lab: Cloud Computing

**Submitted By:** Rabeea Fatima  
**Registration No:** 2023-BSE-049  
**Section:** B  
**Subject:** Cloud Computing  
**Submitted To:** Sir M. Shoaib  

---

## Question 1: AWS IAM Setup Using AWS CLI
[cite_start]This task involved setting up an IAM infrastructure via the AWS CLI and verifying it through the AWS Management Console[cite: 39, 40].

* [cite_start]**Group Creation:** Created an IAM group named `Software Engineering`[cite: 41, 46].
* [cite_start]**User Management:** * Created an IAM user named `RabeeaFatima`[cite: 65, 67].
    * [cite_start]Added the user to the `Software Engineering` group[cite: 84, 85].
* [cite_start]**Policy Attachment:** * Identified the `AdministratorAccess` managed policy ARN[cite: 101, 105].
    * [cite_start]Attached the `AdministratorAccess` policy to the `Software Engineering` group[cite: 115].
* [cite_start]**Verification:** Confirmed the user, group, and assigned permissions within the AWS Console[cite: 120, 153].

## Question 2: Terraform Infrastructure Deployment
[cite_start]Deployed a simple AWS environment featuring an EC2 instance running Nginx over HTTPS using Terraform[cite: 160, 161].

* [cite_start]**Provider Configuration:** Set the AWS provider for the `me-central-1` region[cite: 162, 173].
* [cite_start]**Networking:** * Provisioned a VPC and a public subnet[cite: 211, 217].
    * [cite_start]Configured an Internet Gateway and a default route table for external access[cite: 227, 234].
* [cite_start]**Security:** * Dynamically discovered the public IP of the deployment environment to restrict SSH access[cite: 243, 244].
    * [cite_start]Configured a Security Group allowing SSH (Port 22), HTTP (Port 80), and HTTPS (Port 443)[cite: 253, 277].
* [cite_start]**Compute & Automation:** * Generated an SSH key pair (`id_ed25519`) for instance access[cite: 278, 281].
    * [cite_start]Launched an EC2 instance with an automation script (`entry-script.sh`)[cite: 301, 317].
    * [cite_start]**User Data Script:** Automated system updates, Nginx installation, and the generation of a self-signed SSL certificate for HTTPS[cite: 325, 332].
* [cite_start]**Validation:** Verified successful deployment by accessing the Nginx landing page over HTTPS via the server's public IP[cite: 27].

## Question 3: Ansible Configuration Management
[cite_start]Used Ansible to reconfigure the EC2 instance provisioned in Question 2[cite: 28].

* [cite_start]**Inventory & Config:** Created a `hosts` inventory file and an `ansible.cfg` to manage the target EC2 instance[cite: 28].
* [cite_start]**Playbook Execution:** * Developed a playbook to update system packages[cite: 28].
    * [cite_start]Implemented logic to stop and uninstall Nginx if present, preparing the server for further configuration (e.g., Apache HTTPD)[cite: 29].
* [cite_start]**Connectivity:** Verified successful communication with the instance using the Ansible `ping` module[cite: 29, 30].

## Cleanup
* [cite_start]**Infrastructure Destruction:** Executed `terraform destroy` to remove all AWS networking and compute resources[cite: 30].
* [cite_start]**IAM Cleanup:** Deleted the created IAM user and group to return the environment to its initial state[cite: 30].
