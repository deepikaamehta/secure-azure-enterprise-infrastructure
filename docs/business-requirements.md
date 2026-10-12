# Nexora Technologies — Business Requirements

## 1. Company Overview

**Company:** Nexora Technologies  
**Industry:** B2B Software as a Service (SaaS)  
**Employees:** 100  
**Headquarters:** Toronto, Canada  
**Cloud Platform:** Microsoft Azure  
**Primary Azure Region:** Canada Central

## 2. Business Problem

Nexora Technologies requires a secure, scalable, and manageable Azure infrastructure to support its growing business operations.

The company needs standardized cloud governance, network segmentation, centralized access management, infrastructure monitoring, backup and recovery, and automation.

## 3. Technical Requirements

| ID | Requirement | Priority |
|---|---|---|
| REQ-01 | Establish standardized Azure resource organization and tagging | High |
| REQ-02 | Implement hub-and-spoke network architecture | High |
| REQ-03 | Separate production and development workloads | High |
| REQ-04 | Implement Microsoft Entra ID and role-based access control | High |
| REQ-05 | Deploy securely managed Windows and Linux virtual machines | High |
| REQ-06 | Centralize monitoring using Azure Monitor and Log Analytics | High |
| REQ-07 | Configure VM backups and test recovery procedures | High |
| REQ-08 | Implement security controls using Azure Policy, Key Vault, and Defender for Cloud | High |
| REQ-09 | Automate infrastructure deployments using Terraform | Medium |
| REQ-10 | Implement cost budgets, tagging, and development VM shutdown automation | High |
| REQ-11 | Document and investigate simulated infrastructure incidents | Medium |

## 4. Architecture Principles

- **Security by design:** Apply least privilege and restrict unnecessary network exposure.
- **Environment isolation:** Separate production and development resources.
- **Operational visibility:** Centralize logging, monitoring, and alerting.
- **Infrastructure as Code:** Make deployments repeatable and auditable.
- **Cost awareness:** Prefer small lab resources and remove unused infrastructure.
- **Recoverability:** Maintain backups and validate recovery procedures.

## 5. Project Scope

This is a simulated enterprise infrastructure environment designed for hands-on learning and portfolio demonstration.

The company has 100 fictional employees, but the lab will deploy only the minimum resources needed to demonstrate the architecture.

Production and development environments are simulated. No real customer data or production workloads will be used.

## 6. Success Criteria

The project will be considered successful when the implemented components can be deployed, tested, documented, and demonstrated through GitHub.

Evidence will include architecture diagrams, Terraform code, administrative scripts, configuration screenshots, monitoring queries, security validation, and incident reports.