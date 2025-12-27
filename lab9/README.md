# Lab No 9: Cloud Computing

[cite_start]**Submitted By:** Rabeea Fatima [cite: 9]
[cite_start]**Registration No:** 2023-BSE-049 [cite: 9]
[cite_start]**Section:** B [cite: 10]
[cite_start]**Subject:** Cloud Computing [cite: 10]

---

## Project Overview
[cite_start]This laboratory exercise focuses on using the GitHub CLI and AWS CLI within a Codespace environment to manage AWS resources, including EC2 instances, security groups, IAM users, and resource filtering[cite: 12, 18, 25, 4, 5].

## Tasks Performed

### Task 01: GitHub CLI & Codespace Setup
* [cite_start]Installed the GitHub CLI[cite: 13].
* [cite_start]Authenticated the GitHub CLI for use with Codespaces[cite: 14].
* [cite_start]Listed available Codespaces and established a connection[cite: 15, 16].

### Task 02: AWS CLI Installation & Configuration
* [cite_start]Downloaded and installed the AWS CLI within the Codespace environment[cite: 19].
* [cite_start]Verified the installation and configured the AWS CLI with necessary credentials[cite: 20, 21].
* [cite_start]Verified connectivity and configuration files[cite: 22, 23].

### Task 03: Security Group Management
* [cite_start]Created a new security group and inspected its details[cite: 26, 27].
* [cite_start]Identified the Codespace public IP address[cite: 28].
* [cite_start]Authorized inbound SSH traffic on port 22 specifically for the Codespace IP[cite: 29].
* [cite_start]Added an HTTP rule (port 80) using `ip-permissions` JSON and verified both rules[cite: 31, 32].

### Task 04 & 05: EC2 Instance & Resource Inspection
* [cite_start]Created a key pair and saved the `.pem` file to the workspace[cite: 4].
* [cite_start]Launched an EC2 instance and retrieved its public IP address[cite: 4].
* [cite_start]Performed SSH access into the instance from the Codespace[cite: 4].
* [cite_start]Inspected AWS resources including VPCs, subnets, regions, and availability zones[cite: 4].

### Task 06: IAM User & Group Management
* [cite_start]Created an IAM group and user, then added the user to the group[cite: 4].
* [cite_start]Attached the `AmazonEC2FullAccess` policy to the group[cite: 5].
* [cite_start]Created a console login profile and access keys for the user[cite: 5].
* [cite_start]Authenticated as the new user within the Codespace using environment variables[cite: 5].

### Task 07 & 08: Querying & Reporting
* [cite_start]Used filters to query specific instances based on public tags, subnets, and VPCs[cite: 5].
* [cite_start]Utilized the `--query` parameter to format output reports, including instance names, IPs, states, and types[cite: 5, 6].

### Task 09: Cleanup
* [cite_start]Performed final resource cleanup to ensure no unnecessary AWS charges were incurred[cite: 6].
