# Lab No 12: Cloud Computing

**Submitted By:** Rabeea Fatima  
**Registration No:** 2023-BSE-049  
**Section:** B  
**Subject:** Cloud Computing  

---

## Project Overview
This laboratory exercise focuses on modularizing Terraform code, utilizing different types of provisioners (remote-exec and file), and implementing Terraform modules for reusable infrastructure components.

## Tasks Performed

### Task 0 & 01: Code Organization and File Structure
* **Authentication:** Set up and authenticated the GitHub CLI within the Codespace environment.
* **Modularization:** Organized Terraform code by splitting a monolithic configuration into specialized files:
    * `variables.tf`: For input variable declarations.
    * `outputs.tf`: For defining information to be shared after deployment.
    * `locals.tf`: For local value definitions.
    * `terraform.tfvars`: For assigning values to variables.
    * `main.tf`: For core resource definitions.
* **Automated Setup:** Created an `entry-script.sh` to automate Nginx installation on EC2.
* **Security:** Generated an SSH Ed25519 key pair for secure instance access.

### Task 02: Remote-Exec Provisioner
* Modified the `aws_instance` resource to use the `remote-exec` provisioner.
* Configured the provisioner to connect to the instance via SSH using the generated private key.
* Successfully tested the deployment by verifying the Nginx default page in a web browser.

### Task 03: File Provisioner
* Implemented the `file` provisioner to transfer local files (like `entry-script.sh`) directly to the EC2 instance.
* Integrated the file transfer into the deployment lifecycle and verified the script's presence on the remote machine.

### Task 04: Terraform Modules
* **Module Creation:** Created a reusable module for VPC management including Subnets and Internet Gateways.
* **Module Usage:** Replaced inline resource definitions in the root `main.tf` with module calls.
* **Encapsulation:** Practiced passing variables into modules and retrieving output values from them.
* **Verification:** Re-deployed the infrastructure using the modular approach and verified that all networking components were correctly provisioned.

## Cleanup
* Executed `terraform destroy` to remove all AWS resources and verified the cleanup process.
