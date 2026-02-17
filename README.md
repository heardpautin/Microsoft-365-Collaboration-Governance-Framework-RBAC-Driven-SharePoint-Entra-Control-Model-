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
- Structured site provisioning controls

---

## 🎯 Objective

To design a structured Collaboration Governance Framework that:

- Eliminates direct user permissions
- Enforces group-based access
- Aligns review cadence with risk level
- Controls site creation at inception
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

---

## 🏗 Site Provisioning & Approval Workflow

Effective collaboration governance begins at the point of site creation.  
This framework enforces structured controls during provisioning to prevent unmanaged sprawl and entitlement risk.

### 1️⃣ Site Request Initiation

• Request submitted via standardized intake form (ServiceNow / M365 Request Form)  
• Business justification required  
• Data sensitivity classification selected (Public / Internal / Confidential / Restricted)  
• Primary Business Owner identified  
• Secondary Owner required for redundancy  

---

### 2️⃣ Governance Validation

Before site creation:

• Business Owner validated (must be non-IT data owner)  
• Sensitivity classification reviewed  
• External sharing requirements declared  
• Compliance mapping identified (if applicable)  

High-sensitivity sites require governance approval prior to creation.

---

### 3️⃣ Automated Provisioning Controls

Upon approval:

• Microsoft 365 Group automatically created  
• Entra Security Group aligned to business role  
• SharePoint site provisioned with standardized template  
• Default permission roles applied (Owner / Member / Visitor)  
• Sensitivity label automatically enforced  
• External sharing policy configured based on classification  
• Site expiration policy applied  

No direct user permissions are permitted at creation.

---

### 4️⃣ Lifecycle Controls Applied

Immediately after provisioning:

• Access Review schedule assigned based on sensitivity level  
• Guest access expiration policy enforced (if enabled)  
• Audit logging enabled  
• DLP policies inherited from classification tier  
• Site ownership recorded for audit traceability  

---

### 5️⃣ Ongoing Governance Enforcement

• Quarterly or semi-annual access certification (risk-based)  
• Automatic notification of inactive sites  
• Owner attestation required for renewal  
• Automatic archival or deletion if lifecycle policy not satisfied  

---

### Governance Objective

Provisioning is treated as a control event — not a convenience action.

This structured provisioning model ensures:

• Least privilege from inception  
• Business accountability  
• Elimination of unmanaged site creation  
• Reduced data sprawl risk  
• Alignment with Zero Trust principles  
• Audit-ready evidence trail  

---

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

This demonstrates how collaboration platforms can transition from unmanaged data repositories into structured, auditable control environments.

---

## 📈 Governance Maturity Model

| Level | Description |
|-------|-------------|
| Level 1 | Ad-hoc permissions, direct user assignments, no review cycle |
| Level 2 | Group-based access with partial review and limited oversight |
| Level 3 | Structured matrix, lifecycle automation, compliance mapping, standardized roles |

This project models a Level 3 governance design.

---

## 📊 Risk Exposure Scoring Model

To move beyond static governance design, this framework includes a structured Risk Exposure Scoring Model to quantify collaboration risk within SharePoint environments.

The objective is to prioritize oversight and remediation based on measurable exposure indicators rather than treating all sites equally.

---

### 🔢 Risk Scoring Factors

Each collaboration site is evaluated using weighted control factors:

| Risk Factor | Condition | Score |
|-------------|-----------|-------|
| Data Sensitivity | Restricted | +5 |
| Data Sensitivity | Confidential | +3 |
| External Sharing Enabled | Yes | +4 |
| Guest Users Present | Yes | +3 |
| Large Membership | >50 Members | +2 |
| No Access Review in 6 Months | Yes | +3 |
| No Business Owner Assigned | Yes | +5 |
| Direct User Permissions Detected | Yes | +4 |

---

### 🧮 Risk Tier Classification

Total score determines governance priority:

| Risk Score Range | Risk Tier | Governance Action |
|------------------|----------|------------------|
| 0–4 | Low | Standard review cycle |
| 5–9 | Moderate | Increased monitoring |
| 10–14 | High | Immediate owner review |
| 15+ | Critical | Governance escalation required |

---

### 🎯 Governance Application

Risk scoring enables:

• Prioritized access reviews  
• Targeted remediation of high-risk sites  
• Focused external sharing oversight  
• Escalation workflows for critical exposure  
• Executive-level reporting of collaboration risk posture  

---

### 🏗 Architectural Insight

Risk scoring transforms governance from reactive compliance into proactive risk management.

Rather than asking:
"Are we compliant?"

The framework enables leadership to ask:
"Where is our highest collaboration risk today?"

This aligns IAM, GRC, and cloud security into a measurable risk-based control model.

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
- Risk scoring model for entitlement exposure
- Automated provisioning workflow integration example
- Audit evidence tracking template
- Zero Trust alignment documentation

---

## 💼 Professional Application

This framework demonstrates the ability to:

- Translate IAM principles into collaboration governance
- Design structured entitlement lifecycle controls
- Align technical authorization models with compliance requirements
- Apply GRC discipline to cloud-based collaboration platforms
- Architect lifecycle-based access control models in Microsoft 365 environments

This project reflects practical enterprise governance thinking applicable to financial services, healthcare, and federal environments.
