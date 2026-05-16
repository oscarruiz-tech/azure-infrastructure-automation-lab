# azure-infrastructure-automation-lab
Deployed a secure multi-tier Azure VNet infrastructure and an isolated Linux backend server, including ARM declarative template extraction for automated cloud environment replication.
# Azure Cloud Infrastructure & Automation Lab

## 📌 Project Overview
This repository documents a hands-on technical lab focused on designing, segmenting, and deploying a secure, multi-tier cloud infrastructure using Microsoft Azure. The project demonstrates advanced competencies in cloud networking, virtual computing deployment, security hardening, and Infrastructure as Code (IaC).

---

## 🛠️ Key Deliverables & Architectural Stages

### 1. Secure Network Topology Design
* **Virtual Network Allocation:** Provisioned a centralized virtual network (`VNet-Core-Corporate`) with an primary address space of `10.0.0.0/24`.
* **Subnet Segmentation:** Engineered three distinct subnets with precise, non-overlapping IPv4 CIDR blocks targeting specific tiers:
  * `FrontendSubnet`: `10.0.0.0/26` (64 IP addresses)
  * `BackendSubnet`: `10.0.0.64/26` (64 IP addresses)
  * `DatabaseSubnet`: `10.0.0.128/26` (64 IP addresses)
#### 📊 Architectural Diagram & Subnet Segmentation
<img width="1910" height="1064" alt="image_36f2dc" src="https://github.com/user-attachments/assets/da6c6c30-f8d3-46d0-8426-93ba3213db24" />


### 2. Backend Compute Deployment & Hardening
* **Instance Provisioning:** Deployed an enterprise-grade virtual machine instance running **Ubuntu Server 24.04 LTS**.
* **Network Isolation:** Associated the instance strictly within the `BackendSubnet` and configured **`Public IP: None`**. This architecture explicitly cuts off direct entry from the public internet, ensuring total boundary protection.
* **Access Control:** Implemented distinct, custom administrative account policies for secure, local credential authentication instead of baseline default settings.

### 3. Infrastructure as Code (IaC) Extraction
* **ARM Template Generation:** Successfully extracted the complete deployment blueprint from the Azure Resource Manager (ARM).
* **Declarative Configuration:** Maintained isolated `template.json` and `parameters.json` structures, validating the environment's repeatability and modular automation blueprints.
* **Source Code:** Review the complete blueprint directly in the [template.json](./template.json) file included in this repository.
---

## 📉 Governance & Cost Management
* Managed resource provisioning lifecycle via strict **Resource Group** encapsulation.
* Conducted operational budget protection workflows by systematically decommissioning all virtual computation instances, static disk resources, and networking boundaries immediately post-validation, maintaining a `$0.00` residual overhead.

---

### 🚀 Skills Demonstrated
`Microsoft Azure` · `Cloud Networking (VNet/Subnetting)` · `CIDR Notation` · `Network Security Hardening` · `Linux Systems Administration (Ubuntu)` · `Infrastructure as Code (ARM Templates / JSON)` · `Cloud Governance & Resource Lifecycle Management`
