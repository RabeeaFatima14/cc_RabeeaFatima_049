# Infrastructure Monitoring & Log Collection System

[cite_start]**Submitted By:** Rabeea Fatima (049) & Reena Qureshi (052) [cite: 70]  
[cite_start]**Department:** Software Engineering, Fatima Jinnah Women University [cite: 63, 65]  
[cite_start]**Subject:** Cloud Computing (Semester V) [cite: 67, 71]  
[cite_start]**Instructor:** Sir Waqas Saleem [cite: 68]  

---

## Project Overview
[cite_start]This project implements a comprehensive infrastructure-monitoring and log-collection system using modern DevOps tools[cite: 98]. [cite_start]The system automatically provisions cloud infrastructure on AWS, configures monitoring services, and provides real-time dashboards to track infrastructure health[cite: 99].

### Key Achievements
* [cite_start]**Automated Provisioning:** Deployed a fully automated monitoring infrastructure on AWS using Infrastructure as Code (Terraform)[cite: 101].
* [cite_start]**Scalable Architecture:** Configured a monitoring server and two application servers in the `me-central-1` region[cite: 102].
* [cite_start]**Real-Time Monitoring:** Implemented automated health checks, metrics collection, and a live web dashboard[cite: 102, 103].
* [cite_start]**Automated Log Collection:** Established remote log harvesting from all application servers using Ansible[cite: 104].
* [cite_start]**Scheduled Reporting:** Configured cron-based scheduling for continuous monitoring and periodic report generation[cite: 105].

## Technologies Used
* [cite_start]**Infrastructure:** Terraform (VPC, EC2, Security Groups) [cite: 107]
* [cite_start]**Configuration Management:** Ansible (Roles, Playbooks, Dynamic Inventory) [cite: 108]
* [cite_start]**Monitoring:** Bash Scripts (Metrics collection, service checks, reporting) [cite: 108]
* [cite_start]**Web Services:** Nginx (Reverse proxy and dashboard serving) [cite: 108]
* [cite_start]**Version Control:** Git (Main/Dev branching strategy) [cite: 108]

---

## Architecture Design

### Network Topology
* [cite_start]**VPC:** `10.0.0.0/16` [cite: 115]
* [cite_start]**Public Subnet:** `10.0.1.0/24` (Hosts monitoring and application servers) [cite: 116, 178]
* [cite_start]**Monitoring Server:** Public IP `40.172.46.28` [cite: 126, 127]
* [cite_start]**Application Servers:** Two instances with private IPs `10.0.1.131` and `10.0.1.176` [cite: 132, 133]

### Security Configuration
* [cite_start]**Monitoring SG:** Allows Inbound HTTP (80) and SSH (22) from all sources[cite: 165].
* [cite_start]**App Server SG:** Restricts Inbound HTTP (80) to only the Monitoring Server's security group, while allowing global SSH (22)[cite: 166, 167].

---

## Infrastructure as Code (Terraform)
[cite_start]The project is organized into three reusable modules[cite: 172]:
1. [cite_start]**Network Module:** Provisions the VPC, subnets, IGW, and security groups[cite: 173, 174].
2. [cite_start]**Monitoring Server Module:** Deploys an Ubuntu 20.04 instance with automated Nginx setup[cite: 186, 193, 195].
3. [cite_start]**App Servers Module:** Deploys multiple application servers using count-based logic[cite: 202, 203].

### Multi-Environment Support
[cite_start]Deployment is supported across three environments via `.tfvars` files[cite: 219, 220]:
* [cite_start]**Development:** 2 x `t3.micro` instances[cite: 221, 222].
* [cite_start]**Staging:** 3 x `t3.small` instances[cite: 223, 224].
* [cite_start]**Production:** 5 x `t3.medium` instances[cite: 225, 226].

---

## Configuration Management (Ansible)
[cite_start]Infrastructure configuration is managed through two primary roles[cite: 245, 246]:
* [cite_start]**Nginx App Role:** Configures application servers with Nginx, health endpoints (`/health`), and logging[cite: 247, 248, 251].
* [cite_start]**Dashboard Role:** Sets up the central monitoring server to serve the real-time HTML dashboard and organize collected metrics/logs[cite: 259, 260, 264].

---

## Monitoring & Dashboards
[cite_start]The system features a 5-stage data collection pipeline[cite: 135]:
1. [cite_start]**Metrics:** CPU, memory, disk, and system load collected every 5 minutes[cite: 136, 139].
2. [cite_start]**Service Checks:** Verifies the status of the Nginx service on all hosts[cite: 141, 143].
3. [cite_start]**HTTP Health Checks:** Queries app server endpoints to validate HTTP 200 OK responses[cite: 145, 146, 148].
4. [cite_start]**Dashboard Updates:** Automatically regenerates the HTML dashboard every 5 minutes[cite: 150, 155].
5. [cite_start]**Reports:** Generates daily and weekly infrastructure health reports[cite: 156, 157].

---

## Repository & Links
* [cite_start]**GitHub Repository:** [https://github.com/RabeeaFatima14/FinalProject9](https://github.com/RabeeaFatima14/FinalProject9) [cite: 61]
* [cite_start]**Live Dashboard:** [http://40.172.46.28/](http://40.172.46.28/) [cite: 103]
