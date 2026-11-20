# Enterprise Identity & Access Governance in Microsoft Entra ID

A hands-on Identity and Access Management (IAM) governance lab and security assessment built in **Microsoft Entra ID (Free Tier)**[cite: 6]. This project models Joiner-Mover-Leaver (JML) lifecycle operations, enforces Least-Privilege Role-Based Access Control (RBAC), validates baseline Multi-Factor Authentication (MFA) hardening, and verifies offboarding non-repudiation through directory audit logs[cite: 6, 7, 8, 9].

📄 **[Read the Full Case Study & Risk Assessment Report (PDF)](docs/Entra-ID-IAM-Governance-Case-Study.pdf)**

---

## Project Overview & Architecture

* **Environment:** Microsoft Entra ID (Free Tier)[cite: 6]
* **Departmental Personas & Groups:** Modeled role-separated identities for **Alice Smith (HR)** and **Bob Jones (Finance)** alongside a dedicated security group (`SG-Finance-Access`) and enterprise application (`Finance-App-Prod`)[cite: 6].
* **Least-Privilege RBAC:** Delegated scoped user administration to a non-global administrator via the built-in **User Administrator** role, eliminating standing **Global Administrator** over-provisioning[cite: 7].
* **Baseline Tenant Hardening:** Enabled and verified **Security Defaults** to enforce tenant-wide MFA registration for administrators and block legacy authentication protocols (POP3, IMAP, SMTP) without requiring P1/P2 licenses[cite: 7].
* **Leaver Offboarding & Audit Telemetry:** Simulated employee offboarding by revoking application role assignments on `Finance-App-Prod` and verified non-repudiation in Entra ID Audit Logs[cite: 8, 9].

---

## Repository Structure

```text
entra-id-iam-governance-lab/
├── README.md
├── docs/
│   └── Entra-ID-IAM-Governance-Case-Study.pdf
└── assets/
    ├── 01-tenant-security-defaults.png
    ├── 02-rbac-least-privilege.png
    └── 03-audit-log-offboarding.png
