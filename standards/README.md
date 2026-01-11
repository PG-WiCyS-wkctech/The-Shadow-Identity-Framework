# 📜 Standards: The "Laws" of the Shadow Identity Framework

> **Folder Status:** Regulatory  
> **Primary Goal:** Establish a baseline for Governance, Risk, and Compliance (GRC) across all digital identities.

The documents in this directory represent the "Laws" of the **Shadow Identity Framework (SIF)**. Every account, service, and physical device integrated into this system must comply with these standards to ensure the integrity of the "Vault" and the privacy of the "Mask."

---

## 🏛️ Why We Have Standards

In a fragmented digital world, security fails because of inconsistency. By enforcing these standards, we achieve:
1.  **Risk Mitigation:** Eliminating weak points like SMS-based recovery.
2.  **Operational Consistency:** Ensuring all 7+ email addresses are handled with the same level of care.
3.  **Future-Proofing:** Making it easy for family members (or your future self) to understand the security logic.

---

## 📑 Core Standard Documents

### [SIF-STD-001: Password & Credential Policy](./PASSWORD_POLICY.md)
* **The Law:** No human-memorized passwords for individual services. 
* **Requirement:** Minimum 20-character random strings stored in a zero-knowledge vault.
* **The Master Key:** Requirements for the physical storage of the Master Passphrase.

### [SIF-STD-002: Multi-Factor Authentication (MFA)](./MFA_STANDARDS.md)
* **The Law:** Cryptographic hardware is the primary source of truth.
* **Requirement:** Mandatory Hardware Security Keys (FIDO2) for the Hub. 
* **The Ban:** SMS/Voice-call MFA is strictly prohibited (Deprecated due to SIM-swap risk).

### [SIF-STD-003: Encryption & Digital Certificates](./ENCRYPTION_STANDARDS.md)
* **The Law:** Outgoing professional mail must be verifiable.
* **Requirement:** S/MIME certificate implementation for alumni and professional aliases.
* **The Archive:** AES-256 encryption standards for all physical media (SSDs/M-DISCs).

### [SIF-STD-004: Identity Governance](./IDENTITY_GOVERNANCE.md)
* **The Law:** The "Secret Identity" must never be leaked.
* **Requirement:** Separation of "Identity" (Login) and "Communication" (Alias) for all high-value accounts (Banking, Health, Primary Email).

---

## ⚖️ Enforcement & Auditing

To maintain **GRC Compliance**, a "Security Audit" must be performed annually or whenever a new account is added to the **Master Sync Matrix**.

| Compliance Check | Frequency | Requirement |
| :--- | :--- | :--- |
| **Credential Rotation** | As Needed | Only if a breach is detected in a specific "Mask." |
| **MFA Audit** | Bi-Annually | Verify all backup YubiKeys are functional. |
| **The Purge Audit** | Annually | Confirm data has been moved to M-DISC and cloud storage is below the free-tier threshold. |

---

## 🛠️ How to Propose Changes
As technology evolves (e.g., the transition from passwords to Passkeys), these standards must be updated.
1.  Open an **Issue** in this repository.
2.  Draft the proposed standard update.
3.  Commit the change with a version bump (e.g., v1.0 to v1.1).

---

**Project Lead:** Kathryn Wilson 
**Policy Effective Date:** January 2026  
**Next Review Date:** January 2027
