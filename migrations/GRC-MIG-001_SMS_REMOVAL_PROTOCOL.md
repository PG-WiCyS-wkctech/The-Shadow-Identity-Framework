# 🛡️ GRC-MIG-001: SMS Removal Protocol
> **Index:** [Migrations Standard ID GRC-MIG-000](./README.md)
> **Document ID:** GRC-MIG-001  
> **Status:** Operational / Critical  
> **Target:** Elimination of Carrier-Dependent MFA  
> **Version:** 1.0 (2026)

This migration guide outlines the procedure for removing SMS (Text Message) and Voice-call based Multi-Factor Authentication from your "Vault" and "Hub" accounts. This process is required to comply with **SIF-STD-002 (MFA Standards)**.

---

## 📋 Pre-Flight Requirements
Before beginning this migration, you must have the following items physically present:

* [ ] **Two (2) Hardware Authenticators:** e.g., One Smart Ring (Primary) and one YubiKey (Backup).
* [ ] **The Physical Ledger:** Your printed `Master_Sync_Matrix` template.
* [ ] **Emergency Recovery Folder:** A place to store the printed 28-character recovery keys generated during this process.

---

## 🛠️ The "Safe Bridge" Workflow
To prevent accidental lockout, follow this exact sequence for every account.

### Step 1: Establish the New Factors
1.  Log into the account (Google, Apple, or Microsoft).
2.  Navigate to **Security / 2-Step Verification**.
3.  Add your **Smart Ring** or **Hardware Key** as a primary factor.
4.  Add a **TOTP Authenticator App** (e.g., Bitwarden or Raivo) as a secondary factor.

### Step 2: Generate Recovery Codes
1.  Locate the "Backup Codes" or "Recovery Key" section.
2.  Generate a new set of codes.
3.  **Action:** Print these immediately. Do not store them only on the computer you are currently using.
4.  Store these in your **Fireproof Safe**.

### Step 3: The Verification Test
1.  Open a **Private/Incognito** browser window.
2.  Attempt to log in to the account.
3.  When prompted for MFA, **do not choose SMS**. Use your **Smart Ring** or **Hardware Key**.
4.  If successful, repeat the test using the **Authenticator App**.

### Step 4: Severing the SMS Link
1.  Once you have verified that the hardware works, return to the Security settings.
2.  Locate the phone number used for SMS.
3.  **Delete/Remove** the phone number from the 2FA options.
4.  *Note:* If the platform requires a "Trusted Number" (like Apple), ensure that **"Security Keys"** are toggled as the primary requirement.

---

## 🏛️ Platform-Specific Navigation

### 🍏 Apple ID (The Hub)
* **Path:** Settings > [Name] > Sign In & Security > Two-Factor Authentication.
* **Action:** Add **Security Keys**. Then, go to **Account Recovery** and generate a **Recovery Key**. This 28-character code is your ultimate failsafe.

### 📧 Google (The Vault)
* **Path:** Security > 2-Step Verification.
* **Action:** Add **Passkeys & Security Keys**. Once added, scroll to the bottom and ensure "Backup Codes" are active. Then, delete the "Voice or Text Message" option.

### 🏦 Financial Institutions (The Spoke)
* **Challenge:** Some banks refuse to remove SMS.
* **Workaround:** If they require a number, use a **VOIP/Masked Number** (e.g., Google Voice) that is itself protected by your hardware-secured Google Vault. Never give them your physical SIM card number.

---

## 🚨 Emergency Rollback
If you lose your hardware keys during this migration:
1.  **Do not close your current browser session.**
2.  Immediately re-enable SMS as a temporary bridge.
3.  Re-generate recovery codes.
4.  Locate your backup YubiKey from the fireproof safe before attempting to remove SMS again.

---

## ✅ Migration Completion Checklist
- [ ] SMS/Voice removed from "Vault" and "Hub" accounts.
- [ ] 2x Hardware Keys registered per account.
- [ ] Recovery codes printed and placed in the safe.
- [ ] `Master_Sync_Matrix` updated (Column: MFA Type → FIDO2).

---

**Next Step:** Once SMS is removed, proceed to **[GRC-MIG-002_IDENTITY_DECOUPLING](./GRC-MIG-002_IDENTITY_DECOUPLING.md)** to change your sign-in emails to your secret Vault addresses.
