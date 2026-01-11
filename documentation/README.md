# 📂 Documentation: GRC-Level Setup Guides

> **Standard ID:** GRC-DOC-001  
> **Classification:** Confidential / Internal  
> **Framework:** Shadow Identity & Resilient Archival (SIRA)

This directory contains the definitive technical configurations for the **Shadow Identity Framework (SIF)**. Unlike standard "how-to" guides, these documents are structured as **Compliance Blueprints** to ensure zero-leakage of primary identities and maximum archival durability.

---

## 🏛️ The Three Pillars of GRC-Level Organization

| Pillar | Focus | GRC Goal |
| :--- | :--- | :--- |
| **Governance** | Identity Naming & Hierarchy | Establishing a "System of Record" for all digital personae. |
| **Risk** | Technical Leak Prevention | Mitigating "Header Leakage" and cross-platform tracking. |
| **Compliance** | Verification & Auditing | Ensuring setup meets the 3-2-1 archival and 100% masking standards. |

---

## 🗺️ Directory Map

### 1. Identity Masking & "Shadow" Configs
Detailed guides on isolating your primary communications from public-facing interactions.
* **[Apple iCloud+ Strategy](./apple-icloud-setup.md):** Implementing *Hide My Email* and Native Aliasing for iOS/macOS.
* **[Google Account Isolation](./google-account-grc.md):** Managing the "Primary Address Leak" in Gmail and setting up **Cloaked Logins** via alternate emails.
* **[Microsoft Outlook Hardening](./outlook-alias-policy.md):** Disabling sign-in capability for primary emails while retaining alias functionality.

### 2. Infrastructure & Communication
* **[Header Masking Protocol](./header-masking.md):** Verifying `Return-Path` and `X-Sender` integrity across various SMTP relays.
* **[Secure Recovery Loops](./recovery-loops.md):** Designing a "closed-loop" recovery system between Gmail and iCloud to prevent account lockout.

### 3. Data Resilience & Archival
* **[M-DISC Cold Storage](./m-disc-archival.md):** Technical setup for 1,000-year optical media backups.
* **[Physical Media Rotation](./physical-rotation.md):** Schedules and encryption standards (AES-256) for mobile data and photo archives.

---

## 🛡️ Core Compliance Checklist
*Before a setup is considered "Production Ready," it must satisfy these checks:*

- [ ] **Identity Isolation:** The "Primary Email" (Vault) is never used for a public-facing login.
- [ ] **Header Integrity:** Outgoing test emails show 0% leakage of the primary mailbox address in the `Return-Path`.
- [ ] **MFA Hardening:** All "Shadow Logins" use hardware security keys (FIDO2) or TOTP; no SMS-based recovery.
- [ ] **Archival Redundancy:** Annual data snapshots are committed to M-DISC or an equivalent non
