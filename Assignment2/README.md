# Assignment No 2: Cloud Computing

[cite_start]**Submitted By:** Rabeea Fatima [cite: 16]
[cite_start]**Registration No:** 2023-BSE-049 [cite: 16]
[cite_start]**Section:** B [cite: 17]
[cite_start]**Subject:** Cloud Computing [cite: 17]

---

## Overview
[cite_start]This assignment demonstrates the implementation of a production-ready, highly available multitier web infrastructure on AWS using Terraform Infrastructure as Code (IaC)[cite: 19]. [cite_start]The infrastructure includes an Nginx reverse proxy/load balancer with SSL/TLS termination, intelligent caching, and three Apache backend web servers configured for automatic failover[cite: 20].

## Infrastructure Components
* [cite_start]**VPC:** 10.0.0.0/16 CIDR block[cite: 22].
* [cite_start]**Public Subnet:** 10.0.10.0/24 CIDR block[cite: 23].
* [cite_start]**Internet Gateway:** Provides internet connectivity[cite: 24].
* [cite_start]**Security Groups:** Nginx SG and Backend SG with minimal access[cite: 25].
* [cite_start]**EC2 Instances:** 1 Nginx load balancer + 3 Apache web servers[cite: 26].
* [cite_start]**SSL/TLS:** Self-signed certificate for HTTPS[cite: 27].

## Technologies Used
* [cite_start]**IaC:** Terraform >= 1.0[cite: 29].
* [cite_start]**Cloud Provider:** AWS (me-central-1 region)[cite: 30].
* [cite_start]**Operating System:** Amazon Linux 2023[cite: 31].
* [cite_start]**Load Balancer:** Nginx with reverse proxy[cite: 32].
* [cite_start]**Web Server:** Apache HTTP Server 2.4[cite: 33].
* [cite_start]**Protocols:** HTTPS (TLS 1.2/1.3), HTTP/2[cite: 34].

## Implementation Details

### Part 1: Project & Networking Setup
* [cite_start]Established the project structure and variable configurations[cite: 38, 39].
* [cite_start]Configured the networking module, including VPC, subnets, and internet gateway[cite: 40].
* [cite_start]Set up the security module with controlled inbound and outbound rules[cite: 41, 8].

### Part 2: Web Server Module
* [cite_start]Designed and implemented the web server module for scalability[cite: 43, 44].
* [cite_start]Configured module usage for the deployment of EC2 instances[cite: 45].

### Part 3: Server Configuration Scripts
* [cite_start]Created an Apache backend server script for automated setup[cite: 47].
* [cite_start]Created an Nginx server script to handle load balancing and reverse proxying[cite: 48].

### Part 4: Infrastructure Deployment
* [cite_start]Performed the initial deployment using Terraform commands[cite: 50].
* [cite_start]Configured output variables for easy resource tracking[cite: 51].
* [cite_start]Verified AWS resources (EC2, VPC, Subnets, Security Groups) via the AWS Console[cite: 4].

### Part 5: Testing & Analysis
* [cite_start]Updated Nginx backend configuration and tested the least-connections load balancing algorithm[cite: 4, 9].
* [cite_start]Verified core functionality, high availability, and performed security/performance analysis[cite: 4].

## Bonus Tasks
* [cite_start]**Task 1:** Implemented custom error pages[cite: 4].
* [cite_start]**Task 3:** Implemented a battery health check returning JSON-formatted server status information[cite: 4, 10].

## Conclusion
[cite_start]The project successfully demonstrated the full lifecycle management of cloud resources, from deployment to destruction using Terraform[cite: 12]. [cite_start]It reinforced best practices for deploying production-ready web applications, including load balancing strategies and infrastructure automation on AWS[cite: 13].
