# AWS High-Availability WordPress Infrastructure

[![Build Status](https://github.com/stephen-oni/VPC-EC2-ASG-RDS/actions/workflows/validate.yml/badge.svg)](https://github.com/stephen-oni/VPC-EC2-ASG-RDS/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📖 Overview
This repository provides a production-grade, highly available WordPress environment deployed on AWS. By leveraging **Infrastructure as Code (IaC)** via CloudFormation, the stack ensures consistency, scalability, and security across the deployment lifecycle.

## 🏗️ Architecture
![Architecture Diagram](docs/architecture.png)

This architecture is designed for resilience:
* **Network Layer:** A custom VPC spanning two Availability Zones (AZs) to ensure zero downtime during zonal failures.
* **Compute Layer:** An Auto Scaling Group (ASG) that dynamically adjusts the number of EC2 instances based on traffic, ensuring efficient load distribution.
* **Data Layer:** A Multi-AZ RDS instance, ensuring database redundancy and automated failover.
* **Security:** Isolated subnets (Public for Web, Private for Data) with security group ingress rules restricted to internal traffic only.

## 🚀 Deployment Guide

### Prerequisites
- AWS CLI configured with appropriate permissions.

### Quick Start
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/stephen-oni/VPC-EC2-ASG-RDS.git](https://github.com/stephen-oni/VPC-EC2-ASG-RDS.git)
   cd VPC-EC2-ASG-RDS
