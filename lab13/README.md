# Lab No 13: Cloud Computing

[cite_start]**Submitted By:** Rabeea Fatima [cite: 1]
[cite_start]**Registration No:** 2023-BSE-049 [cite: 1]
[cite_start]**Section:** B [cite: 1]
[cite_start]**Subject:** Cloud Computing [cite: 1]

---

## Project Overview
[cite_start]This laboratory exercise focuses on advanced IAM management using Terraform, including the creation of groups, users, policy attachments, and login profiles[cite: 2]. [cite_start]Additionally, it covers the implementation of remote state management using Amazon S3 and the automation of multiple user creations from external CSV files[cite: 3].

## Tasks Performed

### Task 0: GitHub CLI & Codespace Setup
* [cite_start]Set up and authenticated the GitHub CLI within a Codespace environment[cite: 1].

### Task 01: IAM Group Management
* [cite_start]Created the initial project structure and the main Terraform configuration[cite: 2].
* [cite_start]Configured the AWS provider in `main.tf`[cite: 2].
* [cite_start]Initialized and applied the configuration to create an IAM group[cite: 2].
* [cite_start]Verified the group creation in the AWS Console[cite: 2].

### Task 02: IAM User and Group Membership
* [cite_start]Updated `main.tf` to include an IAM user resource[cite: 2].
* [cite_start]Added the user to the previously created IAM group[cite: 2].
* [cite_start]Verified user deployment and group membership in AWS[cite: 2].

### Task 03: Policy Attachments
* [cite_start]Updated the Terraform configuration to attach specific policies to the IAM group[cite: 2].
* [cite_start]Applied changes and verified policy inheritance for group members in the AWS Console[cite: 2].

### Task 04: IAM Login Profiles
* [cite_start]Created a `variables.tf` file for modular configuration[cite: 2].
* [cite_start]Developed a bash script (`create-login-profile.sh`) to handle login profile creation[cite: 2].
* [cite_start]Utilized a `null_resource` provisioner in `main.tf` to execute the script during deployment[cite: 2].
* [cite_start]Verified the login profile functionality in AWS[cite: 2].

### Task 05: Access Key Generation
* [cite_start]Configured Terraform to generate IAM access keys and defined outputs for them[cite: 3].
* [cite_start]Observed the storage of secrets within the Terraform state file[cite: 3].
* [cite_start]Verified the active access keys in the AWS Console[cite: 3].

### Task 06: Remote State with Amazon S3
* [cite_start]Created an S3 bucket via the AWS Console to act as a remote backend[cite: 3].
* [cite_start]Configured `main.tf` to use the S3 backend for state storage[cite: 3].
* [cite_start]Reinitialized Terraform to migrate the local state to the S3 bucket[cite: 3].
* [cite_start]Verified state file updates in S3 after resource modifications and destruction[cite: 3].

### Task 07: Bulk User Creation from CSV
* [cite_start]Created a `users.csv` file containing details for multiple users[cite: 3].
* [cite_start]Implemented a `locals.tf` file to parse the CSV data[cite: 3].
* [cite_start]Updated `main.tf` to dynamically create multiple users based on the CSV input[cite: 3].
* [cite_start]Verified all users, their group memberships, and access keys in the AWS Console[cite: 4].

## Cleanup
* [cite_start]Destroyed all resources and verified that the remote state file in S3 accurately reflected the changes[cite: 3, 4].
