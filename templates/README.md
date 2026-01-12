# 📊 Templates: The Master Sync Matrix & Control Assets

> **Folder Status:** Operational  
> **Standard ID:** GRC-TMP-001  
> **Purpose:** Centralized tracking of Identity, Communication, and Archival status.

In the **Shadow Identity Framework (SIF)**, documentation is not optional. Because we are decoupling "Logins" from "Aliases," the system becomes too complex to manage by memory alone. These templates provide the structure needed to govern your digital footprint without data duplication.

---

## 📂 Included Templates

| File | Purpose | Recommended Format |
| :--- | :--- | :--- |
| **Master_Sync_Matrix** | Tracks every account, its secret login, and its public mask. | `.csv` or `.xlsx` |
| **Data_Inventory_Ledger** | Maps where your photos/videos live (Cloud vs. M-DISC). | `.xlsx` |
| **Recovery_Loop_Map** | Visualizes which accounts rescue each other during lockouts. | `.drawio` or `.md` |

---

## 🗺️ The Master Sync Matrix (Core Asset)

This is the primary spreadsheet. It is designed to be kept in a secure, encrypted location (e.g., a password-protected Excel file or an encrypted partition on your SSD).

### Essential Columns Explained:

1.  **Service/Domain:** (e.g., Purdue University, Chase Bank, Apple iCloud).
2.  **Identity (Vault):** The secret, hard-to-guess email address used *only* for sign-in.
3.  **Alias (Mask):** The public-facing email address shared with this service.
4.  **Forwarding Logic:** Where the mail goes (e.g., "Auto-forward to Hub").
5.  **Recovery Email:** The account used if you forget your password (The "Safety Net").
6.  **Storage Tier:** Current cost/limit (e.g., "Free - 5GB" or "Paid - 50GB").
7.  **Last Archival Date:** The last time this account was "Purged" to M-DISC/SSD.

---

## 🛡️ Security Warning: Repository Hygiene

> ⚠️ **CRITICAL SECURITY ADVISEMENT** > **DO NOT** upload your *populated* spreadsheets to this GitHub repository. These templates are provided as **BLANK SAMPLES** only. 

To maintain GRC-level security:
1.  Download the template to your local machine.
2.  Fill it out privately.
3.  Store the final file on your **Encrypted SSD** (Hardware Layer) or within a **Secure Vault** (e.g., 1Password, Bitwarden, or a local VeraCrypt volume).
4.  Add `*.xlsx` and `*.csv` to your `.gitignore` file to prevent accidental uploads of your private data.

---

## 🛠️ How to Populate Your Matrix

1.  **Phase 1 (The Spoke Audit):** Open all 7+ email accounts you currently own. Record their current storage levels and recovery settings in the Matrix.
2.  **Phase 2 (The Identity Shift):** As you change your logins to "Secret Identities," update the "Identity (Vault)" column.
3.  **Phase 3 (The Storage Diet):** Use the `Data_Inventory_Ledger` to track which files have been moved to physical media, allowing you to mark those cloud folders for deletion.

---

## 📈 Maintenance Schedule
* **Monthly:** Update "Storage Status" to ensure you are not approaching a "Storage Wall" that would trigger a new billing tier.
* **Quarterly:** Review "Recovery Loops" to ensure all backup phone numbers and secondary emails are still active.
* **Annually:** Perform a "Compliance Audit"—ensure that every account in the Matrix has a corresponding physical backup on M-DISC.

---

# 📊 Template: Master Sync Matrix (v2.0 - Biometric Integrated)

> **File Reference:** `MASTER_SYNC_MATRIX.xlsx` / `.csv`
> **Status:** CORE ASSET
> **Security Level:** RESTRICTED (Store in Encrypted Vault)

The **Master Sync Matrix** is the single source of truth for the Shadow Identity Framework. This version has been updated to support **Multi-Modal Authentication**, specifically tracking the relationship between your "Vault" accounts and your "Authorized Hardware" (Smart Rings, Smart Cards, and FIDO2 keys).

---

## 🗺️ The Identity-to-Hardware Map



---

## 🛠️ Matrix Structure & Column Definitions

| Column | Purpose | GRC Requirement |
| :--- | :--- | :--- |
| **Service/Domain** | The name of the platform (e.g., "Chase Bank", "iCloud"). | Unique identifier. |
| **Vault Address** | Your **Secret Identity** used ONLY for login. | Must not be public-facing. |
| **Mask Address** | The **Public Alias** used for communications. | Primary shield. |
| **MFA Type** | Method of 2FA (e.g., Passkey, TOTP, FIDO2). | SMS is prohibited. |
| **Authorized Hardware**| **The specific Ring, Card, or Key linked to this account.** | **Must match physical labels.** |
| **Recovery Loop** | The fallback account or physical code location. | Printed in Fireproof Safe. |
| **Storage Status** | Current data usage vs. Free tier limit. | Triggers "The Purge" workflow. |

---

## 📝 Example Matrix Entry

| Service | Vault Address (Login) | Mask Address (Alias) | MFA Type | Authorized Hardware | Recovery |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **iCloud Hub** | `x7_vault@icloud.com` | `me@public.com` | Passkey | **Token Ring (Primary)** | Recovery Code #001 |
| **Gmail Vault**| `shadow_99@gmail.com` | `work@mask.com` | FIDO2 | **YubiKey Bio (Backup)** | Recovery Code #002 |
| **Purdue Alumni**| `alumni_id@purdue.edu`| `alumni@mask.com` | TOTP | **Biometric Smart Card** | iCloud Hub |

---

## 🔐 Instructions for "Authorized Hardware" Column

To ensure compliance with **SIF-STD-006 (Authentication Media)**, follow these labeling rules:

1.  **Physical Labeling:** Every piece of hardware (Smart Card, YubiKey) should have a small physical label (e.g., "KEY-01").
2.  **Hardware Nicknames:** When registering a Passkey or Hardware Key on a website, use the **exact name** listed in your "Authorized Hardware" column. 
    * *Example:* If your Matrix says "Token Ring," the website's security dashboard should also say "Token Ring."
3.  **The "Redundancy" Note:** If an account is linked to both a Ring and a backup YubiKey, list both: `[Ring (P), YubiKey-01 (B)]`.

---

## ⚠️ Repository Safety Reminder
**DO NOT** upload your filled-out Matrix to GitHub. 
1. Copy this structure into a local Excel or CSV file.
2. Store that file inside your **Password Manager** or on your **Encrypted SSD**.
3. Ensure your `.gitignore` file includes `*.csv` and `*.xlsx`.

---

**Next Step:** Would you like me to generate a **Python script** that you can run locally to "Audit" your Matrix and flag any accounts that are missing "Authorized Hardware" or are using prohibited MFA (SMS)?
