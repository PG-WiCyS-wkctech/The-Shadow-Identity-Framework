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
