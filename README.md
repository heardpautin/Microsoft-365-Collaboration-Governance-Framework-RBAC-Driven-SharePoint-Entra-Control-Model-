# Microsoft 365 Collaboration Governance Framework  
Author: Craig W. Heard  
Focus Area: IAM + GRC + Cloud Collaboration Governance  

---

## 🔎 Project Overview

This project demonstrates how traditional RBAC (Role-Based Access Control) models can be extended into Microsoft 365 collaboration platforms, specifically:

- Microsoft Entra ID (Identity & Group Management)
- SharePoint Online (Collaboration & Resource Authorization)

The framework mirrors a real-world enterprise RBAC matrix and applies it to SharePoint governance, integrating:

- Group-based authorization
- Business ownership enforcement
- Data sensitivity classification
- Access review lifecycle
- Compliance alignment

---

## 🎯 Objective

To design a structured Collaboration Governance Matrix that:

- Eliminates direct user permissions
- Enforces group-based access
- Aligns review cadence with risk level
- Maps collaboration controls to regulatory frameworks
- Bridges IAM architecture with GRC oversight

---

## 🏗 Architecture Model

User  
→ Entra Security Group  
→ SharePoint Role (Owner / Member / Visitor)  
→ Governance Controls  
→ Access Review Lifecycle  

Identity = Authentication  
SharePoint = Resource Authorization  
Governance = Oversight & Compliance Enforcement  

---

## 🏗 Logical Architecture Diagram

Identity Layer
--------------
User
  ↓
Microsoft Entra ID
  ↓
Security Group Membership

Authorization Layer
-------------------
Security Group
  ↓
SharePoint Role Mapping (Owner / Member / Visitor)
  ↓
SharePoint Online Site / Document Library

Governance Layer
----------------
• Access Reviews (Scheduled Certification)
• Guest Expiration Policies
• Sensitivity Labels
• DLP Enforcement
• Site Expiration Policy

Compliance / Audit Layer
------------------------
• Audit Logs
• Access Review Evidence
• Policy Documentation
• Control Mapping (SOX / HIPAA / NIST / ISO)

Flow Summary:
User → Identity → Group → Role → Resource → Governance Controls → Audit Evidence → Compliance Alignment


## 📊 Core Components

### 1️⃣ Collaboration Governance Matrix (CSV)

Defines structured mapping between:
- Business Unit
- Job Role
- Entra Group
- SharePoint Site
- Permission Role
- Data Sensitivity
- External Sharing Policy
- Access Review Frequency
- Business Owner
- Compliance Framework Mapping

### 2️⃣ Governance Principles

- No direct user permission assignments
- Standardized permission roles (Owner / Member / Visitor)
- Mandatory business ownership of collaboration sites
- Guest access expiration and oversight
- Sensitivity-driven policy enforcement
- Permission inheritance preserved wherever possible

---

## 🛡 Risk & Compliance Integration

Controls are aligned to commonly recognized regulatory and security frameworks including:

- SOX 404
- HIPAA
- FFIEC
- NIST AC-2
- ISO 27001

This demonstrates how collaboration platforms can transition from unmanaged data repositories to structured, auditable environments.

---

## 📈 Governance Maturity Model

| Level | Description |
|-------|-------------|
| Level 1 | Ad-hoc permissions, direct user assignments, no review cycle |
| Level 2 | Group-based access with partial review and limited oversight |
| Level 3 | Structured matrix, lifecycle automation, compliance mapping, standardized roles |

This project models a Level 3 governance design.

---

## 🧠 Key Architectural Insight

Most SharePoint governance issues are not authentication failures — they are entitlement lifecycle and governance maturity gaps.

Microsoft Entra ID handles identity and authentication.  
SharePoint handles resource-level authorization.  
Governance ensures structured oversight and lifecycle enforcement across both layers.

---

## 🏛 Federal / Regulatory Alignment Statement

This framework demonstrates governance maturity aligned to both financial regulatory expectations and federal RMF principles by integrating identity-based access control, least privilege enforcement, and structured entitlement review within cloud collaboration environments.

---

## 📁 Files Included

- sharepoint_collaboration_governance_matrix_v1.csv  
- README.md  

---

## 🚀 Future Enhancements

- Dynamic group logic (attribute-based access control)
- Sensitivity label enforcement mapping
- Data Loss Prevention (DLP) integration model
- Automated provisioning workflow design
- Audit evidence tracking model
- Risk scoring column for entitlement exposure
- Zero Trust alignment documentation

---

## 💼 Professional Application

This framework demonstrates the ability to:

- Translate IAM principles into collaboration governance
- Design structured entitlement lifecycle controls
- Align technical authorization models with compliance requirements
- Apply GRC discipline to cloud-based collaboration platforms

This project reflects practical enterprise governance thinking applicable to financial services, healthcare, and federal environments.
