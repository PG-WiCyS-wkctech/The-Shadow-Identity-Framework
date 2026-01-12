# 📜 Standards: The "Laws" of the Shadow Identity Framework

> **Folder ID:** GRC-STD-000  
> **Folder Status:** Regulatory / Mandatory  
> **Primary Goal:** Establish a baseline for Governance, Risk, and Compliance (GRC) across all digital identities.

The documents in this directory represent the "Laws" of the **Shadow Identity Framework (SIF)**. Every account, service, and physical device integrated into this system must comply with these standards to ensure the integrity of the **Vault** and the privacy of the **Mask**.

---

## 🏛️ Why We Have Standards

In a fragmented digital world, security fails because of inconsistency. By enforcing these standards, we achieve:
1.  **Risk Mitigation:** Eliminating critical vulnerabilities like SIM-swapping and credential stuffing.
2.  **Operational Consistency:** Ensuring all 7+ "Spoke" identities are handled with the same rigor as the "Hub."
3.  **Future-Proofing:** Creating a logical path for family members (or your future self) to maintain access.

---

## ⚖️ Core Standard Documents

| Standard ID | Title | Level | The Law in Brief |
| :--- | :--- | :--- | :--- |
| **[SIF-STD-001](./SIF-STD-001_PASSWORD_&_POLICY.md)** | **Password & Credential** | 🔴 Mandatory | No human-memorized passwords. 20+ char random strings only. |
| **[SIF-STD-002](./SIF-STD-002_MFA_STANDARDS.md)** | **Authentication (MFA)** | 🔴 Mandatory | FIDO2 Hardware is the source of truth. **SMS is Prohibited.** |
| **[SIF-STD-003](./SIF-STD-003_ENCRYPTION_STANDARDS.md)** | **Encryption & Certs** | 🟡 Recommended | Outgoing mail must be S/MIME signed; Archives must be AES-256. |
| **[SIF-STD-004](./SIF-STD-004_IDENTITY_GOVERNANCE.md)** | **Identity Governance** | 🔴 Mandatory | Separation of "Identity" (Login) from "Communication" (Mask). |
| **[SIF-RAT-001](./SIF-RAT-001_WHY_NO_SMS.md)** | **Rationale: No SMS** | 📖 Info | Technical context on SIM-swapping and SS7 vulnerabilities. |

---

## 🏛️ Compliance Levels

* **🔴 Mandatory:** Non-negotiable. Failure to meet this standard results in "Critical Risk." The account is considered compromised until rectified.
* **🟡 Recommended:** Best practice for privacy. Should be implemented on all "Hub" and "Spoke" accounts where the platform supports it.
* **📖 Informative:** Provides the "Control Rationale" (the *Why*) behind the laws to aid in decision-making.

---

## 📊 Enforcement & Auditing

To maintain **GRC Compliance**, a "Security Audit" must be performed annually or whenever a new account is added to the **Master Sync Matrix**.

| Compliance Check | Frequency | Requirement |
| :--- | :--- | :--- |
| **Credential Audit** | As Needed | Verify no password reuse; check for "Mask" breaches via HaveIBeenPwned. |
| **MFA Audit** | Bi-Annually | Physically test all primary and backup Hardware Keys (Smart Rings/YubiKeys). |
| **The Purge Audit** | Annually | Confirm data moved to M-DISC and cloud storage remains below the Free Tier. |
| **Header Audit** | Quarterly | Verify outgoing mail does not leak the "Vault" address in metadata. |

---

## 🛠️ How to Propose Changes
As technology evolves (e.g., the transition from passwords to Passkeys), these standards must be updated to remain effective.
1.  Open an **Issue** or **Draft** in this repository.
2.  Outline the technological shift (e.g., "Replacing TOTP with Passkeys").
3.  Commit the change with a version bump (e.g., v1.0 to v1.1).

---

**Project Lead:** Kathryn Wilson  
**Policy Effective Date:** January 2026  
**Next Review Date:** January 2027
