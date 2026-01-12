# 🎭 Shadow Identity Framework (SIF)

[![Compliance: GRC-Level](https://img.shields.io/badge/Compliance-GRC--Level-blue?style=for-the-badge)](./standards)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey?style=for-the-badge)](https://creativecommons.org/licenses/by-sa/4.0/)
[![Storage Goal: $0 Cloud Cost](https://img.shields.io/badge/Goal-%240_Cloud_Cost-green?style=for-the-badge)](./hardware)
[![Status: Zero-Knowledge Ready](https://img.shields.io/badge/Status-Zero--Knowledge_Ready-brightgreen?style=for-the-badge)](./.gitignore)

> **A professional-grade system for personal data sovereignty.** > Decouple your digital identity from your communication, mask your metadata, and transition from high-cost "Cloud Renting" to permanent physical ownership.

---

## 🚀 The Mission: From Chaos to Sovereignty

Most digital users suffer from **"Email Bloat"** and **"Identity Leakage."** We give out our primary login email to every bank, school, and store, creating a massive security risk and mounting monthly cloud storage fees. 

The **Shadow Identity Framework** solves this through three core pillars:
1.  **Identity Cloaking:** Using secret "Vault" addresses for logins and "Mask" addresses for communications.
2.  **The Storage Diet:** A systematic "Burn and Purge" workflow to move data to **1,000-year M-DISC archives**.
3.  **Cryptographic Assurance:** Enforcing hardware MFA (Smart Rings/YubiKeys) as a non-negotiable standard.



---

## 📂 Repository Architecture

This repository is organized as a **GRC (Governance, Risk, and Compliance)** environment to ensure your security is documented, repeatable, and resilient.

| Directory | Content | Purpose |
| :--- | :--- | :--- |
| **[📜 /standards](./standards)** | The Laws | Non-negotiable rules for MFA, Passwords, and "Why No SMS." |
| **[🚀 /migrations](./migrations)** | The Change | Tactical playbooks for SMS removal, decoupling, and storage offloading. |
| **[🎓 /curriculum](./curriculum)** | The Roadmap | Level 1–4 learning paths from "Beginner" to "Sovereign Archivist." |
| **[🛠️ /hardware](./hardware)** | The Tools | Specs for M-DISC burners, Encrypted SSDs, and Security Keys. |
| **[📊 /templates](./templates)** | The Blueprints | Master Sync Matrix and Data Inventory Ledger spreadsheets. |
| **[🚨 /recovery](./recovery)** | The Failsafe | Break-glass protocols and Digital Inheritance plans. |
| **[✅ /checklists](./checklists)** | The Operations | Daily setup guides, Header Audits, and maintenance. |
| **[📂 /documentation](./documentation)** | The Manuals | Technical blueprints for iCloud, Google, and Outlook Hubs. |

---

## 🛠️ Getting Started (The Workflow)

To implement SIF for your digital life, follow the **Audit → Harden → Pivot → Purge** sequence:

1.  **Audit (Templates):** Populate your local [Master Sync Matrix](./templates) to map existing accounts.
2.  **Learn (Curriculum):** Move through [Level 1 and 2](./curriculum) to master the Hub-and-Spoke model.
3.  **Hardening (Migrations):** Execute **[MIG-001](./migrations/MIGRATION_SMS_REMOVAL.md)** to remove SMS-MFA and enroll hardware.
4.  **Decoupling (Migrations):** Execute **[MIG-002](./migrations/IDENTITY_DECOUPLING.md)** to "flip" logins to your secret Vault.
5.  **Archival (Migrations):** Execute **[MIG-003](./migrations/MIGRATION_STORAGE_OFFLOAD.md)** to move data to physical media.



---

## 🏛️ GRC Compliance Summary

* **Governance:** Every account must have a defined **Vault** (Secret) and **Mask** (Public) identity.
* **Risk:** SMS recovery is prohibited. Hardware-backed 2FA is the minimum standard for the "Hub."
* **Compliance:** Annual audits ensure cloud storage remains below the "Billing Wall" ($0/mo) and physical backups are verified.

---

## 🔐 Security & Privacy
* **Zero-Knowledge:** This repository contains *structures*, not *data*. The **[.gitignore](./.gitignore)** file is configured to prevent accidental commits of private spreadsheets or keys.
* **Local-First:** We prioritize hardware-encrypted local storage over cloud-syncing to ensure long-term data survival.



---

**Project Lead:** Kathryn Wilson  
**Version:** 1.1.0  
**Disclaimer:** This framework involves modifying security settings on sensitive accounts. Always maintain physical recovery codes in a safe location before beginning.
