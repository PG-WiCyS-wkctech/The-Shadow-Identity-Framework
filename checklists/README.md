# ✅ Execution Checklists: Platform Configuration

> **Folder Status:** Operational  
> **Standard ID:** GRC-CHK-001  
> **Purpose:** Step-by-step operational workflows for Hub-and-Spoke implementation.

This directory contains actionable checklists for the three primary platforms supported by the **Shadow Identity Framework (SIF)**. These are designed to be used during "Configuration Sprints" to ensure that settings for privacy, storage, and identity cloaking are applied consistently.

---

## 📋 Available Checklists

| Checklist ID | Platform | Focus | Goal |
| :--- | :--- | :--- | :--- |
| **[CHK-ICLOUD](./icloud-setup.md)** | **iCloud** | The Hub | Establishing the "Central Command" and Masking Layer. |
| **[CHK-GMAIL](./gmail-config.md)** | **Gmail** | The Spoke | Forwarding, Storage Diet, and Vault Recovery setup. |
| **[CHK-OUTLOOK](./outlook-config.md)** | **Outlook** | The Spoke | Legacy account cleanup and Alias-only sign-in. |
| **[CHK-PURGE](./purge-workflow.md)** | **Universal** | Data Purge | The "Burn and Purge" sequence for physical archival. |

---

## 🛡️ The "SIF Standard" Configuration
Every platform setup must meet these four criteria before being marked "Complete" in the Master Sync Matrix:

### 1. The Forwarding Rule (The Flow)
* All incoming mail must be routed to the **iCloud Hub**.
* "Delete local copy" or "Archive local copy" must be enabled on the Spoke (Gmail/Outlook) to prevent storage bloat.

### 2. The Identity Flip (The Vault)
* The login email is changed to a "Secret Identity."
* Public-facing aliases are **disabled** for sign-in purposes.

### 3. The Recovery Loop (The Safety Net)
* Account A is the recovery for Account B.
* Account B is the recovery for Account A.
* Both are secured with **Hardware 2FA (YubiKey)** or **TOTP (Authenticator App)**. No SMS.

### 4. The Storage Diet (The Purge)
* Large attachments and "Trash/Spam" are cleared.
* High-volume media is marked for **M-DISC Archival**.

---

## 🛠️ How to Use These Checklists

1.  **Print or Side-Load:** Open the relevant checklist on a tablet or second monitor while you perform the setup on your computer.
2.  **Verify Headers:** After completing a checklist, perform a "Header Audit" by sending an email from that account to a test service (like Mail-Tester.com) to ensure no "Vault" addresses are leaking.
3.  **Update the Matrix:** Once a checklist is finished, update your `Master_Sync_Matrix` template with the new "Last Audited" date.

---

## ⚠️ Critical Warning: Account Lockouts
When performing "The Identity Flip" (changing your login email), ensure you have your **Recovery Keys** or **Identity Codes** printed out and physically in front of you. Changing security settings on multiple accounts simultaneously can trigger "Suspicious Activity" flags. 

**Always finish one checklist completely before starting the next.**

---
