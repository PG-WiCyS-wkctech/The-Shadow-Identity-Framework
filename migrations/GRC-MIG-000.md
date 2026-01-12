# 🚀 Migrations: The Transition to Sovereignty

> **Folder Status:** Active Operations  
> **Standard ID:** GRC-MIG-000  
> **Purpose:** Controlled execution of identity shifts, security hardening, and data offloading.

This directory contains the "Change Management" playbooks for the **Shadow Identity Framework (SIF)**. Migration is the most high-risk phase of the framework; it involves modifying active security settings, rotating primary credentials, and moving terabytes of legacy data.

---

## 🗺️ The Migration Lifecycle

To prevent lockouts and data loss, all migrations must follow the **Prepare → Pivot → Purge** model.



1.  **Phase 1: Hardening (The Foundation)**
    * Transition from SMS to Hardware MFA.
    * Establish the "Fireproof Safe" recovery assets.
2.  **Phase 2: Decoupling (The Identity Shift)**
    * Separating "Login Identity" (Vault) from "Communication Identity" (Mask).
    * Redirecting "Spoke" accounts (Gmail/Outlook) to the "Hub" (iCloud).
3.  **Phase 3: De-Clouding (The Purge)**
    * Migrating high-volume media from Cloud Storage to physical M-DISC/SSD.
    * Downsizing paid cloud tiers to the "Free" baseline.

---

## 📂 Active Migration Guides

| Guide ID | Focus | Target Outcome |
| :--- | :--- | :--- |
| **[MIG-001: SMS Removal](./MIGRATION_SMS_REMOVAL.md)** | Security | 0% dependency on cellular carriers for MFA. |
| **[MIG-002: Identity Decoupling](./IDENTITY_DECOUPLING.md)** | Anonymity | Secret "Vault" logins established for 100% of critical accounts. |
| **[MIG-003: Storage Offload](./STORAGE_OFFLOAD.md)** | Sovereignty | Total cloud footprint reduced to <5GB; permanent M-DISC archive created. |

---

## 🛡️ Migration Safety Rules

To maintain GRC compliance during a migration, the following rules apply:

* **The "One-at-a-Time" Rule:** Never change the security settings of more than one "Vault" account in a 24-hour period. This prevents triggering automated anti-fraud locks.
* **The "Verified Bridge" Rule:** Never remove an old authentication factor (like a password or SMS) until the new factor (Passkey/Hardware) has been tested on **two different devices**.
* **The Rollback Strategy:** Always keep a "Legacy Recovery" option active until the new identity is fully stabilized (usually 7 days).

---

## ✅ Verification & Auditing
A migration is only considered "Complete" when:
1.  The **Master Sync Matrix** has been updated with the new credentials/MFA.
2.  A **Header Audit** confirms no identity leakage in outgoing mail.
3.  The **Fireproof Safe** contains the updated recovery codes for the new setup.

---

**Project Lead:** Kathryn Wilson 
**Current Milestone:** Phase 1 (Hardening)
