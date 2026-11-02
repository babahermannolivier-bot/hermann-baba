# [PROPOSED] Multi-Cloud Zero-Trust Secure Deployment of Docker Containers in Azure and AWS Using Prisma Cloud Compute and SASE — CNAPP and ZTNA Implementation

> **Status:** Proposed MSc Final Project - Awaiting Lecturer Approval
> **Programme:** MSc Applied Cybersecurity and Cloud Technology — London Metropolitan University
> **Author:** Hermann Baba | Aspiring Cloud Security Engineer (Financial Services)
> **Mentor:** VP, MUFG - Project Finance & Advisory

### 🎯 Proposed Objective
Design and implement a Zero-Trust Architecture for securely deploying containerized workloads across AWS (EKS) and Azure (AKS), enforced by Palo Alto Networks Prisma Cloud Compute (CNAPP) and Prisma SASE with ZTNA.

This project addresses critical cloud security gaps in financial services: misconfigurations, excessive privileges, and insecure container supply chains.

### 🏗️ Proposed Architecture

**Multi-Cloud:** AWS EKS (London) + Azure AKS (UK South)
**Zero-Trust Principle:** Never Trust, Always Verify - NIST 800-207
**Core Security Stack:**
- **Palo Alto Prisma Cloud Compute (CNAPP)** - Image Scanning, Runtime Defense, Compliance & CSPM
- **Palo Alto Prisma SASE / ZTNA** - Identity-aware access, no VPN, device posture check
- **Docker** - Hardened, non-root containers
- **Terraform** - Secure IaC with encrypted state
- **IAM** - Least privilege, federated identities via Azure AD & AWS IAM Identity Center

### 🔐 Planned Implementations

**1. CNAPP - Cloud Native Application Protection**
- Container image vulnerability scanning in CI/CD (Twistlock)
- Runtime protection & compliance for EKS/AKS
- Cloud Security Posture Management (CSPM) for AWS/Azure misconfigurations

**2. ZTNA - Zero Trust Network Access (via Prisma SASE)**
- Identity-based access (no standing VPN)
- Micro-segmentation between workloads
- Conditional access policies + MFA

**3. Secure IaC & Supply Chain**
- Terraform hardened: S3 backend encryption, no hardcoded secrets
- Secrets via Azure Key Vault & AWS Secrets Manager
- Read-only, non-root Dockerfiles

**4. Threat Prevention**
- Palo Alto NGFW policies for East-West traffic in Kubernetes
- Logging & monitoring aligned to financial services governance

### 📂 Repository Structure (Proposal Scaffold)
